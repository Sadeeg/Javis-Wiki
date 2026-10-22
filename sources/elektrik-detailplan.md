---
id: source-elektrik-detailplan
pageType: source
title: Elektrik-Detailplan (03.03.2026)
createdAt: 2026-10-22T16:50:00.000Z
updatedAt: 2026-10-22T16:50:00.000Z
sourceIds: []
tags: [kersbach, elektrik, blocker, detailplan]
---

# Elektrik-Detailplan – Raum-für-Raum-Aufstellung

> **Quelle:** Nextcloud `Javis/Elektrik-Zeitplan.md`, erstellt **03.03.2026** aus der
> Elektro-Planung (Excel). Plus `Javis/Elektrik-Zeitplan-Rohbau.md` und
> `Javis/Abhängigkeitsanalyse-Reihenfolge.md` (24.02.2026, Deck-Board „Refinement", 62 Aufgaben).
> Volltext: `raw/nextcloud-javis/Elektrik-Zeitplan.md`

## Umfang

**91 Zuleitungen · 24 Sicherungen · 134 Dosen/Geräte**
Basis: 2 Personen × 15 h/Woche = 30 h/Woche, 10 % Puffer für Nicht-Handwerker.

## Standardzeiten

| Tätigkeit | Basis | +10 % |
|---|---|---|
| Planung/Markieren pro Raum | 1 h | 1,1 h |
| Schlitz fräsen (pro Leitung) | 45 min | 50 min |
| Unterputzdose setzen | 30 min | 33 min |
| Schalterdose setzen | 25 min | 28 min |
| Leitung verlegen (pro m) | 15 min | 17 min |
| Netzwerkdose setzen | 20 min | 22 min |
| Schlitze verputzen (pro m) | 30 min | 33 min |
| Abdecken/Säubern pro Raum | 1 h | 1,1 h |

## Gesamtsumme nach Raum

| Raum | Leitungen | Sicherungen | Dosen/Geräte | ohne Puffer | mit 10 % |
|---|---|---|---|---|---|
| WC (EG) | 4 | 1 | 5 | 8,1 h | **8,9 h** |
| Küche (EG) | 17 | 8 | 25 | 32,8 h | **36,1 h** |
| Wohnzimmer (EG) | 26 | 6 | 35 | 50,6 h | **55,7 h** |
| Alex Büro (1. OG) | 10 | 3 | 16 | 21,3 h | **23,4 h** |
| Schlafzimmer (1. OG) | 8 | 2 | 10 | 17,3 h | **19,0 h** |
| Kinderzimmer (1. OG) | 7 | 1 | 10 | 15,5 h | **17,1 h** |
| Treppenhaus (1. OG) | 7 | 1 | 10 | 16,1 h | **17,7 h** |
| Treppenhaus + Eingang (EG) | 8 | 1 | 18 | 33,8 h | **37,2 h** |
| Bad | 4 | 1 | 5 | 8,2 h | **9,0 h** |
| **GESAMT** | **91** | **24** | **134** | **203,7 h** | **224,1 h** |

## Phasenplan (bei 30 h/Woche, 2 Personen)

| Phase | Stunden | Wochen | KW |
|---|---|---|---|
| EG (WC, Küche, Wohnzimmer, Treppenhaus) | 137,9 h | ~4,6 | KW 10–15 |
| 1. OG (Alex, Schlafzimmer, Kinderzimmer, Treppenhaus) | 76,2 h | ~2,5 | KW 16–19 |
| Bad + Rest | 10 h | ~0,3 | KW 20 |
| **Gesamt** | **224,1 h** | **~7,5** | **~2 Monate** |

Realistischer Zeitraum Anfang März bis Anfang Mai.

## Die zwei Elektrik-Pläne – und warum sie sich widersprechen

| Plan | Summe | Charakter |
|---|---|---|
| **9-Schritt-Plan** (im Sanierungsfahrplan) | **183 h** | pauschal: Planung 12 · Fräsen+Dosen 30 · Leitungen 40 · Zählerschrank 12 · Verteiler klemmen 25 · Taster klemmen 12 · KNX 10 · Verputzen 30 · Funktionstest 12 |
| **Raum-Detailplan** (dieses Dokument) | **224,1 h** | Arbeitsschritte je Raum × Menge, mit 10 % Puffer |
| **OpenProject-Stand 22.10.2026** | **81 h gebucht / ~102 h offen** | Ist-Stand |

**Die beiden Pläne überlappen, sie sind nicht addierbar.** Der 9-Schritt-Plan enthält
~49 h zentrale Aufgaben (Zählerschrank, Verteiler, Taster, KNX, Test), die im
Raum-Plan als „Leitungen verlegen" oder gar nicht enthalten sind. Der Raum-Plan
enthält dagegen wiederum Raumabdeckung/Säubern, die der 9-Schritt-Plan nicht führt.

**Realistische Größenordnung: 200–225 h für die Elektrik insgesamt**, also
**~120–145 h offen** – mehr als die 102 h, die der Sanierungsfahrplan (183 h)
ausweisen. → Offene Entscheidung, siehe [[syntheses/kersbach-status|Kersbach Status]].

## Abhängigkeiten (Deck-Board-Analyse 24.02.2026)

Drei kritische Pfad-Abhängigkeiten:
1. 🔥 **Bad (1. OG)** – muss als **allerletztes** raus (Anfang Mai)
2. 🌡️ **Heizung außer Betrieb** – blockiert Heizungsnischen in 5 Räumen
3. ⚡ **Elektrik-Gesamtabschluss** – Finale Tests nach dem Verteilerkasten

**Verteilerkasten:** blockiert *nicht* die Dosen-/Leitungsarbeit (Leitungen können bis
zum Kasten gezogen werden), sondern nur den finalen Anschluss, die Systemtests und
die Inbetriebnahme. → Das ist der Grund, warum die Fotodokumentation vom 26.09.2026
(Verteilerkasten unfertig) die Elektrik blockiert, aber die ~134 Dosen parallel
weitergebaut werden können.

**Empfohlene Strategie (3 Phasen, parallel):**
1. Woche 1–3: Vorbereitung + Elektrik EG
2. Woche 4–7: Elektrik 1. OG + Lehmputz EG
3. Woche 8–11: Finalisierung + Bad

## Kritische Hinweise aus dem Dokument

1. Verteilerkasten muss **vorher** gesetzt werden (blockiert alles)
2. Schlafzimmer-Rollladen: **1 oder 2 Motoren?** → beeinflusst die Planung
3. **KNX-Programmierung nicht inkludiert** – nur Verkabelung
4. **Dichtheitsprüfung der Wasserleitung** separat einplanen

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[syntheses/kersbach-status|Kersbach Baustelle – Aktueller Stand]]
- [[sources/scope-reconciliation|Scope-Abgleich Elektrik & Feb-vs-Mai-Plan]]
<!-- openclaw:wiki:related:end -->
