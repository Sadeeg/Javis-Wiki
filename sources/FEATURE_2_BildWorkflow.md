---
id: feature_2_bildworkflow
pageType: source
title: "FEATURE 2: Bild-Workflow"
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# FEATURE 2: Bild-Workflow

## Ziel

Helfer können Bilder per Telegram an den Bot senden. Die Bilder werden gespeichert und in einer Aufgaben-Übersicht verwaltet, wo sie einer OpenProject-Aufgabe und einem Datum zugeordnet werden.

## Datenfluß

### 1. Bild-Einsendung (Telegram)
1. Helper sendet Bild an `@DeegBuild_bot`
2. Bot prüft: ist User `status=active`?
   - Nein → DM: "Nicht freigeschaltet"
   - Ja → Bild wird heruntergeladen + in Nextcloud gespeichert
3. Bot antwortet: "Bild erhalten! Es wird in der Aufgaben-Übersicht angezeigt."
4. Ein Datenbankeintrag wird erstellt: `image_id`, `telegram_id`, `sender_name`, `upload_timestamp`, `file_url`, `op_task_id` (NULL), `assignment_date` (NULL), `status=pending`

### 2. Aufgaben-Übersicht (Web-UI)
- Route: `/tasks` oder `/images`
- Zeigt alle Bilder mit `status=pending` (noch nicht zugeordnet)
- Tabelle/Spalten: Thumbnail | Eingereicht am | Von | Status
- Neue Bilder oben

### 3. Bild einer Aufgabe zuordnen
1. Admin/User klickt auf ein Bild in der Übersicht
2. Modal/Detailansicht öffnet sich
3. Felder:
   - **OpenProject-Aufgabe** (Dropdown mit Suchfeld, lädt aus OP)
   - **Datum** (default = Upload-Zeitstempel, editable)
   - **Notiz** (optional)
4. Beim Speichern:
   - `op_task_id` = ausgewählte Aufgabe
   - `assignment_date` = ausgewähltes Datum
   - `status` = `assigned`
5. Bild verschwindet aus der Übersicht (nur noch in OP-Aufgabe sichtbar)

### 4. Bild in OP-Aufgabe anzeigen
- Ein Kommentar wird in OP erstellt mit Link zum Bild in Nextcloud (Info-Zweck)
- Die Zuordnungs-Info (OP-Aufgabe + Datum) wird **ausschließlich in Postgres gespeichert**
- **Wichtig:** Diese Daten werden später für die Bautagebuch-Generierung benötigt!

## Technische Details

### Datenbank-Schema

```sql
CREATE TABLE submitted_image (
    id              SERIAL PRIMARY KEY,
    telegram_id     BIGINT,
    sender_name     VARCHAR(255),
    upload_timestamp TIMESTAMP DEFAULT NOW(),
    assignment_date  DATE,
    file_url        VARCHAR(500),          -- Nextcloud URL
    file_name       VARCHAR(255),
    file_size       INTEGER,
    op_task_id      INTEGER,               -- NULL = pending
    op_work_package_id VARCHAR(50),
    status          VARCHAR(20) DEFAULT 'pending',  -- pending | assigned | rejected
    notes           TEXT,
    created_at      TIMESTAMP DEFAULT NOW(),
    updated_at      TIMESTAMP DEFAULT NOW()
);

CREATE TABLE telegram_file (
    id              SERIAL PRIMARY KEY,
    image_id        INTEGER REFERENCES submitted_image(id),
    file_id         VARCHAR(255),          -- Telegram file_id
    mime_type       VARCHAR(100),
    downloaded      BOOLEAN DEFAULT FALSE
);
```

### Telegram Bot Erweiterung

- Bei Bild-Empfang: `file_id` extrahieren
- `getFile(file_id)` → Download-URL von Telegram
- Bild herunterladen
- In Nextcloud hochladen via WebDAV

### Nextcloud Integration

- WebDAV Upload: `/remote.php/dav/files/{username}/Bautagebuch/{date}/`
- DateiName: `{timestamp}_{uuid}.{ext}`
- Permissions: Shared folder für das Projekt

### OpenProject Integration

- Work Packages list via `/api/v3/work_packages?project_id=3`
- Attachment upload via `/api/v3/work_packages/{id}/attachments`
- Alternativ: Kommentar mit Bild-Link

### API-Endpunkte

| Methode | Pfad | Beschreibung | Auth |
|---------|------|--------------|------|
| GET | `/api/images` | Alle Bilder (filterbar) | User |
| GET | `/api/images/pending` | Nur pending Bilder | User |
| GET | `/api/images/{id}` | Bild-Details | User |
| PUT | `/api/images/{id}/assign` | Aufgabe+Datum zuweisen | User |
| DELETE | `/api/images/{id}` | Bild löschen | Admin |
| GET | `/api/op/workpackages` | OP Work Packages für Dropdown | User |

### Frontend Views

#### `/images` - Übersicht
- Grid oder Tabelle mit Thumbnails
- Filter: Status (pending/assigned), Datum
- Klick auf Bild → Modal zur Zuordnung

#### `/images/:id` - Detail
- Vollbild-Vorschau
- Zuordnungs-Formular
- History/Änderungen

## Offene Fragen

1. ~~OP Attachment oder Kommentar mit Link?~~ → Kommentar mit Link, Zuordnung NUR in Postgres
2. ~~Wer kann zuordnen?~~ → Alle active User
3. ~~Thumbnail-Generierung~~ → Ja, serverseitig

## Status

- [x] Datenbank-Schema erweitern (SubmittedImage Entity)
- [x] Nextcloud Upload Service
- [x] Telegram Bild-Download (als Reference, Upload bei Zuordnung)
- [x] OP Work Packages laden
- [x] Bild-Zuordnungs-API
- [x] Frontend Bilder-Übersicht (/images)
- [x] Frontend Zuordnungs-Modal
- [ ] Thumbnail-Anzeige (noch nicht implementiert)

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
