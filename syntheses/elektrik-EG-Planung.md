---
id: elektrik-eg-planung
pageType: synthesis
title: Elektrik EG-Planung – KNX
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-10-25T08:30:00.000Z
sourceIds: [source.elektrik-eg-planung-knx]
---

## Inhalt (Rohnotiz)

> **Provenienz:** Aus der Bau-Wiki-Rohnotiz übernommen (Erstellung 20.05.2026 bzw. Notizdatum der Quelle). Zahlen können zwischenzeitlich überholt sein – der **aktuelle** Projektstand steht in [[syntheses/kersbach-status]].
> Quelle: [[sources/elektrik-eg-planung-knx]]

# Elektrik EG-Planung – KNX

> Typ: Summary | Erstellt: 2026-05-20 | Quelle: `bau-wiki/raw/planung/Elektrik/EG-Planung-Detail.pdf`

## Überblick

Elektroplanung für das Erdgeschoss mit **KNX-Smart-Home-System** und moderner Netzwerkinfrastruktur.

## Zuleitungen (Kabel)

| Kabeltyp | Menge |
|----------|-------|
| NYM 3x1,5mm² | 18x |
| NYM 3x2,5mm² | 12x |
| NYM 5x2,5mm² | 4x |
| CAT7 – KNX | 17x |
| CAT7 – Netzwerk | 14x |
| **Summe** | **65 (51 ohne Netzwerk)** |

## KNX-Komponenten

| Komponente | Menge | Beschreibung |
|------------|-------|---------------|
| Sicherungen | 19x | Leitungsschutzschalter |
| Binäreingänge | 26x | Taster, Schalter, Fensterkontakte |
| Schaltaktoren (o.SM) | 6x | Einfaches Ein/Aus |
| Schaltaktoren (m.SM) | 11x | Mit Strommessung |
| Dimmer | 3x | Stufenloses Licht |
| Rollo-Aktoren | 3x | Jalousien/Rollläden |
| Heizaktoren | 5x | Fußbodenheizung |

## Besonderheiten

- **11 Schaltaktoren mit Strommessung** – für Geräteüberwachung (z.B. "Waschmaschine fertig")
- **26 Binäreingänge** – für herkömmliche Taster und Fensterkontakte
- **14 Netzwerkanschlüsse** – LAN-Dosen für PC, TV, Access Points
- **5 Heizaktoren** – Einzelraumregelung für Fußbodenheizung
- **3 Rollo-Aktoren** – für elektrische Rollläden/Jalousien

## Funktionalitäten

- Lichtsteuerung (ein/aus + dimmbar)
- Rollläden automatisch
- Einzelraumheizung
- Energieüberwachung
- Netzwerk (14 Anschlüsse)
- KNX-Bus für Sensoren/Aktoren

## Quelle

Original: `Projekt Haus/Planung/Elektrik/EG-Planung-Detail.pdf`

## Related
<!-- openclaw:wiki:related:start -->
### Sources

- [[sources/elektrik-eg-planung-knx|Elektrik EG-Planung – KNX]]

### Referenced By

- [[concepts/Elektro-Grundwissen|Elektro-Installation – Grundwissen für Heimwerker]]
- [[sources/fussbodenheizung|Fussbodenheizung]]
<!-- openclaw:wiki:related:end -->
