# WireGuard VPN Setup - Firma Puls

> VPN-Lösung für Firma Puls: Server als Zentrale, 3x FritzBox als Clients

## Übersicht

```
┌─────────────────────────────────────────────────────────────────────────┐
│                              INTERNET                                     │
│                                                                          │
│     ┌──────────────────────────────────────────────────────────┐        │
│     │              VPS Server (Ubuntu)                         │        │
│     │              Public IP: xxx.xxx.xxx.xxx                 │        │
│     │                                                          │        │
│     │   WireGuard Port: 51820/UDP                            │        │
│     │   WireGuard UI: localhost:5000 (nur SSH Tunnel!)        │        │
│     │                                                          │        │
│     │   ┌────────────────────────────────────────────────┐    │        │
│     │   │              WireGuard Interface                │    │        │
│     │   │                                                  │    │        │
│     │   │   VPN Network: 10.0.0.0/24                     │    │        │
│     │   │                                                  │    │        │
│     │   │   Peers:                                        │    │        │
│     │   │   - FritzBox 1 (Büro)                          │    │        │
│     │   │   - FritzBox 2 (Lager)                         │    │        │
│     │   │   - FritzBox 3 (HomeOffice)                    │    │        │
│     │   └────────────────────────────────────────────────┘    │        │
│     └──────────────────────────────────────────────────────────┘        │
│                                    │                                       │
│                      WireGuard UDP 51820                                │
│                                    │                                       │
└────────────────────────────────────│────────────────────────────────────┘
                                     │
         ┌────────────────────────────┼────────────────────────────┐
         │                            │                            │
         │                            │                            │
┌────────▼────────┐        ┌────────▼────────┐        ┌────────▼────────┐
│    FritzBox 1     │        │    FritzBox 2     │        │    FritzBox 3     │
│    Büro           │        │    Lager          │        │    HomeOffice     │
│  192.168.1.0/24   │        │  192.168.2.0/24   │        │  192.168.3.0/24   │
└────────┬─────────┘        └────────┬─────────┘        └────────┬─────────┘
         │                             │                             │
         │    FritzBox WireGuard       │                             │
         │    Client Mode             │                             │
         │    Verbunden zu VPS        │                             │
         └─────────────────────────────┘                             │
                                                                         │
                    Alle Netze sind über VPN erreichbar                  │
```

---

## Komponenten

| Komponente | IP/Domain | Funktion |
|------------|-----------|----------|
| **VPS Server** | `vps.puls.firma.de` (oder IP) | WireGuard Gateway |
| **FritzBox 1** | Büro | WireGuard Client |
| **FritzBox 2** | Lager | WireGuard Client |
| **FritzBox 3** | HomeOffice | WireGuard Client |
| **WireGuard UI** | `localhost:5000` | Administration (nur SSH!) |

---

## Server Setup (VPS)

### 1. WireGuard installieren

```bash
# Ubuntu/Debian
apt update && apt install -y wireguard

# WireGuard UI (Docker)
docker run -d \
  --name wireguard-ui \
  -v /opt/wireguard:/data \
  -v /etc/wireguard:/etc/wireguard \
  -p 5000:5000 \
  -e "WGUI_ADDR=localhost" \
  -e "WGUI_PORT=5000" \
  -e "SSH_HOST=<server-ip>" \
  -e "SSH_PORT=22" \
  -e "SSH_USER=<user>" \
  --restart=unless-stopped \
  ngodry/whoise:latest
```

### 2. WireGuard Konfiguration (Server)

```ini
# /etc/wireguard/wg0.conf

[Interface]
Address = 10.0.0.1/24
ListenPort = 51820
PrivateKey = <server-private-key>
PostUp = iptables -A FORWARD -i wg0 -j ACCEPT; iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE
PostDown = iptables -D FORWARD -i wg0 -j ACCEPT; iptables -t nat -D POSTROUTING -o eth0 -j MASQUERADE

# FritzBox 1 - Büro
[Peer]
PublicKey = <fb1-public-key>
AllowedIPs = 10.0.0.2/32, 192.168.1.0/24

# FritzBox 2 - Lager
[Peer]
PublicKey = <fb2-public-key>
AllowedIPs = 10.0.0.3/32, 192.168.2.0/24

# FritzBox 3 - HomeOffice
[Peer]
PublicKey = <fb3-public-key>
AllowedIPs = 10.0.0.4/32, 192.168.3.0/24
```

### 3. IP Forwarding aktivieren

```bash
# /etc/sysctl.conf
net.ipv4.ip_forward = 1

# Anwenden
sysctl -p
```

### 4. Firewall (UFW)

```bash
ufw allow 22/tcp    # SSH
ufw allow 51820/udp  # WireGuard
ufw enable
```

---

## WireGuard UI Zugriff (NUR via SSH!)

### Wichtig: WireGuard UI ist NICHT öffentlich!

```
╔════════════════════════════════════════════════════════════════╗
║  WARNUNG: WireGuard UI NUR via SSH Tunnel erreichbar!        ║
║  Kein Port 5000 öffentlich öffnen!                          ║
╚════════════════════════════════════════════════════════════════╝
```

### SSH Tunnel für Administration

```bash
# Lokal auf deinem Rechner:
ssh -L 5000:localhost:5000 user@vps.puls.firma.de

# Dann im Browser:
# https://localhost:5000
```

### Alternativ: SSH Reverse Tunnel

```bash
# Auf dem VPS Server (als systemd service):
# /etc/systemd/system/wgui-tunnel.service
[Unit]
Description=WireGuard UI SSH Tunnel
After=network.target

[Service]
ExecStart=/usr/bin/ssh -N -L 5000:localhost:5000 user@localhost
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target
```

---

## FritzBox 1 - Büro (Client)

### FritzBox Einstellungen (VPN WireGuard Client)

In FritzBox UI: **System → FritzBox Name → VPN**

```
Name: Puls-VPN-Büro
VPN-Server: vps.puls.firma.de:51820
VPN-Netzwerk: 192.168.1.0/24
Tunnelprotokoll: WireGuard

Lokaler WireGuard Endpunkt:
  - Private Key: <fb1-private-key>
  - IP: 10.0.0.2/32

Remote WireGuard Endpunkt:
  - Public Key: <server-public-key>
  - IP: 10.0.0.1/32
  - Erlaubte IPs: 0.0.0.0/0 (oder nur bestimmte Netze)

Allowed IPs:
  - 10.0.0.0/24 (VPN Netz)
  - 192.168.2.0/24 (Lager)
  - 192.168.3.0/24 (HomeOffice)
```

### FritzBox LAN-LAN Kopplung

```
VPN-Verbindung: Aktiv
Netzwerk: 192.168.1.0/24 → VPN Tunnel
LAN-LAN Kopplung: Alle Geräte im VPN
```

---

## FritzBox 2 - Lager (Client)

```ini
Lokaler WireGuard Endpunkt:
  - Private Key: <fb2-private-key>
  - IP: 10.0.0.3/32

Remote WireGuard Endpunkt:
  - Public Key: <server-public-key>
  - IP: 10.0.0.1/32

Allowed IPs:
  - 10.0.0.0/24
  - 192.168.1.0/24 (Büro)
  - 192.168.3.0/24 (HomeOffice)
```

---

## FritzBox 3 - HomeOffice (Client)

```ini
Lokaler WireGuard Endpunkt:
  - Private Key: <fb3-private-key>
  - IP: 10.0.0.4/32

Remote WireGuard Endpunkt:
  - Public Key: <server-public-key>
  - IP: 10.0.0.1/32

Allowed IPs:
  - 10.0.0.0/24
  - 192.168.1.0/24 (Büro)
  - 192.168.2.0/24 (Lager)
```

---

## Netzwerk-Übersicht

| Standort | Netzwerk | WireGuard IP | FritzBox |
|----------|----------|---------------|----------|
| VPS Server | - | 10.0.0.1 | - |
| Büro | 192.168.1.0/24 | 10.0.0.2 | FB1 |
| Lager | 192.168.2.0/24 | 10.0.0.3 | FB2 |
| HomeOffice | 192.168.3.0/24 | 10.0.0.4 | FB3 |

---

## VPN Routing

### Von FritzBox 1 (Büro) aus erreichbar:

```
✅ 10.0.0.0/24 (VPN Netz)
✅ 192.168.2.0/24 (Lager)
✅ 192.168.3.0/24 (HomeOffice)
✅ 10.0.0.1 (VPS Server)
```

### Internet-Traffic:

- **Option A:** Nur VPN-Netzwerk über Tunnel, rest direkt (Split Tunnel)
- **Option B:** Alles über VPN (Full Tunnel) - bei Bedarf

---

## Sicherheit

### SSH Zugang zum Server

```bash
# Nur SSH Keys erlauben (kein Password!)
# /etc/ssh/sshd_config
PubkeyAuthentication yes
PasswordAuthentication no
PermitRootLogin no

# Fail2Ban installieren
apt install -y fail2ban
```

### Firewall Regeln (VPS)

```bash
# Default: Alles blocken
ufw default deny incoming
ufw default allow outgoing

# Nur SSH und WireGuard erlauben
ufw allow 22/tcp    # SSH
ufw allow 51820/udp  # WireGuard

# Kein Port 5000 (WireGuard UI) öffentlich!
```

### WireGuard Keys

```bash
# Server Keys generieren
wg genkey | tee server_private.key | wg pubkey > server_public.key

# FritzBox Keys generieren (in WireGuard UI oder locally)
wg genkey | tee fb1_private.key | wg pubkey > fb1_public.key
```

---

## Wartung & Monitoring

### Logs prüfen

```bash
# WireGuard Status
wg show

# System Logs
journalctl -u wg-quick@wg0 -f

# WireGuard UI Logs
docker logs wireguard-ui -f
```

### Neuen Client hinzufügen

1. SSH Tunnel zu Server aufbauen
2. WireGuard UI öffnen (localhost:5000)
3. Neuen Peer hinzufügen
4. FritzBox Konfiguration exportieren
5. In FritzBox importieren

---

## Troubleshooting

### FritzBox verbindet sich nicht

```bash
# Auf Server prüfen:
wg show

# Sollte:
# - Interface mit PublicKey zeigen
# - Peer mit "latest handshake" (wenn verbunden)
```

### Keine Antwort von anderen Netzen

```bash
# IP Forwarding prüfen
cat /proc/sys/net/ipv4/ip_forward
# Sollte "1" sein

# Firewall prüfen
ufw status
iptables -L FORWARD
```

### WireGuard UI nicht erreichbar

```bash
# SSH Tunnel aktiv?
ps aux | grep ssh | grep 5000

# Docker Container laufend?
docker ps | grep wireguard-ui
```

---

## Nächste Schritte

1. [ ] VPS Server mieten/konfigurieren
2. [ ] WireGuard + WireGuard UI installieren
3. [ ] FritzBox 1 (Büro) konfigurieren
4. [ ] FritzBox 2 (Lager) konfigurieren
5. [ ] FritzBox 3 (HomeOffice) konfigurieren
6. [ ] VPN-Verbindungen testen
7. [ ] SSH Tunnel für Admin einrichten

---

## Alternativen

| Lösung | Vorteil | Nachteil |
|--------|----------|----------|
| **WireGuard (dieses Setup)** | Schnell, sicher, einfach | FritzBox muss WireGuard unterstützen |
| FritzBox VPN (IPSec) | Native FritzBox Unterstützung | Komplexer, langsamer |
| OpenVPN | Sehr verbreitet | Langsamer, komplexer |

---

## Links

- [WireGuard Offizielle Website](https://www.wireguard.com/)
- [WireGuard UI (ngodry/whoise)](https://github.com/ngodry/whoise)
- [WireGuard in FritzBox](https://en.avm.de/service/fritzbox/knowledge-base/view/FAQ/How_to_set_up_a_VPN_connection_with_WireGuard/)

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
