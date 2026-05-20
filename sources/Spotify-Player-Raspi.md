# Spotify-Player — Raspberry Pi 4 + 7" Display

> Konzept für einen eigenen Spotify-Streaming-Player mit Touchscreen und Javis-Sprachsteuerung

---

## 1. Ziel

Ein fest installierter Musik-Player im Haus (z.B. Küche, Wohnzimmer), der:
- **Spotify abspielt** (Spotify Connect + lokale MP3s)
- **Touchscreen-Bedienung** hat (7 Zoll HDMI)
- **Von Javis steuerbar** ist (Sprache + Telegram)
- **Offline-fähig** ist (lokale Bibliothek als Backup)
- **Gut aussieht** — kein Bastel-Look

---

## 2. Hardware

### Basis
| Komponente | Empfehlung | ca. Preis |
|---|---|---|
| Raspberry Pi 4 (4 GB) | Bausatz oder Solo | ~60 € |
| 7" HDMI Touchscreen | WaveShare 7" Capacitive (1024×600) | ~80 € |
| SD-Karte | Samsung EVO Plus 32 GB | ~10 € |
| **Gehäuse** | **3D-Druck** (Stackable Design) | — |

### Audio (optional aber empfohlen)
| Variante | HAT | ca. Preis |
|---|---|---|
| Line-Out | HiFiBerry DAC+ RCA | ~35 € |
| Verstärkt (passive Lautsprecher) | HiFiBerry Amp2 | ~55 € |
| Kopfhörer | Onboard 3.5mm | 0 € |

### Extras
- IR-Fernbedienung (für Basic-Steuerung)
- Rotary Encoder (Lautstärke-Drehregler)
- LED-Ring (Zustandsanzeige: Playing/Paused/Error)

---

## 3. Software-Stack

```
┌─────────────────────────────────────────┐
│         Python Dashboard (PyQt5)        │
│  - Album Art     - Playlist-Browser     │
│  - Playback-Control (Play/Pause/Skip)  │
│  - Lautstärke     - Now Playing         │
├─────────────────────────────────────────┤
│         Javis Integration (REST API)    │
│  - Sprachsteuerung via Telegram        │
│  - Playlist-Auswahl per Sprache         │
│  - Text-to-Speech (Now Playing Ansagen) │
├─────────────────────────────────────────┤
│         Musik-Quellen                   │
│  ┌───────────────┐  ┌───────────────┐  │
│  │  Spotify      │  │  Lokale MP3s  │  │
│  │  (Librespot)  │  │  (MPD)        │  │
│  └───────────────┘  └───────────────┘  │
├─────────────────────────────────────────┤
│         Basis-System                    │
│  - Raspberry Pi OS Lite (Bookworm)     │
│  - Audio: ALSA / PipeWire               │
│  - Auto-Login + Auto-Start              │
└─────────────────────────────────────────┘
```

### Software-Komponenten

| Komponente | Technologie | Funktion |
|---|---|---|
| **Spotify Connect** | `librespot` (Rust) | Empfängt Spotify-Stream direkt |
| **Spotify Web API** | `spotipy` (Python) | Playlist-/Search-Browsing |
| **Lokale Musik** | `MPD` + `mpc` | MP3-Dateien vom NAS/USB |
| **Touch-GUI** | `PyQt5` oder `EGT` | 7-Zoll-Oberfläche |
| **Javis-Interface** | `FastAPI` (lokaler Webserver) | REST-Endpunkt für mich |
| **IR-Fernbedienung** | `LIRC` | Retro-Fernbedienung |

---

## 4. Display-Oberfläche

### Layout (1024×600 Pixel)

```
┌────────────────────────────────────────────────┐
│  [Album Art 400×400]  │  ▶ NOW PLAYING          │
│                       │  Song Title            │
│                       │  Artist                │
│                       │  ═══════════ 2:34/4:12 │
│                       │  [⏮] [⏯] [⏭]  🔊 ████░░ │
├────────────────────────┴───────────────────────┤
│  📋 Playlists  🔍 Suche  💾 Lokal  ⚙️ Settings │
└────────────────────────────────────────────────┘
```

### Screens
1. **Now Playing** — Album Art + Song + Fortschritt + Controls
2. **Playlists** — Spotify-Playlists + lokale Playlists
3. **Suche** — Spotify-Suche
4. **Einstellungen** — Lautstärke, Display-Helligkeit, Sleep-Timer

---

## 5. Javis-Integration (Wie ich ihn bediene)

### Telegram-Befehle
```
/spiele <song>      — Song suchen und abspielen
/spiele playlist    — Playlist-Auswahl starten
/pause               — Pause
/weiter              — Weiter
/next                — Nächster Track
/lautstärke 60       — Lautstärke auf 60%
/song                — Was läuft gerade?
/sound               — Sound-Profil wechseln
```

### Spracheingabe (Javis)
Ich kann auf Deutsch antworten und z.B. sagen:
- *"Javis, spiele etwas Entspannungsmusik"*
- *"Was läuft gerade auf dem Küchenplayer?"*
- *"Nächster Song bitte"*

### Jetzt-Wird-Gesprochen (TTS)
Auf dem Player kann ich Ansagen machen:
- *"Der nächste Song ist von Queen"* (Via Piper TTS auf dem Raspi)
- *"Musik ist pausiert"*

---

## 6. Gehäuse (3D-Druck)

Design-Prinzip: **"Retro-Modern"**
- Sandwich-Bauweise (Display + Raspi + Audio-HAT)
- Abgerundete Ecken, sichtbare Schrauben als Style-Element
- Material: PLA oder PETG

**Farben:**
- Gehäuse: Dunkelgrau (RAL 7016) oder Schwarz
- Frontplatte: Akzentfarbe (Orange oder Blau)
-Display-Rahmen: Schwarz

**3D-Modelle (Fusion 360):**
- `gehaeuse_boden.stl`
- `gehaeuse_deckel.stl`
- `frontplatte.stl`
- `display_ausschnitt.stl`

---

## 7. Betriebssystem & Setup

### Installation (Bookworm Lite)
```bash
# System
sudo apt update && sudo apt upgrade -y
sudo raspi-config # Expand FS, Enable SSH, Set Hostname

# Audio
sudo apt install -y alsa-utils pipewire
echo "dtparam=audio=on" >> /boot/config.txt

# PyQt5 GUI
sudo apt install -y python3-pyqt5 python3-pip
pip install spotipy requests pillow python-json-logger

# Spotify Connect
curl -L https://github.com/librespot-org/librespot/releases/download/2024.09.06/librespot_2024.09.06-1_arm64.deb -o librespot.deb
sudo dpkg -i librespot.deb

# MPD für lokale Musik
sudo apt install -y mpd mpc

# Javis API Server
pip install fastapi uvicorn
```

### Autostart
```bash
# .bashrc oder systemd service für:
# 1. Display-Login (autologin + startx optional)
# 2. Python Dashboard starten
# 3. Librespot starten
# 4. Javis API Server starten
```

---

## 8. Stromverbrauch

| Komponente | Verbrauch |
|---|---|
| Raspberry Pi 4 (idle) | ~3 W |
| Raspberry Pi 4 (Spotify) | ~5-7 W |
| 7" Display (max brightness) | ~5-7 W |
| **Gesamt** | **~10-15 W** |

→ Dauerlauf ~8 ct/Tag (bei 30 ct/kWh)

---

## 9. Kostenübersicht

| Komponente | Variante "Mini" | Variante "Vollausstattung" |
|---|---|---|
| Raspi 4 (4 GB) | 60 € | 60 € |
| 7" Touchscreen | 80 € | 80 € |
| Gehäuse (3D-Druck) | — | — |
| HiFiBerry Amp2 | — | 55 € |
| Passende Lautsprecher | — | 50 € |
| IR-Fernbedienung | 8 € | 8 € |
| **Summe** | **~150 €** | **~260 €** |

---

## 10. Zeitplanung

| Phase | Aufgabe | Aufwand |
|---|---|---|
| **1** | Hardware bestellen + Gehäuse designen | 1 Woche |
| **2** | OS aufsetzen + librespot + MPD | 1 Abend |
| **3** | PyQt5 Dashboard bauen | 1-2 Wochenenden |
| **4** | Javis API Server + Telegram-Integration | 1 Wochenende |
| **5** | 3D-Druck + Zusammenbau + Feinschliff | 1 Wochenende |

---

## 11. Nächste Schritte

- [ ] Hardware-Liste finalisieren (welcher Audio-HAT?)
- [ ] 3D-Gehause designen (Fusion 360)
- [ ] Spotify Dev Account / Librespot-Konfiguration
- [ ] Python Dashboard booten

---

*Erstellt: 2026-04-17*
*Kategorie: Hardware / Raspberry Pi / Spotify*

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
