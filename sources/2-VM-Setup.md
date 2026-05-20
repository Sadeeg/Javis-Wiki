# 2-VM Home-Lab Setup

> Infrastruktur mit 2 VMs: Apps + Traefik auf VM1, External DNS auf VM2

## Architektur

```
┌─────────────────────────────────────────────────────────────────────────┐
│                          INTERNET                                        │
│                                                                          │
│     Netcup DNS (NS: dev.deeg-mail.de → VM2 Public IP)                  │
│                                                                          │
│     Let's Encrypt ────DNS-01 Challenge─────→ VM2:53 (Technitium)       │
│     (validiert TXT Record)                      │                        │
└─────────────────────────────────────────────────│────────────────────────┘
                                                  │
                                          Port Forwarding
                                          Router: 53 → VM2
                                                  │
┌─────────────────────────────────────────────────│────────────────────────┐
│                    VM 2 (192.168.1.20)                                    │
│                    External DNS + Docker                                   │
│                                                                          │
│     ┌──────────────────────────────────────────────────────────┐         │
│     │              Technitium DNS (Docker)                     │         │
│     │                                                              │         │
│     │   Zone: dev.deeg-mail.de                                   │         │
│     │   Ports: 53 (TCP/UDP)                                     │         │
│     │   WebUI: 5380 (intern)                                    │         │
│     │                                                              │         │
│     │   Empfängt RFC-2136 Updates von VM1                       │         │
│     │   Let's Encrypt fragt TXT Record von außen ab              │         │
│     └──────────────────────────────────────────────────────────┘         │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
                                    │ RFC-2136 (UDP 53)
                                    │ Nur intern!
                                    ↓
┌─────────────────────────────────────────────────────────────────────────┐
│                    VM 1 (192.168.1.10)                                    │
│                    Apps + Internal DNS + Traefik                          │
│                                                                          │
│     ┌──────────────────────────────────────────────────────────┐         │
│     │              Docker + Traefik                             │         │
│     │                                                              │         │
│     │   Traefik :443                                             │         │
│     │   ├── Javis :18789                                        │         │
│     │   ├── Nextcloud :11000                                    │         │
│     │   ├── OpenProject :8080                                   │         │
│     │   └── ...                                                 │         │
│     └──────────────────────────────────────────────────────────┘         │
│                                                                          │
│     ┌──────────────────────────────────────────────────────────┐         │
│     │              Technitium DNS (Docker) - Internal            │         │
│     │                                                              │         │
│     │   Zone: dev.deeg-mail.de (interner Cache)                 │         │
│     │   Forward zu VM2 für externe Queries                      │         │
│     └──────────────────────────────────────────────────────────┘         │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## VM2: External DNS

### docker-compose.yml

```yaml
# /opt/dns-external/docker-compose.yml
version: '3.8'

services:
  technitium:
    image: technitium/dns-server:latest
    container_name: dns-external
    restart: unless-stopped
    ports:
      - "53:53/tcp"
      - "53:53/udp"
      - "5380:5380"  # Nur intern erreichbar
    volumes:
      - ./config:/etc/opt/technitium
      - ./logs:/var/log/technitium
    networks:
      - dns-net

networks:
  dns-net:
    name: dns-external-net
    driver: bridge
```

### Zone: dev.deeg-mail.de

```
Records:

1. A Record (Wildcard)
   Name: *
   Value: 192.168.1.10 (VM1 Traefik)
   TTL: 300

2. A Record (DNS Server selbst)
   Name: dns
   Value: 192.168.1.20 (VM2)
   TTL: 300

3. NS Record
   Name: dev.deeg-mail.de
   Name Server: dns.dev.deeg-mail.de

4. TXT Record (ACME - wird via RFC-2136 geschrieben)
   Name: _acme-challenge
   Type: TXT
   TTL: 60
```

### RFC-2136 Access Control

```
Allow: 192.168.1.0/24 UPDATE dev.deeg-mail.de
```

### Netcup DNS Konfiguration

```
Typ:  NS
Name: dev
Wert: dns.dev.deeg-mail.de

Typ:  A
Name: dns.dev
Wert: <IP des Servers> (oder Router IP mit Port Forwarding)
```

---

## VM1: Traefik

### docker-compose.yml

```yaml
# /opt/traefik/docker-compose.yml
version: '3.8'

services:
  traefik:
    image: traefik:v3.0
    container_name: traefik
    restart: unless-stopped
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock:ro
      - ./acme.json:/acme.json
    environment:
      - TZ=Europe/Berlin
    command:
      - "--certificatesresolvers.letsencrypt.acme.dnschallenge=true"
      - "--certificatesresolvers.letsencrypt.acme.dnschallenge.provider=rfc2136"
      - "--certificatesresolvers.letsencrypt.acme.dnschallenge.resolvers=192.168.1.20:53"
      - "--certificatesresolvers.letsencrypt.acme.email=dein@deeg-mail.de"
      - "--certificatesresolvers.letsencrypt.acme.storage=/acme.json"
      - "--providers.docker.exposedbydefault=false"
      - "--log.level=INFO"
    networks:
      - traefik-net
      - dns-net

networks:
  traefik-net:
    name: traefik-net
    driver: bridge
  dns-net:
    name: dns-external-net
    external: true
```

---

## Service Template (auf VM1)

### Javis

```yaml
# /opt/javis/docker-compose.yml
version: '3.8'

services:
  javis:
    image: ghcr.io/openclaw/openclaw:latest
    container_name: javis
    restart: unless-stopped
    volumes:
      - /home/sascha/.openclaw:/home/sascha/.openclaw
    labels:
      - "traefik.enable=true"
      - "traefik.http.routers.javis.rule=Host(`javis.dev.deeg-mail.de`)"
      - "traefik.http.routers.javis.entrypoints=websecure"
      - "traefik.http.routers.javis.tls=true"
      - "traefik.http.routers.javis.tls.certresolver=letsencrypt"
      - "traefik.http.services.javis.loadbalancer.server.port=18789"
    networks:
      - traefik-net

networks:
  traefik-net:
    name: traefik-net
    external: true
```

### Nextcloud

```yaml
# /opt/nextcloud/docker-compose.yml
version: '3.8'

services:
  nextcloud:
    image: nextcloud:latest
    container_name: nextcloud
    restart: unless-stopped
    environment:
      - TZ=Europe/Berlin
      - MYSQL_HOST=database
      - MYSQL_DATABASE=nextcloud
      - MYSQL_USER=nextcloud
      - MYSQL_PASSWORD=${NEXTCLOUD_DB_PASSWORD}
    volumes:
      - ./data:/var/www/html
      - ./config:/var/www/html/config
    labels:
      - "traefik.enable=true"
      - "traefik.http.routers.nextcloud.rule=Host(`nextcloud.dev.deeg-mail.de`)"
      - "traefik.http.routers.nextcloud.entrypoints=websecure"
      - "traefik.http.routers.nextcloud.tls=true"
      - "traefik.http.routers.nextcloud.tls.certresolver=letsencrypt"
      - "traefik.http.services.nextcloud.loadbalancer.server.port=80"
    depends_on:
      - database
    networks:
      - traefik-net

  database:
    image: postgres:15-alpine
    container_name: nextcloud-db
    restart: unless-stopped
    environment:
      - POSTGRES_DB=${DB_NAME}
      - POSTGRES_USER=${DB_USER}
      - POSTGRES_PASSWORD=${DB_PASSWORD}
    volumes:
      - ./postgres-data:/var/lib/postgresql/data
    networks:
      - traefik-net

networks:
  traefik-net:
    name: traefik-net
    external: true
```

### OpenProject

```yaml
# /opt/openproject/docker-compose.yml
version: '3.8'

services:
  openproject:
    image: openproject/community:latest
    container_name: openproject
    restart: unless-stopped
    environment:
      - TZ=Europe/Berlin
    volumes:
      - ./data:/var/openproject
    labels:
      - "traefik.enable=true"
      - "traefik.http.routers.project.rule=Host(`project.dev.deeg-mail.de`)"
      - "traefik.http.routers.project.entrypoints=websecure"
      - "traefik.http.routers.project.tls=true"
      - "traefik.http.routers.project.tls.certresolver=letsencrypt"
      - "traefik.http.services.project.loadbalancer.server.port=8080"
    networks:
      - traefik-net

networks:
  traefik-net:
    name: traefik-net
    external: true
```

---

## Setup Scripts

### VM2: External DNS Setup

```bash
#!/bin/bash
# setup-dns-external.sh

set -e

# Docker Network erstellen
docker network create dns-external-net

# Config erstellen
mkdir -p /opt/dns-external/config
mkdir -p /opt/dns-external/logs

# docker-compose.yml erstellen
cat > /opt/dns-external/docker-compose.yml << 'EOF'
version: '3.8'
services:
  technitium:
    image: technitium/dns-server:latest
    container_name: dns-external
    restart: unless-stopped
    ports:
      - "53:53/tcp"
      - "53:53/udp"
      - "5380:5380"
    volumes:
      - ./config:/etc/opt/technitium
      - ./logs:/var/log/technitium
    networks:
      - dns-net
networks:
  dns-net:
    name: dns-external-net
    driver: bridge
EOF

# Starten
cd /opt/dns-external
docker-compose up -d

echo "DNS External gestartet!"
echo "WebUI: http://192.168.1.20:5380"
```

### VM1: Traefik Setup

```bash
#!/bin/bash
# setup-traefik.sh

set -e

# Docker Network erstellen (muss auf VM1 und VM2 gleich heißen)
docker network create traefik-net

# Docker Network auf VM2 verbinden
docker network connect dns-external-net dns-external 2>/dev/null || true

# Config erstellen
mkdir -p /opt/traefik

# docker-compose.yml erstellen
cat > /opt/traefik/docker-compose.yml << 'EOF'
version: '3.8'
services:
  traefik:
    image: traefik:v3.0
    container_name: traefik
    restart: unless-stopped
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock:ro
      - ./acme.json:/acme.json
    environment:
      - TZ=Europe/Berlin
    command:
      - "--certificatesresolvers.letsencrypt.acme.dnschallenge=true"
      - "--certificatesresolvers.letsencrypt.acme.dnschallenge.provider=rfc2136"
      - "--certificatesresolvers.letsencrypt.acme.dnschallenge.resolvers=192.168.1.20:53"
      - "--certificatesresolvers.letsencrypt.acme.email=dein@deeg-mail.de"
      - "--certificatesresolvers.letsencrypt.acme.storage=/acme.json"
      - "--providers.docker.exposedbydefault=false"
      - "--log.level=INFO"
    networks:
      - traefik-net
      - dns-net
networks:
  traefik-net:
    name: traefik-net
    driver: bridge
  dns-net:
    name: dns-external-net
    external: true
EOF

# Starten
cd /opt/traefik
docker-compose up -d

echo "Traefik gestartet!"
```

---

## Port Forwarding (Router)

```
Port 53 (TCP/UDP) → 192.168.1.20 (VM2)
```

---

## DNS Flow

```
┌─────────────────────────────────────────────────────────────────┐
│                     DNS Auflösung                                 │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Client (192.168.1.x)                                          │
│       │                                                          │
│       │ /etc/resolv.conf → 192.168.1.20 (VM2 DNS)              │
│       │                                                          │
│       ▼                                                          │
│  VM2 Technitium DNS                                              │
│       │                                                          │
│       ├── Internal Query?                                         │
│       │     └── Zone: dev.deeg-mail.de → A Record → VM1        │
│       │                                                          │
│       └── External Query?                                        │
│             └── Forward zu 1.1.1.1 / 8.8.8.8                   │
│                                                                  │
│  Let's Encrypt (von außen)                                        │
│       │                                                          │
│       ├── NS: dev.deeg-mail.de → VM2 Public IP                  │
│       └── TXT Query: _acme-challenge.dev.deeg-mail.de           │
│             └── VM2 antwortet mit TXT Value                     │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Service hinzufügen (IAC)

```yaml
# 1. Neues Verzeichnis
mkdir -p /opt/mein-service

# 2. docker-compose.yml mit Labels
cat > /opt/mein-service/docker-compose.yml << 'EOF'
version: '3.8'
services:
  mein-service:
    image: mein/image:latest
    labels:
      - "traefik.enable=true"
      - "traefik.http.routers.mein-service.rule=Host(`mein-service.dev.deeg-mail.de`)"
      - "traefik.http.routers.mein-service.entrypoints=websecure"
      - "traefik.http.routers.mein-service.tls=true"
      - "traefik.http.routers.mein-service.tls.certresolver=letsencrypt"
      - "traefik.http.services.mein-service.loadbalancer.server.port=8080"
    networks:
      - traefik-net
networks:
  traefik-net:
    name: traefik-net
    external: true
EOF

# 3. Starten
cd /opt/mein-service
docker-compose up -d

# 4. FERTIG - Traefik erkennt automatisch
```

---

## Troubleshooting

### DNS Test

```bash
# Intern
dig @192.168.1.20 *.dev.deeg-mail.de

# ACME TXT Record prüfen
dig @192.168.1.20 _acme-challenge.dev.deeg-mail.de TXT

# Von außen (nach Port Forwarding)
dig @<public-ip> _acme-challenge.dev.deeg-mail.de TXT
```

### Logs

```bash
# VM2 DNS
docker logs dns-external -f

# VM1 Traefik
docker logs traefik -f
```

### Netzwerk prüfen

```bash
# Auf VM1
docker network inspect traefik-net
docker network inspect dns-external-net
```

---

## Service URLs

| Service | URL | Port |
|---------|-----|------|
| Traefik Dashboard | http://192.168.1.10:8080 | 8080 |
| DNS WebUI (VM2) | http://192.168.1.20:5380 | 5380 |
| Javis | https://javis.dev.deeg-mail.de | 18789 |
| Nextcloud | https://nextcloud.dev.deeg-mail.de | 11000 |
| OpenProject | https://project.dev.deeg-mail.de | 8080 |

---

## Ansible/IAC

> Automatisiertes Setup mit Ansible: [IAC-Internal-Dev](https://github.com/Sadeeg/IAC-Internal-Dev)

```bash
git clone git@github.com:Sadeeg/IAC-Internal-Dev.git
cd IAC-Internal-Dev
# Inventory anpassen, dann:
ansible-playbook -i inventory/prod/hosts.yml vm2-external-dns/site.yml
ansible-playbook -i inventory/prod/hosts.yml vm1-apps/site.yml
```

---

## Nächste Schritte

1. [ ] Netcup DNS konfigurieren (NS Delegation für dev.deeg-mail.de)
2. [ ] Port Forwarding auf Router (53 → VM2)
3. [ ] VM2: Technitium DNS installieren + Zone einrichten
4. [ ] VM1: Traefik installieren
5. [ ] Services deployen
6. [ ] Ersten Service testen

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
