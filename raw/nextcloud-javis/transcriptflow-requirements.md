# TranscriptFlow - Audio Transcription Service

## Projekt-Beschreibung

Webanwendung zum Hochladen von Audio-Dateien (OGG, MP3, WAV) mit asynchroner Transkription und Sprechererkennung. Gesichert durch Nextcloud OAuth2.

## Architektur

```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│   Angular   │───▶│   Spring    │───▶│  RabbitMQ   │
│   Frontend  │    │   Backend   │    │  (Queues)   │
└─────────────┘    └─────────────┘    └──────┬──────┘
       ▲                 │                    │
       │                 │                    ▼
       │                 ▼             ┌─────────────┐
       │           ┌─────────────┐     │   Python    │
       └──────────▶│  Nextcloud  │     │   Worker    │
                   │   OAuth2    │     │(faster-whisper) │
                   └─────────────┘     └─────────────┘
```

## Technologie-Stack

| Komponente | Technologie |
|------------|-------------|
| Frontend | Angular 17+ |
| Backend | Spring Boot 3.x |
| Auth | Nextcloud OAuth2 (Resource Server) |
| Message Queue | RabbitMQ |
| Worker | Python + faster-whisper + whisperx |
| Database | PostgreSQL oder H2 (dev) |
| Web Server | Nginx (Reverse Proxy) |
| Container | Docker Compose |

## Funktionale Anforderungen

### 1. Authentication
- [ ] OAuth2-Login über Nextcloud
- [ ] User können nur ihre eigenen Jobs sehen und abrufen
- [ ] JWT-Token Validierung im Spring Backend

### 2. Audio Upload
- [ ] Upload von OGG, MP3, WAV Dateien
- [ ] Max. Dateigröße: 500MB
- [ ] Speicherung im Spring Backend (Filesystem oder S3)
- [ ] Validierung der Dateitypen

### 3. Asynchrone Verarbeitung
- [ ] Job-Erstellung bei Upload → Job-ID zurückgeben
- [ ] Job in RabbitMQ Queue einreihen (`transcription.jobs`)
- [ ] Python Worker verarbeitet Queue
- [ ] Result in andere Queue schreiben (`transcription.results`)
- [ ] Spring empfängt Result und speichert in DB

### 4. Transkription
- [ ] WhisperX für Transkription mit Sprecher-Diarisierung
- [ ] Output: TXT-Datei mit Sprecher-Labels (SPEAKER_01, SPEAKER_02, ...)

### 5. Status & Download
- [ ] Status-Abfrage: PENDING → PROCESSING → COMPLETED / FAILED
- [ ] Download der Transkription wenn COMPLETED
- [ ] Anzeige der Fehlermeldung wenn FAILED

### 6. REST API

```
POST   /api/jobs          - Job erstellen (Upload)
GET    /api/jobs          - Alle Jobs des Users
GET    /api/jobs/{id}     - Job Status/Details
GET    /api/jobs/{id}/download - Transkription downloaden
DELETE /api/jobs/{id}     - Job löschen
```

## Docker Compose Anforderungen

### Services
1. **nginx** - Port 80, Angular + Proxy
2. **spring** - Spring Boot Backend
3. **worker** - Python Transkription Worker
4. **rabbitmq** - Message Queue
5. **postgres** - Database (optional, für Prod)

### Konfiguration (.env)
```env
# Nextcloud OAuth
OAUTH2_ISSUER_URI=https://cloud.deeg-mail.de
OAUTH2_CLIENT_ID=your-client-id
OAUTH2_CLIENT_SECRET=your-secret

# RabbitMQ
RABBITMQ_HOST=rabbitmq
RABBITMQ_PORT=5672
```

### Nginx Konfiguration
- `/` → Angular App (static files)
- `/api` → Spring Backend (proxy_pass)

### Datenmodell

```sql
Jobs Table:
- id: UUID (PK)
- user_id: VARCHAR (aus Nextcloud)
- filename: VARCHAR
- original_filename: VARCHAR
- status: ENUM (PENDING, PROCESSING, COMPLETED, FAILED)
- result_text: TEXT (nullable)
- error_message: TEXT (nullable)
- created_at: TIMESTAMP
- updated_at: TIMESTAMP
```

## Message Queues

### transcription.jobs (Java → Python)
```json
{
  "jobId": "uuid",
  "userId": "nextcloud-user-id",
  "filePath": "/path/to/audio/file"
}
```

### transcription.results (Python → Java)
```json
{
  "jobId": "uuid",
  "status": "COMPLETED|FAILED",
  "resultText": "transcribed text...",
  "errorMessage": "error if failed"
}
```

## Build & Start

```bash
# 1. .env Datei anlegen mit OAuth-Daten
cp .env.example .env

# 2. Bauen
docker compose build

# 3. Starten
docker compose up -d

# 4. Öffnen
# http://localhost → Angular App
# http://localhost/api → API
```

## Abnahmekriterien

- [ ] Docker Compose startet alle Services ohne Fehler
- [ ] OAuth2 Login mit Nextcloud funktioniert
- [ ] User kann OGG/MP3/WAV hochladen
- [ ] Transkription läuft asynchron (Job wird verarbeitet)
- [ ] Status wird korrekt angezeigt
- [ ] Transkription kann heruntergeladen werden
- [ ] User sieht nur eigene Jobs
- [ ] Sprecher werden unterschieden (wenn vorhanden)