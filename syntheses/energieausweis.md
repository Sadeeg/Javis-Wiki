---
id: energieausweis
pageType: synthesis
title: Energieausweis – Kersbach
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-10-25T08:30:00.000Z
sourceIds: [source.energieausweis-kersbach]
---

## Inhalt (Rohnotiz)

> **Provenienz:** Aus der Bau-Wiki-Rohnotiz übernommen (Erstellung 20.05.2026 bzw. Notizdatum der Quelle). Zahlen können zwischenzeitlich überholt sein – der **aktuelle** Projektstand steht in [[syntheses/kersbach-status]].
> Quelle: [[sources/energieausweis-kersbach]]

# Energieausweis – Kersbach

> Typ: Summary | Erstellt: 2026-05-20 | Quelle: `bau-wiki/raw/bauleitung/Energieausweis.pdf`

## Grunddaten

| Kennzahl | Wert |
|----------|------|
| Gebäudetyp | Einfamilienreiheneckhaus (Doppelhaushälfte) |
| Baujahr Gebäude | 1971 (Anbau: 1988) |
| Baujahr Wärmeerzeuger | 1996 (Brenner: 1999) |
| Heizung | Heizöl EL |
| Gebäudenutzfläche (A_N) | 216,4 m² |
| Lüftung | Fensterlüftung |
| Gültigkeit | bis 24.01.2034 |
| Anlass | Vermietung / Verkauf |

## Energieklasse

> ✅ **28.10.2026 ausgewertet** (Original-PDF aus Nextcloud
> `Projekt Haus/Dokumente/Gutachter-Asbest/Wie_besprochen_anbei_den_Energieausweis_Energieausweis (2).pdf`,
> Registriernummer **BY-2024-004908552**, Rechtsgrundlage GEG vom 20.07.2022,
> 6 Seiten, Scan → Auswertung per Vision-Modell):

| Kennzahl | Wert |
|---|---|
| Endenergiebedarf | **303,0 kWh/(m²·a)** |
| Primärenergiebedarf (Ist) | **335,2 kWh/(m²·a)** |
| Anforderungswert (Neubau) | 111,1 kWh/(m²·a) |
| Spez. Transmissionswärmeverlust H_T' (Ist) | **1,46 W/(m²·K)** |
| Anforderungswert H_T' | 0,63 W/(m²·K) |
| Treibhausgasemissionen | 94,6 kg CO₂-eq/(m²·a) |
| **Energieeffizienzklasse** | **H** (schlechteste) |

Heizöl EL, Lüftung: **Fensterlüftung**, Kessel: Wolf HK2-22 (BJ 1996, Brenner 1999).

## Modernisierungsempfehlungen

> ✅ **28.10.2026 ausgewertet** (Seite 4 des Originals). Die Spalten
> „geschätzte Amortisationszeit" und „geschätzte Kosten pro eingesparte kWh
> Endenergie" sind im Dokument **leer** (freiwillige Angaben, nicht ausgefüllt).
> **Einzelne U-Werte nennt der Ausweis nicht** – nur die Bauteile und die
> empfohlene Maßnahme.

| Nr. | Bauteil | Empfohlene Maßnahme | Art |
|---|---|---|---|
| 1 | **Dach / oberste Geschossdecke** | Dämmung nach GEG/EnEV | Einzelmaßnahme |
| 2 | Wände | Dämmung der **Rollladenkästen** | Einzelmaßnahme |
| 3 | Keller | Dämmung des **auskragenden Geschosses gegen Außenluft im kleinen beheizten Wintergarten** | Einzelmaßnahme |
| 4 | Heizung | Austausch des **alten Heizkessels**, Umrüstung auf erneuerbare Energien | bei größerer Modernisierung |
| 5 | **Lüftung** | „Nach größeren Sanierungsvorhaben sind lüftungstechnische Maßnahmen notwendig und zu empfehlen" | bei größerer Modernisierung |
| 6 | Warmwasser | Dämmung der Wärmeverteilung / Heizungsrohre nach GEG/EnEV | Einzelmaßnahme |

**Damit sind drei Maßnahmen offiziell empfohlen, aber im Sanierungsfahrplan
(9 Blöcke) NICHT enthalten:** Dachdämmung (1), Lüftung (5), Keller-Außenwand
am Wintergarten (3). Details: [[syntheses/heizlast-berechnung]] und
Abschnitt „Scope-Lücken" in [[sources/scope-reconciliation]].

## Interpretation

- **Altbau ohne moderne Dämmung** – Baujahr 1971
- **Ölheizung von 1996** – sollte auf Wärmepumpe umgestellt werden
- **Fensterlüftung** – keine kontrollierte Wohnraumlüftung
- **216m² Nutzfläche** vs. 105m² Wohnfläche – Differenz durch Keller + DG

## Nächste Schritte

- [x] Energieklasse von Seite 2 extrahieren → **Klasse H, 303 kWh/(m²·a)** (28.10.2026)
- [x] Modernisierungsempfehlungen von Seite 4 auswerten → 6 Maßnahmen, 3 davon nicht im Fahrplan (28.10.2026)
- [ ] Vergleich mit heutigen Anforderungen (GEG 2023)

## Related
<!-- openclaw:wiki:related:start -->
### Sources

- [[sources/energieausweis-kersbach|Energieausweis – Kersbach]]

### Referenced By

- [[syntheses/baustelle-wiki-index|Index – Kersbach Baustelle Wiki]]
<!-- openclaw:wiki:related:end -->
