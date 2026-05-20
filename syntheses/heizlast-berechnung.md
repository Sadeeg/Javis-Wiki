# Heizlast-Berechnung – Wohngebäude Deeg

> Typ: Summary | Erstellt: 2026-05-20 | Quelle: [[raw/heizlast/Heizlast-Deeg.pdf]]

## Überblick

**Datum:** 26.08.2025
**Erstellt von:** Philipp Bott, BK Energieberater GmbH
**Software:** EVEBI Version 13.10.5
**Norm:** DIN EN 12831-1

## Gebäudedaten

| Kennzahl | Wert |
|----------|------|
| Grundfläche | 66,4 m² |
| Volumen | 570,6 m³ |
| Hüllfläche | 357,4 m² |
| Wärmeverlustkoeffizient (L) | 291 W/K |
| Wärmespeicherkapazität | 31.423 Wh/K |
| Zeitkonstante | 108h |
| Kategorie | C – innengedämmtes Gebäude mit einbindenden Massivdecken |

## Transmissionswärmeverluste

| Kennzahl | Wert |
|----------|------|
| Transmissionswärmeverluste | 9.690 W |
| Lüftungswärmeverluste | 993 W |
| **Gebäudeheizlast (Total)** | **10.683 W (10,68 kW)** |

## Aufheizzuschläge

| Raum | Aufheizschlag (W) |
|------|-------------------|
| Wohnzimmer | 425 W |
| Bad | 78 W |
| Kinderzimmer 2 | 181 W |
| Kinderzimmer 1 | 124 W |
| Küche | 108 W |

## Raumtemperaturen (Auslegung)

| Raum | Innentemperatur |
|------|-----------------|
| Bad | 24°C |
| Wohnzimmer | 20°C |
| Küche | 20°C |
| Kinderzimmer | 20°C |
| Schlafzimmer | 20°C |
| WC | 20°C |
| Flur | 15°C |
| Waschküche | 17°C |
| Hobbyraum | 17°C |

## Bedeutung für Wärmepumpe

| Zustand | Heizlast | Benötigte WP-Leistung |
|---------|----------|----------------------|
| Komplett saniert, alles beheizt | 10,68 kW | 11-12 kW |
| Ohne Fassade+Dachdämmung, kalt-DG/KG | ~12-13 kW | 13-15 kW |
| Ohne Fassade+Dachdämmung, alles beheizt | ~15,5 kW | 15-16 kW |

**Anmerkung:** U-Wert-sanierte Wand = 0,58 W/m²K (vorher 1,2). Differenz = 0,62 × 150m² × 32K ≈ 3.000W Einsparung nur durch Wand.

**Empfehlung:** Wärmepumpe mit **mindestens 15 kW** Nennleistung wählen (für Worst-Case ohne Dämmung).

## Annahmen für Berechnung

- U-Wert Außenwand (Altbau): 1,2 W/m²K
- U-Wert Außenwand (sanierter Zustand): 0,58 W/m²K
- U-Wert Dach (Altbau): 1,0 W/m²K  
- U-Wert Dach (saniert): 0,2 W/m²K
- DG und KG bleiben unbeheizt

## Quelle

Original: `Heizlast_-_Wohnhaus_Deeg_saniert_mit_Keller_1---e4fb75cf-6314-48b5-9ec5-b3023710efdb.pdf`
Hinweis: Dies ist Teil 1 von ?. Weitere Seiten (Raumweise Aufschlüsselung) können folgen.

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
