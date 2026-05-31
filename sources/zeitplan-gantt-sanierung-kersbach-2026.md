---
pageType: source
id: source.zeitplan-gantt-sanierung-kersbach-2026
title: Zeitplan Gantt Sanierung Kersbach 2026
sourceType: local-file
sourcePath: /home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html
ingestedAt: 2026-05-31T13:27:02.619Z
updatedAt: 2026-05-31T13:27:02.619Z
status: active
---

# Zeitplan Gantt Sanierung Kersbach 2026

## Source
- Type: `local-file`
- Path: `/home/sascha/.openclaw/workspace/obsidian_vault/Baustelle/bau-wiki/wiki/konzepte/Zeitplan-Gantt.html`
- Bytes: 16477
- Updated: 2026-05-31T13:27:02.619Z

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
    padding: 16px;
    min-height: 100vh;
  }
  h1 { text-align: center; color: #fff; margin-bottom: 2px; font-size: 18px; }
  .subtitle { text-align: center; color: #666; margin-bottom: 16px; font-size: 10px; }

  .legend { display: flex; gap: 12px; justify-content: center; margin-bottom: 16px; flex-wrap: wrap; }
  .legend-item { display: flex; align-items: center; gap: 4px; font-size: 9px; color: #888; }
  .legend-color { width: 10px; height: 10px; border-radius: 2px; }

  .chart-container { overflow-x: auto; padding-bottom: 12px; }
  .chart { min-width: 1200px; }

  .header-row { display: flex; border-bottom: 1px solid #333; padding-bottom: 4px; margin-bottom: 4px; }
  .header-label { width: 150px; flex-shrink: 0; font-size: 9px; color: #555; padding-right: 8px; }
  .header-months { flex: 1; display: flex; }
  .month { flex: 1; text-align: center; font-size: 8px; color: #555; border-left: 1px solid #1a1a1a; padding: 1px 0; }
  .month.current { background: rgba(74, 222, 128, 0.15); color: #4ade80; font-weight: bold; }
  .month.done { background: rgba(74, 222, 128, 0.08); color: #4ade80; }

  .task-row { display: flex; align-items: center; margin-bottom: 4px; min-height: 22px; }
  .task-label { width: 150px; flex-shrink: 0; font-size: 10px; color: #ccc; padding-right: 8px; display: flex; align-items: center; gap: 4px; }
  .status-dot { width: 6px; height: 6px; border-radius: 50%; flex-shrink: 0; }
  .status-dot.done { background: #4ade80; }
  .status-dot.in-progress { background: #f59e0b; }
  .status-dot.planned { background: #3b82f6; }
  .status-dot.future { background: #6b7280; }

  .task-bar-container { flex: 1; height: 16px; position: relative; background: #151515; border-radius: 2px; }
  .task-bar { position: absolute; height: 100%; border-radius: 2px; display: flex; align-items: center; padding: 0 4px; font-size: 8px; color: #fff; font-weight: 500; overflow: hidden; white-space: nowrap; }
  .task-bar.done { background: linear-gradient(90deg, #22c55e, #16a34a); }
  .task-bar.in-progress { background: linear-gradient(90deg, #f59e0b, #d97706); }
  .task-bar.planned { background: linear-gradient(90deg, #3b82f6, #2563eb); }
  .task-bar.future { background: linear-gradient(90deg, #5a6270, #4b5563); }

  .year-divider { margin: 8px 0 6px 150px; border-top: 1px dashed #333; padding-top: 4px; font-size: 9px; color: #444; }

  .phase-box { max-width: 1200px; margin: 12px auto; background: #2a2a3e; border-radius: 8px; padding: 10px 14px; border-left: 3px solid #f59e0b; }
  .phase-box h3 { font-size: 10px; color: #f59e0b; margin-bottom: 6px; }
  .phase-box p { font-size: 9px; color: #aaa; line-height: 1.4; }

  .stats { display: grid; grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); gap: 8px; max-width: 1200px; margin: 12px auto; }
  .stat { background: #2d2d44; border-radius: 6px; padding: 8px; text-align: center; }
  .stat-value { font-size: 14px; font-weight: bold; color: var(--accent, #3b82f6); }
  .stat-label { font-size: 8px; color: #666; margin-top: 1px; }

  .breakdown { max-width: 1200px; margin: 12px auto; background: #2d2d44; border-radius: 8px; padding: 10px 14px; }
  .breakdown h3 { font-size: 10px; color: #888; margin-bottom: 6px; }
  .breakdown-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 5px; }
  .breakdown-item { display: flex; justify-content: space-between; font-size: 9px; padding: 3px 6px; background: #1a1a2e; border-radius: 3px; }
  .breakdown-item .name { color: #bbb; }
  .breakdown-item .hours { color: #4ade80; font-weight: bold; }

  .milestones { max-width: 1200px; margin: 12px auto; background: #2d2d44; border-radius: 8px; padding: 10px 14px; border-left: 3px solid #4ade80; }
  .milestones h3 { font-size: 10px; color: #4ade80; margin-bottom: 6px; }
  .milestone-list { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 4px; }
  .milestone-item { font-size: 9px; color: #bbb; padding-left: 12px; position: relative; }
  .milestone-item::before { content: '◆'; position: absolute; left: 0; color: #4ade80; font-size: 6px; top: 2px; }

  .calc-box { max-width: 1200px; margin: 12px auto; background: #2d2d44; border-radius: 8px; padding: 10px 14px; border-left: 3px solid #a855f7; }
  .calc-box h3 { font-size: 10px; color: #a855f7; margin-bottom: 6px; }
  .calc-item { font-size: 9px; color: #bbb; margin-bottom: 3px; }
  .calc-total { font-size: 10px; color: #f59e0b; font-weight: bold; margin-top: 6px; }

  .note { max-width: 1200px; margin: 10px auto; font-size: 9px; color: #444; text-align: center; }
</style>
</head>
<body>

<h1>🏠 Sanierung Kersbach – Zeitplan (REALISTISCH)</h1>
<div class="subtitle">32h/Woche · 642,25h gebucht · Stand: 31. Mai 2026</div>

<div class="legend">
  <div class="legend-item"><div class="legend-color" style="background: #22c55e;"></div>Abgeschlossen</div>
  <div class="legend-item"><div class="legend-color" style="background: #f59e0b;"></div>In Bearbeitung</div>
  <div class="legend-item"><div class="legend-color" style="background: #3b82f6;"></div>Geplant</div>
  <div class="legend-item"><div class="legend-color" style="background: #6b7280;"></div>Zukünftig</div>
</div>

<div class="stats">
  <div class="stat" style="--accent: #4ade80;"><div class="stat-value">642,25h</div><div class="stat-label">Gebucht</div></div>
  <div class="stat" style="--accent: #f59e0b;"><div class="stat-value">~900h</div><div class="stat-label">Noch offen</div></div>
  <div class="stat" style="--accent: #3b82f6;"><div class="stat-value">~1.536h</div><div class="stat-label">Gesamt</div></div>
  <div class="stat" style="--accent: #a855f7;"><div class="stat-value">32h/Wo</div><div class="stat-label">Tempo</div></div>
</div>

<!-- Calculation -->
<div class="calc-box">
  <h3>📐 Realistische Berechnung</h3>
  <div class="calc-item">• Elektrik Rest: ~140h | Boden: ~175h | Lehmputz: ~284h | Decke: ~140h | Türen: ~21h</div>
  <div class="calc-item">• Aktiv: 140+175+284+140+21 = 760h</div>
  <div class="calc-item">• Lehmputz Trocknung (6 Wochen): = 192h Wartezeit (parallel zu anderen Arbeiten)</div>
  <div class="calc-item">• Aktiv mit Parallelarbeit: ~568h</div>
  <div class="calc-item">• 568h ÷ 32h/Woche = ~18 Wochen</div>
  <div class="calc-total">→ Realistisch: KW32 bis KW51 (~19 Wochen)</div>
</div>

<!-- Phase 1 -->
<div class="phase-box">
  <h3>📋 PHASE 1: Vor Estrich (KW22-KW27)</h3>
  <p>Trockenbau + Elektrik-Vorbereitung + Sockel-Leisten → Estrichleger KW28</p>
</div>

<div class="chart-container">
<div class="chart">

  <!-- Header: Aug'25 - Apr'27 -->
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
      <div class="month in-progress">Jun'26</div>
      <div class="month current">Jul'26</div>
      <div class="month">Aug'26</div>
      <div class="month">Sep'26</div>
      <div class="month">Okt'26</div>
      <div class="month">Nov'26</div>
      <div class="month">Dez'26</div>
      <div class="month">Jan'27</div>
      <div class="month">Feb'27</div>
      <div class="month">Mär'27</div>
      <div class="month">Apr'27</div>
    </div>
  </div>

  <!-- 1. ABRISS: Aug'25-Jan'26 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot done"></span>1. Abriss</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 0%; width: 24%;">✅ 269h</div>
    </div>
  </div>

  <!-- 4. WÄRMEPUMPE: Jan-Mai'26 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot done"></span>4. Wärmepumpe</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 24%; width: 20%;">✅ 85h</div>
    </div>
  </div>

  <!-- 3. TROCKENBAU: Feb-Jul'26 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot in-progress"></span>3. Trockenbau</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 19%; width: 19%;">~105h ✅</div>
      <div class="task-bar in-progress" style="left: 38%; width: 10%;">Rest</div>
    </div>
  </div>

  <!-- Elektrik VORBEREITUNG -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot done"></span>2. Elektrik (Vorb.)</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 33%; width: 14%;">~43h ✅</div>
    </div>
  </div>

  <!-- Boden bisher -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot done"></span>5. Boden (Vorb.)</div>
    <div class="task-bar-container">
      <div class="task-bar done" style="left: 33%; width: 14%;">~140h ✅</div>
    </div>
  </div>

</div>
</div>

<!-- Phase 2 -->
<div class="phase-box" style="border-color: #3b82f6;">
  <h3>📋 PHASE 2: Estrich + Trocknung (KW28-KW31)</h3>
  <p>Estrichleger KW28 → ~4 Wochen Trocknung → Ab KW32: Phase 3</p>
</div>

<div class="chart-container">
<div class="chart">
  <div class="header-row">
    <div class="header-label">Fortsetzung</div>
    <div class="header-months">
      <div class="month done">Aug'25</div><div class="month done">Sep'25</div><div class="month done">Okt'25</div><div class="month done">Nov'25</div><div class="month done">Dez'25</div>
      <div class="month done">Jan'26</div><div class="month done">Feb'26</div><div class="month done">Mär'26</div><div class="month done">Apr'26</div><div class="month done">Mai'26</div>
      <div class="month in-progress">Jun'26</div><div class="month current">Jul'26</div>
      <div class="month">Aug'26</div><div class="month">Sep'26</div><div class="month">Okt'26</div><div class="month">Nov'26</div><div class="month">Dez'26</div>
      <div class="month">Jan'27</div><div class="month">Feb'27</div><div class="month">Mär'27</div><div class="month">Apr'27</div>
    </div>
  </div>

  <!-- Estrich: Jul-Aug -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot planned"></span>⏸ Estrich-Trocknung</div>
    <div class="task-bar-container">
      <div class="task-bar planned" style="left: 48%; width: 19%;">Jul-Sep: Pause</div>
    </div>
  </div>

</div>
</div>

<!-- Phase 3 -->
<div class="phase-box" style="border-color: #22c55e;">
  <h3>📋 PHASE 3: Nach Estrich (KW32-KW50)</h3>
  <p>18 Wochen Arbeitszeit · Parallelarbeit möglich · Lehmputz-Trocknung überbrückt Wartezeit</p>
</div>

<div class="chart-container">
<div class="chart">
  <div class="header-row">
    <div class="header-label">Aufgabe</div>
    <div class="header-months">
      <div class="month done">Aug'25</div><div class="month done">Sep'25</div><div class="month done">Okt'25</div><div class="month done">Nov'25</div><div class="month done">Dez'25</div>
      <div class="month done">Jan'26</div><div class="month done">Feb'26</div><div class="month done">Mär'26</div><div class="month done">Apr'26</div><div class="month done">Mai'26</div>
      <div class="month in-progress">Jun'26</div><div class="month current">Jul'26</div>
      <div class="month current">Aug'26</div><div class="month">Sep'26</div><div class="month">Okt'26</div><div class="month">Nov'26</div><div class="month">Dez'26</div>
      <div class="month">Jan'27</div><div class="month">Feb'27</div><div class="month">Mär'27</div><div class="month">Apr'27</div>
    </div>
  </div>

  <!-- 2. ELEKTRIK: Aug-Okt'26 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot future"></span>2. Elektrik</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 52%; width: 14%;">Aug-Okt</div>
    </div>
  </div>

  <!-- 5. BODEN: Aug-Sep'26 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot future"></span>5. Bodenbelag</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 52%; width: 10%;">Aug-Sep</div>
    </div>
  </div>

  <!-- 6. LEHMPUTZ: Aug-Nov'26 (inkl. Trocknung) -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot future"></span>6. Lehmputz</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 52%; width: 19%;">Aug-Nov: 6 Wochen</div>
    </div>
  </div>

  <!-- 7. DECKE: Sep-Nov'26 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot future"></span>7. Decke</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 57%; width: 14%;">Sep-Nov</div>
    </div>
  </div>

  <!-- 8. TÜREN: Nov'26 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot future"></span>8. Türen</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 67%; width: 5%;">Nov</div>
    </div>
  </div>

</div>
</div>

<!-- Year divider -->
<div class="year-divider">—— 2027 ——</div>

<div class="chart-container">
<div class="chart">
  <div class="header-row">
    <div class="header-label">Fortsetzung</div>
    <div class="header-months">
      <div class="month done">Aug'25</div><div class="month done">Sep'25</div><div class="month done">Okt'25</div><div class="month done">Nov'25</div><div class="month done">Dez'25</div>
      <div class="month done">Jan'26</div><div class="month done">Feb'26</div><div class="month done">Mär'26</div><div class="month done">Apr'26</div><div class="month done">Mai'26</div>
      <div class="month in-progress">Jun'26</div><div class="month current">Jul'26</div>
      <div class="month current">Aug'26</div><div class="month">Sep'26</div><div class="month">Okt'26</div><div class="month">Nov'26</div><div class="month">Dez'26</div>
      <div class="month">Jan'27</div><div class="month">Feb'27</div><div class="month">Mär'27</div><div class="month">Apr'27</div><div class="month">Mai'27</div>
    </div>
  </div>

  <!-- 9. WDVS: Apr-Mai'27 -->
  <div class="task-row">
    <div class="task-label"><span class="status-dot future"></span>9. WDVS</div>
    <div class="task-bar-container">
      <div class="task-bar future" style="left: 81%; width: 19%;">Apr-Mai 2027</div>
    </div>
  </div>

</div>
</div>

<!-- Hours Breakdown -->
<div class="breakdown">
  <h3>📊 Gebuchte Stunden (642,25h)</h3>
  <div class="breakdown-grid">
    <div class="breakdown-item"><span class="name">1. Abriss</span><span class="hours">269h ✅</span></div>
    <div class="breakdown-item"><span class="name">4. Wärmepumpe</span><span class="hours">85h ✅</span></div>
    <div class="breakdown-item"><span class="name">3. Trockenbau</span><span class="hours">105h ✅</span></div>
    <div class="breakdown-item"><span class="name">2. Elektrik (Vorb.)</span><span class="hours">43h ✅</span></div>
    <div class="breakdown-item"><span class="name">5. Boden (Vorb.)</span><span class="hours">140h ✅</span></div>
  </div>
</div>

<!-- Meilensteine -->
<div class="milestones">
  <h3>📍 Meilensteine (REALISTISCH)</h3>
  <div class="milestone-list">
    <div class="milestone-item">✅ Abriss + Wärmepumpe fertig</div>
    <div class="milestone-item">⚡ KW27: Trockenbau fertig</div>
    <div class="milestone-item">🏠 KW28: Estrichleger</div>
    <div class="milestone-item">⏸ KW29-31: Estrich-Trocknung</div>
    <div class="milestone-item">🔌 KW34: Elektrik + Boden</div>
    <div class="milestone-item">🏡 KW44: Lehmputz fertig</div>
    <div class="milestone-item">🔧 KW46: Decke + Türen</div>
    <div class="milestone-item">🏗️ Mai 2027: WDVS fertig</div>
  </div>
</div>

<div class="note">
  Basis: 32h/Woche · Parallelarbeit möglich · Lehmputz-Trocknung überbrückt Wartezeit<br>
  Realistisch: ~19 Wochen für Phase 3 → Fertig Mai 2027
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
