---
id: kersbach-aktueller-status
pageType: synthesis
title: Kersbach Baustelle – Aktueller Stand
createdAt: 2026-05-21T10:25:00.000Z
updatedAt: 2026-10-26T11:50:00.000Z
sourceIds: [openproject-api, source.wasserinstallation-material-2026-10]
---

# Kersbach Baustelle – Aktueller Stand

> Stand: **26.10.2026** | Quellen: OpenProject API, Nextcloud `Projekt Haus/`,
> Saschas eigener `Sanierungsfahrplan.docx` (autoritativ), Fotodokumentation 26.09.2026

## Die Zahlen

| | Wert |
|---|---|
| **Erfasste Arbeitszeit** | **878,50 h** (227 API-Einträge, 13.08.2025 – 18.07.2026) |
| Planvolumen (Saschas Fahrplan) | **1.613 h** |
| **Real offen** | **~990 h** (909,5 h + **80,5 h Elektrik-Endmontage**) |
| davon Innenbereich | ~674,5 h |
| davon WDVS (März–Okt 2027) | 235 h |
| **Materialbudget** | **~97.033 €** (davon 60.205 € WP+FBH Fremdfirma) |
| **Eigenleistungswert** | **64.520 €** (1.613 h × 40 €/h), davon 42.080 € offen |
| Gesamtbedarf | ~161.553 € · Finanzierung 260.000 € + 84.500 € Kredit |
| Letzte Buchung | 18.07.2026 (KW29/2026, 15,0 h) – seither **14 Wochen 0h** |

## Blöcke

| # | Block | Plan | API | Rest |
|---|---|---|---|---|
| 1 | Abrissarbeiten | 288 h | 398,75 h | 0 ✅ |
| 2 | Elektrik | 183 h (vollständig: **263,5 h**) | 81 h | **~182,5 h** |
| 3 | Trockenbau | 122 h | 143 h | 0 ✅ |
| 4 | Wärmepumpe + FBH | 86 h | 96,25 h | 0 ✅ |
| 5 | Boden (Fliesen/Estrich) | 162 h | 53 h | **109 h** |
| 6 | Wandputz (Lehmputz 190 m²) | 368 h | 103,5 h | **264,5 h** |
| 7 | Decke abhängen | 140 h | 0 h | **140 h** |
| 8 | Türen einbauen | 29 h | 0 h | **29 h** |
| 9 | Fassadendämmung (WDVS) | 235 h | 0 h | **235 h** |
| 10 | Wasserinstallation | ~30 h | 0 h | **~30 h** |

> ⚠️ **Der Plan von 1.613 h ist durch Block-Überschreitungen bereits verbraucht**
> (Abriss +110,75 h, Trockenbau +21 h, WP +10,25 h).

## Bauzustand – belegt durch Fotos vom 26.09.2026

- ✅ **Estrich liegt** (glatte Fläche, grüner Randdämmstreifen, kein Trocknungsriss)
- ⏳ **Elektrik NICHT fertig**: offene Frässchlitze, Dosen nicht geschlossen,
  Hauptverteilerkasten unfertig, Leitungen hängen lose
- ⏳ **Wände**: nur grober Altputz, kein Lehmputz
- ❌ Keine Fliesen, keine abgehängte Decke, keine Türen

**Das ist die letzte belegte Sichtung.** Danach: keine Fotos in Nextcloud, keine Stunden in OpenProject.

## Kritische Kette

```
Elektrik (102 h)  ←── BLOCKIERT ALLES
   ↓
Wasserinstallation (30 h)  ←── Rohre vor dem Lehmputz
   ↓
Lehmputz 190 m² (264,5 h) + Rollputz 80 m²
   ↓
Grundieren + Fliesen (109 h)  ← Estrich liegt, nur Belag fehlt
   ↓
Türen (29 h) → Decke abhängen (140 h)
```

WDVS (235 h) läuft parallel ab Innenende, Fenster 01.03.–31.10.2027.

**Harte Constraints:**
1. Trockenbau + Sockel-Leisten vor Estrich ✅ erledigt (KW27/2026)
2. Lehmputz nach Elektrik – Schlitze und Dosen müssen mit verputzt werden
3. Wasserinstallations-Schlitze vor Lehmputz
4. WDVS nicht im Winter
5. Estrich 3–4 Wochen trocknen vor Fliesen

## Terminierung

| Rate | Innen fertig | WDVS | **Fertig** |
|---|---|---|---|
| 18,1 h/Woche (Gesamtlaufzeit) | 07.08.2027 | **06.11.2027** ⚠️ | **WDVS-Fenster verfehlt!** |
| **19,6 h/Woche (Kalenderbasis 2026)** | 16.07.2027 | bis 08.10.2027 | **08.10.2027** |
| 20,3 h/Woche (Mittel) | 06.07.2027 | bis 25.09.2027 | **25.09.2027** |
| 21,2 h/Woche (aktive Wochen) | 25.06.2027 | bis 11.09.2027 | **11.09.2027** |
| 25 h/Woche | 18.05.2027 | bis 23.07.2027 | **23.07.2027** |
| 30 h/Woche | 13.04.2027 | bis 07.06.2027 | **07.06.2027** |
| 35 h/Woche | 19.03.2027 | bis 05.05.2027 | **05.05.2027** |

> ⚠️ **Korrigiert 22.10.2026:** +80,5 h Elektrik-Endmontage und +30 h Wasserinstallation
> waren in der Innen-Berechnung nicht enthalten. Konsistent gerechnet: 25.09.2027
> statt 18.08.2027. → [[sources/scope-reconciliation|Scope-Abgleich]]
>
> ⚠️ **WDVS ist NICHT immer unkritisch:** Bei 18,1 h/Woche (Gesamtlaufzeit-Rate
> 878,5 h / 48,4 Wochen) endet das Projekt am **06.11.2027** – das WDVS-Fenster
> 01.03.–31.10.2027 ist dann **verfehlt** und die Fassade rutscht in die Saison 2028.
> Ab **19,6 h/Woche** (Kalenderbasis 2026) passt sie noch. → **Die Rate entscheidet
> über die Fassade, nicht die Fassade über die Termine.**
>
> **Die Rate ist selbst eine Rechengröße mit Unsicherheit:**
> - 2025: 311,00 h (13.08.–31.12.) ≈ 15,5 h/Woche
> - 2026: 567,50 h (KW01–KW29, 29 Kalender-Wochen) ≈ **19,6 h/Woche**
> - nur Wochen mit Buchungen: 21,2 h/Woche
> - Gesamtlaufzeit 878,50 h / 48,4 Wochen ≈ 18,1 h/Woche
>
> **In den API-Daten gibt es keine 0h-Wochen** – die 37 erfassten Wochen haben alle
> > 0 h. „KW30–KW43/2026 = 0 h" bedeutet: **keine Buchung vorhanden**, nicht
> „gearbeitet und nicht gebucht".

Saschas eigener Zeitplan sagt **27.05.2027** – er unterstellt 27–41 h/Woche, real waren
es 20,3 h/Woche über 26 Wochen. **Das WDVS-Fenster passt in allen Szenarien;
die Tagesrate ist die kritische Größe, nicht die Fassade.**

## Die 0h sind ein Buchungsproblem, kein Stillstand

**Kommunikationsstand (verifiziert 26.10.2026 aus allen Session-Trajectories,
284 Nachrichten von Sascha, 16.03.–26.09.2026):**

| | Datum | Abstand |
|---|---|---|
| Letzte **direkte Nachricht** von Sascha (Telegram) | **26.09.2026 11:30 UTC** | 30 Tage |
| Letzte **Buchung** (KW29/2026) | 18.07.2026 | 14 Wochen |
| Letzte **Foto-Aufnahme** | 26.09.2026 (15:34–20:50) | 30 Tage |
| Letzte **Datei-Upload** (letzte Aktivitätsspur) | **01.10.2026** | 25 Tage |

→ Die **14-Wochen-Lücke ist die Buchung**, die **4-Wochen-Lücke ist die
Kommunikation**. Zwei verschiedene Dinge, die oft vermischt werden.
Am 26.09.2026 hat Sascha noch geschrieben **und** Fotos geschickt – danach
4 Wochen Stille. Grund unbekannt (Urlaub? Krankheit? Reise?).
OpenProject bleibt die Source of Truth für *Stunden*, die Nachrichtenlage
für *Erreichbarkeit*.

Belege für aktive Arbeit nach dem 18.07.2026:
- **23.10.2026:** Software-Projekt **Bautagebuch** aktiv bearbeitet – Commits im Repo
  `Sadeeg/Bautagebuch` (`fb3f4cf` Test-Harness, `8ac3523` Bugfix), Teststand
  **64 Tests / 0 Fehler / 0 Errors** (Docker/JDK21). Dazu die Materialbestellung vom
  20.10.2026 (Uponor-Rohre, 410,95 €) → Start Trinkwasser-Installation.
  **Die 0h-Wochen betreffen ausschließlich die OpenProject-Buchung, nicht die Arbeit.**
- **20.10.2026:** Materialbestellung MeinHausShop 410,95 € – Uponor Uni Pipe PLUS d16 +
  S-Press Fittinge → Start Trinkwasser-Installation
- **26.09.2026:** Baustellenfotos – Estrich verlegt, Elektro-Schlitze in Arbeit
  (roh, mit Kabeln in Schlitzen)

Sascha bucht Zeiten teils Wochen später (KW28/KW29 erst am 23.09.2026 erfasst) → bei
0h-Wochen immer Nextcloud `Projekt Haus/` prüfen.

## Plan-Historie – warum sich alle Zahlen geändert haben

| | Originalplan 2025 | Bank-Fahrplan Mai 2026 |
|---|---|---|
| Eigenleistung | **763 h** / 30.500 € | **1.613 h** / 64.520 € |
| Heizung | Deckenheizung 88 m² | **Fußbodenheizung** + FBH |
| Wände | Rollputz 400 m² | Lehmputz 190 m² |
| Fassade | Innendämmung (Dach/Keller) | **WDVS** 153 m² |
| Geplantes Ende | **Juni 2026** | 27.05.2027 |

Die Umstellung auf Fußbodenheizung hat den Umfang **verdoppelt** (Estrich raus,
Türerneuerung, Trockenbauwände, erweiterte Elektrik) – und das WP-Angebot stieg
von 50.000 € auf 60.205 €. → [[sources/plan-historie|Plan-Historie]]

**Die alten Wiki-Zahlen (410 h, 660 € Rollputz) waren eine überholte Planversion,
kein Rechenfehler** – sie waren nur als „aktuell" dargestellt.

**Wichtig für die Terminierung:** Die Pläne unterstellen **2 Personen × 15 h/Woche**
(Sascha + Vater Alexander bzw. Bruder Ranan). Die Ist-Rate 20,3 h/Woche ist also
eine **Zwei-Personen**-Rate.

## Offene Entscheidungen

0. **Elektrik-Scope fixieren** – der Fahrplan führt 183 h (= nur Rohbau). Die
   Endmontage (Schalter/Steckdosen, Geräte, KNX-Programmierung, Tests) **~80 h**
   fehlt in jedem Block → realistisch **263,5 h**, also **~182,5 h offen statt 102 h**.
   → [[sources/elektrik-detailplan|Elektrik-Detailplan]] · [[sources/scope-reconciliation|Scope-Abgleich]]
0b. **Bad-Umbau 1. OG** – im Bank-Fahrplan kein Top-Level-Block, aber in OpenProject
   als #102/#132/#145/#163 geführt (Abriss erledigt, Umbau offen).
   Ebenso offen: Materialbesorgung (41 h), Unterboden-Prep (55 h), Logistik (15 h).
   → [[sources/openproject-taskbilanz|Task-Bilanz (89 Tasks)]]
1. **Rate festlegen** – 20 h/Woche (→ 18.08.2027) oder 30 h/Woche (→ 12.05.2027)?
2. **Lehmputz-Fläche** – alle 190 m² oder Kernräume zuerst?
3. **WDVS-Vergabe** – nur Material (235 h Eigenleistung bleiben) oder an die Firma?
4. **Lüftung** – Anlage (6.000–10.000 €) oder Stoßlüften?
5. **Dach- + Kellerdämmung** (190 h / 13.000 €) – mit in die WDVS-Runde 2027?
6. **Heizlast-Original** (EVEBI, 26.08.2025) anfordern – einzige Lücke in der Belegkette

## Primärquellen im Wiki (importiert 22.10.2026)

Nextcloud `Javis/` – 24 Markdown-Dateien in `raw/nextcloud-javis/`:
`Sanierungsfahrplan-Bank-komplett.md` (Originalfassung für die Bank),
`Elektrik-Zeitplan.md` (Raum-Detailplan), `Abhängigkeitsanalyse-Reihenfolge.md`,
`Wandflaechen-Berechnung.md` (190 m² Lehmputz, hergeleitet), `Zeitplan_*.md`,
`Helferliste.md`, `gantt_fahrplan.html` sowie `sanierungsaufstellung/` mit den
11 Blöcken Abriss → Fassade inkl. vollständiger Materiallisten.

## Elektrik-Material – verifiziert

`Javis/Input/Elektronik.xlsx` ausgewertet: **8.944,12 €** ausgewertete
Einkaufsliste (31 FI/LS-Sicherungen, 60 Steckdosen, 7 KNX-Raumtemperaturregler,
2.079 m Leitungen/Kabel) → **9.127 € im Fahrplan, Abweichung nur 2 %** ✅
→ [[sources/elektrik-materialliste|Elektrik-Materialliste]]

## Lücken in der Belegkette

- **Heizlast-Deeg.pdf** – Original nicht auffindbar (nur Wiki-Auszug: 10,68 kW, EVEBI)
- ~~78 Bautagebuch-Fotos fehlen~~ → **ERLEDIGT 22.10.2026:** liegen vollständig in
  `Projekt Haus/Baustellentagebuch/img/` (114 Dateien, 79/79 Buch-Referenzen auflösbar).
- **Rechnungen** teilweise belegt – **13 Belege ausgewertet: 1.664,29 €**
  (13.09.2025 – 07.02.2026, OBI/Hornbach/Baumarkt). Trockenbau, Heizung, Estrich und
  erste WDVS-Materialien sind belegt. Die Großpositionen (WP+FBH 60.205 €, WDVS 13.179 €,
  Fliesen 5.000 €, Türen 2.590 €, Elektro 9.127 €) haben **keine Belege**.
  `Kosten.xlsx` erfasst nur 319,05 € – die 13 Belege sind dort nicht verbucht.
  → [[sources/rechnungen-2025-2026|Materialbelege 2025/2026]]
- **Buchungsrückstand** 14 Wochen (KW30–KW43/2026)

## Entscheidung Fassade

**Status: EINGESCHRÄNKT** ⚠️
- Aufgrund **Bebauungsplan** ist nur **Putz mit Wärmedämmverbundsystem (WDVS)** erlaubt
- Vorgehängte hinterlüftete Fassade (VHF/Cedral) **nicht möglich**
- Konsequenz: WDVS statt Innendämmung → mehr FBH-Module, besserer U-Wert, bessere Energieklasse
- Umsetzung: 153 m², Mineralwolle 140 mm (WLG 035), U 3,3 → 0,23, 13.179 € (OBI-Paket
  59,99 €/m² + 4.000 € Gerüst), 235 h Eigenleistung

## Gestrichene / verschobene Maßnahmen

| Maßnahme | Status | Begründung |
|----------|--------|------------|
| Dachdämmung (110 h / 4.000 €) | ⏸ verschoben | in einem Zug mit dem Dach |
| Kellerdämmung (35 h / 1.800 €) | ⏸ verschoben | gehört zur WDVS-Runde 2027 |
| Solaranlage (45 h / 7.200 €) | ⏸ verschoben | zusammen mit Dach |
| Wärmepumpe | ✅ fertig | Angebot 60.205,04 € + 374,21 € Eigenleistung |

**Fokus:** WDVS 2027 → Elektrik → Innenausbau (Lehmputz, Böden)

## Prinzipien (Bautagebuch)

Siehe [[concepts/baustelle-prinzipien]]

## Related
<!-- openclaw:wiki:related:start -->
### Sources

- [[sources/openproject-api|OpenProject API v3 (Instanz Kersbach)]]
- [[sources/wasserinstallation-material-2026-10|Wasserinstallation Materialbestellung 2026-10]]
<!-- openclaw:wiki:related:end -->

## ⚠️ Task-Status korrigiert (23.10.2026)

Die OpenProject-Task-Liste **ist nicht geschlossen** – das Projekt läuft:
**52 offene Tasks** (41 „New", 11 „In progress") + 37 geschlossene.

> Die erste Fassung von `sources/openproject-taskbilanz.md` markierte **alle 89 Tasks
> als „geschlossen"** – ein Fehler meines Generators, nicht der Daten. Seite neu erzeugt.

**Zwei Rest-Maße, die nicht verwechselt werden dürfen:**
| Maß | Wert | Bedeutung |
|---|---|---|
| Rest-Schätzung auf den 52 offenen Tasks | **253 h** | was die Task-Liste kennt (alte Schätzungen, teils ohne Schätzung) |
| Planrest aus Fahrplan + Scope-Lücken | **~990 h** | verlässliche Planungsgröße |

Die ~737 h Differenz ist **keine Buchungsdifferenz**, sondern Arbeit ohne Task:
Elektrik-Endmontage 80,5 h · Wasserinstallation 30 h · Bad-Umbau 1. OG 62 h · WDVS 235 h.
→ **Der Task-Status ersetzt den Fahrplan nicht.** Nur die Zeitbuchungen sind belastbar.
