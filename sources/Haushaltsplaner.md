# Haushaltsplaner - App Idee

> Aufgabenverteilung im Haushalt nach fairen Regeln

## Problem

- Haushaltsaufgaben werden oft unfair verteilt
- Kochen UND Abwaschen für dieselbe Person = nicht fair
- Keine klare Übersicht wer was wann machen muss
- Aufgaben werden vergessen oder ignoriert

---

## Kern-Features

### 1. Haushaltsmitglieder anlegen

```
Mitglied: Sascha
Mitglied: Alexandra

Regel: "Wer kocht, macht NICHT Abwasch"
```

### 2. Aufgaben-Kategorien

| Kategorie | Häufigkeit | Beispiele | Erledigungszeitraum |
|-----------|------------|-----------|---------------------|
| **Täglich** | Täglich | Kochen, Abwaschen, Müll rausbringen | - |
| **Wöchentlich** | Einmal pro Woche | Staubsaugen, Boden wischen | Freitag, Samstag, Sonntag? |
| **Zwei-Wöchentlich** | Alle 2 Wochen | Bad putzen, Fenster putzen | Wochenende? |
| **Monatlich** | Einmal pro Monat | Große Küche, Kelleraufräumen | Monatsende? |

**Erledigungszeitraum einstellbar:**
- Wöchentliche Aufgabe → z.B. "bis Freitag erledigen"
- Zwei-Wöchentliche Aufgabe → z.B. "Wochenende"
- Monatliche Aufgabe → z.B. "bis Ende des Monats"

### 3. Faire Verteilungsregeln (Algorithmen)

**Aufgaben-Abhängigkeiten (Exclusion Rules):**
- "Wer kocht, macht NICHT Katzenklos"
- "Wer Müll rausbringt, muss nicht saugen"
- Konfigurierbar pro Haushalt

```
Aufgabe A (Kochen) ← Sascha
Aufgabe B (Katzenklos) ← Alexandra (weil Sascha kocht)

Nächster Tag:
Aufgabe A (Kochen) ← Alexandra
Aufgabe B (Katzenklos) ← Sascha (weil Alexandra kocht)
```

**Skip oder Verschieben:**
- Person ist abends nicht da / kann Aufgabe nicht erledigen?
  - **Skip:** Aufgabe fällt weg, nächste Person übernimmt
  - **Verschieben:** Aufgabe geht an nächste Person, aber此人 übernimmt am nächsten Tag

### 4. Aufgaben-Übersicht (TODO Liste)

```
📋 Haushaltsplaner

Heute:
☐ Sascha - Kochen
☐ Alexandra - Abwaschen

Offene Aufgaben:
☐ Sascha - Müll rausbringen (gestern, übernehmen?)
☐ Alexandra - Saugen (diese Woche)
```

### 5. Erinnerungen (Telegram - nur eigene Aufgaben)

**Tägliche Morgen-Benachrichtigung (08:00 Uhr):**
```
🌅 Guten Morgen Sascha!

Heute für dich:
☐ Kochen
☐ Müll rausbringen

Diese Woche noch:
☐ Saugen (Freitag)

Dein Punktestand:
⭐ Du: 12 Punkte
⭐ Alexandra: 10 Punkte
```

**Aufgaben-Erinnerungen:**
```
🔔 "Sascha, heute ist Kochen dran!"
```

**Skip/Verschieben Anfrage:**
```
🔔 "Sascha, du bist heute Abend nicht da? Kochen skippen oder verschieben?"
```

---

## Spezifikationen

| Kriterium | Wert |
|-----------|------|
| **Plattformen** | PWA (iOS + Android + Web) |
| **Personen** | 2-10 |
| **Benachrichtigungen** | Telegram (täglich 08:00 Uhr) |
| **Bestrafung** | Nein, nur Hinweis/Erinnerung |
| **Auth** | Nextcloud OAuth |
| **Telegram Verknüpfung** | Code-Verifikation (Key Exchange) |
| **Architektur** | Eine Instanz (ein Haushalt) |
| **Mitgliedschaft** | Jeder registriert sich einzeln |
| **Sichtbarkeit** | Jeder sieht nur seine eigenen Aufgaben |
| **Punktestand** | MVP (Fairness-Übersicht) |
| **Nextcloud** | Optionale Integration |

---

## Registrierungs-Prozess

### Telegram Verknüpfung

```
┌─────────────────┐         ┌─────────────────┐
│   Telegram Bot   │         │   Angular App   │
└────────┬────────┘         └────────┬────────┘
         │                            │
         │  /start                    │
         │ ─────────────────────────→│
         │                            │
         │  "Dein Code: ABC-123-XYZ" │
         │←──────────────────────────│
         │                            │
         │                     User gibt Code ein
         │                     "ABC-123-XYZ"
         │                            │
         │                    ┌──────┴──────┐
         │                    │ Verknüpft!   │
         │                    │ TG + App User│
         │                    └─────────────┘
```

### Ablauf:

1. **In der App:**
   - Registrieren mit Nextcloud OAuth
   - Profil → "Telegram verknüpfen"

2. **Im Telegram:**
   - Bot öffnen → `/start`
   - Bot antwortet: `Dein Verifikations-Code: ABC-123-XYZ`

3. **Zurück in der App:**
   - Code eingeben: `ABC-123-XYZ`
   - → Telegram Account + App Account sind verknüpft!

### Vorteile:
- ✅ Sicher - kein Login mit Passwörtern nötig
- ✅ Simpel - nur Code tauschen
- ✅ Privatsphäre - kein Phone Number nötig

---

## Infrastruktur (Docker Compose)

```
┌─────────────────────────────────────────────────────────┐
│                     Nginx (Port 80/443)                  │
│                                                          │
│   /api/*  ──────────────────────────→  Spring API       │
│   /*      ──────────────────────────→  Angular PWA       │
└─────────────────────────────────────────────────────────┘
                           │
         ┌─────────────────┼─────────────────┐
         │                 │                 │
         ▼                 ▼                 ▼
┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│   Spring    │  │    DB       │  │  Telegram    │
│   Backend   │  │  PostgreSQL │  │    Bot       │
└─────────────┘  └─────────────┘  └─────────────┘
```

### Nginx Config

```nginx
server {
    listen 80;
    server_name haushalt.deeg-mail.de;

    location /api/ {
        proxy_pass http://spring:8080/;
    }

    location / {
        root /usr/share/nginx/html;
        index index.html;
        try_files $uri $uri/ /index.html;
    }
}
```

### Docker Compose

```yaml
version: '3.8'

services:
  nginx:
    image: nginx:latest
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf:ro
      - ./frontend/dist:/usr/share/nginx/html:ro
    depends_on:
      - spring
    networks:
      - app-net

  spring:
    image: haushaltsplaner/spring:latest
    environment:
      - SPRING_DATASOURCE_URL=jdbc:postgresql://db:5432/haushalt
      - SPRING_DATASOURCE_USER=postgres
      - SPRING_DATASOURCE_PASSWORD=${DB_PASSWORD}
    depends_on:
      - db
    networks:
      - app-net

  db:
    image: postgres:15-alpine
    environment:
      - POSTGRES_DB=haushalt
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=${DB_PASSWORD}
    volumes:
      - ./postgres-data:/var/lib/postgresql/data
    networks:
      - app-net

  telegram-bot:
    image: haushaltsplaner/bot:latest
    environment:
      - TELEGRAM_BOT_TOKEN=${TELEGRAM_TOKEN}
      - API_URL=http://spring:8080
    depends_on:
      - spring
    networks:
      - app-net

networks:
  app-net:
    driver: bridge
```

---

## Mögliche Features

### MVP (Minimal Viable Product)
- [ ] Registrierung via Nextcloud OAuth
- [ ] Telegram Verknüpfung (Code-Verifikation)
- [ ] Aufgaben-Templates (vordefinierte Aufgaben)
- [ ] Eigene Aufgaben erstellen (frei)
- [ ] Abhängigkeiten/Exclusion Rules ("Kochen ≠ Katzenklos")
- [ ] Rotation berechnen (fairness)
- [ ] Wer muss heute was machen? (TODO Liste - eigene Aufgaben)
- [ ] Erinnerungen via Telegram (nur eigene Aufgaben)
- [ ] Aufgabe als "erledigt" abhacken
- [ ] Skip oder Verschieben bei Abwesenheit
- [ ] **Punktestand** (Eigene Punkte sehen)
- [ ] **Tägliche Morgen-Benachrichtigung** (Telegram, 08:00 Uhr - eigene Aufgaben)

### Possibly interesante Features
- [ ] KI-generierte Aufgaben-Vorschläge
- [ ] Bild Erkennung (Ist das Bad wirklich sauber? 📸)
- [ ] Sprachsteuerung ("Hey Javis, ich hab gekocht!")

---

## Technologie-Stack

| Komponente | Option |
|-----------|--------|
| **Frontend** | Angular PWA |
| **Backend** | Spring (Java/Kotlin) |
| **Deployment** | Docker Compose + Nginx |
| **Proxy** | Nginx (Port 80/443) |
| **API Pfad** | /api |
| **Static Files** | / |
| **Notifications** | Telegram Bot API |
| **Auth** | Nextcloud OAuth (via OpenID Connect) |
| **Nextcloud Integration** | Calendar Sync, Files App Integration (optional) |

---

## UI/UX Anforderungen

### Design
| Kriterium |要求 |
|-----------|-----|
| **Stil** | Modern, Clean, Minimalistisch |
| **Design System** | Material Design 3 / Tailwind CSS |
| **Farben** | Angenehm, nicht zu bunt |
| **Dark Mode** | Ja (System-Präferenz) |
| **Icons** | Lucide Icons / Material Symbols |

### Usability
| Kriterium |要求 |
|-----------|-----|
| **Intuitiv** | Selbsterklärend, keine Erklärung nötig |
| **Mobile First** | Optimiert für Smartphone |
| **Touch-Freundlich** | Große Buttons, genug Abstand |
| **Ladezeiten** | Schnell (< 2s) |
| **Offline** | PWA Cache |

### UI Prinzipien
- ✅ One-Hand-Bedienung möglich
- ✅ Keine verschachtelten Menüs
- ✅ Schneller Zugriff auf "heutige Aufgaben"
- ✅ Pull-to-Refresh
- ✅ Swipe-Actions für Skip/Verschieben
- ✅ Einfaches Abhaken mit Checkbox

---

## Qualitätssicherung

### Test-Abdeckung (MVP Requirement!)

| Test-Typ |要求 | Tool |
|-----------|-----|------|
| **Unit Tests** | ≥80% Coverage | JUnit, Mockito (Backend), Jasmine/Karma (Frontend) |
| **BDD Tests** | Alle User Flows | Cucumber (Gherkin Syntax) |
| **Integration Tests** | API Endpunkte | Spring Test, RestAssured |
| **E2E Tests** | Kritische Pfade | Cypress / Playwright |

### BDD mit Cucumber

**Beispiel: Skip-Aufgabe Feature**

```gherkin
# src/test/resources/skip_aufgabe.feature
Feature: Aufgabe skippen

  Scenario: Person ist abends nicht da
    Given Sascha hat eine Aufgabe "Kochen" heute
    And Sascha ist heute Abend nicht da
    When Sascha skippt die Aufgabe
    Then Alexandra übernimmt die Aufgabe "Kochen"
    And Der Punktestand bleibt unverändert

  Scenario: Person möchte verschieben
    Given Sascha hat eine Aufgabe "Kochen" heute
    And Sascha möchte verschieben
    When Sascha verschiebt die Aufgabe
    Then Sascha hat "Kochen" morgen
    And Alexandra hat heute keine额外 Aufgabe
```

### Test-Pyramide

```
        ┌─────────────┐
        │    E2E     │  ← Wenige, kritische Pfade
        ├─────────────┤
        │ Integration │  ← API Tests
        ├─────────────┤
        │    Unit     │  ← Viele, schnelle Tests
        └─────────────┘
```

### Requirements

- [ ] **Unit Tests:** ≥80% Coverage für Backend + Frontend
- [ ] **BDD:** Alle User Stories als Cucumber Tests
- [ ] **CI/CD:** Tests laufen bei jedem Push
- [ ] **Test-Daten:** Isolierte Test-DB, keine Production-Daten

---

## Beispiel: Rotation-Algorithmus

```
Input:
- Members: [Sascha, Alex]
- Tasks: [Kochen, Abwasch, Saugen]
- Regeln: [{Kochen, NOT, Abwasch}]

Output (heute):
- Sascha: Kochen
- Alex: Abwasch

Rotation nach jedem Kochen:
- Nächstes Mal: Alex kocht, Sascha macht Abwasch
```

---

## Offene Fragen / Diskussionsbedarf

- [x] Wie viele Personen max? → 2-10
- [x] Push-Benachrichtigungen oder nur Telegram? → Telegram
- [x] Bestrafung bei Vergessen? → Skip oder Übernehmen
- [x] Mehrere Haushalte? → Nein, eine Instanz
- [x] Mitgliedschaft? → Nach Login automatisch dabei
- [x] Aufgaben-Vorlagen? → Ja, vordefiniert + frei
- [x] Aufgaben-Abhängigkeiten? → Ja, Exclusion Rules
- [x] Nextcloud OAuth? → Ja, als Auth-Provider
- [x] Nextcloud Integration? → Optional, Calendar Sync

---

## Verwandte Apps

- [ ] Todoist (zu generisch)
- [ ] OurHome (US, nicht in DE)
- [ ] Trellis (AI-basiert, aber anders)

---

## Next Steps

1. [ ] Konzept finalisieren
2. [ ] Wireframes/skizzen
3. [ ] Technologie entscheiden
4. [ ] MVP Scope definieren

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
