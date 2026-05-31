---
pageType: source
id: source.zeitplan-gantt-sanierung-kersbach-2026
title: Zeitplan Gantt Sanierung Kersbach 2026
sourceType: local-file
sourcePath: /home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html
ingestedAt: 2026-05-31T12:20:25.120Z
updatedAt: 2026-05-31T12:20:25.120Z
status: active
---

# Zeitplan Gantt Sanierung Kersbach 2026

## Source
- Type: `local-file`
- Path: `/home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html`
- Bytes: 12010
- Updated: 2026-05-31T12:20:25.120Z

## Content
```text
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sanierung Kersbach – Gantt Diagramm</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: #1a1a2e;
    color: #e0e0e0;
    padding: 20px;
    min-height: 100vh;
  }
  h1 {
    text-align: center;
    color: #fff;
    margin-bottom: 4px;
    font-size: 20px;
  }
  .subtitle {
    text-align: center;
    color: #666;
    margin-bottom: 20px;
    font-size: 11px;
  }

  .legend {
    display: flex;
    gap: 16px;
    justify-content: center;
    margin-bottom: 20px;
    flex-wrap: wrap;
  }
  .legend-item {
    display: flex;
    align-items: center;
    gap: 5px;
    font-size: 10px;
    color: #888;
  }
  .legend-color {
    width: 12px;
    height: 12px;
    border-radius: 3px;
  }

  .chart-container {
    overflow-x: auto;
    padding-bottom: 16px;
  }

  .chart {
    min-width: 1400px;
  }

  /* Header row with months */
  .header-row {
    display: flex;
    border-bottom: 2px solid #333;
    padding-bottom: 6px;
    margin-bottom: 6px;
  }
  .header-label {
    width: 180px;
    flex-shrink: 0;
    font-size: 10px;
    color: #666;
    padding-right: 12px;
  }
  .header-months {
    flex: 1;
    display: flex;
  }
  .month {
    flex: 1;
    text-align: center;
    font-size: 9px;
    color: #666;
    border-left: 1px solid #222;
    padding: 2px 0;
  }
  .month.current {
    background: rgba(74, 222, 128, 0.15);
    color: #4ade80;
    font-weight: bold;
  }

  /* Task rows */
  .task-row {
    display: flex;
    align-items: center;
    margin-bottom: 5px;
    min-height: 28px;
  }
  .task-label {
    width: 180px;
    flex-shrink: 0;
    font-size: 11px;
    color: #ccc;
    padding-right: 12px;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .task-label .status-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    flex-shrink: 0;
  }
  .task-label .status-dot.done { background: #4ade80; }
  .task-label .status-dot.in-progress { background: #f59e0b; }
  .task-label .status-dot.planned { background: #3b82f6; }
  .task-label .status-dot.future { background: #6b7280; }

  .task-bar-container {
    flex: 1;
    height: 20px;
    position: relative;
    background: #1a1a1a;
    border-radius: 3px;
  }
  .task-bar {
    position: absolute;
    height: 100%;
    border-radius: 3px;
    display: flex;
    align-items: center;
    padding: 0 6px;
    font-size: 9px;
    color: #fff;
    font-weight: 500;
    overflow: hidden;
    white-space: nowrap;
  }
  .task-bar.done { background: linear-gradient(90deg, #22c55e, #16a34a); }
  .task-bar.in-progress { background: linear-gradient(90deg, #f59e0b, #d97706); }
  .task-bar.planned { background: linear-gradient(90deg, #3b82f6, #2563eb); }
  .task-bar.future { background: linear-gradient(90deg, #6b7280, #4b5563); }

  /* Year divider */
  .year-divider {
    margin: 12px 0 8px 180px;
    border-top: 1px dashed #333;
    padding-top: 6px;
    font-size: 10px;
    color: #444;
  }

  /* Stats */
  .stats {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    gap: 10px;
    max-width: 1400px;
    margin: 20px auto;
  }
  .stat {
    background: #2d2d44;
    border-radius: 8px;
    padding: 10px;
    text-align: center;
  }
  .stat-value {
    font-size: 18px;
    font-weight: bold;
    color: var(--accent, #3b82f6);
  }
  .stat-label {
    font-size: 9px;
    color: #666;
    margin-top: 2px;
  }

  /* Hours breakdown */
  .breakdown {
    max-width: 1400px;
    margin: 20px auto;
    background: #2d2d44;
    border-radius: 10px;
    padding: 14px 18px;
  }
  .breakdown h3 {
    font-size: 12px;
    color: #888;
    margin-bottom: 10px;
  }
  .breakdown-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 8px;
  }
  .breakdown-item {
    display: flex;
    justify-content: space-between;
    font-size: 11px;
    padding: 4px 8px;
    background: #222;
    border-radius: 4px;
  }
  .breakdown-item .name { color: #ccc; }
  .breakdown-item .hours { color: #4ade80; font-weight: bold; }

  /* Milestones */
  .milestones {
    max-width: 1400px;
    margin: 20px auto;
    background: #2d2d44;
    border-radius: 10px;
    padding: 14px 18px;
    border-left: 4px solid #f59e0b;
  }
  .milestones h3 {
    font-size: 12px;
    color: #f59e0b;
    margin-bottom: 10px;
  }
  .milestone-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 6px;
  }
  .milestone-item {
    font-size: 10px;
    color: #ccc;
    padding-left: 14px;
    position: relative;
  }
  .milestone-item::before {
    content: '◆';
    position: absolute;
    left: 0;
    color: #4ade80;
    font-size: 7px;
    top: 3px;
  }

  .note {
    max-width: 1400px;
    margin: 14px auto;
    font-size: 10px;
    color: #444;
    text-align: center;
  }
</style>
</head>
<body>

<h1>🏠 Sanierung Kersbach – Zeitplan</h1>
<div class="subtitle">Daten aus OpenProject · Stand: 31. Mai 2026 · 642,25h gebucht</div>

<!-- Legend -->
<div class="legend">
  <div class="legend-item">
    <div class="legend-color" style="background: #22c55e;"></div>
    Abgeschlossen
  </div>
  <div class="legend-item">
    <div class="legend-color" style="background: #f59e0b;"></div>
    In Bearbeitung
  </div>
  <div class="legend-item">
    <div class="legend-color" style="background: #3b82f6;"></div>
    Geplant
  </div>
  <div class="legend-item">
    <div class="legend-color" style="background: #6b7280;"></div>
    Zukünftig
  </div>
</div>

<!-- Stats -->
<div class="stats">
  <div class="stat" style="--accent: #4ade80;">
    <div class="stat-value">642,25h</div>
    <div class="stat-label">Bisher geleistet</div>
  </div>
  <div class="stat" style="--accent: #f59e0b;">
    <div class="stat-value">~894h</div>
    <div class="stat-label">Noch offen</div>
  </div>
  <div class="stat" style="--accent: #3b82f6;">
    <div class="stat-value">~1.536h</div>
    <div class="stat-label">Gesamt geplant</div>
  </div>
</div>

<!-- Chart -->
<div class="chart-container">
<div class="chart">

  <!-- Header -->
  <div class="header-row">
    <div class="header-label">Aufgabe</div>
    <div class="header-months">
      <div class="month">Aug '25</div>
      <div class="month">Sep '25</div>
      <div class="month">Okt '25</div>
      <div class="month">Nov '25</div>
      <div class="month">Dez '25</div>
      <div class="month">Jan '26</div>
      <div class="month">Feb '26</div>
      <div class="month">Mär '26</div>
      <div class="month">Apr '26</div>
      <div class="month">Mai '26</div>
      <div class="month">Jun '26</div>
      <div class="month current">Jul '26</div>
      <div class="month">Aug '26</div>
      <div class="month">Sep '26</div>
      <div class="month">Okt '26</div>
      <div class="month">Nov '26</div>
      <div class="month">Dez '26</div>
      <div class="month">Jan '27</div>
      <div class="month">Feb '27</div>
      <div class="month">Mär '27</div>
      <div class="month">Apr '27</div>
      <div class="month">Mai '27</div>
      <div class="month">Jun '27</div>
    </div>
  </div>

  <!-- 1. ABRISS -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot done"></span>
1. Abriss (~269h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 0%; width: 35%;">✅ ~269h fertig</div>
    </div>
  </div>

  <!-- 2. WÄRMEPUMPE + FBH -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot done"></span>
4. Wärmepumpe (~85h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 30%; width: 25%;">✅ ~85h fertig</div>
    </div>
  </div>

  <!-- 3. TROCKENBAU -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot in-progress"></span>
3. Trockenbau (~167h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 20%; width: 20%;">~105h ✅</div>
      <div class="task-bar in-progress" style="left: 40%; width: 17%;">Rest läuft</div>
    </div>
  </div>

  <!-- 4. BODEN -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot in-progress"></span>
5. Boden (~175h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 25%; width: 10%;">~140h ✅</div>
      <div class="task-bar planned" style="left: 43%; width: 13%;">Estrich</div>
    </div>
  </div>

  <!-- 5. ELEKTRIK -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot in-progress"></span>
2. Elektrik (~183h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 0%; width: 15%;">~43h ✅</div>
      <div class="task-bar in-progress" style="left: 15%; width: 17%;">Rest läuft</div>
    </div>
  </div>

  <!-- 6. DECKE -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot planned"></span>
7. Decke (~140h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar planned" style="left: 43%; width: 22%;">Geplant: Aug-Okt</div>
    </div>
  </div>

  <!-- 7. LEHMPUTZ -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot future"></span>
6. Lehmputz (~284h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 52%; width: 26%;">Sep-Okt: ~6 Wochen</div>
    </div>
  </div>

  <!-- 8. TÜREN -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot future"></span>
8. Türen (~21h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 74%; width: 9%;">Okt '26</div>
    </div>
  </div>

  <!-- Year divider -->
  <div class="year-divider">—— 2027 ——</div>

  <!-- 9. FASSADE -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot future"></span>
9. WDVS (~235h)
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 78%; width: 22%;">Mär-Jun '27</div>
    </div>
  </div>

</div>
</div>

<!-- Hours Breakdown -->
<div class="breakdown">
  <h3>📊 Stunden-Aufschlüsselung (642,25h gebucht)</h3>
  <div class="breakdown-grid">
    <div class="breakdown-item">
      <span class="name">1. Abriss</span>
      <span class="hours">269h</span>
    </div>
    <div class="breakdown-item">
      <span class="name">2. Trockenbau</span>
      <span class="hours">105h</span>
    </div>
    <div class="breakdown-item">
      <span class="name">3. Boden</span>
      <span class="hours">140h</span>
    </div>
    <div class="breakdown-item">
      <span class="name">4. Elektrik</span>
      <span class="hours">43h</span>
    </div>
    <div class="breakdown-item">
      <span class="name">5. Wärmepumpe</span>
      <span class="hours">85h</span>
    </div>
    <div class="breakdown-item">
      <span class="name">Verbleibend</span>
      <span class="hours">~894h</span>
    </div>
  </div>
</div>

<!-- Milestones -->
<div class="milestones">
  <h3>📍 Meilensteine</h3>
  <div class="milestone-list">
    <div class="milestone-item">✅ Abriss + Wärmepumpe fertig</div>
    <div class="milestone-item">⚡ KW27: Trockenbau + Sockel → Estrich</div>
    <div class="milestone-item">🏠 KW28-31: Estrich-Trocknung (Pause)</div>
    <div class="milestone-item">🔌 KW34: Elektrik + Boden + Decke</div>
    <div class="milestone-item">🏡 KW40: Lehmputz fertig</div>
    <div class="milestone-item">🚪 KW42: Türen + Rest</div>
    <div class="milestone-item">🏗️ Juni 2027: WDVS fertig</div>
  </div>
</div>

<div class="note">
  Zeitstrahl: Aug 2025 → Jun 2027 · KW 35 = September 2026 · KW 52 = Dezember 2026
</div>

</body>
</html>
```

## Notes
<!-- openclaw:human:start -->
<!-- openclaw:human:end -->

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
