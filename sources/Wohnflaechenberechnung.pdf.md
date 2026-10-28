---
id: wohnflaechenberechnung.pdf
pageType: source
title: Wohnflaechenberechnung.Pdf
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-10-28T16:15:00.000Z
sourceIds: [source.wohnflächenberechnung-kersbach]
tags: [kersbach, wohnflaeche, baugenehmigung, gutachter]
---

# Wohnflächenberechnung – Kersbach (PDF, 1 Seite)

> **Originaldokument** der detaillierten Wohnflächenberechnung (vermutlich DIN 283).
> Anhang: `_attachments/raw/dokumente/gutachter-asbest/Wohnflaechenberechnung.pdf`
> (1.126.486 Bytes, PDF 1.7, 1 Seite, md5 `36b0902beace5a657d39b51f92888dfe`) –
> byte-identisch mit dem Vault-Original
> `obsidian_vault/Baustelle/bau-wiki/raw/bauleitung/Wohnflaechenberechnung.pdf`.

## Anhang war defekt – am 28.10.2026 repariert

Bis 28.10.2026 enthielt der Wiki-Anhang **kein PDF**, sondern eine 295 Byte
große SabreDAV-Fehlerantwort:

```xml
<s:exception>Sabre\DAV\Exception\NotFound</s:exception>
<s:message>File with name /Projekt Haus/Dokumente/Gutachter-Asbest/Wohnflaechenberechnung.pdf could not be located</s:message>
```

Ursache: der Import holte die Datei aus dem Nextcloud-Ordner
`Projekt Haus/Dokumente/Gutachter-Asbest/`, wo sie **nicht (mehr) liegt**.
Das Original existiert im Obsidian-Vault unter
`raw/bauleitung/Wohnflaechenberechnung.pdf` und wurde am 28.10.2026
byte-identisch in den Anhang übernommen. Siehe [[sources/anhang-audit-2026-10-28]].

## Dokumenttyp

| Merkmal | Wert |
|---|---|
| Creator / Producer | PDF24 Creator / GPL Ghostscript 10.02.1 |
| Erstellt | 07.04.2025 |
| Seiten | 1 |
| Text extrahierbar | **nein** – es ist ein Scan |

> Da kein Textlayer vorhanden ist, stammen alle Zahlen unten aus **Saschas
> Auslesen des Scans** (erfasst am 20.05.2026 in der Rohnotiz
> [[sources/wohnflächenberechnung-kersbach]]). Sie sind nicht maschinell
> gegen das PDF geprüft – die Summe ist es immerhin in sich schlüssig.

## Werte laut Dokument

| Geschoss | Fläche |
|---|---|
| Erdgeschoss | 72,81 m² |
| Obergeschoss | 49,34 m² |
| Dachgeschoss | 28,77 m² |
| **Gesamt** | **150,92 m²** |

Rechnerisch konsistent: 72,81 + 49,34 + 28,77 = **150,92 m²**.

### Erdgeschoss – 72,81 m²

| Raum | Fläche |
|---|---|
| Windfang | 1,75 m² |
| WC | 1,57 m² |
| Garderobe | 1,41 m² |
| Diele | 6,21 m² |
| Wohnen | 32,36 m² |
| Küche | 8,76 m² |
| **Wintergarten (beheizt)** | **23,00 m²** |

Brutto 75,06 m² − 3 % Putz (−2,25 m²) = **72,81 m²**

### Obergeschoss – 49,34 m²

| Raum | Fläche |
|---|---|
| Bad | 6,34 m² |
| Flur | 5,48 m² |
| Abstellraum | 0,42 m² |
| Kinder 1 | 14,28 m² |
| Eltern | 14,30 m² |
| Kinder 2 | 10,05 m² |

Brutto 50,87 m² − 3 % Putz (−1,53 m²) = **49,34 m²**

### Dachgeschoss – 28,77 m²

| Raum | Fläche |
|---|---|
| Studio | 24,26 m² |
| DG-Flur | 4,51 m² (× 0,97 wegen Dachschrägen) |

= **28,77 m²**

## Zwei Punkte, die Beachtung brauchen

1. **Der Wintergarten zählt mit.** 23,00 m² beheizte Wintergartenfläche sind in
   der Wohnfläche enthalten. Das ist der Grund, warum die Zahl (150,92 m²)
   über den üblichen Grundriss-Werten liegt – und zugleich der Anknüpfungspunkt
   für die WDVS-Betrachtung (Fassadenfläche 153 m²).
2. **Die Differenz zum Grundriss ist offen.** Die Rohnotiz stellt dem
   Energieausweis (Nutzfläche 216,4 m²) und dem Grundriss (Wohnfläche DIN 283
   **105,09 m²**) gegenüber. Zwischen 105,09 m² und 150,92 m² liegen
   **45,83 m²** – das ist **nicht** durch Keller und Dachboden erklärbar und
   bleibt eine offene Frage der Quelldokumentation. Hier wird nichts
   interpretiert; die Werte stehen so, wie sie in den Quellen stehen.

## Weiterführend

- [[sources/wohnflächenberechnung-kersbach]] – Rohnotiz (Erstellt 20.05.2026)
- [[syntheses/wohnflaechenberechnung]] – Synthese mit Vergleichstabelle
- [[syntheses/kersbach-status]] – aktueller Projektstand

## Related
<!-- openclaw:wiki:related:start -->
### Sources

- [[sources/wohnflächenberechnung-kersbach|Wohnflächenberechnung – Kersbach]]

### Referenced By

- [[sources/anhang-audit-2026-10-28|Anhang-Audit Wiki-Vault (28.10.2026)]]
- [[syntheses/baustelle-wiki-index|Index – Kersbach Baustelle Wiki]]

### Related Pages

- [[syntheses/wohnflaechenberechnung|Wohnflächenberechnung – Kersbach]]
<!-- openclaw:wiki:related:end -->
