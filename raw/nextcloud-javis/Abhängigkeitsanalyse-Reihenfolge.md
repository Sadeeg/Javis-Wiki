# 📊 Abhängigkeitsanalyse & Reihenfolge - Projekt Haus

**Erstellt:** 24. Februar 2026, 01:05 Uhr
**Analyst:** Kimi 2.5 (OpenClaw)
**Quelle:** Deck Board "Arbeitsplanung" - Stack "Refinement" (62 Aufgaben)
**Aktualisiert:** 24.02.2026 - Korrektur Elektrik-Abhängigkeiten

---

## 🎯 Exekutive Zusammenfassung

### Kritische Erkenntnis

Das Projekt hat **drei kritische Pfad-Abhängigkeiten**, die den gesamten Zeitplan bestimmen:

1. **🔥 Bad (1.OG)** → Muss als ALLERLETZTES raus (Anfang Mai)
2. **🌡️ Heizung außer Betrieb** → Blockiert Heizungsnischen in 5 Räumen
3. **⚡ Elektrik-Gesamtabschluss** → Finale Tests nach Verteilerkasten

### Empfohlene Strategie

**Drei-Phasen-Ansatz** mit parallelen Teams:

- **Phase 1 (Woche 1-3):** Vorbereitung + Elektrik EG
- **Phase 2 (Woche 4-7):** Elektrik 1.OG + Lehmputz EG
- **Phase 3 (Woche 8-11):** Finalisierung + Bad-Rauswurf

---

## 🔴 KRITISCHE ABHÄNGIGKEITEN (Blocker)

### 1. VERTEILERKASTEN - Wichtig, aber kein Blocker für Elektrik

**Aufgabe:** 🔥 VERTEILERKASTEN setzen (Treppenhaus)

**Korrektur zur Abhängigkeit:**
Die Elektrik-Arbeiten (Dosen setzen, Leitungen ziehen) sind **NICHT** vom Verteilerkasten abhängig. Die Leitungen können bis zum Kasten gezogen werden und später angeschlossen werden.

**Der Verteilerkasten blockiert:**

- Nur die finale Anschlussarbeit der Leitungen
- Systemtests und Inbetriebnahme

**Der Verteilerkasten blockiert NICHT:**

- ✅ Dosen setzen in allen Räumen
- ✅ Leitungen ziehen (bis zum Kasten)
- ✅ Schlitze fräsen
- ✅ Rohinstallation

**Empfohlene Reihenfolge:**

1. Elektrik-Arbeiten parallel starten (Dosen, Leitungen)
2. Leitungen bis zum Kasten ziehen (noch nicht anschließen)
3. Verteilerkasten setzen (wenn Dad Zeit hat)
4. Leitungen anschließen und testen

**Zeitkritischer Pfad:**

- **Muss erledigt sein bis:** Vor Inbetriebnahme/Test (Ende der Elektrik-Phase)
- **Konsequenz bei Verzug:** Keine Verzögerung der Elektrik-Arbeiten, nur Verzögerung der finalen Tests
- **Lösung bei Verzug:** Leitungen liegen bereit, Anschluss kann später erfolgen

**Empfohlene Aktion:**

- [ ] Termin mit Dad klären (Karte 55) - aber ohne Zeitdruck für Elektrik-Start
- [ ] Elektrik-Arbeiten können sofort beginnen!

---

### 2. BAD (1.OG) - Der Zeit-Fixpunkt

**Aufgaben:**

- 🔥 Bad: Decke abhängen [46]
- 🔥 Bad: Fußboden raus [47]
- 🔥 Bad: Estrich rausklopfen [48]

**Fixierter Zeitpunkt:** Anfang Mai (2 Wochen vor Estrichleger, 15.5.)

**Abhängigkeiten VOR dem Bad-Rauswurf:**

- EG/1.OG: ALLE Elektrik muss fertig sein
- EG/1.OG: ALLE Trockenbauwände müssen fertig sein
- EG/1.OG: ALLE Unterboden-Mörtelreste müssen entfernt sein
- EG/1.OG: Lehmputz sollte fertig sein (außer evtl. Nachbesserungen)

**Risiken:**

- ❓ Toiletten-Lösung noch unklar [49]
- Risiko: Badewanne/Dusche müssen evtl. abgebaut werden
- Alternative Dusche muss organisiert werden

**Empfohlene Aktion:**

- [ ] Toiletten-Lösung KLÄREN (mobile Toilette? Nachbarn?)
- [ ] Alternative Duschmöglichkeit organisieren
- [ ] Material für schnellen Bad-Ausbau bereitstellen

---

### 3. HEIZUNG AUßER BETRIEB - Der Winter-Blocker

**Aufgabe:** 🌡️ Heizung außer Betrieb nehmen [103]

**Blockiert (kann erst danach gemacht werden):**

- EG Wohnzimmer: Heizungsnischen [73]
- EG Küche: Heizungsnische [76]
- EG Wintergarten: Estrich entfernen [77], Heizung abbauen [78]
- 1.OG Schlafzimmer: Heizungsnischen [nicht explizit gelistet, aber impliziert]
- 1.OG Kinderzimmer: Heizungsnischen [89]

**Zeitfenster:** Nach Winter/Winterum

**Empfohlene Aktion:**

- [ ] Termin mit Heizungsbauer klären
- [ ] Parallel: Alle anderen Arbeiten (Elektrik, Trockenbau) vorziehen

---

## 📋 ABHÄNGIGKEITSGRAPHEN

### Elektrik-Abhängigkeiten

```
VORHER: Tiefengrund (wo nötig)
    ↓
EG Elektrik (alle Räume parallel möglich) - KANN SOFORT STARTEN!
    ↓
1.OG Elektrik (alle Räume parallel möglich)
    ↓
DG Leitungen
    ↓
VERTEILERKASTEN setzen (zwischendurch möglich)
    ↓
Leitungen anschließen
    ↓
DANACH: Schlitze verputzen
    ↓
DANACH: Lehmputz
```

### Trockenbau-Abhängigkeiten

```
EG WC: Elektrik → Trennwand → Duschwand → Klo-Verkleidung
    ↓
EG Treppenhaus: Elektrik → Rigips → Holz-Geländer → Kellerabgang
    ↓
EG Essbereich: Elektrik → Trockenbauwand Heizkreisverteiler
    ↓
1.OG Flur: Elektrik → Trockenbauwand Treppe → Heizkreisverteiler
```

### Lehmputz-Abhängigkeiten

```
VORHER: Elektrik komplett
    ↓
VORHER: Schlitze verputzt
    ↓
VORHER: Wände abgeschliffen + Tiefengrund
    ↓
LEHMPUTZ (alle Räume parallel möglich)
    ↓
DANACH: Heizungsnischen (wenn Heizung aus)
```

---

## ⚡ EMPFOHLENE REIHENFOLGE

### WOCHE 1 (24.02. - 02.03.) - 30h

**Thema: Vorbereitung & Elektrik-Start**

| Priorität | Aufgabe                                                | Team             | Warum zuerst?                     |
|-----------|--------------------------------------------------------|------------------|-----------------------------------|
| 🔴 1      | ⚡ EG Elektrik starten (Dosen setzen, Leitungen ziehen) | Sascha/Alexander | KANN SOFORT BEGINNEN!             |
| 🟡 2      | 🚀 07.03. SPRINT organisieren                          | Sascha           | Muss geplant werden               |
| 🟡 3      | 🛒 Material Wasserleitung kaufen                       | Sascha           | Für Küche nötig                   |
| 🟢 4      | 🧹 Wände Putzreste entfernen (alle Räume)              | Team B           | Einfach, parallel                 |
| 🟢 5      | 🧹 Tiefengrund (wo nötig)                              | Team B           | Vorbereitung Elektrik             |
| 🟢 6      | 🧹 Unterboden Mörtelreste (EG)                         | Team B           | Einfach, zeitintensiv             |
| 🟡 7      | 📞 Termin mit Dad klären (Verteilerkasten)             | Sascha           | Nicht dringend für Elektrik-Start |

**Zielwoche:** Elektrik läuft, Sprint geplant, Vorbereitung parallel

---

### WOCHE 2 (03.03. - 09.03.) - 30h + 42h Sprint

**Thema: SPRINT-WOCHE & Elektrik vorantreiben**

#### Vorbereitung (Mo-Mi): 30h

| Priorität | Aufgabe                                          | Team         |
|-----------|--------------------------------------------------|--------------|
| 🔴 1      | ⚡ EG Elektrik fortsetzen (alle Räume)            | Sascha/Team  |
| 🔴 2      | 🔥 VERTEILERKASTEN setzen (wenn Dad Zeit hat)    | Dad + Sascha |
| 🟡 3      | 🚪 EG Windfang: Estrich-Rest entfernen           | Team B       |
| 🟡 4      | 🪜 EG Treppenhaus: Alte Installationen entfernen | Team B       |

#### 🚀 SPRINT-SAMSTAG (07.03.): 42h mit 6 Personen

| Team                       | Aufgaben                                                                   | Stunden |
|----------------------------|----------------------------------------------------------------------------|---------|
| **Team 1 (2 Pers., erfahren)** | EG Elektrik durchziehen (WC, Windfang, Treppenhaus) + Leitungen bis Kasten | 14h     |
| **Team 2 (2 Pers., gemischt)** | Wohnzimmer/Essbereich Unterboden + Tiefengrund                             | 14h     |
| **Team 3 (2 Pers., Helfer)**   | Transport + Küche Vorbereitung                                             | 14h     |

**Zielwoche:** EG Elektrik 70% fertig (Rohinstallation), Verteilerkasten steht

---

### WOCHE 3 (10.03. - 16.03.) - 30h

**Thema: EG Elektrik fertig + 1.OG starten**

| Priorität | Aufgabe                                              | Abhängigkeit     |
|-----------|------------------------------------------------------|------------------|
| 🔴 1      | ⚡ EG Wohnzimmer: Elektrik + Rollladen                | \-                |
| 🔴 2      | 🍳 EG Küche: Elektrik + Wasserleitung                | \-                |
| 🔴 3      | 🍽️ EG Essbereich: Elektrik                          | \-                |
| 🔴 4      | ⚡ 1.OG Elektrik starten                              | \-                |
| 🟡 5      | 🛠️ EG Essbereich: Trockenbauwand Heizkreisverteiler | Elektrik         |
| 🟢 6      | 🧹 Unterboden Mörtelreste (1.OG)                     | Parallel möglich |

**Zielwoche:** EG Elektrik 100% Rohinstallation fertig

---

### WOCHE 4 (17.03. - 23.03.) - 30h

**Thema: 1.OG Elektrik**

| Priorität | Aufgabe                                     | Abhängigkeit |
|-----------|---------------------------------------------|--------------|
| 🔴 1      | 🪜 1.OG Flur: Elektrik + Trockenbauwand     | \-            |
| 🔴 2      | 🔥 1.OG Kaminzimmer: Tiefengrund + Elektrik | \-            |
| 🔴 3      | 🧸 1.OG Kinderzimmer: Elektrik              | \-            |
| 🟡 4      | 🛠️ 1.OG Flur: Verschalung Treppenhaus      | Parallel     |

**Zielwoche:** 1.OG Elektrik 60% fertig

---

### WOCHE 5 (24.03. - 30.03.) - 30h

**Thema: 1.OG Elektrik fertig + Lehmputz-Start**

| Priorität | Aufgabe                                                                | Abhängigkeit     |
|-----------|------------------------------------------------------------------------|------------------|
| 🔴 1      | 🛏️ 1.OG Schlafzimmer: Elektrik + Rollladen-Entscheidung!              | \-                |
| 🔴 2      | 🛁 1.OG Bad: Strom-Zuleitungen (außer Decke!)                          | \-                |
| 🔴 3      | 🔥 VERTEILERKASTEN: Leitungen anschließen (falls noch nicht geschehen) | Elektrik EG/1.OG |
| 🟡 4      | 🟤 EG Kaminzimmer: Lehmputz                                            | Elektrik fertig  |
| 🟡 5      | 🧱 EG WC: Schlitze verputzen                                           | Elektrik fertig  |

**Zielwoche:** 1.OG Elektrik 90% fertig, erste Lehmputz-Räume, Verteilerkasten angeschlossen

---

### WOCHE 6-7 (31.03. - 13.04.) - 60h

**Thema: Lehmputz-Phase**

| Woche | Aufgaben                                      | Anmerkung             |
|-------|-----------------------------------------------|-----------------------|
| **6**     | 🟤 EG: Wohnzimmer, Essbereich, Küche Lehmputz | Nach Elektrik         |
| **7**     | 🟤 1.OG: Schlafzimmer, Kinderzimmer Lehmputz  | Nach Elektrik         |
| **Beide** | 🌡️ Heizung außer Betrieb (wenn Winter um)    | Dann: Heizungsnischen |

**Zielwoche:** Lehmputz 80% fertig

---

### WOCHE 8-9 (14.04. - 27.04.) - 60h

**Thema: Finalisierung**

| Woche | Aufgaben                                                          |
|-------|-------------------------------------------------------------------|
| **8**     | 🛁 Bad: Vorbereitung (außer Decke), 🌿 Wintergarten: Vorbereitung |
| **9**     | 📋 Estrichleger-Besprechung, Qualitätskontrolle alle Räume        |

**Zielwoche:** 95% fertig außer Bad

---

### WOCHE 10-11 (28.04. - 11.05.) - 60h

**Thema: 🔥🔥🔥 ENDSPURT**

| Woche | Aufgaben                                                             | Kritisch? |
|-------|----------------------------------------------------------------------|-----------|
| **10**    | 🔥 Bad: Decke, Fußboden, Estrich raus; 🌿 Wintergarten: Estrich raus | 🔥🔥🔥    |
| **11**    | Letzte Nachbesserungen, 🎯 ESTRICHLEGER (15.5.)                      | 🎯        |

**Zielwoche:** ALLES fertig!

---

## 🔄 PARALLELISIERUNGSMÖGLICHKEITEN

### Teams Aufteilung (immer möglich)

| Team A (Erfahren)  | Team B (Helfer)      |
|--------------------|----------------------|
| Elektrik           | Putzreste entfernen  |
| Wasserleitungen    | Tiefengrund          |
| Rollladen          | Unterboden säubern   |
| Trockenbau-Planung | Transport/Entsorgung |

### Räume parallel bearbeiten (gleiche Phase)

- **Elektrik EG:** Alle 6 Räume parallel möglich (KEINE Abhängigkeit vom Verteilerkasten!)
- **Elektrik 1.OG:** Alle 5 Räume parallel möglich
- **Lehmputz:** Alle Räume parallel möglich (nach Elektrik)
- **Unterboden:** Alle Räume parallel möglich

---

## ⚠️ RISIKOANALYSE

### Hohes Risiko (>30% Wahrscheinlichkeit)

| Risiko                        | Auswirkung                    | Mitigation                          |
|-------------------------------|-------------------------------|-------------------------------------|
| Bad dauert länger als geplant | Estrichleger-Termin gefährdet | Puffer in Woche 11                  |
| Material nicht verfügbar      | Wartezeiten                   | Früh bestellen, Lieferzeiten prüfen |

### Mittleres Risiko (10-30%)

| Risiko                           | Auswirkung                         | Mitigation                   |
|----------------------------------|------------------------------------|------------------------------|
| 07.03. Wetter schlecht           | Sprint beeinträchtigt              | Indoor-Aufgaben priorisieren |
| Rollladen-Entscheidung verzögert | Elektrik im Schlafzimmer blockiert | Entscheidung vorab treffen   |
| Toiletten-Lösung unklar          | Chaos im Mai                       | Mobile Toilette vorbestellen |

### Niedriges Risiko (<10%) - KORRIGIERT!

| Risiko                    | Auswirkung                  | Mitigation                                                                                         |
|---------------------------|-----------------------------|----------------------------------------------------------------------------------------------------|
| Dad kommt nicht pünktlich | ~~Gesamter Zeitplan verzögert~~ | Kein Problem mehr! Elektrik kann ohne ihn starten. Verteilerkasten-Anschluss kann später erfolgen. |

---

## 📝 DETAILLIERTE ABHÄNGIGKEITSLISTE

### Muss VOR Elektrik erledigt sein:

1. ✅ Tiefengrund (wo noch nicht geschehen)
2. ✅ Wände Putzreste entfernen

### Muss VOR Trockenbau erledigt sein:

1. ✅ Elektrik in der jeweiligen Wand
2. ✅ Leitungsführung geplant

### Muss VOR Lehmputz erledigt sein:

1. ✅ Elektrik komplett (Rohinstallation)
2. ✅ Schlitze verputzt
3. ✅ Wände abgeschliffen
4. ✅ Tiefengrund

### Muss VOR Fußbodenheizung (15.5.) erledigt sein:

1. ✅ ALLE Elektrik (inkl. Verteilerkasten-Anschluss)
2. ✅ ALLE Trockenbauwände
3. ✅ ALLE Unterboden-Mörtelreste entfernt
4. ✅ ALLE Heizungsnischen (wenn Heizung aus)
5. 🔥 BAD komplett raus (als letztes)

---

## 🎯 HANDLUNGSEMPFEHLUNGEN

### SOFORT (heute/diese Woche)

1. 🚀 **Elektrik SOFORT starten!** - Keine Wartezeit auf Verteilerkasten nötig
2. 🚀 **07.03. Sprint planen** - Helfer einladen, Material-Liste erstellen
3. ❓ **Toiletten-Lösung klären** - Entscheidung treffen
4. ❓ **Rollladen-Entscheidung** - 1 oder 2 Motoren?
5. 📞 Termin mit Dad klären - Aber ohne Druck, Elektrik läuft parallel

### BIS ENDE WOCHE 1

1. ✅ Elektrik-Arbeiten laufen bereits
2. ✅ Material Wasserleitung kaufen
3. ✅ Vorbereitungsarbeiten (Putzreste, Tiefengrund) parallel

### BIS 07.03.

1. 🔥 **EG Elektrik 70% fertig** (Rohinstallation)
2. 🔥 **VERTEILERKASTEN setzen** (wenn Dad Zeit hat)

### BIS ANFANG MAI

1. ✅ EG + 1.OG komplett fertig (außer Bad)
2. ✅ Lehmputz überall fertig
3. 🔥 **BAD als letztes rausnehmen**

---

## 📊 STATISTIK

| Kategorie            | Anzahl | %    |
|----------------------|--------|------|
| **Gesamt Aufgaben**      | 62     | 100% |
| 🔴 Komplex           | 25     | 40%  |
| 🟡 Mittel            | 24     | 39%  |
| 🟢 Einfach           | 13     | 21%  |
| 🔥 Kritische Blocker | 2      | 3%   |
| **EG Aufgaben**          | 29     | 47%  |
| **1.OG Aufgaben**        | 22     | 35%  |
| **DG Aufgaben**          | 1      | 2%   |
| **Global**               | 10     | 16%  |

---

## 📝 ÄNDERUNGSHISTORIE

| Datum      | Änderung                                                 | Grund                                                           |
|------------|----------------------------------------------------------|-----------------------------------------------------------------|
| 24.02.2026 | **Korrektur:** Verteilerkasten ist kein Blocker für Elektrik | Richtigstellung: Leitungen können bis zum Kasten gezogen werden |

---

**Dokument erstellt von:** Kimi 2.5 via OpenClaw  
**Nächster Review:** Nach Woche 2 (09.03.2026)  
**Letzte Aktualisierung:** 24.02.2026, 12:30 Uhr