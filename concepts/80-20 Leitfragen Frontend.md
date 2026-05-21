---
id: 80-20-leitfragen-frontend
pageType: concept
title: 80/20 Leitfragen für Software (Frontend)
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

# 80/20 Leitfragen für Software (Frontend)

---

## 🔴 Die kritischen Fragen (bevor du startest)

**1. "Was passiert wenn ich das NICHT mache?"**
- → Frontend bootet nicht / Seite funktioniert nicht? → **20% - volle Kraft**
- → Nur nice-to-have Feature? → **80% - kann warten**

**2. "Was passiert wenn ich es FALSCH mache?"**
- → Daten kaputt / Security Bug? → **Jetzt durchdenken**
- → Nur visuell etwas anders? → **Später änderbar**

**3. "Blockiert dieses Task andere Tasks?"**
- → Braucht API-Endpoint? → **Sofort priorisieren**
- → Unabhängig? → **Kann parallel**

---

## ⚡ Frontend-spezifisch

**4. "Wird das Component öfter gebraucht?"**
- → Ja (Button, Input, Modal)? → **Wiederverwendbar bauen**
- → Nein (einmaliger Banner)? → **Quick & Dirty ok**

**5. "Ändert sich die Anforderung noch?"**
- → Vague Specs / early Stage? → **Erstmal einfach machen**
- → Specs stable? → **Richtig durchdenken**

**6. "Ist das semantisch korrekt HTML?"**
- → Nein? → **Korrigieren,Accessibility leidet**
- → Ja? → ** Gut**

---

## 👥 Delegations-Fragen

**7. "Kann ein Junior/AI das machen?"**
- → Ja (repetitive Components, einfache Pages)? → **Delegieren**
- → Nein (komplexe Logik, Performance)? → **Weiter zu 8**

**8. "Braucht es Architektur-Entscheidung?"**
- → Ja (State Management, Routing, API Design)? → **Selbst oder Senior**
- → Nein (UI Components)? → **Junior ok**

**9. "Wie groß ist der Schaden wenn was kaputt geht?"**
- → Groß (Auth, Payments, Daten)? → **Profi/Senior**
- → Klein (Content, Styling)? → **Delegieren ok**

---

## ⏰ Zeit-Fragen

**10. "Wie viele Tage bis Sprint/Deadline?"**
- → <2 Tage → **Kritisch - nur das Nötigste**
- → >2 Tage → **Etwas Luft**

**11. "Wie lange dauert das wirklich?"** (×1.5 für Bugs + Edge Cases!)

**12. "Was ist der erste Schritt?"** (Nicht "ganz fertig" denken)

---

## 🔙 Reversibilitäts-Fragen

**13. "Kann ich das später refaktoren?"**
- → Ja (innere Logik, Helper Functions)? → **Quick & Dirty ok**
- → Nein (Public API, Component Interface)? → **Jetzt sauber**

**14. "Ist das an einer Stelle die schwer zu testen ist?"**
- → Ja (nested callbacks, State)? → **Jetzt testbar machen**
- → Nein? → **Kann später bleiben**

---

## 🎯 Fokus-Fragen

**15. "Was sind die 20% Components die 80% der Nutzer sehen?"**
- → Navigation, Main Content, CTA? → **Volle Detailstufe**
- → Footer, rarely used Modal? → **Quick ok**

**16. "Was kann ich drop/scope-down ohne dass Nutzer es merken?"**

**17. "Wofür ist die eine Pomodoro die ich gerade habe?"** → **Nur das eine Component**

---

## 📋 Quick-Check pro Task:

```
Task: ________________

❓ Blockiert was? ____________
❓ Wiederverwendbar? Ja / Nein
❓ Risiko wenn kaputt? Hoch / Mittel / Niedrig
❓ Specs stable? Ja / Nein
❓ First Step? ____________

→ Jetzt machen? Ja / Nein / Delegieren
```

---

## 🚀 Die 20% die bei Frontend wirklich zählen

1. **State Management** – wenn das Chaos ist, wird alles Chaos
2. **Error Handling** – was passiert wenn API down ist
3. **Loading States** – niemand mag blanke Seiten
4. **Input Validation** – Security + UX
5. **Accessibility** – damit es wirklich nutzbar ist

## Die 80% die weniger zählen (aber trotzdem wichtig)

- Perfekte Pixel-Positionierung
- CSS Shortcuts die 2 Zeichen kürzer sind
- File Structure Variationen
- Comments die erklären was der Code schon sagt
- Fancy Animations die keiner bemerkt

---

**Die meisten Frontend-Fails kommen davon:** Man baute Features die keiner brauchte, während die kritischen 20% halbfertig waren.

**Refaktorieren ist kein Versagen – es ist Lernen.** 🦞</code>

## Related
<!-- openclaw:wiki:related:start -->
- No related pages yet.
<!-- openclaw:wiki:related:end -->
