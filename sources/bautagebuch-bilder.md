---
id: source-bautagebuch-bilder
pageType: source
title: Bautagebuch-Bilder (Nextcloud-Archiv)
createdAt: 2026-10-22T16:20:00.000Z
updatedAt: 2026-10-22T16:20:00.000Z
sourceIds: []
tags: [kersbach, bautagebuch, bilder, nextcloud, belegkette]
---

# Bautagebuch-Bilder – Nextcloud-Archiv

> **Fund am 22.10.2026.** Die Bilder des Bautagebuchs waren nie verloren –
> sie liegen in `Projekt Haus/Baustellentagebuch/img/` im Nextcloud-Account `openclaw`.

## Inhalt

```
Projekt Haus/Baustellentagebuch/img/
├── 2025/08/   32 Bilder
├── 2025/09/   16 Bilder
├── 2025/10/    2 Bilder
├── 2025/11/    8 Bilder
├── 2025/12/    2 Bilder
├── 2026/01/   21 Bilder
└── Whatsapp/  (2008, 2010, …)
```

**114 Bild-/Videodateien**, davon 81 im Namensmuster `dd-MM-YY_HH-MM-SS_ID.jpg`
(die ID = OpenProject-Attachment-ID, aus der die Datei ursprünglich benannt wurde).

## Abgleich

79 Referenzen im Bautagebuch (`book.md`, `book-2026-kw03-29.md`) → **79/79 auflösbar**.
Vier sahen zunächst unauffindbar aus: drei ältere Dateinamen ohne Zeitstempel
(`25-08-16-1673.jpg` etc.) und ein Tippfehler im Buch (`5-08-16_…` → `25-08-16_…`,
korrigiert am 22.10.2026).

## Warum die OpenProject-API 0/404 lieferte

Die Bilder wurden offenbar **in OpenProject hochgeladen** (daher die ID im Dateinamen)
und **nach Nextcloud kopiert**. Der OpenProject-Attachment-Store ist für den
API-Key-Benutzer nicht lesbar (`/work_packages/{id}/attachments` → 0,
`/attachments/{id}` → 404) – **das war kein Datenverlust.**

## Zugriff

```bash
curl -u "openclaw:$NC_PW" -o lokal.jpg \
  "https://cloud.deeg-mail.de/remote.php/dav/files/openclaw/Projekt%20Haus/Baustellentagebuch/img/2025/08/25-08-16_10-42-55_1676.jpg"
```

## Bedeutung

Die **Bauakte ist vollständig belegt**: Bautagebuch-Text + alle Fotos + Fotos vom
26.09.2026 (Zustandsaufnahme Estrich/Elektrik). Offen in der Belegkette bleiben nur
das **Heizlast-Original** (EVEBI, 10,68 kW) und die **Rechnungen**.

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
