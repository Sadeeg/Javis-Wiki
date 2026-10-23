---
id: openproject-api
pageType: source
title: "OpenProject API v3 (Instanz Kersbach)"
sourceType: web-reference
sourceUrl: https://www.openproject.org/docs/api/v3/
ingestedAt: 2026-10-23T12:45:00.000Z
updatedAt: 2026-10-23T12:45:00.000Z
status: active
---

# OpenProject API v3

Schnittstelle, über die der Bauzeiter die Stundenbuchungen des Projekts
„Kersbach Baustelle" (Projekt-ID 3) liest. Instanz: `project.deeg-mail.de`,
Auth als Basic Auth mit `username=apikey` und dem API-Key als Passwort
(Credentials: `~/.openclaw/credentials/openproject.json`).

## Verwendete Endpunkte

| Zweck | Endpunkt |
|---|---|
| Work Packages (Tasks) | `GET /api/v3/projects/3/work_packages` |
| Zeitbuchungen | `GET /api/v3/time_entries` |
| Projekte | `GET /api/v3/projects` |

## Dokumentation

- API-Referenz: https://www.openproject.org/docs/api/v3/
- Im Projekt abgerufene Daten: [[sources/openproject-taskbilanz]]

## ⚠️ Stolperstellen (verifiziert 22.10.2026)

- `page` wird von der API **ignoriert** – es kommt immer Seite 1.
- `offset` funktioniert, ist aber **1-indexiert** (`offset=1` → Einträge 1..pageSize).
- Ohne Pagination liefert `pageSize=124` nur 124 von 227 Zeitbuchungen
  (787 h statt 878,50 h) → **immer `pageSize=500` verwenden**.

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[syntheses/kersbach-status|Kersbach Baustelle – Aktueller Stand]]
<!-- openclaw:wiki:related:end -->
