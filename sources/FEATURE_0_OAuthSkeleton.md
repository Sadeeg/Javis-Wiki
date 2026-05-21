---
id: feature_0_oauthskeleton
pageType: source
title: "FEATURE 0: OAuth-Skelett (Minimalgerüst)"
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# FEATURE 0: OAuth-Skelett (Minimalgerüst)

## Ziel

Ein minimales Grundgerüst: OAuth-Login + leere Shell. Keine Business-Logik.

## Backend (Spring Boot)

### Endpunkte

| Methode | Pfad | Beschreibung | Auth |
|---------|------|--------------|------|
| GET | `/api/start` | Gibt `200` zurück wenn authentifiziert, sonst `401` | ✓ (JWT) |
| GET | `/api/health` | Health-Check, immer `200` | ✗ |

### OAuth-Setup

- Nextcloud OAuth 2.0 (OIDC) wie in STACK beschrieben
- `spring-boot-starter-oauth2-resource-server`
- JWT-Token-Validierung gegen `https://cloud.deeg-mail.de/apps/oidc/jwks`

### Minimale Struktur

```
backend/
├── src/main/java/de/baustellentagebuch/
│   ├── BaustellentagebuchApplication.java
│   ├── config/
│   │   └── SecurityConfig.java        # OAuth + /api/start
│   └── controller/
│       └── StartController.java       # /api/start → 200/401
├── src/main/resources/
│   └── application.yml
└── Dockerfile
```

## Frontend (Angular)

### Flow

1. User ruft `http://javis/` auf
2. Kein gültiger Token → Redirect zu Nextcloud OAuth
3. Nach Login → Callback → Token speichern
4. Zeigt leeres Bootstrap-Layout
5. Ruft `/api/start` auf (Token im Header)

### Minimale Struktur

```
frontend/
├── src/app/
│   ├── app.component.ts              # Leeres Bootstrap-Layout
│   ├── auth.service.ts               # OAuth Token Handling
│   └── home/                         # Redirect nach Login
├── src/environments/
└── Dockerfile
```

### Design

- Modernes Bootstrap (Desktop-first)
- Einfache leere Seite nach Login
- Login-Seite: Nextcloud-Login-Button

## Docker Compose

```yaml
services:
  backend:
    build: ./backend
    ports:
      - "8080:8080"
    env_file:
      - .env
    depends_on:
      - postgres
    networks:
      - baustelle

  frontend:
    build: ./frontend
    ports:
      - "80:80"
    networks:
      - baustelle

  postgres:
    image: postgres:16
    env_file:
      - .env
    volumes:
      - pgdata:/var/lib/postgresql/data
    networks:
      - baustelle

volumes:
  pgdata:

networks:
  baustelle:
```

## .env (nicht im Repo!)

```env
# Database
POSTGRES_DB=baustellentagebuch
POSTGRES_USER=baustelle
POSTGRES_PASSWORD=CHANGEME

# Backend
SPRING_DATASOURCE_URL=jdbc:postgresql://postgres:5432/baustellentagebuch
SPRING_DATASOURCE_USERNAME=baustelle
SPRING_DATASOURCE_PASSWORD=CHANGEME
OAUTH2_ISSUER_URI=https://cloud.deeg-mail.de

# Frontend
NGINX_HOST=localhost
```

## Status

- [ ] Backend: Projekt-Struktur anlegen
- [ ] Backend: SecurityConfig mit OAuth
- [ ] Backend: /api/start Endpunkt
- [ ] Backend: Dockerfile
- [ ] Frontend: Angular-Projekt anlegen
- [ ] Frontend: OAuth-Login-Flow
- [ ] Frontend: Leeres Bootstrap-Layout
- [ ] Frontend: Ruft /api/start auf
- [ ] Frontend: Dockerfile
- [ ] Docker-compose.yml
- [ ] .env.example erstellen

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
