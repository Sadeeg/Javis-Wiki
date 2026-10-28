---
id: source-anhang-audit-2026-10-28
pageType: source
title: Anhang-Audit Wiki-Vault (28.10.2026)
createdAt: 2026-10-28T16:30:00.000Z
updatedAt: 2026-10-28T16:30:00.000Z
sourceIds: [source.wohnflächenberechnung-kersbach]
tags: [kersbach, wiki, anhaenge, datenqualitaet, audit]
---

# Anhang-Audit: alle 36 Dateien unter `_attachments/` geprüft

> **Anlass:** Beim Befüllen der leeren Quellseite
> [[sources/Wohnflaechenberechnung.pdf]] fiel auf, dass der zugehörige Anhang
> kein PDF, sondern eine Fehlermeldung war. → systematische Prüfung aller
> Anhänge statt Reparatur im Einzelfall.

## Methode

Zwei Prüfungen pro Datei:

1. **SabreDAV-Fehlerkennung** – Nextcloud liefert bei fehlender Datei eine
   200-große XML-Antwort statt der Datei:
   `<s:exception>Sabre\DAV\Exception\NotFound</s:exception>`
2. **Magic-Byte-Prüfung** – jede Datei muss mit dem erwarteten Format beginnen
   (`%PDF` = PDF, `\xff\xd8\xff` = JPEG, `PK\x03\x04` = ZIP/Office, `<?xml`/`<mxfile` = XML)

## Ergebnis: 2 defekte Anhänge, beide repariert

| # | Anhang | vorher | Ursache | nachher |
|---|---|---|---|---|
| 1 | `_attachments/raw/dokumente/gutachter-asbest/Wohnflaechenberechnung.pdf` | 295 B SabreDAV-404 | Datei liegt in Nextcloud **nicht** unter `Projekt Haus/Dokumente/Gutachter-Asbest/`, das Original aber im Vault unter `raw/bauleitung/` | **1.126.486 B**, PDF 1.7, 1 Seite, md5 `36b0902b…` – byte-identisch zum Vault-Original |
| 2 | `_attachments/raw/planung/elektrik/wohnzimmer/WandTuerZuGang.drawio` | 291 B SabreDAV-404 | **Umlaut-Umschreibung:** Nextcloud heißt die Datei `WandTüreZuGang.drawio`, der Wiki-Import suchte `WandTuerZuGang.drawio` | **6.729 B**, gültiges `mxfile` mit 23 Zellen (Wandmaße 110 cm / 14 cm / 30 cm / 35 cm) |

> **Die Ursache ist nicht „Nextcloud kaputt"**, sondern der Import: er hat
> Umlaute transliteriert und danach unter dem falschen Namen gesucht. Bei
> `WandTüreZuGang` ist die Datei vorhanden – nur nicht unter dem Namen, den
> der Import wollte.

### Neu hinzugekommen (fehlten im Wiki, aber in Nextcloud vorhanden)

| Datei | Größe | Quelle |
|---|---|---|
| `_attachments/raw/planung/elektrik/EG-Planung-fuer-KI.ods` | 30.533 B | `Projekt Haus/Planung/Elektrik/EG-Planung-für-KI.ods` |
| `_attachments/raw/planung/elektrik/EG-Haus.drawio` | 19.296 B | `Projekt Haus/Planung/Elektrik/EG-Haus.drawio` |

Die ODS war **kein Luxus**: [[sources/scope-reconciliation]] stützt die
gesamte Endmontage-Schätzung (~80 h) auf ihre 9 Raumblätter, und die Datei
war im Wiki **gar nicht vorhanden** – die Zahlen also nicht nachprüfbar.
Mit der Datei ist die Rechnung jetzt reproduzierbar (Ergebnis: 54 von 63
Werten exakt bestätigt, die Spalte „Zuleitungen" der 1.-OG-Räume war falsch
übernommen – Details dort).

## Nach dem Audit: alle 38 Anhänge valide

PDF 9 · JPEG 14 · XML/drawio 8 · Office (ZIP) 4 · Markdown 3 — **kein
defekter Anhang mehr**.

## Was im Nextcloud liegt, aber nicht im Wiki (bewusst offen)

Aus `Projekt Haus/Planung/Elektrik/` fehlen weiterhin:

| Datei | Einordnung |
|---|---|
| `EG-Haus.drawio` | ✅ **nachträglich importiert** (28.10.2026) |
| `EG-Planung-Bereinigt.ods` | Variante der EG-Planung |
| `EG-Planung-für-KI.ods` | ✅ **nachträglich importiert** (28.10.2026) |
| `EG-Planung-ohne-Dach.ods` | Variante ohne Dachgeschoss |
| `EG-Planung-Detail.ods` | **Achtung:** die `.ods`-Fassung des Detailplans fehlt, die `.pdf` ist da – die im Wiki ausgewerteten Detailplan-Zahlen (183,5 h / 224,1 h) stammen aus der PDF-Fassung, nicht aus dieser Tabelle |
| `EG.odt`, `Unbenannt 2.ods` | vermutlich Zwischenstände |
| `.*.bkp` (5 Stück) | Nextcloud-Automatik-Backups, kein Inhalt |

→ Diese Dateien sind **nicht** importiert worden: Es gibt keine Wiki-Seite,
die sie referenziert, und sie zu importieren hieße, das Wiki mit
Fassungen zu fluten, von denen niemand weiß, welche die gültige ist.
Der Punkt ist hier nur **sichtbar gemacht**.

## Lehre für künftige Importe

1. **Nach jedem Import die Magic-Bytes prüfen** – ein 404-Stub ist 291 Byte
   groß und sieht in einer Dateiliste völlig harmlos aus.
2. **Umlaute transliterieren und dann mit dem Originalnamen suchen** war die
   Ursache beider Fälle. Korrekt ist: Originalname beibehalten oder die
   Umlaut-Dateien per Liste suchen, nicht per geratenem Namen.
3. **Dateien, die eine Wiki-Seite als Quelle zitiert, gehören ins Wiki.**
   Vorher war `EG-Planung-für-KI.ods` nur ein Name in einem Fließtext.

## Related

- [[sources/Wohnflaechenberechnung.pdf]] – die Seite, an der der Defekt auffiel
- [[sources/scope-reconciliation]] – Verifikation der Endmontage-Zahlen
- [[sources/wohnflächenberechnung-kersbach]] – Rohnotiz zur Wohnflächenberechnung

## Related
<!-- openclaw:wiki:related:start -->
### Sources

- [[sources/wohnflächenberechnung-kersbach|Wohnflächenberechnung – Kersbach]]

### Referenced By

- [[sources/scope-reconciliation|Scope-Abgleich Elektrik & Feb-vs-Mai-Plan]]
- [[sources/Wohnflaechenberechnung.pdf|Wohnflaechenberechnung.Pdf]]

### Related Pages

- [[syntheses/wohnflaechenberechnung|Wohnflächenberechnung – Kersbach]]
<!-- openclaw:wiki:related:end -->
