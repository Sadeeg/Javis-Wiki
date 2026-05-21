---
id: memory-import
pageType: synthesis
title: MEMORY.md – Langzeitgedächtnis Javis
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# MEMORY.md – Langzeitgedächtnis Javis

> Persistentes Wissen über Sascha, die Baustelle und OpenClaw-Setup.

---

## Termine & Zeitzone

**Zeitzone:** Deutschland verwendet UTC+1 (Winter) oder UTC+2 (Sommer)

**Kalender:** Termine immer in `deeg_shared_by_sascha` eintragen (der geteilte Kalender)

**Berechnung:**
- Winterzeit: 15:00 UTC = 16:00 MEZ
- Sommerzeit: 15:00 UTC = 17:00 MESZ

**iCal Format:** DTSTART/DTEND immer in UTC (z.B. 150000Z für 15:00 UTC)

---

## Hausrenovierung (1973er Haus)

**Erstes Wissens-Repository: `Baustelle/bau-wiki/`**
Für ALLE Fragen zur Baustelle: Erst das Wiki lesen, dann antworten.
Das Wiki enthält: Grundrisse, Kosten, Stunden, Pläne, Heizlast, Elektrik, etc.

**Thema: Vorgehängte Hinterlüftete Fassade (VHF)**

Siehe: `Baustelle/bau-wiki/wiki/konzepte/VHF-Fassade` und `Baustelle/bau-wiki/wiki/konzepte/Fassade-Material-Vergleich`

### Kerninformationen
- **Fassade:** Cedral (Faserzement) empfohlen
- **Wandfläche:** 190m² (korrigiert von 330m²)
- **Heizlast:** 10,68 kW (für WP-Dimensionierung)
- **Wohnfläche:** 151m² (inkl. 23m² Wintergarten)
- **Kaufpreis:** 298.000€
- **Bisherige Stunden:** ~500h seit Aug 2025

---

## Bautagebuch Workflow

Siehe: `Baustelle/Workflow.md`

- KW15 existiert ✅ (06.04. – 12.04.2026, 6h)
- KW16, KW17, KW18, KW19, KW20: ausstehend
- Bilder werden OpenProject gehängt, Stunden per API gebucht
- Fotos: `Baustelle/img/{YYYY}/{MM}/{dd-MM-YY_HH-MM-SS_ID}.jpg`

**Erinnerung:** Sonntag 19:00 MESZ

---

## Memory-Wiki (OpenClaw Plugin)

| | |
|---|---|
| **Vault** | `~/.openclaw/wiki/main` |
| **Repo** | git@github.com:Sadeeg/Javis-Wiki.git |
| **Auto-Push** | Täglich 22:00 MESZ per Cron |

**CLI:** `openclaw wiki compile` (nach Änderungen), `openclaw wiki status`, `openclaw wiki lint`

---

## Obsidian Vault

| | |
|---|---|
| **Pfad** | `~/.openclaw/workspace/obsidian_vault/` |
| **Sync** | Git (auto-commit nach Änderungen) |
| **Regel** | Änderungen an Notizen immer committen |

---

## Letzte Änderungen

- 2026-05-21: MEMORY.md ins Wiki importiert, Auto-Push Cron aktiviert

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
