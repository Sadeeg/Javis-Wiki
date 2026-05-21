---
id: heartbeat
pageType: source
title: HEARTBEAT.md – OpenClaw Cron Jobs für Second Brain
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# HEARTBEAT.md – OpenClaw Cron Jobs für Second Brain

## Syntax
Jede Zeile: `minute hour day month weekday task`

## Wöchentlicher Knowledge Digest
```
0 20 * * 0 weekly_digest
```
Jeden **Sonntag um 20:00 MESZ**:
- KW-Stunden aus OpenProject abrufen
- Neue Dokumente in Nextcloud/Projekt Haus prüfen  
- Wiki-Lint Check
- Zusammenfassung per Telegram senden

## Morning Resurface
```
0 9 * * 1-5 morning_resurface
```
**Mo-Fr um 9:00 MESZ**:
- Today's KW und offene Aufgaben
- 2-3 relevante Wiki-Einträge
- Per Telegram senden

## Auto-Wiki-Push (täglich um 22:00 MESZ) ✅ Aktiviert
```
0 22 * * * cd ~/.openclaw/wiki/main && git add -A && git commit -m "auto: $(date +\%Y-\%m-\%d)" && git push
```
Automatischer Git-Push jeden Abend um 22:00 MESZ.

## Auto-Capture (on-demand)
Wenn Sascha "merk dir" / "capture" sagt → automatisch:
1. URL/Content analysieren
2. Core-Insight in 1-2 Sätzen
3. 2-3 Topic-Tags
4. In bau-wiki/ einordnen
5. In log/ protokollieren

## Capture Trigger
- "merk dir" / "remember" / "capture"
- "schreib das auf" / "note this"  
- "für später" / "for later"
- "das solltest du wissen" / "you should know this"

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
