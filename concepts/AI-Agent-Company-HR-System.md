---
title: AI Agent Company / Agent HR System
description: Konzept eines virtuellen Unternehmens aus spezialisierten KI-Agents mit zentralem HR Manager
tags:
  - ai-agents
  - orchestration
  - hr-manager
  - agent-lifecycle
  - mattermost
  - qwen
created: 2026-08-04
---

# AI Agent Company / Agent HR System

## 1. Ziel

Wir bauen ein System, in dem ein zentraler HR Manager Agent andere KI-Agents konzipiert, erstellt, testet, überwacht und kontinuierlich verbessert.

Der Benutzer gibt dem HR Manager Anforderungen wie:
> „Erstelle einen Agenten, der technische Dokumentationen analysiert und daraus verständliche Kundenanleitungen erstellt."

Der HR Manager übersetzt diese Anforderungen in konkrete Agent-Spezifikationen und koordiniert anschließend weitere Agents.

**Endziel:** Das System soll sich langfristig wie ein virtuelles Unternehmen aus KI-Agents verhalten.

---

## 2. Grundprinzip

Es gibt einen zentralen HR Manager Agent. Dieser ist nicht für jede Aufgabe selbst zuständig, sondern koordiniert spezialisierte Agents.

```
USER
  │
  ▼
HR MANAGER
  │
  ├──► ARCHITECT AGENT
  ├──► RESEARCH AGENT
  ├──► BUILDER AGENT
  ├──► TESTER AGENT
  ├──► EVALUATOR AGENT
  └──► IMPROVEMENT AGENT
```

Der HR Manager entscheidet anhand der Anforderungen, welche Agents benötigt werden.

---

## 3. Agent Lifecycle

Jeder neu erstellte Agent durchläuft einen kontrollierten Lifecycle:

```
Requirement → Specification → Architecture → Build → Testing → Evaluation → Approval → Deployment → Monitoring → Review → Improvement → Testing → New Version
```

**Regel:** Ein Agent darf sich nicht unkontrolliert selbst verändern. Verbesserungen müssen zuerst als neue Version erstellt, getestet und evaluiert werden. Nur wenn die neue Version besser ist, darf sie übernommen werden.

---

## 4. Kommunikation zwischen Agents

Agents kommunizieren über strukturierte Nachrichten — nicht unstrukturiert.

```json
{
  "message_id": "msg_123",
  "task_id": "task_456",
  "type": "task",
  "from": "hr_manager",
  "to": "architect_agent",
  "payload": {
    "goal": "Create customer support agent"
  }
}
```

**Message Types:** `task`, `result`, `event`, `error`, `review`, `evaluation`, `improvement`, `approval`

Agents werden über **Capabilities** angesprochen — nicht über konkrete Agent-IDs. Der Orchestrator findet automatisch den passenden Agenten.

---

## 5. Agent Registry

Alle Agents werden in einer zentralen Registry verwaltet:

| Feld | Beschreibung |
|------|-------------|
| `agent_id` | Eindeutige ID (z.B. `architect_01`) |
| `name` | Anzeigename |
| `version` | Aktuelle Version |
| `status` | `active`, `inactive`, `deprecated` |
| `capabilities` | Liste der Fähigkeiten |
| `model` | Verwendetes KI-Modell |
| `tools` | Verfügbare Tools |
| `permissions` | Berechtigungen |
| `quality` | Qualitäts-Score |
| `last_evaluation` | Zeitstempel letzte Evaluation |

---

## 6. Agent Workspace / Mattermost

Das System soll für den Benutzer **transparent** sein. Mattermost dient als virtuelles Büro der Agents.

**Channels:**
```
🏢 AGENT HQ
#general
#hr-manager
#agent-factory
#evaluations
#improvements
#mission-001
#mission-002
...
```

**Agents als Benutzer:**
```
👤 User
🤖 HR Manager
🤖 Architect
🤖 Researcher
🤖 Builder
🤖 Tester
🤖 Critic
🤖 Evaluator
```

**Beispiel-Protokoll:**
```
🤖 HR Manager
Ich analysiere die neue Anforderung.

🤖 Architect
Architecture erstellt.

🤖 Research Agent
Ich habe verfügbare Komponenten geprüft.

🤖 Builder
Version 0.1 wurde erstellt.

🤖 Tester
12/15 Tests bestanden.

🤖 Critic
3 Probleme gefunden.

🤖 Builder
Probleme behoben.

🤖 Tester
15/15 Tests bestanden.

🤖 Evaluator
Score: 94%.

🤖 HR Manager
Version 1.0 ist bereit.
```

> **Hinweis:** Mattermost ist primär die sichtbare Kommunikations- und Beobachtungsebene.

---

## 7. Technische Kommunikation

### V1 (einfach)
```
Qwen Agents
      ↓
Python Orchestrator
      ↓
SQLite/PostgreSQL
      ↓
Mattermost
```

### V2 (skalierbar)
```
Qwen Agents
      ↓
NATS / JetStream
      ↓
Orchestrator
      ↓
PostgreSQL
      ↓
Mattermost
```

**Prinzip:** Nicht unnötig früh komplexe Infrastruktur einführen. NATS/JetStream erst, wenn es tatsächlich benötigt wird.

---

## 8. Mission-Konzept

Anstatt eines vollständigen Projektmanagementsystems arbeitet das System mit **Missions**.

```markdown
MISSION #42

Goal:
Erstelle einen Agenten für technische Dokumentenanalyse.

Status: RUNNING

Agents:
- HR Manager
- Architect
- Researcher
- Builder
- Tester
- Evaluator

Messages: ...

Artifacts: ...

Result: ...
```

**Enthalten:**
- Goal
- Status
- Beteiligte Agents
- Tasks
- Messages
- Artifacts
- Tests
- Evaluations
- Finale Entscheidung

---

## 9. Beispiel-Ablauf

```
USER: "Erstelle einen Agenten für technische Dokumentenanalyse."
  │
  ▼
HR MANAGER
  │
  ▼
Mission erstellen
  │
  ▼
ARCHITECT → RESEARCH → BUILDER → TESTER → CRITIC → IMPROVEMENT → EVALUATOR
  │
  ▼
HR MANAGER
  │
  ▼
Version freigeben
```

Die gesamte Kommunikation wird in Mattermost protokolliert.

---

## 10. Automatische Verbesserung

**Weekly Agent Review:**

```
Weekly Agent Review
      ↓
Performance analysieren
      ↓
Fehler analysieren
      ↓
Evaluation durchführen
      ↓
Verbesserung identifizieren
      ↓
Neue Version erstellen
      ↓
Tests
      ↓
Evaluation
      ↓
Vergleich mit alter Version
      │
      ├── Wenn besser → Approval / Deployment
      └── Wenn schlechter → Reject
```

**Zu berücksichtigende Faktoren:**
- Qualität
- Genauigkeit
- Robustheit
- Fehlerquote
- Geschwindigkeit
- Kosten
- Tool-Nutzung
- Sicherheitsregeln

---

## 11. Open-Source-Stack

| Komponente | Verwendung |
|------------|------------|
| **Qwen Code** | Entwicklung |
| **Qwen-Agent** | Agent Runtime / Agent-Funktionen |
| **Python** | Orchestrator und Backend |
| **Mattermost** | Sichtbare Agent-Kommunikation |
| **PostgreSQL** | Registry, Tasks, Messages, Evaluations |
| **NATS / JetStream** | Optional für skalierbare Kommunikation |
| **Docker** | Deployment und Isolation |
| **Git** | Agent-Versionierung |

> Temporal oder ähnliche Workflow-Technologien erst einführen, wenn tatsächlich benötigt.

---

## 12. Grundprinzipien

- Agents sind modular
- Agents kommunizieren über strukturierte Messages
- Agents werden über Capabilities gefunden
- Jeder Agent besitzt eine Version
- Jede Änderung ist nachvollziehbar
- Neue Agent-Versionen müssen evaluiert werden
- Agents dürfen sich nicht unkontrolliert selbst deployen
- Der Benutzer kann die Agent-Kommunikation beobachten
- Missions enthalten den vollständigen Kontext einer Aufgabe
- Die Architektur soll zunächst einfach bleiben und später skalieren können
- Open-Source und Self-Hosting haben Priorität
- Der HR Manager ist der zentrale Koordinator und nicht zwingend der ausführende Agent

---

## HR Manager — Verantwortlichkeiten

Der HR Manager entscheidet:

1. Welche Agents benötigt werden
2. Welche Agents bereits existieren
3. Welche Agents neu erstellt werden müssen
4. Welche Aufgaben an welche Agents delegiert werden
5. Wie die Agents miteinander kommunizieren
6. Wie die Ergebnisse evaluiert werden
7. Wann ein Agent verbessert werden sollte
8. Wann eine neue Version freigegeben werden kann

**Der Benutzer** kann währenddessen über Mattermost beobachten, was seine Agents gerade machen, miteinander besprechen und entscheiden.
