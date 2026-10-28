---
id: source-sanierungsfahrplan-2026
pageType: source
title: Sanierungsfahrplan 2026 (Sascha)
createdAt: 2026-10-22T13:30:00.000Z
updatedAt: 2026-10-22T13:30:00.000Z
sourceIds: []
tags: [kersbach, sanierung, kosten, stunden, autoritaet]
---

# Sanierungsfahrplan 2026 – Saschas eigene Planung

> **Autoritative Quelle für alle Blockstunden und Materialkosten.**
> Auszug aus drei Nextcloud-Dateien in `Projekt Haus/`:
> `Saninerungsfahrplan.docx` (31.05.2026), `Zeitplan.docx` (07.06.2026),
> `Vergleiche_Stunden.xlsx` (07.06.2026).
> Vollständige Kopien: `_attachments/raw/planung/`

## Kernzahlen

| | Wert |
|---|---|
| Planvolumen gesamt | **1.613 h** |
| Material gesamt | **~97.033 €** |
| davon Wärmepumpe + FBH Fachbetrieb | 60.205,04 € |
| Eigenleistungswert (1.613 h × 40 €/h) | **64.520 €** |
| Finanzierung | 260.000 € Hauskredit + 84.500 € Sanierungskredit |

## Blöcke (Plan / gebucht laut Dokument / Delta)

| Block | Plan | gebucht | Delta offen | Material |
|---|---|---|---|---|
| Abrissarbeiten | 288 h | 272 h | 16 h | – |
| Elektrik | 183 h | 43 h | 140 h | 10.000 € |
| Trockenbau | 122 h | 78 h | 44 h | 1.200 € |
| Wärmepumpe Eigenleistung | 86 h | 84 h | 2 h | 374,21 € |
| Wärmepumpe Fachbetrieb | – | – | – | 60.205,04 € |
| Bodenbeläge | 162 h | 0 h | 162 h | 5.000 € |
| Wandputz | **368 h** | 84 h | 284 h | 1.064 € |
| Decken | 140 h | 0 h | 140 h | 1.600 € |
| Türen | 29 h | 0 h | 29 h | 2.590 € |
| Fassade (WDVS) | 235 h | 0 h | 235 h | 15.000 € |
| **Summe** | **1.613 h** | **561 h** | **1.052 h** | **97.033 €** |

> Die „gebucht"-Spalte ist der Dokumentstand (25.05.2026). Der tatsächliche API-Stand
> (22.10.2026) liegt bei **878,50 h** – die Blöcke Abriss, Trockenbau und Wärmepumpe
> haben ihren Planwert überschritten.

## Warum der Plan von 763 h auf 1.613 h gewachsen ist

1. **Decken- → Fußbodenheizung**: Estrich entfernen, alle Innentüren und Haustür ausbauen,
   Trockenbau-Vorbereitungen für Estrich, Verteilerkästen, Elektrikverkleidung
   → Abriss 145 h → 288 h
2. **Trockenbau-Wände für Elektrik** (33,29 m²): Wohnzimmer, Esszimmer, Gänge,
   Heizkreisverteiler-Verkleidung, Kernbohrung kaschieren, WC auf Dusch-WC vorbereiten
3. **WDVS statt Innendämmung** → mehr FBH-Module, besserer U-Wert
4. **Wärmepumpen-Angebot 50.000 € → 60.205 €** (+20 %)

## Saschas Zeitplan (Zeitplan.docx)

| Block | Zeitraum | implizierte Rate |
|---|---|---|
| Abriss | 13.08.25 – 20.06.26 | |
| Elektrik Planung | 25.08.25 – 04.04.26 | |
| Trockenbau | 17.01.26 – 20.06.26 | |
| Wärmepumpe | 04.04.26 – 26.04.26 | |
| Elektrik | 04.04.26 – 30.09.26 | 7,1 h/Woche (parallel) |
| FBH | 18.06.26 – 31.08.26 | |
| **Lehmputz** | 30.09.26 – 02.12.26 | **40,9 h/Woche** |
| Boden | 02.12.26 – 13.01.27 | 27,0 h/Woche |
| Decke | 13.01.27 – 17.02.27 | 28,0 h/Woche |
| Türen | 17.02.27 – 24.02.27 | 29,0 h/Woche |
| **WDVS** | 01.04.27 – 27.05.27 | 29,4 h/Woche |
| **Ende** | **27.05.2027** | |

> Der Plan unterstellt 27–41 h/Woche. Real wurden KW03–KW29/2026 ⌀ **20,3 h/Woche** gebucht.

## Verschoben (bewusst, nicht gestrichen)

Dachdämmung 110 h / 4.000 € · Kellerdämmung 35 h / 1.800 € · Solaranlage 45 h / 7.200 €
→ 190 h / 13.000 €, gehören zur WDVS-Runde 2027.

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[syntheses/baustelle-wiki-index|Index – Kersbach Baustelle Wiki]]
- [[sources/scope-reconciliation|Scope-Abgleich Elektrik & Feb-vs-Mai-Plan]]
<!-- openclaw:wiki:related:end -->
