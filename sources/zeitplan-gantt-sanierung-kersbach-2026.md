---
pageType: source
id: source.zeitplan-gantt-sanierung-kersbach-2026
title: Zeitplan Gantt Sanierung Kersbach 2026
sourceType: local-file
sourcePath: /home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html
ingestedAt: 2026-05-31T13:48:18.040Z
updatedAt: 2026-05-31T13:48:18.040Z
status: active
---

# Zeitplan Gantt Sanierung Kersbach 2026

## Source
- Type: `local-file`
- Path: `/home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html`
- Bytes: 11058
- Updated: 2026-05-31T13:48:18.040Z

## Content
```text
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sanierung Kersbach – Zeitplan</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: #1a1a2e;
    color: #e0e0e0;
    padding: 20px;
    min-height: 100vh;
  }
  h1 { text-align: center; color: #fff; margin-bottom: 4px; font-size: 20px; }
  .subtitle { text-align: center; color: #666; margin-bottom: 20px; font-size: 11px; }

  .legend { display: flex; gap: 16px; justify-content: center; margin-bottom: 20px; flex-wrap: wrap; }
  .legend-item { display: flex; align-items: center; gap: 6px; font-size: 10px; color: #888; }
  .legend-color { width: 14px; height: 14px; border-radius: 3px; }

  .stats { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 12px; max-width: 900px; margin: 0 auto 24px; }
  .stat { background: #2d2d44; border-radius: 10px; padding: 14px; text-align: center; }
  .stat-value { font-size: 22px; font-weight: bold; color: var(--accent, #3b82f6); }
  .stat-label { font-size: 10px; color: #888; margin-top: 4px; }

  .chart-container { overflow-x: auto; padding-bottom: 20px; }
  .chart { min-width: 1000px; }

  .header-row { display: flex; border-bottom: 2px solid #333; padding-bottom: 8px; margin-bottom: 10px; }
  .header-label { width: 120px; flex-shrink: 0; font-size: 10px; color: #666; }
  .header-months { flex: 1; display: flex; }
  .month { flex: 1; text-align: center; font-size: 9px; color: #555; border-left: 1px solid #222; padding: 3px 0; }
  .month.current { background: rgba(74, 222, 128, 0.15); color: #4ade80; }
  .month.done { background: rgba(74, 222, 128, 0.08); color: #4ade80; }

  .task-row { display: flex; align-items: center; margin-bottom: 10px; min-height: 32px; }
  .task-label { width: 120px; flex-shrink: 0; font-size: 12px; color: #ccc; padding-right: 10px; display: flex; align-items: center; gap: 6px; }
  .task-label .num { font-size: 10px; color: #555; }

  .task-bar-container { flex: 1; height: 24px; position: relative; background: #181818; border-radius: 4px; }
  .task-bar {
    position: absolute;
    height: 100%;
    border-radius: 4px;
    display: flex;
    align-items: center;
    padding: 0 10px;
    font-size: 10px;
    color: #fff;
    font-weight: 500;
    overflow: hidden;
    white-space: nowrap;
  }
  .task-bar.done { background: linear-gradient(90deg, #22c55e, #16a34a); }
  .task-bar.active { background: linear-gradient(90deg, #f59e0b, #d97706); }
  .task-bar.planned { background: linear-gradient(90deg, #3b82f6, #2563eb); }
  .task-bar.future { background: linear-gradient(90deg, #6b7280, #4b5563); }

  .year-divider { margin: 20px 0 10px; border-top: 1px dashed #444; font-size: 11px; color: #555; padding-top: 8px; }

  .milestones {
    max-width: 900px;
    margin: 24px auto;
    background: #2d2d44;
    border-radius: 12px;
    padding: 18px 24px;
    border-left: 4px solid #4ade80;
  }
  .milestones h3 { font-size: 13px; color: #4ade80; margin-bottom: 12px; }
  .milestone-list { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 8px; }
  .milestone-item { font-size: 11px; color: #ccc; padding-left: 16px; position: relative; }
  .milestone-item::before { content: '◆'; position: absolute; left: 0; color: #4ade80; font-size: 8px; top: 3px; }

  .note { max-width: 900px; margin: 20px auto; font-size: 11px; color: #555; text-align: center; }

  .footer { max-width: 900px; margin: 30px auto; text-align: center; font-size: 10px; color: #444; }
</style>
</head>
<body>

<h1>🏠 Sanierung Kersbach – Zeitplan</h1>
<div class="subtitle">Nach deinen Vorgaben · Stand: 31. Mai 2026</div>

<!-- Stats -->
<div class="stats">
  <div class="stat" style="--accent: #4ade80;"><div class="stat-value">642,25h</div><div class="stat-label">Gebucht</div></div>
  <div class="stat" style="--accent: #f59e0b;"><div class="stat-value">~900h</div><div class="stat-label">Noch offen</div></div>
  <div class="stat" style="--accent: #3b82f6;"><div class="stat-value">~1.536h</div><div class="stat-label">Gesamt</div></div>
  <div class="stat" style="--accent: #a855f7;"><div class="stat-value">Mai '27</div><div class="stat-label">Fertig</div></div>
</div>

<!-- Legend -->
<div class="legend">
  <div class="legend-item"><div class="legend-color" style="background: #22c55e;"></div>Abgeschlossen</div>
  <div class="legend-item"><div class="legend-color" style="background: #f59e0b;"></div>Aktuell/In Bearbeitung</div>
  <div class="legend-item"><div class="legend-color" style="background: #3b82f6;"></div>Geplant</div>
  <div class="legend-item"><div class="legend-color" style="background: #6b7280;"></div>Zukünftig</div>
</div>

<div class="chart-container">
<div class="chart">

  <!-- Header: Aug'25 - Jun'27 = 23 months -->
  <div class="header-row">
    <div class="header-label">Aufgabe</div>
    <div class="header-months">
      <div class="month done">Aug'25</div>
      <div class="month done">Sep'25</div>
      <div class="month done">Okt'25</div>
      <div class="month done">Nov'25</div>
      <div class="month done">Dez'25</div>
      <div class="month done">Jan'26</div>
      <div class="month done">Feb'26</div>
      <div class="month done">Mär'26</div>
      <div class="month done">Apr'26</div>
      <div class="month done">Mai'26</div>
      <div class="month current">Jun'26</div>
      <div class="month">Jul'26</div>
      <div class="month">Aug'26</div>
      <div class="month">Sep'26</div>
      <div class="month">Okt'26</div>
      <div class="month">Nov'26</div>
      <div class="month">Dez'26</div>
      <div class="month">Jan'27</div>
      <div class="month">Feb'27</div>
      <div class="month">Mär'27</div>
      <div class="month">Apr'27</div>
      <div class="month">Mai'27</div>
    </div>
  </div>

  <!-- 1. Abriss: Aug'25 - Jun'26 -->
  <div class="task-row">
    <div class="task-label"><span class="num">1.</span>Abriss</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 0%; width: 44%;">13.08.25 - 20.06.26</div>
    </div>
  </div>

  <!-- Elektrik Planung: Aug'25 - Apr'26 -->
  <div class="task-row">
    <div class="task-label"><span class="num">2a.</span>Elektrik Planung</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 0%; width: 35%;">25.08.25 - 04.04.26</div>
    </div>
  </div>

  <!-- Trockenbau: Jan'26 - Jun'26 -->
  <div class="task-row">
    <div class="task-label"><span class="num">3.</span>Trockenbau</div>
    <div class="task-bar-container">
      <div class="task-bar active" style="left: 22%; width: 22%;">17.01.26 - 20.06.26</div>
    </div>
  </div>

  <!-- Wärmepumpe: Apr'26 - Apr'26 -->
  <div class="task-row">
    <div class="task-label"><span class="num">4.</span>Wärmepumpe</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 35%; width: 4%;">04.04.26 - 26.04.26</div>
    </div>
  </div>

  <!-- Elektrik: Apr'26 - Sep'26 -->
  <div class="task-row">
    <div class="task-label"><span class="num">2b.</span>Elektrik</div>
    <div class="task-bar-container">
      <div class="task-bar planned" style="left: 35%; width: 26%;">04.04.26 - 30.09.26</div>
    </div>
  </div>

</div>
</div>

<div class="year-divider">—— 2026 / 2027 ——</div>

<div class="chart-container">
<div class="chart">

  <div class="header-row">
    <div class="header-label">Aufgabe</div>
    <div class="header-months">
      <div class="month done">Aug'25</div>
      <div class="month done">Sep'25</div>
      <div class="month done">Okt'25</div>
      <div class="month done">Nov'25</div>
      <div class="month done">Dez'25</div>
      <div class="month done">Jan'26</div>
      <div class="month done">Feb'26</div>
      <div class="month done">Mär'26</div>
      <div class="month done">Apr'26</div>
      <div class="month done">Mai'26</div>
      <div class="month current">Jun'26</div>
      <div class="month">Jul'26</div>
      <div class="month">Aug'26</div>
      <div class="month">Sep'26</div>
      <div class="month">Okt'26</div>
      <div class="month">Nov'26</div>
      <div class="month">Dez'26</div>
      <div class="month">Jan'27</div>
      <div class="month">Feb'27</div>
      <div class="month">Mär'27</div>
      <div class="month">Apr'27</div>
      <div class="month">Mai'27</div>
    </div>
  </div>

  <!-- Lehmputz: Sep'26 - Dez'26 -->
  <div class="task-row">
    <div class="task-label"><span class="num">5.</span>Lehmputz</div>
    <div class="task-bar-container">
      <div class="task-bar planned" style="left: 57%; width: 13%;">30.09.26 - 02.12.26</div>
    </div>
  </div>

  <!-- Boden: Dez'26 - Jan'27 -->
  <div class="task-row">
    <div class="task-label"><span class="num">6.</span>Boden</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 70%; width: 9%;">02.12.26 - 13.01.27</div>
    </div>
  </div>

  <!-- Decke: Jan'27 - Feb'27 -->
  <div class="task-row">
    <div class="task-label"><span class="num">7.</span>Decke</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 74%; width: 9%;">13.01.27 - 17.02.27</div>
    </div>
  </div>

  <!-- Türen: Feb'27 -->
  <div class="task-row">
    <div class="task-label"><span class="num">8.</span>Türen</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 78%; width: 4%;">17.02.27 - 24.02.27</div>
    </div>
  </div>

  <!-- WDVS: Apr'27 - Mai'27 -->
  <div class="task-row">
    <div class="task-label"><span class="num">9.</span>WDVS</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 87%; width: 13%;">01.04.27 - 27.05.27</div>
    </div>
  </div>

  <!-- FBH: Jun'27 - Aug'27 -->
  <div class="task-row">
    <div class="task-label"><span class="num">4.a</span>FBH</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 91%; width: 9%;">18.06.27 - 31.08.27</div>
    </div>
  </div>

</div>
</div>

<!-- Meilensteine -->
<div class="milestones">
  <h3>📍 Meilensteine</h3>
  <div class="milestone-list">
    <div class="milestone-item">✅ Abriss: Jun 2026</div>
    <div class="milestone-item">✅ Trockenbau: Jun 2026</div>
    <div class="milestone-item">⚡ Elektrik: Sep 2026</div>
    <div class="milestone-item">🏡 Lehmputz: Dez 2026</div>
    <div class="milestone-item">🔧 Boden: Jan 2027</div>
    <div class="milestone-item">🔨 Decke: Feb 2027</div>
    <div class="milestone-item">🚪 Türen: Feb 2027</div>
    <div class="milestone-item">🏗️ WDVS: Mai 2027</div>
    <div class="milestone-item">🔥 FBH: Jun-Aug 2027</div>
  </div>
</div>

<div class="note">
  Basierend auf deiner Timeline-Datei · 32h/Woche
</div>

<div class="footer">
  Sanierung Kersbach · 642,25h gebucht · Stand: 31. Mai 2026
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
