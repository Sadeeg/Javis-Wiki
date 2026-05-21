---
id: meeting-recorder-projekt
pageType: source
title: Meeting Recorder - Projekt
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# Meeting Recorder - Projekt

> Eigenbau-Gerät für automatische Besprechungs-Protokollierung mit Sprecher-Erkennung

## Vision

Ein Raspberry Pi-basiertes Gerät, das per Knopfdruck Besprechungen aufzeichnet, automatisch transkribiert, die Sprecher erkennt, und am Ende eine strukturierte Zusammenfassung mit Action Items liefert.

**Zielgruppe:** Handwerker, Bauleiter, Familien - alle die Besprechungen festhalten wollen ohne manuell Notizen zu schreiben.

---

## Problem statement

Bei Baustellen-Besprechungen (oder anderen Besprechungen am Tisch):
- ❌ Niemand schreibt mit → hinterher vergessen
- ❌ Selbst wenn jemand tippt, geht viel verloren
- ❌ Zeit vergeudet mit nachträglichem Erinnern
- ❌ Action Items werden vergessen oder falsch zugeordnet

**Lösung:** Gerät einschalten → sprechen → fertig. Am Ende kommt eine saubere Zusammenfassung raus.

---

## Features

### Must-Have (MVP)

- [ ] **Aufnahme starten/stoppen** - Ein Knopf, LEDs zeigen Status
- [ ] **Audio aufnehmen** - Gute Mikrofon-Qualität, evtl. Array-Mic
- [ ] **Sprach-Transkription** - Whisper (lokal, kein Cloud)
- [ ] **Sprecher-Erkennung (Diarization)** - Wer hat was gesagt?
- [ ] **Zusammenfassung** - KI fasst automatisch zusammen
- [ ] **Action Items extrahieren** - "X macht Y bis Datum Z"
- [ ] **Export als Datei** - Text/Markdown zum Teilen

### Nice-to-Have

- [ ] **Display** - OLED/LCD für Statusanzeige (Aufnahme läuft, Zeit, Sprecher-Count)
- [ ] **Lokale KI-Zusammenfassung** - Ollama oder ähnlich lokal
- [ ] **Kalender-Integration** - Termin erkennen → automatisch Erinnerung
- [ ] **OpenProject-Export** - Action Items direkt als Tasks anlegen
- [ ] **Cloud-Sync** - Nextcloud oder eigener Server
- [ ] **Mehrere Sprachen** - Deutsch + Englisch erkennen

---

## Hardware

### Basis-Setup

| Komponente | Option | Preis (ca.) |
|------------|--------|-------------|
| **Raspberry Pi** | Pi Zero 2 W / Pi 4 | 15-50€ |
| **Mikrofon** | ReSpeaker USB Mic Array / ICS-43434 | 20-40€ |
| **Gehäuse** | 3D-Druck / fertiges Case | 5-20€ |
| **Display** | OLED 0.96" I2C / 1.3" LCD | 5-10€ |
| **Taster/LEDs** | Arcade-Button + RGB LED | 3-8€ |
| **Stromversorgung** | USB-Powerbank / Akku 5V | 10-20€ |

### Erweiterungen für später

- [ ]外 **GPS-Modul** - Standort der Baustelle automatisch
- [ ] **Extra-LED-Ring** - Status auf einen Blick

---

## Software-Stack

### Sprach-Erkennung

```
Whisper (faster-whisper)
├── Modell: medium (besser) oder base (schneller)
├── Sprache: de, en (per Sprache-Detektion)
└── Läuft: Lokal auf Raspberry Pi 4 / Cloud-Server
```

### Sprecher-Erkennung (Diarization)

```
pyannote-audio
├── Erkennt: Anzahl Sprecher + Zeitstempel
├── Training: Fertiges Modell nutzen (nicht selbst trainieren)
└── Problem: Sprecher-Namen? → LÖSUNG: Warm-up Phase
```

**Sprecher-Lösung - "Warm-up":**
1. Gerät startet → "Bitte stellt euch kurz vor: Ich bin [Name]"
2. Jeder Teilnehmer sagt seinen Namen (5 Sekunden)
3. System ordnet Stimme → Name zu
4. Fortan wird "[Name]:" vorangestellt

### Zusammenfassung

```
Option A: Cloud-KI (Schnell, braucht Internet)
├── GPT-4 / Claude API
└── Kosten: ~0.01€ pro Besprechung

Option B: Lokale KI (Privat, langsamer)
├── Ollama + llama3/mistral
└── Läuft auf: Starkem Pi oder lokalem Server
```

### Export

```
Zusammenfassung:
├── Markdown (.md) → Obsidian, Nextcloud
├── PDF → Teilen per Mail
└── Audio-Datei → Archivierung

Action Items:
├── OpenProject API → Tasks anlegen
├── iCal → Kalender-Einträge
└── CSV/JSON → andere Systeme
```

---

## Technical Flow

```
[1] KNOPF DRÜCKEN
         │
         ▼
[2] LEDs: BLAU (Aufnahme)
         │
         ▼
[3] Warm-up: "Ich bin [Name]" (5 sec pro Person)
         │
         ▼
[4] SPRACHE ERKENNEN (VAD)
         │
         ▼
[5] AUDIO SPEICHERN ( continuous)
         │
         ▼
[6] KNOPF DRÜCKEN (Stopp)
         │
         ▼
[7] LEDs: LILA (Verarbeitung)
         │
         ▼
[8] TRANSKRIPTION (Whisper)
         │
         ▼
[9] DIARIZATION (pyannote)
         │
         ▼
[10] ZUSAMMENFASSUNG (KI)
         │
         ▼
[11] EXPORT (Markdown/OpenProject)
         │
         ▼
[12] LEDs: GRÜN (Fertig)
```

---

## Datenstruktur

### Output: Markdown

```markdown
# Besprechung: Baustelle Kersbach
**Datum:** 2026-03-30
**Teilnehmer:** Sascha, Alexandra, Niko

## Zusammenfassung
[KI-generierte Zusammenfassung hier]

## Transkript

**[00:00 - 00:01]** Sascha:
> Ich bin Sascha.

**[00:01 - 00:02]** Alexandra:
> Ich bin Alexandra.

**[00:03 - 00:45]** Sascha:
> Die Heizung muss bis April fertig sein...

## Action Items

| Aufgabe | Person | Bis |
|---------|--------|-----|
| Heizungsbauer kontaktieren | Sascha | 05.04.2026 |
| Antrag Förderung einreichen | Alexandra | 10.04.2026 |

---
*Erstellt mit Meeting Recorder v0.1*
```

---

## Kosten-Schätzung (MVP)

| Komponente | Preis |
|------------|-------|
| Raspberry Pi 4 (4GB) | ~50€ |
| Mikrofon (ReSpeaker USB) | ~25€ |
| Gehäuse (3D-Druck) | ~5€ |
| Taster + LED | ~5€ |
| **Gesamt** | **~85€** |

---

## Zeitplan / Meilensteine

- [ ] **Phase 1:** Hardware zusammenbauen, LEDs+Taster (1 Woche)
- [ ] **Phase 2:** Audio-Aufnahme + Whisper Transkription (1 Woche)
- [ ] **Phase 3:** Sprecher-Erkennung + Warm-up (1 Woche)
- [ ] **Phase 4:** KI-Zusammenfassung integrieren (1 Woche)
- [ ] **Phase 5:** Export (Markdown/OpenProject) (1 Woche)
- [ ] **Phase 6:** Display + Gehäuse (1 Woche)

**Gesamt:** ~6 Wochen für MVP

---

## Offene Fragen

- [ ] **Sprecher-Diarization:** pyannote oder selbst gebaut?
- [ ] **Strom:** Powerbank mit autom. Abschaltung? LiPo mit USB-C?
- [ ] **Display:** OLED 0.96" reicht? Brauchts überhaupt?
- [ ] **Wo läuft Whisper?** Lokal (langsam) oder Cloud (schnell, aber Internet nötig)?
- [ ] **Benachrichtigung:** Wenn Action Item fällig → Telegram?

---

## Links & Inspiration

- [Whisper](https://github.com/openai/whisper)
- [Faster-Whisper](https://github.com/SYSTRAN/faster-whisper)
- [pyannote-audio](https://github.com/pyannote/pyannote-audio)
- [Teams Meeting Recap](https://learn.microsoft.com/en-us/microsoftteams/ai-meeting-recap)
- [Otter.ai](https://otter.ai)

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[sources/Ideen-fuer-Apps|Ideen für Apps]]
<!-- openclaw:wiki:related:end -->
