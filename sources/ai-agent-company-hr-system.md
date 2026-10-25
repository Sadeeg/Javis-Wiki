---
id: source.ai-agent-company-hr-system
pageType: source
title: "Konzept: AI Agent Company / Agent HR System"
sourceType: conversation
sourcePath: /home/sascha/.openclaw/agents/main/sessions/29725e2a-a2ad-484d-a934-03bc0b2927cb.trajectory.jsonl
ingestedAt: 2026-10-25T12:00:00.000Z
updatedAt: 2026-10-25T12:00:00.000Z
status: active
---

# Konzept: AI Agent Company / Agent HR System

## Herkunft

| | |
|---|---|
| **Kanal** | Telegram (Direktchat mit Sascha Deeg) |
| **Nachricht vom** | Tue 2026-08-04 09:25:07 UTC |
| **Telegram message_id** | 6419 |
| **Session** | `29725e2a-a2ad-484d-a934-03bc0b2927cb` |
| **Auftrag** | „Kannst du folgendes Konzept anschauen und es in meinem Wiki ablegen" |

**Wichtige Ehrlichkeits-Anmerkung:** Der übermittelte Text beginnt mit der
Antwort-Formulierung „Klar — hier ist eine kompakte, aber ausreichend technische
Konzeptbeschreibung…". Sascha hat die Beschreibung also **aus einem früheren
Chat kopiert** (vermutlich aus einer anderen KI-Unterhaltung) und selbst
eingereicht. Der Urheber der *Formulierung* ist damit nicht sicher
Sascha selbst; belegt ist nur: **Sascha hat dieses Konzept am 04.08.2026
als eigenes im Wiki abgelegt.**

## Inhalt (Originaltext der Nachricht)

```text
- Klar — hier ist eine kompakte, aber ausreichend technische Konzeptbeschreibung, die du direkt einem KI-Agenten geben kannst, damit dieser das System versteht und weiterentwickeln kann.
Konzept: AI Agent Company / Agent HR System
1. Ziel
Wir bauen ein System, in dem ein zentraler HR Manager Agent andere KI-Agents konzipiert, erstellt, testet, überwacht und kontinuierlich verbessert.
Der Benutzer gibt dem HR Manager Anforderungen wie:
„Erstelle einen Agenten, der technische Dokumentationen analysiert und daraus verständliche Kundenanleitungen erstellt.“
Der HR Manager übersetzt diese Anforderungen in konkrete Agent-Spezifikationen und koordiniert anschließend weitere Agents.
Das System soll sich langfristig wie ein virtuelles Unternehmen aus KI-Agents verhalten.


⸻


2. Grundprinzip
Es gibt einen zentralen HR Manager Agent.
Dieser ist nicht für jede Aufgabe selbst zuständig, sondern koordiniert spezialisierte Agents.
Beispiel:
USER
 │
 ▼
HR MANAGER
 │
 ├──► ARCHITECT AGENT
 │
 ├──► RESEARCH AGENT
 │
 ├──► BUILDER AGENT
 │
 ├──► TESTER AGENT
 │
 ├──► EVALUATOR AGENT
 │
 └──► IMPROVEMENT AGENT
Der HR Manager entscheidet anhand der Anforderungen, welche Agents benötigt werden.


⸻


3. Agent Lifecycle
Jeder neu erstellte Agent durchläuft einen kontrollierten Lifecycle:
Requirement
 ↓
Specification
 ↓
Architecture
 ↓
Build
 ↓
Testing
 ↓
Evaluation
 ↓
Approval
 ↓
Deployment
 ↓
Monitoring
 ↓
Review
 ↓
Improvement
 ↓
Testing
 ↓
New Version
Ein Agent darf sich nicht unkontrolliert selbst verändern.
Verbesserungen müssen zuerst als neue Version erstellt, getestet und evaluiert werden.
Nur wenn die neue Version besser ist, darf sie übernommen werden.


⸻


4. Kommunikation zwischen Agents
Agents sollen nicht einfach unstrukturiert miteinander chatten.
Die Kommunikation erfolgt über strukturierte Nachrichten.
Beispiel:
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
Mögliche Message Types:
task
result
event
error
review
evaluation
improvement
approval
Agents sollen über Capabilities angesprochen werden können.
Beispiel:
capability = agent_architecture
Der Orchestrator sucht automatisch einen passenden Agenten.
Dadurch muss ein Agent nicht wissen, welcher konkrete Agent eine Fähigkeit besitzt.


⸻


5. Agent Registry
Alle Agents werden in einer zentralen Registry verwaltet.
Beispiel:
agent_id: architect_01

name: Agent Architect
version: 1.3.0

status: active

capabilities:
 - agent_architecture
 - workflow_design
 - tool_selection

quality:
 score: 0.94
Die Registry soll Informationen über folgende Punkte enthalten:
Agent ID
Name
Version
Status
Fähigkeiten
verwendetes Modell
verfügbare Tools
Berechtigungen
Performance
Qualität
letzte Evaluation
aktuelle Tasks


⸻


6. Agent Workspace / Kommunikation sichtbar machen
Das System soll für den Benutzer transparent sein.
Es soll ein bestehendes Open-Source-Kommunikationstool verwendet werden, statt eine komplette eigene Projektmanagement-Software zu entwickeln.
Als bevorzugte Oberfläche ist Mattermost vorgesehen.
Mattermost dient als virtuelles Büro der Agents.
Beispiel:
🏢 AGENT HQ

#general
#hr-manager
#agent-factory
#evaluations
#improvements

#mission-001
#mission-002
#mission-003
Agents werden als eigene Benutzer dargestellt:
👤 User

🤖 HR Manager
🤖 Architect
🤖 Researcher
🤖 Builder
🤖 Tester
🤖 Critic
🤖 Evaluator
Der Benutzer kann die Kommunikation und den Fortschritt der Agents beobachten.
Beispiel:
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
Version 1.0 ist bereit.Mattermost ist dabei primär die sichtbare Kommunikations- und Beobachtungsebene.


⸻


7. Technische Kommunikation
Für die interne Kommunikation zwischen Agents soll zunächst eine möglichst einfache Architektur verwendet werden.
Empfohlene Entwicklung:
V1
Qwen Agents
 ↓
Python Orchestrator
 ↓
SQLite/PostgreSQL
 ↓
Mattermost
Wenn das System wächst:
Qwen Agents
 ↓
NATS / JetStream
 ↓
Orchestrator
 ↓
PostgreSQL
 ↓
Mattermost
NATS/JetStream kann später als Message Bus für Tasks, Events und persistente Kommunikation verwendet werden.
Es soll nicht unnötig früh komplexe Infrastruktur eingeführt werden.


⸻


8. Mission-Konzept
Anstatt ein komplettes Projektmanagementsystem zu verwenden, arbeitet das System mit Missions.
Eine Mission ist eine übergeordnete Aufgabe.
Beispiel:
MISSION #42

Goal:
Erstelle einen Agenten für technische Dokumentenanalyse.

Status:
RUNNING

Agents:
- HR Manager
- Architect
- Researcher
- Builder
- Tester
- Evaluator

Messages:
...

Artifacts:
...

Result:
...
Eine Mission enthält:
Goal
Status
beteiligte Agents
Tasks
Messages
Artifacts
Tests
Evaluations
finale Entscheidung


⸻


9. Beispiel eines kompletten Ablaufs
Der Benutzer schreibt:
Erstelle einen Agenten für technische Dokumentenanalyse.
Der Ablauf:
USER
 ↓
HR MANAGER
 ↓
Mission erstellen
 ↓
ARCHITECT
 ↓
RESEARCH
 ↓
BUILDER
 ↓
TESTER
 ↓
CRITIC
 ↓
IMPROVEMENT
 ↓
EVALUATOR
 ↓
HR MANAGER
 ↓
Version freigeben
Die gesamte Kommunikation wird für den Benutzer sichtbar in Mattermost protokolliert.


⸻


10. Automatische Verbesserung
Der HR Manager soll Agents regelmäßig überprüfen.
Beispiel:
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
 ↓
Wenn besser → Approval / Deployment
Wenn schlechter → Reject
Dabei müssen mindestens folgende Faktoren berücksichtigt werden:
Qualität
Genauigkeit
Robustheit
Fehlerquote
Geschwindigkeit
Kosten
Tool-Nutzung
Sicherheitsregeln


⸻


11. Open-Source-Stack
Der Stack soll möglichst Open Source und selbst hostbar sein.
Vorgesehen:
Qwen Code – Entwicklung
Qwen-Agent – Agent Runtime / Agent-Funktionen
Python – Orchestrator und Backend
Mattermost – sichtbare Agent-Kommunikation
PostgreSQL – Registry, Tasks, Messages, Evaluations und Metadaten
NATS / JetStream – optional für skalierbare Agent-Kommunikation
Docker – Deployment und Isolation
Git – Agent-Versionierung
Komplexere Workflow-Technologien wie Temporal sollen erst eingeführt werden, wenn sie tatsächlich benötigt werden.


⸻


12. Grundprinzipien
Das System soll folgende Prinzipien einhalten:
Agents sind modular.
Agents kommunizieren über strukturierte Messages.
Agents werden über Capabilities gefunden.
Jeder Agent besitzt eine Version.
Jede Änderung ist nachvollziehbar.
Neue Agent-Versionen müssen evaluiert werden.
Agents dürfen sich nicht unkontrolliert selbst deployen.
Der Benutzer kann die Agent-Kommunikation beobachten.
Missions enthalten den vollständigen Kontext einer Aufgabe.
Die Architektur soll zunächst einfach bleiben und später skalieren können.
Open-Source und Self-Hosting haben Priorität.
Der HR Manager ist der zentrale Koordinator und nicht zwingend der ausführende Agent.
Endziel
Das System soll sich langfristig wie ein virtuelles Unternehmen aus spezialisierten KI-Agents verhalten.
Der Benutzer gibt nur ein Ziel vor.
Der HR Manager entscheidet:
Welche Agents benötigt werden
Welche Agents bereits existieren
Welche Agents neu erstellt werden müssen
Welche Aufgaben an welche Agents delegiert werden
Wie die Agents miteinander kommunizieren
Wie die Ergebnisse evaluiert werden
Wann ein Agent verbessert werden sollte
Wann eine neue Version freigegeben werden kann
Der Benutzer kann währenddessen über Mattermost beobachten, was seine Agents gerade machen, miteinander besprechen und entscheiden.Wenn du möchtest, kann ich daraus als nächsten Schritt auch einen konkreten Master-Prompt für Qwen Code machen, den du direkt als Ausgangspunkt für die Implementierung verwenden kannst.
```

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[concepts/AI-Agent-Company-HR-System|AI Agent Company / Agent HR System]]
<!-- openclaw:wiki:related:end -->
