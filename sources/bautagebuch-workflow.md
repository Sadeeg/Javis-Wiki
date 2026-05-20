# Bautagebuch-Workflow — Spezifikation (v2)

> Automatisierte Erfassung von Arbeitsstunden, Fotos und Kommentaren aus OpenProject.
> **Eine Markdown-Datei pro KW** im Obsidian Vault.
> Export aller KW-Dateien zu **einer einzigen PDF** bei Bedarf.

---

## 1. Überblick

```
OpenProject                    Javis (dieses System)              Obsidian Vault
    │                                   │                            │
    │ ← Time Entries pro Tag            │                            │
    │ ← Attachments (Fotos) an WP       │                            │
    │                                   │                            │
    │              ┌─────────────────────┴───────────────────────┐   │
    │              │                                             │   │
    │              ▼                                             ▼   │
    │   SCRAPE (täglich)                             KW15.md erstellen │
    │   + Fotos runterladen                          + Fotos in      │
    │   + Bildbeschreibungen (Vision AI)               img/ Ordner   │
    │   + KW-Block bauen                                         │
    │              │                                             │
    │              ▼                                             │
    │   ERINNERUNG (Sonntag 19:00)                               │
    │   "KW XX fertig? [Ja] [Nein]"                              │
    │              │                                             │
    │              ▼                                             │
    └──────── Generierung → KW{NN}.md → Obsidian Vault ───────────┘
```

**Frequenz:** Wöchentlich — Erinnerung jeden **Sonntag um 19:00 Uhr** (MESZ) solange die Kalenderwoche noch nicht als Datei existiert.

---

## 2. Datenquellen

### 2.1 OpenProject API

| Quelle | Endpunkt | Felder |
|---|---|---|
| Time Entries | `GET /api/v3/time_entries` (alle, client-seitig filtern) | `hours`, `user`, `workPackage`, `activity`, `comment`, `spentOn` |
| Work Package Details | `GET /api/v3/work_packages/{id}` | `subject`, `status`, `percentageDone` |
| Attachments | `GET /api/v3/work_packages/{id}/attachments` | `filename`, `downloadUrl`, `createdAt` |

**Projekt-ID:** `3` (Kersbach Baustelle)
**Credentials:** `~/.openclaw/credentials/openproject.json`

### 2.2 Obsidian Vault

| Aktion | Pfad |
|---|---|
| KW-Dateien | `Obsidian Vault/Baustelle/KW/` |
| Fotos | `Obsidian Vault/Baustelle/img/{YYYY}/{MM}/` |
| Index-Datei | `Obsidian Vault/Baustelle/README.md` |

---

## 3. Verzeichnisstruktur

```
Baustelle/
├── README.md              # Übersicht / Index aller KW-Einträge
├── KW/                    # Eine Datei pro KW
│   ├── KW01.md
│   ├── KW02.md
│   └── ...
├── img/                   # Fotos, nach Jahr/Monat sortiert
│   └── {YYYY}/
│       └── {MM}/
│           └── {dd-MM-YY_HH-MM-SS_ID}.jpg
└── scripts/
    ├── openproject_scrape.py
    ├── image_describer.py
    ├── bautagebuch_template.py
    └── export_pdf.py
```

---

## 4. Workflow

### Phase 1 — Laufende Erfassung (jederzeit)

1. **Fotos** → direkt in OpenProject Web UI an das Work Package hängen
2. **Stunden** → via OpenProject buchen: `spentOn`, `hours`, `activity`, `workPackage`
3. **Kommentare** → im Time Entry `comment`-Feld

### Phase 2 — Wöchentliche Erinnerung (Sonntag 19:00 Uhr)

**Trigger:** Cron-Job jeden Sonntag um 19:00 Uhr (MESZ)
→ prüft ob `Baustelle/KW/KW{NN}.md` existiert.

**Wenn KW noch nicht existiert → Nachricht an Sascha:**

```
🦞 Hey Sascha,

📅 KW {NN} ({dd.MM. - dd.MM.YYYY}) ist noch nicht im Bautagebuch.

Heute erfasst:
  • {N}h {M}m auf {X} Work Packages
  • {Y} Fotos in OpenProject

[✅ OK, generier den Eintrag]
[✏️ Ich mach noch was fertig]
[📝 Kommentar / Beschreibung ergänzen]
```

### Phase 3 — Generierung (nach Bestätigung)

1. **Scrape** → Time Entries + Attachments für die KW aus OpenProject
2. **Fotos downloaden** → von OpenProject in `img/{YYYY}/{MM}/`
3. **Bildbeschreibung** → EXIF-Datum aus Dateinamen parsen
4. **KW-Block bauen** → `Baustelle/KW/KW{NN}.md`
5. **README updaten** → neue KW in Index eintragen

---

## 5. KW-Dateiformat

### 5.1 Dateiname

```
KW15.md   → KW {Nummer}
```

### 5.2 Inhalt

```markdown
---
tags: [bautagebuch, kw15]
datum: 2026-04-06 – 2026-04-12
---

# KW 15 – 06.04. – 12.04.2026

**Arbeitszeit gesamt:** 6h 30m

## Geleistete Arbeiten

### 🏗️ 97 – Aushub Wärmepumpe
- **Status:** In progress
- **Zeit:** 6h 30m

| Person | Stunden | Datum | Activity |
|--------|---------|-------|----------|
| Sascha Deeg | 1h 30m | 09.04. | Erdarbeiten/Aushub |
| Alexandra Deeg | 1h 30m | 09.04. | Erdarbeiten/Aushub |
| Eva Krompasky | 0h 30m | 09.04. | Erdarbeiten/Aushub |
| Tina Augsdörfer | 1h 00m | 09.04. | Erdarbeiten/Aushub |
| Anke Chaboski | 1h 30m | 09.04. | Erdarbeiten/Aushub |

### 🏗️ 58 – 133 – Trockenbau EG Eingang/WC/ Türe
- **Status:** In progress (68%)
- **Zeit:** 3h 30m

| Person | Stunden | Datum | Activity |
|--------|---------|-------|----------|
| Sascha Deeg | 3h 30m | 10.04. | Trockenbau |

## Fotos

<img src="../img/2026/04/09-04-11_17-58-32_1965.jpg" width="100">
*Aushub Grube für Wärmepumpe - Grube ausgehoben, ready für Verrohrung*

<img src="../img/2026/04/10-04-11_18-22-38_6.jpg" width="100">
*Decke im Eingangsbereich - neue Rigipsplatten montiert*

---

*Eintrag generiert: 2026-04-11*
```

---

## 6. PDF-Export

### 6.1 Anforderung

Alle KW-Dateien zu **einer einzigen PDF** zusammenführen.

### 6.2 Umsetzung

```bash
# Annahme: alle KW*.md im Baustelle/KW/ Ordner
pandoc Baustelle/KW/KW*.md \
  --pdf-engine=wkhtmltopdf \
  -o Baustelle/Bautagebuch-{jahr}.pdf
```

**Alternativ (ohne wkhtmltopdf):**
```bash
pandoc Baustelle/KW/KW*.md \
  -o Baustelle/Bautagebuch-{jahr}.pdf
```

Das Script `export_pdf.py` übernimmt:
1. Sammelt alle `KW*.md` aus `Baustelle/KW/`
2. Sortiert nach KW-Nummer
3. Generiert ein Deckblatt
4. Führt alles mit pandoc zu einer PDF zusammen

### 6.3 Deckblatt (automatisch)

```markdown
# Bautagebuch {jahr}

**Bauvorhaben:** Sanierung/Umbau, Kersbach  
**Bauherren:** Sascha Deeg und Alexandra Deeg  
**Dokumentationszeitraum:** {erste KW} – {letzte KW} {jahr}

---

## Inhaltsverzeichnis

| KW | Zeitraum | Gesamtzeit |
|----|----------|------------|
| KW 01 | 29.12.2025 – 04.01.2026 | 12h 30m |
| KW 02 | 05.01. – 11.01.2026 | 8h 00m |
...
```

---

## 7. Komponenten

### 7.1 Scripts

| Script | Beschreibung |
|---|---|
| `openproject_scrape.py` | Time Entries + Attachments aus OpenProject holen |
| `image_describer.py` | EXIF-Datum aus Dateinamen parsen |
| `bautagebuch_template.py` | KW-Block als Markdown-Datei erzeugen |
| `export_pdf.py` | Alle KW-Dateien via pandoc zu einer PDF zusammenführen |
| `cron_bautagebuch_reminder.py` | Cron-Job: KW-Status prüfen, Erinnerung senden |

### 7.2 Cron

| Job | Wann | Was |
|---|---|---|
| `bautagebuch-reminder` | Sonntag 19:00 MESZ | Prüft ob KW-Datei existiert → Erinnerung |
| *(Trigger)* | Nach Bestätigung | Vollständig: Scrape → Template → KW-Datei + Fotos |

---

## 8. Erinnerungs-Logik

```
Jeden Sonntag 19:00:
  1. Aktuelle KW bestimmen
  2. Obsidian Vault lesen → prüfen ob Baustelle/KW/KW{NN}.md existiert
  3. Wenn ja → HEARTBEAT_OK (keine Aktion)
  4. Wenn nein → Erinnerung an Sascha
```

---

## 9. Bildbeschreibung

### Priorität

1. **Manuell** — Sascha gibt eine Beschreibung ein
2. **EXIF-Datum** — aus Dateinamen parsen (`DD-MM-YY_HH-MM-SS_ID.jpg`)
3. **Vision-AI** — optional, später

### EXIF-Datum parsen

```python
# Dateiname: 09-04-11_17-58-32_1965.jpg
# = 11. April 2026, 17:58:32
from datetime import datetime
date_part, time_part, _ = "09-04-11_17-58-32_1965".split("_")
dt = datetime.strptime(f"{date_part}_{time_part}", "%d-%m-%y_%H-%M-%S")
# → 2026-04-11 17:58:32
```

---

## 10. Offene Fragen / Future

- [ ] **Vision-AI Integration** — Automatische Bildbeschreibung
- [ ] **Seitenzahlen in PDF** — automatisches Inhaltsverzeichnis
- [ ] **Deckblatt-Grafik** — Foto der Baustelle als Deckblatt
- [ ] **Mehrere Fotos pro Work Package** — zusammenfassen

---

*Zuletzt aktualisiert: 2026-04-11*

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
