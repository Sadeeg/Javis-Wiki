---
id: source-openproject-taskbilanz
pageType: source
title: OpenProject Task-Bilanz (alle Work Packages)
createdAt: 2026-10-22T19:05:00.000Z
updatedAt: 2026-10-23T07:30:00.000Z
sourceIds: []
tags: [kersbach, openproject, taskbilanz, status]
---

# OpenProject Task-Bilanz – alle Work Packages

> **Korrigiert 23.10.2026:** Die erste Fassung dieser Seite hatte **in allen 89 Zeilen
> den Status „geschlossen"**. Das war ein Fehler des Generators, nicht der Daten.
> Korrekt aus der API: **52 offene Tasks** (41 „New", 11 „In progress") + **37 geschlossene**
> (nur über ihre Zeitbuchungen auffindbar). Die Seite wurde vollständig neu erzeugt.

## Die wichtigste Zahl auf dieser Seite

| | |
|---|---|
| **Offene Tasks** | **52** (41 New, 11 In progress) |
| Geschlossene Tasks (mit Buchung) | 37 |
| Erfasste Stunden | **878,50 h** (227 Buchungen auf 50 Tasks) |
| **Rest-Schätzung auf offenen Tasks** | **318,0 h** |
| **Planrest gesamt (Fahrplan + Scope-Lücken)** | **~990 h** |

### ⚠️ 318 h vs. ~990 h – zwei verschiedene Dinge, bitte nicht verwechseln

- **318 h** = Summe „Schätzung minus gebucht" über die **52 offenen Tasks**.
  Das ist der **Rest, den die Task-Liste selbst kennt** – mit uralten Schätzungen aus
  2025/2026 (viele Tasks haben gar keine oder eine völlig überholte Schätzung).
- **~990 h** = **Planrest aus dem Sanierungsfahrplan** (1.613 h minus 878,50 h erfasst)
  **plus die Scope-Lücken, die als Task gar nicht existieren**:
  Elektrik-Endmontage 80,5 h · Wasserinstallation 30 h · Bad-Umbau 1. OG 62 h ·
  WDVS 235 h.
- Die Lücke (~670 h) ist **keine Buchungsdifferenz**, sondern Arbeit, die im
  OpenProject **nicht als Task angelegt** ist. Der Task-Status ersetzt den Fahrplan nicht.

### ⚠️ Die Task-Liste ist kein Fortschrittsmaß

Die Schätzwerte sind teils absurd (z. B. Task „Trockenbau" mit 0 h Schätzung und 108 h
Buchung, Task „Planung Elektro" mit 36 h gebucht aber 0 h Rest). **Nur die Zeitbuchungen
sind belastbar** – die Task-Liste nicht.

## Die 52 offenen Tasks

| ID | Task | Status | geschätzt | erfasst | Rest | Buchungen | letzte Buchung |
|---|---|---|---|---|---|---|---|
| #62 | 40 – Planung Elektro | In progress | 24 h | 36.0 h | 0 h | 10 | 2026-02-27 |
| #66 | 21 – Entsorgung | In progress | 36 h | 50.0 h | 0 h | 16 | 2026-07-01 |
| #85 | 1.OG Schlafzimmer / Wintergarten Ventilator entferne | New | 0 h | 0.0 h | 0 h | 0 | – |
| #94 | Elektrik (must vor Estrich) | New | 0 h | 0.0 h | 0 h | 0 | – |
| #95 | Trockenbau | In progress | 0 h | 0.0 h | 0 h | 0 | – |
| #96 | Abriss | In progress | 0 h | 13.0 h | 0 h | 3 | 2026-02-28 |
| #98 | Wandvorbereitung | In progress | 0 h | 0.0 h | 0 h | 0 | – |
| #99 | EG Wasserleitungen Küche vorbereiten | New | 2 h | 0.0 h | 2 h | 0 | – |
| #100 | Bodenvorbereitungen | New | 0 h | 0.0 h | 0 h | 0 | – |
| #101 | Wandputz | In progress | 0 h | 0.0 h | 0 h | 0 | – |
| #102 | Badumbau 1.OG | New | 0 h | 0.0 h | 0 h | 0 | – |
| #104 | Türen ausbauen  EG + 1.OG | New | 6 h | 4.0 h | 2 h | 1 | 2026-05-27 |
| #105 | Elektrik (Optional vor Estrich) | New | 0 h | 0.0 h | 0 h | 0 | – |
| #106 | Wohnzimmer Elektrik | New | 28 h | 18.0 h | 10 h | 5 | 2026-02-28 |
| #107 | Küche Elektrik | New | 14 h | 0.0 h | 14 h | 0 | – |
| #108 | Schlafzimmer Elektrik | New | 15 h | 0.0 h | 15 h | 0 | – |
| #109 | Alex Büro Elektrik | New | 19 h | 0.0 h | 19 h | 0 | – |
| #110 | Kaminzimmer Elektrik | In progress | 19 h | 15.0 h | 4 h | 4 | 2026-05-05 |
| #111 | Zählerkasten setzten und anschließen | In progress | 16 h | 12.0 h | 4 h | 4 | 2026-05-09 |
| #112 | Verteilerkasten setzten und am Zählerkasten anschlie | In progress | 10 h | 0.0 h | 10 h | 0 | – |
| #113 | WC Duschwand | New | 12 h | 0.0 h | 12 h | 0 | – |
| #114 | EG Heizkreisverteiler Trockenbau | New | 4 h | 0.0 h | 4 h | 0 | – |
| #116 | Trockenbau Wand Leitungs- Kernborhung 1.OG | New | 10 h | 0.0 h | 10 h | 0 | – |
| #125 | Lehmputz Wohnzimmer | New | 28 h | 0.0 h | 28 h | 0 | – |
| #126 | Lehmputz Essbereich | New | 20 h | 0.0 h | 20 h | 0 | – |
| #127 | Lehmputz Küche | New | 20 h | 0.0 h | 20 h | 0 | – |
| #128 | Lehmputz Büro Alex | New | 24 h | 0.0 h | 24 h | 0 | – |
| #129 | Lehmputz Schlafzimmer | New | 24 h | 0.0 h | 24 h | 0 | – |
| #130 | Lehmputz Kaminzimmer | New | 28 h | 0.0 h | 28 h | 0 | – |
| #131 | 1.OG Abriss Bad Fließen und Estrich + Heizkörperrohr | New | 10 h | 16.0 h | 0 h | 3 | 2026-07-04 |
| #132 | Abbauen im Bad | New | 20 h | 0.0 h | 20 h | 0 | – |
| #136 | Wärmepumpe | In progress | 0 h | 0.0 h | 0 h | 0 | – |
| #145 | Bad Elektrik erstes OG | New | 8 h | 0.0 h | 8 h | 0 | – |
| #150 | Entfernen alter Rohre im Keller | New | 0 h | 5.0 h | 0 h | 1 | 2026-05-09 |
| #156 | Rohr-Arbeiten | New | 0 h | 0.0 h | 0 h | 0 | – |
| #158 | Elektrik | In progress | 0 h | 0.0 h | 0 h | 0 | – |
| #159 | Vorbereitungen für Estrich | New | 0 h | 15.0 h | 0 h | 5 | 2026-07-18 |
| #160 | DG aufräumen, Teppich und Estrich entfernen für Heiz | New | 4 h | 0.0 h | 4 h | 0 | – |
| #162 | 1.OG Spachtel Trockenbau | New | 2 h | 0.0 h | 2 h | 0 | – |
| #163 | 1.OG Bad Tür und Türrahmen entfernen | New | 3 h | 0.0 h | 3 h | 0 | – |
| #164 | 1.OG Treppenhaus Trockenbau | New | 8 h | 4.0 h | 4 h | 2 | 2026-06-28 |
| #165 | 1.OG Trockenbau Heizkreisverteiler | New | 2 h | 0.0 h | 2 h | 0 | – |
| #167 | EG Trockenbau Spachteln | New | 3 h | 0.0 h | 3 h | 0 | – |
| #169 | EG WC Leitung  Waschbecken verkleiden | New | 4 h | 2.0 h | 2 h | 2 | 2026-06-27 |
| #170 | EG Tür Wintergarten (Groß) Estrichreste entfernen | New | 1 h | 0.0 h | 1 h | 0 | – |
| #172 | EG Haustüre abschneiden für Estrichleger | New | 2 h | 0.0 h | 2 h | 0 | – |
| #173 | Allgemein – Räume freiräumen | New | 4 h | 0.0 h | 4 h | 0 | – |
| #174 | Allgemein – Boden-Löcher auffüllen | New | 2 h | 0.0 h | 2 h | 0 | – |
| #175 | Allgemein – Kanten prüfen/Putz | New | 2 h | 0.0 h | 2 h | 0 | – |
| #176 | Allgemein – Wintergarten Steckdose | New | 1 h | 0.0 h | 1 h | 0 | – |
| #177 | Einkaufen Material | New | 3 h | 3.0 h | 0 h | 2 | 2026-07-02 |
| #180 | Keller – Hobbykeller vorbereiten | New | 8 h | 0.0 h | 8 h | 0 | – |

**Summe:** geschätzt 446 h · erfasst 193.0 h · **Rest 318 h** · 41 New · 11 In progress

## Die 37 geschlossenen Tasks (mit Buchungen)

| ID | Task | erfasst | Buchungen | letzte Buchung |
|---|---|---|---|---|
| #58 | EG Trockenbau EG Eingang/WC/ Türe | 108.0 h | 28 | 2026-06-28 |
| #59 | 85 – Estrich entfernen | 78.0 h | 16 | 2026-05-04 |
| #61 | 115 – Wände Gipsputz EG entfernen | 43.0 h | 10 | 2026-01-13 |
| #64 | 80 – Wand Küche entfernen | 17.0 h | 3 | 2025-11-11 |
| #67 | 20 – Holzdecken entfernen (50 m²) | 44.0 h | 6 | 2025-10-20 |
| #68 | 18 – Tapeten entfernen | 69.0 h | 13 | 2025-09-20 |
| #72 | 6 – Laminat verlegen | 12.0 h | 2 | 2025-08-30 |
| #73 | 2 – Bodenbeläge entfernen | 33.0 h | 6 | 2025-08-25 |
| #74 | 127 – Fliesen Küche entfernen | 3.0 h | 1 | 2025-08-20 |
| #84 | 1.OG Kaminzimmer Lampen entfernen | 1.0 h | 1 | 2026-03-07 |
| #86 | Trockenbau Wand Wohnzimmer | 27.0 h | 3 | 2026-03-07 |
| #87 | Kinderzimmer ausräumen -> Wintergarten | 2.0 h | 2 | 2026-03-07 |
| #91 | 1.OG Kaminzimmer Wand vorbereitungen | 15.0 h | 5 | 2026-03-07 |
| #92 | 1.OG Schlafzimmer Wandvorbereitungen | 18.0 h | 7 | 2026-05-11 |
| #93 | 1. OG Kinderzimmer (Alex Büro) Wandvorbereitungen | 27.0 h | 8 | 2026-05-07 |
| #97 | Aushub Wärmepumpe | 7.0 h | 6 | 2026-04-09 |
| #117 | Boden Küche EG | 4.0 h | 1 | 2026-05-22 |
| #118 | Boden Ess-/Wohnzimmer EG | 8.0 h | 1 | 2026-06-03 |
| #119 | Boden WC EG | 1.0 h | 1 | 2026-06-11 |
| #120 | Boden Windfang/ Treppenhaus EG | 4.0 h | 1 | 2026-07-03 |
| #121 | Boden Treppenhaus 1.OG | 11.0 h | 2 | 2026-05-16 |
| #122 | Boden Büro Alex 1.OG | 1.5 h | 1 | 2026-03-21 |
| #123 | Boden Schlafzimmer 1.OG | 4.2 h | 2 | 2026-03-21 |
| #124 | Boden Kaminzimmer 1.OG | 4.2 h | 2 | 2026-03-21 |
| #135 | Heizkörper und Nieschen | 37.2 h | 13 | 2026-05-28 |
| #137 | Vorbereitung WP Garten und Durchgänge | 6.0 h | 1 | 2026-04-11 |
| #138 | Vorbereitung Keller für WP | 8.0 h | 1 | 2026-04-12 |
| #139 | Elektrik Wärmepumpe | 26.0 h | 4 | 2026-04-18 |
| #140 | Aushub wieder verschließen | 4.0 h | 1 | 2026-04-26 |
| #148 | Mauer im Tankraum entfernen | 9.8 h | 3 | 2026-05-29 |
| #151 | Wohnzimmer Tiefengrund | 13.0 h | 6 | 2026-02-14 |
| #152 | Tiefengrund Küche | 5.5 h | 3 | 2026-02-21 |
| #161 | 1.OG Putzrand 20 cm | 15.0 h | 3 | 2026-07-04 |
| #166 | EG - Putz 20 cm | 10.0 h | 2 | 2026-07-11 |
| #168 | EG WC altes Abflussrohr entfernen | 2.0 h | 2 | 2026-06-27 |
| #171 | EG Trockenbau Treppe | 4.0 h | 1 | 2026-07-04 |
| #179 | Keller – Heizraum vorbereiten | 3.0 h | 1 | 2026-06-27 |

**Summe erfasst auf geschlossenen Tasks:** 685.5 h
**Summe erfasst auf offenen Tasks:** 193.0 h
**Gesamt:** 878.50 h auf 50 Tasks · 227 Buchungen

## API-Hinweise
- `GET /projects/3/work_packages?pageSize=500` → **nur die 52 offenen** (41 New, 11 In progress).
  Geschlossene Tasks erscheinen dort nicht – sie sind nur über `/time_entries` auffindbar.
- `estimatedTime` und `spentTime` sind ISO-8601-Dauern; die API rechnet **8 h pro Tag**
  (`P1DT12H` = 20 h). `hours` bei Zeitbuchungen ist die echte Stundenangabe.
- `page` wird **ignoriert** (immer Seite 1), `offset` funktioniert 1-indexiert.
  `pageSize=500` fasst alle 227 Buchungen in eine Response.

→ [[sources/scope-reconciliation|Scope-Abgleich]] · [[syntheses/kersbach-status|Projektstatus]]

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[syntheses/kersbach-status|Kersbach Baustelle – Aktueller Stand]]
- [[sources/openproject-api|OpenProject API v3 (Instanz Kersbach)]]
- [[sources/scope-reconciliation|Scope-Abgleich Elektrik & Feb-vs-Mai-Plan]]
<!-- openclaw:wiki:related:end -->
