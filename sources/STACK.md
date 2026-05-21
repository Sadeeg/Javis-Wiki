---
id: stack
pageType: source
title: STACK - Technologie-Stack
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# STACK - Technologie-Stack

## Anwendung

- **Framework:** Spring Boot (Java)
- **Datenbank:** PostgreSQL

## Frontend

- **Angular**
- **Design:** Modernes Bootstrap (Desktop-first, Mobile optional)

## Infrastruktur / Integration

- **Autorisierung:** Nextcloud OAuth 2.0 (OIDC)
  - JWKS-Endpoint: `https://cloud.deeg-mail.de/apps/oidc/jwks`
  - Issuer: `https://cloud.deeg-mail.de`
  - Token-Typ: `at+jwt` (Access Token als JWT)
  - Algorithmus: RS256
- **Telegram Bot:** Java Telegram Bot API (org.telegram:telegrambots)
- **Bild-Speicherung:** Nextcloud (Files API)

## Konfiguration

- Credentials: `~/.openclaw/credentials/baustellentagebuch/nextcloud.json` (neu für dieses Projekt)

## Deployment

- **Erstes Test-System:** `http://javis` (Port 80, Docker)
- **docker-compose.yml** mit 2 Containern:
  - Frontend (Angular) → `/`
  - Backend (Spring Boot) → `/api`
- **Alle Credentials** → `.env` (nicht im Repo!)
- **Env-Variablen:** DB-Zugang, Nextcloud-Credentials, JWT-Secret, etc.

## Offene Fragen

- [ ] Hosting: Wo soll das deployed werden?
- [ ] Nextcloud App für OAuth muss in Nextcloud registriert werden?

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
