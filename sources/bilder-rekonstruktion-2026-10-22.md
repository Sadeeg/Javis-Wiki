---
id: bilder-rekonstruktion-2026-10-22
pageType: source
title: Bilder-Rekonstruktion – alle Quellen geprüft (22.10.2026)
createdAt: 2026-10-22T16:20:00.000Z
updatedAt: 2026-10-22T16:20:00.000Z
sourceIds: []
tags: [kersbach, bilder, baulebuch, rekonstruktion, belegkette]
---

# Bilder-Rekonstruktion: alle Quellen geprüft

> **Ergebnis: Die 78 fehlenden Bautagebuch-Bilder sind aus keinem vorhandenen System
> rekonstruierbar.** Die Quelle existiert nicht mehr. Dokumentiert, damit die Suche
> nicht wiederholt wird.

## Geprüfte Quellen

| # | Quelle | Ergebnis |
|---|---|---|
| 1 | Nextcloud `Projekt Haus/Bilder/` | nur `20260926/` – 14 Fotos + Videos (26.09.2026) ✅ |
| 2 | Nextcloud `Projekt Haus/Fotos/` | `1801/`, `KW0226/`, `KW0326/` – **andere Benennung**, ~30 Fotos (Jan–Mär 2026) ✅ |
| 3 | Nextcloud `Projekt Haus/Bilder/` tiefer | alle 3 Ebenen geprüft, 25 Dateien, keine weiteren Unterordner |
| 4 | OpenProject `/work_packages/{id}/attachments` | **0** bei allen 52 Work Packages |
| 5 | OpenProject `/attachments/{id}` | **404** – Route existiert nicht |
| 6 | OpenProject `/attachments?pageSize=500` | **404** – keine globale Attachment-Liste |
| 7 | **Nextcloud-Share „Bautagebuch"** | **404 – existiert nicht mehr** ❌ |
| 8 | Bautagebuch-App: Docker-Volume `image-data` | 5 Bilder (13.05., 23.05., 24.05., 06.06.2026) |
| 9 | Bautagebuch-App: Postgres `submitted_image` | 9 Zeilen – alle `file_url` zeigen auf den **gelöschten Share** |
| 10 | Bautagebuch-App: Postgres `time_entry` | 165 Einträge / 682 h, Cache bis 29.05.2026 |
| 11 | Bautagebuch-App: Postgres `week_description` | 1 Zeile (KW21/2026, AI-generiert) |
| 12 | OpenProject Time-Entry-Kommentare | 30 von 227 – alle **bis KW22/2026** |
| 13 | OpenProject WP-Activities | nur Auto-„Parent updated by child", letzte **06.07.2026** |

## Die entscheidende Spur

Die App (`submitted_image.file_url`) speichert Links in der Form:

```
https://cloud.deeg-mail.de/s/Bautagebuch/{datum}/{uuid}_{datei}.jpg
```

Der Share-Token war `Bautagebuch`. **Dieser Share liefert heute 404.**
Die Bilder wurden also nie in `Projekt Haus/` abgelegt, sondern in einen eigenen
Share, der inzwischen gelöscht wurde.

⇒ **Einzige verbleibende Rettung:** Sascha prüft, ob der Share in seinem
Nextcloud-Konto unter „Teilen" noch reaktivierbar ist (gelöschte Shares bleiben
oft im Papierkorb / in „Shares" als inaktiv sichtbar).

## Was trotzdem rekonstruierbar ist

- **5 Bilder** aus dem App-Volume (Mai/Juni 2026) – lokal kopierbar
- **15 Arbeitskommentare** aus der App-DB (KW–Mai 2026) → textualer Bautagebuch-Inhalt
- **AI-Wochenbeschreibung KW21/2026** aus `week_description`
- **14 Fotos 26.09.2026** → Zustandsaufnahme (siehe [[sources/zustandsaufnahme-2026-09-26]])

## Nebenbefund für das Software-Projekt

Der Share „Bautagebuch" wird von der App als **fester Token** benutzt. Ist er
gelöscht, schlägt der Bildupload fehl – entweder muss die App den Share anlegen
oder einen konfigurierbaren Share-Namen nutzen. Die 5 Bilder im Volume sind
lokal, aber die 9 `submitted_image`-Einträge zeigen ins Leere.

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
