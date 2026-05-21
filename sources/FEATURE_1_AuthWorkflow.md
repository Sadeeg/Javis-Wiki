---
id: feature_1_authworkflow
pageType: source
title: "FEATURE 1: Authentifizierung & Benutzer-Verwaltung"
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# FEATURE 1: Authentifizierung & Benutzer-Verwaltung

## Ziel

Telegram-Bot + Web-UI für Benutzer-Authentifizierung und -Verwaltung. Jeder genehmigte Benutzer kann Bilder per Telegram an das Bautagebuch senden.

## Datenfluß

### Telegram Bot
1. **Neue Person** schreibt an Bot → Bot erkennt `telegram_id`, `username`
2. Neue Zeile in DB: `status=pending`, kein OpenProject-User zugeordnet
3. Person erhält DM: "Du bist noch nicht freigeschaltet. Bitte warte auf Freischaltung durch einen Admin."
4. **Approved User** schreibt an Bot → DM: "Willkommen! Du kannst jetzt Bilder senden."
5. **Blocked User** → DM: "Dein Zugang wurde gesperrt."

### Bild-Upload via Telegram
1. User sendet Bild an Bot
2. Bot prüft: ist User `status=active`?
   - Ja → Bild speichern, mit `telegram_id` + Datum verknüpfen
   - Nein → DM: "Du bist noch nicht freigeschaltet."

### Web-UI Admin
1. Admin öffnet `/admin/users`
2. Liste aller `pending` Users → Dropdown mit OpenProject-Benutzern → Approve
3. Beim Approve: `openproject_id` setzen, `status=active`
4. Alle genehmigten User können auch geblockt werden

## Technische Details

### Stack
- Java (Spring Boot)
- org.telegram:telegrambots
- PostgreSQL

### Datenbank-Schema

```sql
CREATE TABLE app_user (
    id              SERIAL PRIMARY KEY,
    telegram_id     BIGINT UNIQUE,           -- Telegram User ID
    telegram_username VARCHAR(255),             -- Telegram Username
    openproject_id  INTEGER,                   -- Verknüpfung zu OpenProject
    nextcloud_sub   VARCHAR(255),              -- Nextcloud OAuth subject
    status          VARCHAR(20) DEFAULT 'pending',  -- pending | active | blocked
    created_at      TIMESTAMP DEFAULT NOW(),
    updated_at      TIMESTAMP DEFAULT NOW()
);

CREATE TABLE openproject_user (
    id              SERIAL PRIMARY KEY,
    op_user_id      INTEGER UNIQUE,            -- OpenProject User ID
    name            VARCHAR(255),
    email           VARCHAR(255),
    last_synced     TIMESTAMP
);
```

### Telegram Bot Events
- `onUpdateReceived` → prüft MessageType PHOTO
- Bei `/start` → Willkommensnachricht oder Statusprüfung
- Neue User automatisch als `pending` anlegen

### Endpunkte

| Methode | Pfad | Beschreibung | Auth |
|---------|------|--------------|------|
| GET | `/api/admin/users` | Alle Users mit Status | Admin |
| GET | `/api/admin/users/pending` | Nur Pending-Users | Admin |
| POST | `/api/admin/users/{id}/approve` | User freischalten (body: {opUserId}) | Admin |
| POST | `/api/admin/users/{id}/block` | User blockieren | Admin |
| GET | `/api/admin/openproject/users` | OP-User-Liste (Dropdown) | Admin |
| POST | `/api/admin/sync/openproject` | OP-Benutzer syncen | Admin |
| POST | `/api/telegram/webhook` | Telegram Bot Webhook | - |

### Web-UI Admin-Page
- `/admin` → Admin-Panel mit User-Liste
- Pending-User → Dropdown (OP-User) → Approve Button
- Action-Buttons: Approve / Block pro User

## Status

- [x] Datenbank-Schema (AppUser, OpenProjectUser)
- [x] User-Entity + Repository
- [x] OpenProject-User-Entity + Sync
- [x] Admin REST-Endpunkte
- [x] Admin Web-UI (Angular)
- [ ] Telegram Bot (DEFERRED - telegrambots API-Version Issue)
- [ ] Bild-Empfang + Speicherung (hängt von Telegram ab)

## Offene Fragen

1. OpenProject URL + API-Key (für User-Sync)
2. Bild-Speicherung: Nextcloud Files API (wie geplant)

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
