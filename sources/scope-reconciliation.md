---
id: source-scope-reconciliation
pageType: source
title: Scope-Abgleich Elektrik & Feb-vs-Mai-Plan
createdAt: 2026-10-22T17:20:00.000Z
updatedAt: 2026-10-28T16:30:00.000Z
sourceIds: []
tags: [kersbach, elektrik, terminierung, recon, luecke]
---

# Scope-Abgleich – was im Fahrplan fehlt

> Grundlage: 24 Nextcloud-Primärquellen `Javis/` (importiert 22.10.2026),
> vgl. [[sources/elektrik-detailplan|Elektrik-Detailplan]] und
> [[sources/sanierungsfahrplan-2026|Sanierungsfahrplan 2026]].

## 1. Elektrik: vier Zahlen, ein Block

| Plan | Summe | Was drin ist |
|---|---|---|
| 9-Schritt-Plan (Bank-Fahrplan, 25.05.2026) | **183 h** | Planung, Fräsen, Leitungen, Zählerschrank, Verteiler klemmen, Taster, KNX-Geräte, Verputzen, Test |
| Raum-Detailplan **Rohbau** (03.03.2026) | **183,5 h** | nur Rohbau: Planung, Fräsen, Dosen, Leitungen, Verputzen, Säubern |
| Raum-Detailplan **komplett** (03.03.2026) | **224,1 h** | Rohbau + Schalter/Steckdosen-Endmontage (~40 h) |
| **Rohbau + Endmontage komplett** | **263,5 h** | zusätzlich KNX-Programmierung (~20 h) + Tests/Inbetriebnahme (~10 h) |

**Der Bank-Fahrplan führt 183 h – das ist der Rohbau-Umfang. Die Endmontage
(Schalter/Steckdosen montieren, Geräte anschließen, KNX-Programmierung,
Inbetriebnahme = **~80 h**) ist in keinem Block enthalten.**

⚠️ **Nicht addierbar:** 9-Schritt-Plan und Raum-Detailplan überlappen.
Realistische Größenordnung: **~200–265 h** je nach Auslegung, mit Sicherheit
**mehr als die 102 h**, die der Fahrplan als „Elektrik offen" ausweist.

### Die Kette, die daraus folgt

```
Elektrik-ROHBAU (183,5 h)
   → Schlitze müssen TROCKNEN (Trocknungszeit einplanen)
      → Lehmputz (264,5 h)
         → Elektrik-ENDMONTAGE (80 h)   ← Schalter sitzen auf dem Putz
            → Funktionstest / Inbetriebnahme (10 h)
```

**Die Endmontage liegt zeitlich hinter dem Lehmputz**, nicht davor. Sie verlängert
also nicht die Vorlaufzeit, sondern die Schlussphase.

## 1b. Harte Zahlen zur Endmontage (aus EG-Planung-für-KI.ods)

Die Elektrik-Planungs-ODS (9 Raumblätter) wurde ausgewertet – das ist die
Plangrundlage des 224,1-h-Detailplans.

> 📎 **Primärquelle jetzt im Wiki:** `EG-Planung-für-KI.ods` (30.533 Bytes)
> liegt seit 28.10.2026 unter
> `_attachments/raw/planung/elektrik/EG-Planung-fuer-KI.ods` und kann damit
> direkt nachgerechnet werden. Die Tabelle unten ist **am 28.10.2026 gegen die
> Datei verifiziert** – siehe [[sources/anhang-audit-2026-10-28]].

| Raum | Zuleitungen | Sicherungen | Dosen | Schalter | Steckdosen | Geräte | KNX-Punkte |
|---|---|---|---|---|---|---|---|
| WC (EG) | 4 | 1 | 5 | 1 | 4 | 5 | 5 |
| Küche (EG) | 17 | 8 | 25 | 4 | 19 | 25 | 15 |
| Wohnzimmer (EG) | 26 | 6 | 35 | 4 | 21 | 35 | 20 |
| Treppenhaus + Eingang EG | 10 | 3 | 15 | 6 | 8 | 16 | 13 |
| Alex Büro (1. OG) | 4 | 2 | 10 | 2 | 7 | 10 | 8 |
| Schlafzimmer (1. OG) | 4 | 1 | 18 | 4 | 13 | 18 | 10 |
| Kinderzimmer (1. OG) | 4 | 1 | 10 | 2 | 7 | 10 | 8 |
| Bad | 2 | 2 | 8 | 3 | 5 | 8 | 8 |
| Treppenhaus 1. OG | 2 | 1 | 8 | 4 | 3 | 9 | 8 |
| **Summe** | **73** | **25** | **134** | **30** | **87** | **136** | **95** |

**Plausibilitätsprüfung der Endmontage-Schätzung:**
- **348 Endmontage-Positionen** (30 Schalter + 87 Steckdosen + 136 Geräte + 95 KNX)
- 40 h Endmontage → **6,9 min/Position** ✔ realistisch
- 20 h KNX-Programmierung → **12,6 min/KNX-Punkt** ✔ realistisch (ETS)

→ **Die ~80 h Endmontage sind durch die Planungsdaten gedeckt, nicht geraten.**

⚠️ Kleine Abweichung: die ODS listet **73** Zuleitungen, der Detailplan nennt **91**.
Die Summe-Zellen der 1.-OG-Blätter sind in der ODS leer, die Planzahlen sind dort
etwas höher. Dosen (134) und Sicherungen (25/24) stimmen exakt. → Plan oder ODS
ist die ältere Fassung – **klein, aber eine offene Mini-Frage.**

### Verifikation gegen die ODS (28.10.2026) – Ergebnis

Die Tabelle oben wurde aus den 9 Blättern der ODS **neu berechnet**, nicht
übernommen:

| Blatt | Zuleitungen (ODS) | Zuleitungen (Wiki-Tabelle) | Quelle im Blatt |
|---|---|---|---|
| WC | 4 | 4 | Summe-Zeile |
| Küche | 17 | 17 | Summe-Zeile |
| Wohnzimmer | 26 | 26 | Summe-Zeile |
| Treppenhaus + Eingang EG | 10 | 10 | Summe-Zeile |
| Alex Büro | **8** | 4 | keine Summe-Zeile |
| Schlafzimmer | **8** | 4 | keine Summe-Zeile |
| Kinderzimmer | **9** | 4 | keine Summe-Zeile |
| Bad | **5** | 2 | keine Summe-Zeile |
| Treppenhaus 1. OG | **8** | 2 | keine Summe-Zeile |
| **Summe** | **95** | **73** | |

**Ergebnis 1 – die Endmontage-Schätzung ist bestätigt.** Die sechs übrigen
Spalten (Sicherungen, Dosen, Schalter, Steckdosen, Geräte, KNX) sind **alle 54
Werte exakt reproduzierbar**. Damit stehen die **348 Endmontage-Positionen**
(30 + 87 + 136 + 95) auf einer geprüften Grundlage – die ~80 h Endmontage sind
**nicht geraten**.

**Ergebnis 2 – die Spalte „Zuleitungen" war bei den 1.-OG-Räumen falsch
übernommen.** In den 4 EG-Blättern steht die „Summe"-Zeile (NYM + CAT7) im
Blatt, und die Wiki-Zahlen (4/17/26/10) stimmen damit exakt. In den 5
1.-OG-Blättern ist diese **Summe-Zelle leer** – und die Werte 4/4/4/2/2 der
Wiki-Tabelle sind durch **keine** konsistente Regel reproduzierbar: nur NYM
ergäbe 4/4/5/3/6, NYM + CAT7 ergibt 8/8/9/5/8. → **+22 Zuleitungen fehlen**
(95 statt 73).

**Ergebnis 3 – die offene Mini-Frage ist damit aufgelöst.** Die frühere
Diskrepanz „ODS 73 vs. Detailplan 91" (18) war ein Artefakt der falschen
1.-OG-Zahlen. Mit der korrekten ODS-Summe **95** liegt der Detailplan mit 91
nur noch **4** auseinander → **die ODS ist die neuere und vollständigere
Fassung**, nicht die ältere.

> ⚠️ **Konsequenz:** Die Spalte „Zuleitungen" dieser Tabelle darf künftig nicht
> als Summe 73 zitiert werden – korrekt sind **95** (alle 9 Blätter, inkl.
> CAT7/KNX/Netzwerk). Für die Endmontage-Schätzung ist die Zahl **ohne
> Bedeutung** (dort zählen nur Schalter, Steckdosen, Geräte und KNX-Punkte).
> Die 348 Positionen bleiben unverändert gültig.

## 2. Februar-Plan (788 h, 20 Blöcke) vs. Mai-Fahrplan (1.613 h, 9 Blöcke)

Der Zeitplan vom 23.02.2026 kennt Blöcke, die im Bank-Fahrplan vom 25.05.2026
**nicht vorkommen**:

| Block (Feb-Plan) | Stunden | im Mai-Fahrplan? |
|---|---|---|
| Bad-Umbau 1. OG | 62 h | ⚠️ kein Top-Level-Block, **aber** in OpenProject als #102/#132/#145/#163 geführt |
| Unterboden-Prep | 55 h | ❌ nicht als Block |
| Materialbesorgung (pauschal) | 41 h | ❌ nicht als Block |
| Entsorgung (pauschal) | 30 h | ✅ in Abriss (#66, 44 h) |
| Wasserleitung Küche | 20 h | ❌ **nicht als Block** – passt zur Trinkwasser-Installation Okt 2026 |
| Aushub Fundament WP | 19 h | ✅ in Wärmepumpe |
| Lehmputz-Logistik (500 kg) | 15 h | ❌ nicht als Block |
| Heizungsnischen | 15 h | ✅ in Wärmepumpe (#135) |
| TÜV Anhänger | 9 h | ❌ nicht als Block |
| Haustür provisorisch | 9 h | ✅ in Abriss (#103) |
| BLOCKER (Termin Dad, Verteilerkasten) | 11 h | ❌ nicht als Block |

**→ Bis zu ~180 h könnten außerhalb der 9 Blöcke liegen** – entweder in anderen
Blöcken absorbiert oder tatsächlich nicht geplant. Das ist mit Sascha zu klären.

### Bad (1. OG) – der am deutlichsten markierte Blocker

Der Bad-Umbau ist im Feb-Plan mit **62 h** und in der Abhängigkeitsanalyse als
**„muss als ALLERLETZTES raus (Anfang Mai)"** geführt.

**Korrektur (22.10.2026, nach Task-Bilanz):** Die Aussage „im Bank-Fahrplan gibt es
keinen Bad-Block" war **zu stark**. In OpenProject existieren vier Bad-Tasks:

| Task | geschätzt | erfasst | Status |
|---|---|---|---|
| #131 1.OG Abriss Bad Fließen und Estrich + Heizkörperrohre | 10 h | **16 h** | ✅ erledigt |
| #132 Abbauen im Bad | 20 h | 0 h | ⬜ offen |
| #145 Bad Elektrik erstes OG | 8 h | 0 h | ⬜ offen |
| #163 1.OG Bad Tür und Türrahmen entfernen | 3 h | 0 h | ⬜ offen |
| #102 Badumbau 1.OG | – | 0 h | ⬜ offen |

→ Der **Abriss-Teil ist erledigt** (#131, 16 h – passt zum Estrichfoto vom
26.09.2026: Bad-Fliesen raus, Estrich darüber). Der **Umbau selbst ist offen**,
ist aber **keine vergessene Scope-Lücke** im Blockplan – nur kein Top-Level-Block.

→ [[sources/openproject-taskbilanz|OpenProject Task-Bilanz]]

## 3. Korrigierte Restterminierung

Basis: Innen offen = 644,5 h (Basisblöcke) + 30 h (Wasserinstallation)
+ **80,5 h (Elektrik-Endmontage)** = **755 h**; WDVS 235 h; Start KW43/2026 (19.10.2026).

| Rate | Innen fertig | WDVS | **Fertig** | vorher berechnet |
|---|---|---|---|---|
| **20,3 h/Woche (Ist-Rate)** | 06.07.2027 | – 25.09.2027 | **25.09.2027** | 18.08.2027 |
| 25 h/Woche | 18.05.2027 | – 23.07.2027 | **23.07.2027** | 22.06.2027 |
| 30 h/Woche | 13.04.2027 | – 07.06.2027 | **07.06.2027** | 12.05.2027 |
| 35 h/Woche | 19.03.2027 | – 05.05.2027 | **05.05.2027** | 17.04.2027 |

⚠️ **Die „vorher"-Spalte ist nicht nur durch die +80,5 h verschoben**, sie war auch
in sich inkonsistent: die 30 h Wasserinstallation waren im Innen-Pool nicht
enthalten. Konsistent gerechnet (ohne Endmontage, mit Wasser) ergibt sich
**29.08.2027** statt 18.08.2027 – die echte Verschiebung durch die Endmontage
beträgt also **+4,0 Wochen**.

**Das WDVS-Fenster (01.03.–31.10.2027) bleibt in allen Szenarien unkritisch.**

## 4. Was das für die Offenen Entscheidungen heißt

1. **Elektrik-Scope fixieren** (200 h? 224 h? 263,5 h?) – davon hängt die Terminierung ab
2. **Bad-Umbau 1. OG** – in OpenProject als Tasks geführt (Abriss erledigt, Umbau offen),
   aber ohne Top-Level-Block im 1.613-h-Fahrplan. Blockgröße klären.
3. **Materialbesorgung/Entsorgung/Logistik** – eigene Blöcke oder in den Gewerken?
4. **Rate festlegen** – 20,3 h (→ 25.09.2027) oder 30 h (→ 07.06.2027)?

## 4. Verifikation gegen das Primärdokument (28.10.2026)

Der Juni-Fahrplan (`Saninerungsfahrplan.docx`, 31.05.2026, Nextcloud
`Projekt Haus/`) wurde **am 28.10.2026 im Original ausgelesen** (40.205 Bytes,
506 Absätze) und die Blocktabelle dagegen geprüft:

| Block | Plan (Wiki) | Plan (Original-Dokument) | Material (Original) |
|---|---|---|---|
| Abrissarbeiten | 288 h | „Summe gebucht: 272 h \| Geplant gesamt: ~288 h" | – |
| Elektrik | 183 h | 183 h | „9.127,45 € / ca. 10.000 €" |
| Trockenbau | 122 h | ~122 h | ~1.200 € |
| Wärmepumpe + FBH | 86 h | 86 h | 60.579 € |
| Bodenbeläge | 162 h | 162 h | 5.000 € |
| Wandputz | 368 h | ~368 h | 1.064 € |
| Decken | 140 h | ~140 h | 1.600 € |
| Türen | 29 h | ~29 h | 2.590 € |
| Fassade (WDVS) | 235 h | 235 h | 15.000 € |
| **Summe** | **1.613 h** | **~1.613 h** | **~97.033 €** |

→ Die Blocktabelle in [[sources/sanierungsfahrplan-2026]] ist **faithful**; auch
die Materialsumme (97.033 €) und der gebuchte Stand (561 h) stehen so im
Original. Ergänzend verifiziert: **878,50 h gebuchte Arbeitszeit** aus der
OpenProject-API (227 Einträge, 13.08.2025 – 18.07.2026).

### Der Bad-Umbau 1. OG (62 h) wird NICHT zusätzlich addiert

Die 62 h stammen aus dem **März-Feinplan** (`Zeitplan_Fussbodenheizung.md`,
03.03.2026): dort ist der Bad-Umbau ein **eigenes Arbeitspaket**
(38 h ohne Puffer / 42 h mit 10 % Puffer / 62 h mit Risiko-Puffer).

Im Juni-Fahrplan gibt es **keinen Bad-Block** – das Bad kommt dort nur
**ein einziges Mal** vor, als Zeit-Hinweis im Änderungsabschnitt:

> „Fliesen und Estrich im Bad (zeitlich so spät wie möglich vor der
> Fußbodenheizung geplant, da wir weiterhin im OG wohnen)"

Die Bad-Arbeiten stecken in den vorhandenen Blöcken:

| Bad-Teil | Task / Block | Rest |
|---|---|---|
| Abbauen | #131 (16 h, erledigt), #102 Badumbau → Kind von WP 96 Abriss | 0 h (Abriss überbucht) |
| Fliesen/Estrich | Bodenbeläge | 109 h |
| Putz | Wandputz | 264,5 h |
| Elektrik | #145 Bad Elektrik → Kind von WP 94 Elektrik | in 182,5 h enthalten |

→ **Die 62 h sind bereits in den 990 h enthalten.** Sie **nicht** zusätzlich
zu addieren – das wäre eine Doppelzählung und würde den Fertigtermin
fälschlich um ~3 Wochen verschieben. Offen bleibt allein: **#102 Badumbau
hat keine Stundenschätzung** – die Task-Liste kennt für den Bad-Umbau
selbst keine verlässliche Größe.

### Auflösung der Zuordnung (28.10.2026, 2. Nachweis)

Mit den Task-Namen aller 50 Workpackages lässt sich die Zuordnung der
182 h auf WP 159 **reproduzierbar** auflösen (nicht mehr nur geschätzt):

| WP 159 – Kind | h | Einordnung |
|---|---|---|
| 58 EG Trockenbau EG Eingang/WC/Türe | 108 | Trockenbau |
| 131 1.OG Abriss Bad Fließen/Estrich + Heizkörperrohre | 16 | Abriss (Bad) |
| 161 1.OG Putzrand 20 cm | 15 | Trockenbau |
| 166 EG – Putz 20 cm | 10 | Trockenbau |
| 171 EG Trockenbau Treppe | 4 | Trockenbau |
| 164 1.OG Treppenhaus Trockenbau | 4 | Trockenbau |
| 177 Einkaufen Material | 3 | Boden |
| 179 Keller – Heizraum vorbereiten | 3 | Boden |
| 169 EG WC Leitung Waschbecken verkleiden | 2 | Trockenbau |
| 168 EG WC altes Abflussrohr entfernen | 2 | Abriss |
| 159 selbst | 15 | Estrich-Vorbereitung → Boden |

→ **Trockenbau 141 h + 2 h = 143 h** – das ist **exakt** der Wert, der im
Wiki steht. Die Zuordnung ist damit **bestätigt, nicht geraten**.

### Warum die offenen Stunden zwischen 920 h und 990 h liegen

Offen = Plan − Σ min(Plan_b, gebucht_b). Jede gebuchte Stunde, die auf einen
**überbuchten** Block fällt, reduziert den Rest **nicht** – sie ist
verbraucht, ohne Plan abzubauen. Genau das erzeugt die Bandbreite:

| Block | Plan | gebucht (API) | überbucht | wirkt auf den Rest |
|---|---|---|---|---|
| Abriss | 288 h | 398,75 h | 40,75 h | nein |
| Trockenbau | 122 h | 143 h | 21 h | nein |
| Wärmepumpe + FBH | 86 h | 96,25 h | 10,25 h | nein |

Die **72 h Überbuchung** sind unvermeidbar – Abriss war 110,75 h teurer
geplant, Trockenbau 21 h, Wärmepumpe 10,25 h. Sie sind in den 990 h bereits
berücksichtigt.

Zusätzlich hängen **70 h** der „Vorbereitungen für Estrich" am Abriss-Block
(dort ohne Wirkung auf den Rest). Würden sie stattdessen Wandputz oder Boden
zugeordnet (beide haben Reserve), sänke der Rest um bis zu 70 h.

→ **Bandbreite der offenen Stunden: ~920 h bis 990 h.** Der dokumentierte Wert
**990 h ist das konservative Ende** (nicht die optimistische Schätzung).
Zur Erinnerung: Elektrik-Endmontage 80,5 h und Wasserinstallation 30 h sind
darin enthalten, der **Bad-Umbau ebenfalls**.

### Die 84 h Differenz „368 h vs. 284 h" sind die Aufteilung Vorbereitung/Auftrag

Der Wandputz-Block des Primärdokuments lässt sich vollständig auflösen
(`Saninerungsfahrplan.docx`, Block 6, Zeitschätzung):

| Arbeitsschritt | Fläche | Zeit/m² | Gesamt |
|---|---|---|---|
| Vorbereitung (Abschleifen) | 190 m² | – | **84 h** |
| Lehmputz auftragen | 190 m² | 1,2 h | ~228 h |
| Rollputz | 80 m² | 0,7 h | ~56 h |
| **Summe** | **270 m²** | | **~368 h** |

→ **84 + 228 + 56 = 368 h** ✅ exakt. Die im Wiki genannten „~284 h" sind
**228 + 56 = die reine Auftragszeit** – es ist also **kein Widerspruch**,
sondern die Sicht auf denselben Block ohne den Vorbereitungsteil.

**Entscheidend:** Die 84 h Vorbereitung sind in OpenProject **bereits gebucht**
(121,5 h auf WP 101 „Wandputz" → WP 98 „Wandvorbereitung":
43 Gipsputz EG entfernen · 27 Alex Büro · 18 Schlafzimmer · 15 Kaminzimmer ·
13 Wohnzimmer Tiefengrund · 5,5 Küche Tiefengrund).
→ Der offene Rest von 264,5 h ist damit **reine Auftragsarbeit**
(Lehmputz + Rollputz), **keine Doppelzählung einer erledigten Vorbereitung**.

**Gleiches Muster im Boden-Block (162 h):** Grundieren 12 h · Fliesen schneiden
& verlegen 100 h · Verfugen + Reinigung 50 h. Das Primärdokument führt dort
„Gebucht: –"; die 38 h Bodenvorbereitung stehen laut eigener Tabelle des
Dokuments (#100) **im Wärmepumpe-Block**, nicht im Boden-Block. Die 162 h
sind also tatsächlich unberührt → die Zurechnung von 53 h (Boden gebucht)
ist die **konservative** Variante.

→ **Zweite, unabhängige Bestätigung:** Die gebuchten Stunden decken
überall die **Vorbereitungsarbeiten** ab, die offenen Stunden sind reine
Ausführungsarbeit. Die dokumentierten 990 h sind damit erneut das
**konservative Ende** (die Zurechnung der 53 h Boden-Stunden auf den
Boden-Block unterdrückt den Rest).

### Auswirkung auf den Fertigtermin

| offene Stunden | 20,3 h/Woche | 25 h/Woche | 30 h/Woche |
|---|---|---|---|
| 920 h | ~11.09.2027 | ~28.06.2027 | ~13.05.2027 |
| **990 h (dokumentiert)** | **25.09.2027** | **23.07.2027** | **07.06.2027** |

→ Das **WDVS-Fenster (01.03.–31.10.2027) bleibt in beiden Fällen unkritisch**,
bei der dokumentierten Rate mit 5 Wochen Reserve.

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[sources/anhang-audit-2026-10-28|Anhang-Audit Wiki-Vault (28.10.2026)]]
- [[syntheses/baustelle-wiki-index|Index – Kersbach Baustelle Wiki]]
- [[syntheses/kersbach-status|Kersbach Baustelle – Aktueller Stand]]
- [[sources/openproject-taskbilanz|OpenProject Task-Bilanz (alle Work Packages)]]
<!-- openclaw:wiki:related:end -->
