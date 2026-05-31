---
pageType: source
id: source.zeitplan-gantt-sanierung-kersbach2026
title: Zeitplan Gantt Sanierung Kersbach2026
sourceType: local-file
sourcePath: /home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html
ingestedAt: 2026-05-31T11:52:25.948Z
updatedAt: 2026-05-31T11:52:25.948Z
status: active
---

# Zeitplan Gantt Sanierung Kersbach2026

## Source
- Type: `local-file`
- Path: `/home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html`
- Bytes: 11088
- Updated: 2026-05-31T11:52:25.948Z

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
    padding: 24px;
    min-height: 100vh;
  }
  h1 {
    text-align: center;
    color: #fff;
    margin-bottom: 4px;
    font-size: 22px;
  }
  .subtitle {
    text-align: center;
    color: #666;
    margin-bottom: 24px;
    font-size: 12px;
  }

  .legend {
    display: flex;
    gap: 20px;
    justify-content: center;
    margin-bottom: 24px;
    flex-wrap: wrap;
  }
  .legend-item {
    display: flex;
    align-items: center;
    gap: 6px;
    font-size: 11px;
    color: #888;
  }
  .legend-color {
    width: 14px;
    height: 14px;
    border-radius: 3px;
  }

  .chart-container {
    overflow-x: auto;
    padding-bottom: 20px;
  }

  .chart {
    min-width: 1200px;
    position: relative;
  }

  /* Header row with months */
  .header-row {
    display: flex;
    border-bottom: 2px solid #333;
    padding-bottom: 8px;
    margin-bottom: 8px;
  }
  .header-label {
    width: 200px;
    flex-shrink: 0;
    font-size: 11px;
    color: #666;
    padding-right: 16px;
  }
  .header-months {
    flex: 1;
    display: flex;
  }
  .month {
    flex: 1;
    text-align: center;
    font-size: 11px;
    color: #888;
    border-left: 1px solid #333;
    padding: 4px 0;
  }
  .month.current {
    background: rgba(74, 222, 128, 0.1);
    color: #4ade80;
  }

  /* Task rows */
  .task-row {
    display: flex;
    align-items: center;
    margin-bottom: 6px;
    min-height: 32px;
  }
  .task-label {
    width: 200px;
    flex-shrink: 0;
    font-size: 12px;
    color: #ccc;
    padding-right: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .task-label .status-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    flex-shrink: 0;
  }
  .task-label .status-dot.done { background: #4ade80; }
  .task-label .status-dot.in-progress { background: #f59e0b; }
  .task-label .status-dot.new { background: #6b7280; }

  .task-bar-container {
    flex: 1;
    height: 24px;
    position: relative;
    background: #222;
    border-radius: 4px;
 }
  .task-bar {
    position: absolute;
    height: 100%;
    border-radius: 4px;
    display: flex;
    align-items: center;
    padding: 0 8px;
    font-size: 10px;
    color: #fff;
    font-weight: 500;
    overflow: hidden;
    white-space: nowrap;
  }
  .task-bar.done { background: linear-gradient(90deg, #22c55e, #16a34a); }
  .task-bar.in-progress { background: linear-gradient(90deg, #f59e0b, #d97706); }
  .task-bar.planned { background: linear-gradient(90deg, #3b82f6, #2563eb); }
  .task-bar.future { background: linear-gradient(90deg, #6b7280, #4b5563); }

  .task-hours {
    font-size: 10px;
    color: #888;
    margin-left: 8px;
  }

  /* Year divider */
  .year-divider {
    margin: 16px 0 8px 200px;
    border-top: 1px dashed #333;
    padding-top: 8px;
    font-size: 11px;
    color: #555;
  }

  /* Stats */
  .stats {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 12px;
    max-width: 1200px;
    margin: 24px auto;
  }
  .stat {
    background: #2d2d44;
    border-radius: 8px;
    padding: 12px;
    text-align: center;
  }
  .stat-value {
    font-size: 20px;
    font-weight: bold;
    color: var(--accent, #3b82f6);
  }
  .stat-label {
    font-size: 10px;
    color: #666;
    margin-top: 2px;
  }

  /* Milestones */
  .milestones {
    max-width: 1200px;
    margin: 24px auto;
    background: #2d2d44;
    border-radius: 12px;
    padding: 16px 20px;
    border-left: 4px solid #f59e0b;
  }
  .milestones h3 {
    font-size: 13px;
    color: #f59e0b;
    margin-bottom: 12px;
  }
  .milestone-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 8px;
  }
  .milestone-item {
    font-size: 11px;
    color: #ccc;
    padding-left: 16px;
    position: relative;
  }
  .milestone-item::before {
    content: '◆';
    position: absolute;
    left: 0;
    color: #4ade80;
    font-size: 8px;
    top: 3px;
  }

  /* Note */
  .note {
    max-width: 1200px;
    margin: 16px auto;
    font-size: 11px;
    color: #555;
    text-align: center;
  }
</style>
</head>
<body>

<h1>🏠 Sanierung Kersbach – Zeitplan</h1>
<div class="subtitle">Daten aus OpenProject · Stand: 31. Mai 2026</div>

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
  <div class="stat" style="--accent: #22c55e;">
    <div class="stat-value">~500h</div>
    <div class="stat-label">Bisher geleistet</div>
  </div>
  <div class="stat" style="--accent: #f59e0b;">
    <div class="stat-value">~1.536h</div>
    <div class="stat-label">Gesamt geplant</div>
  </div>
  <div class="stat" style="--accent: #3b82f6;">
    <div class="stat-value">~1.000h</div>
    <div class="stat-label">Noch offen</div>
  </div>
  <div class="stat" style="--accent: #8b5cf6;">
<div class="stat-value">~235h</div>
    <div class="stat-label">WDVS (März 2027)</div>
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

  <!-- Abriss -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot done"></span>
1. Abriss
    </div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 0%; width: 47%;">~288h ✅</div>
    </div>
  </div>

  <!-- Wandvorbereitung -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot done"></span>
      Wandvorbereitung
    </div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 21%; width: 10%;">~88h ✅</div>
    </div>
  </div>

  <!-- Trockenbau -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot in-progress"></span>
      2. Trockenbau
    </div>
    <div class="task-bar-container">
      <div class="task-bar in-progress" style="left: 30%; width: 18%;">~105h ·52%</div>
    </div>
  </div>

  <!-- Elektrik -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot in-progress"></span>
3. Elektrik
    </div>
    <div class="task-bar-container">
      <div class="task-bar in-progress" style="left: 0%; width: 42%;">~183h · 23%</div>
    </div>
  </div>

  <!-- Bodenvorbereitungen -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot in-progress"></span>
4. Boden (Vorbereitung)
    </div>
    <div class="task-bar-container">
      <div class="task-bar in-progress" style="left: 41%; width: 7%;">~50h</div>
    </div>
  </div>

  <!-- Estrich -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot new"></span>
      Estrich + FBH
    </div>
    <div class="task-bar-container">
      <div class="task-bar planned" style="left: 45%; width: 12%;">Juli '26</div>
    </div>
  </div>

  <!-- Lehmputz -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot new"></span>
      5. Lehmputz
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 52%; width: 26%;">Sep-Okt '26 · ~284h</div>
    </div>
  </div>

  <!-- Decke -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot new"></span>
      6. Decke abhängen
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 48%; width: 22%;">Aug-Okt '26 · ~140h</div>
    </div>
  </div>

  <!-- Türen -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot new"></span>
      7. Türen einbauen
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 74%; width: 9%;">Okt '26 · ~21h</div>
    </div>
  </div>

  <!-- Badumbau -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot new"></span>
      Badumbau
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 46%; width: 4%;">Jul '26</div>
    </div>
  </div>

  <!-- Year divider -->
  <div class="year-divider">—— 2027 ——</div>

  <!-- WDVS Fassade -->
  <div class="task-row">
    <div class="task-label">
      <span class="status-dot new"></span>
      8. WDVS Fassade
    </div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 78%; width: 22%;">Mär-Jun '27 · ~235h</div>
    </div>
  </div>

</div>
</div>

<!-- Milestones -->
<div class="milestones">
  <h3>📍 Meilensteine</h3>
  <div class="milestone-list">
    <div class="milestone-item">✅ Abriss + Wandvorbereitung fertig</div>
    <div class="milestone-item">⚡ KW27: Trockenbau + Sockel fertig → Estrich</div>
    <div class="milestone-item">🏠 KW 28-31: Estrich-Trocknung (Pause)</div>
    <div class="milestone-item">🔌 KW 34: Elektrik + Boden + Decke fertig</div>
    <div class="milestone-item">🏡 KW 40: Lehmputz fertig</div>
    <div class="milestone-item">🚪 KW 42: Türen + Rest fertig</div>
    <div class="milestone-item">🏗️ Juni 2027: WDVS Fassade fertig</div>
  </div>
</div>

<div class="note">
  Datenquelle: OpenProject API · Zeitplan basiert auf Sanierungsfahrplan + OpenProject Tasks<br>
  Hinweis:Estrich benötigt ~4 Wochen Trocknung · Lehmputz benötigt ~6 Wochen (3 Lagen + Trocknung)
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
