---
id: 97-things-every-software-architect-should-know-auf-deutsch
pageType: source
title: 7. Steh auf!
createdAt: 2026-05-21T10:10:00.000Z
updatedAt: 2026-05-21T10:10:00.000Z
---

[[97 Things Every Software Architect Should Know - The Book]]
## 1. Stelle deinen Lebenslauf nicht über die Anforderungen

Als Ingenieure empfehlen wir manchmal Technologien, Methoden oder Ansätze zur Problemlösung, weil wir sie gerne in unserem Lebenslauf sehen möchten – und nicht, weil sie wirklich die beste Lösung für das Problem sind. Solche Entscheidungen führen nur selten zu guten Ergebnissen.

Das Beste für deine Karriere ist eine lange Reihe zufriedener Kunden, die dich weiterempfehlen, weil du für sie und für das Projekt die richtigen Entscheidungen getroffen hast. Dieses Vertrauen wird deiner Karriere um Größenordnungen mehr helfen als das neueste „glänzende“ Tool, die neueste Programmiersprache oder das neueste Paradigma.

Es ist wichtig – sogar entscheidend – über neue Trends und Technologien informiert zu bleiben. Aber das darf niemals auf Kosten des Kunden geschehen. Man sollte nicht vergessen, dass man eine treuhänderische Verantwortung hat. Als Architekt wurde dir das Wohl deiner Organisation anvertraut, und es wird erwartet, dass du Interessenkonflikte vermeidest und deiner Organisation loyal dienst.

Wenn ein Projekt nicht modern oder herausfordernd genug für deine Karriereziele ist, dann suche dir ein anderes.  
Wenn du das nicht kannst und in einem solchen Projekt arbeiten musst, dann wird es für alle Beteiligten besser sein, die richtige Technologie für den Kunden zu verwenden – nicht für deinen Lebenslauf.

Es ist oft schwer, einer neuen und coolen Lösung zu widerstehen, selbst wenn sie für die aktuelle Situation ungeeignet ist.

Mit der richtigen Lösung wird das Projekt ein zufriedeneres Team, einen zufriedeneren Kunden und insgesamt deutlich weniger Stress haben. Oft bleibt dann sogar Zeit, sich tiefer mit bestehender Technologie zu beschäftigen oder neue Dinge in der eigenen Zeit zu lernen – oder endlich den Malkurs zu besuchen, den man schon immer machen wollte. Deine Familie wird den Unterschied merken, wenn du nach Hause kommst.

Kurz gesagt: Stelle immer die langfristigen Bedürfnisse des Kunden über deine kurzfristigen persönlichen Interessen – dann liegst du selten falsch.

*Von Nitin Borwankar*

---

## 2. Vereinfache essentielle Komplexität; reduziere zufällige Komplexität

Essentielle Komplexität beschreibt die Schwierigkeit, die in einem Problem selbst liegt.  
Ein Beispiel ist die Koordination des Luftverkehrs eines Landes. Die genaue Position jedes Flugzeugs (inklusive Höhe), Geschwindigkeit, Richtung und Ziel müssen in Echtzeit verfolgt werden, um Zusammenstöße in der Luft oder auf der Landebahn zu vermeiden. Flugpläne müssen so organisiert werden, dass Flughäfen nicht überlastet werden – selbst kleine Wetteränderungen können den gesamten Plan durcheinanderbringen.

Zufällige Komplexität entsteht dagegen durch Lösungen, die wir bauen, um diese essentielle Komplexität zu bewältigen. Das heutige Luftverkehrskontrollsystem ist ein Beispiel dafür. Es wurde entwickelt, um den Flugverkehr von tausenden Flugzeugen zu steuern – hat aber selbst enorme zusätzliche Komplexität erzeugt. Tatsächlich ist es inzwischen so komplex, dass eine Modernisierung extrem schwierig ist. In vielen Teilen der Welt basiert die Flugsteuerung auf Technologien, die über 30 Jahre alt sind.

Viele Frameworks und „Vendor-Lösungen“ sind Symptome dieser zufälligen Komplexität. Frameworks, die konkrete Probleme lösen, sind hilfreich. Überengineerte Frameworks schaffen jedoch oft mehr Komplexität, als sie beseitigen.

Entwickler fühlen sich häufig von komplexen Problemen angezogen. Rätsel zu lösen macht Spaß, und Entwickler sind Problemlöser. Wer liebt nicht das Gefühl, ein extrem schwieriges Problem gelöst zu haben? In großen Softwaresystemen besteht die Herausforderung jedoch darin, zufällige Komplexität zu entfernen, während die Lösung der essentiellen Komplexität erhalten bleibt.

Wie gelingt das?

- Bevorzuge Frameworks, die aus funktionierendem Code entstanden sind, statt solche aus theoretischen Konzepten.
- Prüfe, wie viel Code tatsächlich das Geschäftsproblem löst und wie viel nur die Schnittstelle zwischen Anwendung und Benutzer bedient.
- Betrachte Vendor-Lösungen kritisch. Sie sind nicht unbedingt schlecht, erzeugen aber häufig zusätzliche Komplexität.
- Stelle sicher, dass die Lösung wirklich zum Problem passt.

Die Aufgabe eines Architekten ist es, die essentielle Komplexität eines Problems zu lösen, ohne dabei zusätzliche zufällige Komplexität einzuführen.

*Von Neal Ford*

---

## 3. Wahrscheinlich ist dein größtes Problem nicht technischer Natur

Gerade jetzt arbeitet irgendwo jemand an einem gescheiterten Projekt zur Entwicklung eines Gehaltssystems. Wahrscheinlich sogar mehrere.

Warum?

Lag es daran, dass Ruby statt Java gewählt wurde? Oder Python statt Smalltalk? Oder Postgres statt Oracle? Oder Windows statt Linux?

Oft wird die Technologie für gescheiterte Projekte verantwortlich gemacht. Aber wie wahrscheinlich ist es wirklich, dass das Problem so schwierig war, dass Java es nicht lösen konnte?

Die meisten Projekte werden von Menschen gebaut. Diese Menschen sind die Grundlage für Erfolg oder Misserfolg. Deshalb lohnt es sich, darüber nachzudenken, was diese Menschen erfolgreich macht.

Ebenso wahrscheinlich gibt es jemanden im Team, von dem du denkst, dass er „es einfach falsch macht“ und das Projekt sabotiert. In solchen Fällen ist die Technologie, die du brauchst, sehr alt – wahrscheinlich sogar die wichtigste technische Innovation der Menschheit: **ein Gespräch**.

Es reicht jedoch nicht, einfach zu wissen, dass Gespräche wichtig sind. Menschen respektvoll zu behandeln und ihnen zunächst gute Absichten zu unterstellen, gehört zu den Kernfähigkeiten eines effektiven Architekten.

Ein paar Tipps für bessere Gespräche:

1. **Betrachte solche Situationen als Gespräche – nicht als Konfrontationen.**  
   Wenn du vom Besten im anderen ausgehst und Fragen stellst, lernst du mehr und bringst andere weniger in eine Verteidigungshaltung.

2. **Beginne solche Gespräche erst, wenn deine eigene Haltung stimmt.**  
   Wenn du wütend, frustriert oder gereizt bist, wird dein Gegenüber deine Körpersprache als Angriff interpretieren.

3. **Nutze Gespräche, um gemeinsame Ziele festzulegen.**  
   Statt einem Entwickler zu sagen, er solle in Meetings weniger reden, bitte ihn, dir zu helfen, die Beteiligung anderer zu erhöhen.

Wenn du mit einem gemeinsamen Ziel startest, Menschenprobleme als Lernchance siehst und deine eigenen Emotionen kontrollierst, wirst du nicht nur effektiver – du wirst auch jedes Mal etwas dazulernen.

*Von Mark Ramm*

---

## 4. Kommunikation ist König; Klarheit und Führung sind seine Diener

Zu oft sitzen Softwarearchitekten im Elfenbeinturm und diktieren Spezifikationen, Technologieentscheidungen und Architekturvorgaben an Entwickler. Das führt häufig zu Unzufriedenheit im Team und letztlich zu einem Produkt, das kaum noch den ursprünglichen Anforderungen entspricht.

Jeder Softwarearchitekt sollte wissen, wie man die Ziele eines Projekts kommuniziert. Der Schlüssel dazu ist **Klarheit und Führung**.

### Klarheit

Niemand im Team liest ein 100-seitiges Architektur-Dokument.  
Ideen müssen klar und prägnant kommuniziert werden.

Tipps:

- Halte Dinge am Anfang eines Projekts so einfach wie möglich.
- Schreibe nicht sofort lange Dokumente.
- Nutze Diagramme (z. B. mit Visio).
- Halte Diagramme einfach – sie werden sich ohnehin häufig ändern.
- Nutze Whiteboard-Meetings für Diskussionen.
- Fotografiere Whiteboards und teile die Ergebnisse im Wiki.

Konzentriere dich zuerst darauf, Ideen verständlich zu machen – die Dokumentation der Details kann später folgen.

### Führung

Viele Architekten vergessen, dass sie auch **Leader** sind.

- Entwickler müssen das große Bild verstehen.
- Entscheidungen sollten transparent sein.
- Entwickler sollten in Architekturentscheidungen eingebunden werden.

Arbeite **mit** Entwicklern, nicht gegen sie.  
Das gilt auch für QA, Business-Analysten und Projektmanager.

Wenn **Kommunikation der König** ist, dann sind **Klarheit und Führung seine Diener**.

*Von Mark Richards*

---

## 5. Architektur bedeutet Balance

Beim Entwurf von Software denken wir oft zuerst an technische Aufgaben:

- Modularisierung
- Schnittstellen definieren
- Verantwortlichkeiten verteilen
- Patterns anwenden
- Performance optimieren

Doch Architekten müssen auch andere Aspekte berücksichtigen:

- Sicherheit
- Usability
- Support
- Deployment
- Release-Management

All diese technischen Themen müssen mit den Interessen der **Stakeholder** ausbalanciert werden.

Eine Analyse von Stakeholdern und ihren Interessen hilft, Anforderungen vollständig zu verstehen. Die Prioritäten eines Unternehmens beeinflussen direkt die Architektur.

Beispielsweise in einem SaaS-Unternehmen:

Geschäftsprioritäten können sein:

- Verträge erfüllen
- Umsatz generieren
- Kosten kontrollieren
- Kundenreferenzen gewinnen
- Technologie-Assets aufbauen

Diese übersetzen sich in technische Prioritäten wie:

- Funktionalität und Korrektheit
- Qualitätsmerkmale („-ilities“)
- Produktivität des Entwicklungsteams
- Wartbarkeit
- langfristige Anpassbarkeit

Die Aufgabe des Architekten ist es, Software zu entwickeln, die:

- für Benutzer funktioniert
- gleichzeitig Unternehmensziele erfüllt
- wartbar und administrierbar bleibt
- für zukünftige Entwickler verständlich ist

Manchmal muss kurzfristig eine Priorität stärker gewichtet werden.  
Langfristig muss jedoch die Balance erhalten bleiben.

Softwarearchitektur bedeutet daher mehr als Technik – sie bedeutet das **Ausbalancieren technischer und geschäftlicher Anforderungen**.

*Von Randy Stafford*

 6. Den Wert in den geforderten Fähigkeiten suchen

Häufig formulieren Kunden und Endnutzer das, was sie für eine praktikable Lösung eines Problems halten, als Anforderung. Die klassische Geschichte dazu erzählte Harry Hillaker, der leitende Designer des F-16 Falcon. Sein Team wurde beauftragt, ein Flugzeug mit Mach 2–2,5 zu entwerfen – damals und wahrscheinlich auch heute noch eine anspruchsvolle Aufgabe, insbesondere wenn das Ziel darin besteht, ein „günstiges" und leichtes Flugzeug zu entwickeln. Man bedenke, dass sich der Widerstandswiderstand vervierfacht, wenn die Geschwindigkeit verdoppelt wird, und welche Auswirkungen das auf das Gewicht des Flugzeugs hat.

Als das Designteam die Luftwaffe fragte, warum sie Mach 2–2,5 benötige, lautete die Antwort: um aus Kampfsituationen entkommen zu können. Mit dem eigentlichen Bedarf auf dem Tisch war das Designteam in der Lage, das grundlegende Problem anzugehen und eine funktionierende Lösung zu entwickeln. Ihre Lösung war ein wendiges Flugzeug mit einem hohen Schub-Gewichts-Verhältnis, das Beschleunigung und Manövrierfähigkeit bot – und keine Höchstgeschwindigkeit.

Diese Lektion sollte auch in die Softwareentwicklung einfließen. Indem nach dem Wert gefragt wird, den ein angefordertes Feature oder eine Anforderung liefern soll, sind Architekten in der Lage, das eigentliche Problem zu adressieren und hoffentlich eine bessere und günstigere Lösung anzubieten, als wenn sie lediglich die vom Kunden vorgeschlagene Lösung umsetzen würden. Der Fokus auf den Wert vereinfacht auch die Priorisierung. Die wertvollsten Anforderungen werden zu den treibenden Anforderungen.

Wie soll man also vorgehen? In vielerlei Hinsicht findet sich der erforderliche Ansatz im Agilen Manifest: **„Zusammenarbeit über Verträge"**. In der Praxis bedeutet das, Workshops und Meetings zu organisieren, bei denen Architekten ihren Fokus auf die Kundenbedürfnisse legen und den Kunden dabei helfen, die „Warum"-Frage zu beantworten. Dabei sollte man sich bewusst sein, dass die Beantwortung der „Warum"-Frage schwierig sein kann, da es sich dabei sehr häufig um implizites Wissen handelt. Diskussionen über technische Lösungsansätze sollten in diesen Workshops vermieden werden, da sie die Gespräche aus der Domäne des Kunden heraus und in die Domäne der Softwareentwicklung verlagern.

# 7. Steh auf!

Als Architekten sind viele von uns aus hochgradig technischen Positionen gewachsen, in denen unser Erfolg hauptsächlich auf unserer Fähigkeit beruhte, mit Maschinen zu kommunizieren. In der Rolle des Architekten findet ein Großteil unserer Kommunikation jedoch mit anderen Menschen statt. Ob es darum geht, Entwicklern die Vorteile eines bestimmten Musters zu erklären oder dem Management die Kosten-Nutzen-Abwägungen beim Kauf von Middleware darzulegen – Kommunikation ist der Kern unseres Erfolgs.

Obwohl es schwierig ist, den Einfluss eines Architekten auf ein Projekt zu messen, gilt: Wenn Entwickler seine Empfehlungen konsequent ignorieren und das Management ihnen nicht folgt, wird die „Richtigkeit" dieser Empfehlungen wenig zur Karriere beitragen. Erfahrene Architekten wissen, dass sie ihre Ideen „verkaufen" müssen und dafür effektiv kommunizieren müssen.

Es wurden viele Bücher über zwischenmenschliche Kommunikation geschrieben, aber ich möchte einen einfachen, praktischen und leicht umsetzbaren Tipp hervorheben, der die Wirksamkeit Ihrer Kommunikation – und damit Ihren Erfolg als Architekt – drastisch steigern wird: **Stehen Sie auf**, wann immer Sie mit mehr als einer Person über Ihre Empfehlungen sprechen. Ob es sich um ein formelles Design-Review oder eine informelle Diskussion über Diagramme handelt – es spielt keine Rolle. Stehen Sie auf, besonders wenn alle anderen sitzen.

Aufstehen vermittelt automatisch Autorität und Selbstvertrauen. Sie beherrschen den Raum. Die Menschen werden Sie weniger unterbrechen. All das macht einen großen Unterschied dafür, ob Ihre Empfehlungen angenommen werden oder nicht.

Sie werden auch bemerken, dass Sie, sobald Sie stehen, mehr Ihre Hände und andere Körpersprache einsetzen. Bei Gruppen von 10 oder mehr Personen ermöglicht das Stehen außerdem, mit allen Augenkontakt herzustellen. Augenkontakt, Körpersprache und andere visuelle Elemente machen einen großen Teil der Kommunikation aus. Stehen beeinflusst auch Tonfall, Lautstärke, Tonhöhe und Sprechtempo: Die Stimme wird in größere Räume projiziert, das Tempo verlangsamt sich bei wichtigen Aussagen. Diese stimmlichen Elemente tragen wesentlich zur Wirksamkeit der Kommunikation bei.

Der einfachste Weg, die Wirksamkeit Ihrer Kommunikation mehr als zu verdoppeln, ist ganz einfach: **Stehen Sie auf.**

*Von Udi Dahan*

---

# 8. Wolkenkratzer sind nicht skalierbar

Wir hören oft, dass Softwareentwicklung mit dem Bau von Wolkenkratzern, Staudämmen oder Straßen verglichen wird. In einigen wichtigen Aspekten stimmt das.

Der schwierigste Teil des Ingenieurbaus ist nicht die Planung eines Gebäudes, das nach seiner Fertigstellung standhält, sondern die Ausarbeitung des Bauprozesses. Der Bauprozess muss von einem leeren Grundstück zu einem fertigen Gebäude führen. In der Zwischenzeit muss jeder Arbeiter sein Handwerk ausüben können, und die unfertige Struktur muss die ganze Zeit stabil bleiben. Daraus können wir eine Lehre für die Bereitstellung großer integrierter Systeme ziehen. (Mit „integriert" sind praktisch alle Unternehmens- und Webanwendungen gemeint!) Traditionelle „Big-Bang"-Deployments sind wie das Aufstapeln von Trägern und Balken, das Werfen in die Luft und die Erwartung, dass sie sich in der Form eines Gebäudes zusammenfügen.

Stattdessen sollten wir planen, jeweils eine Komponente zu deployen. Ob es sich um eine Ablösung oder ein Greenfield-Projekt handelt – dies hat zwei große Vorteile.

**Erstens:** Wenn wir Software deployen, setzen wir uns dem angesammelten technischen Risiko im Code aus. Durch das schrittweise Deployen einer Komponente nach der anderen verteilen wir das technische Risiko über einen längeren Zeitraum. Jede Komponente hat ihre eigene Chance, in der Produktion zu scheitern, sodass wir jede einzeln absichern können.

**Zweitens** zwingt uns dieser Ansatz dazu, klar definierte Schnittstellen zwischen den Komponenten zu schaffen. Das Deployen einer einzelnen Komponente eines neuen Systems bedeutet oft, sie rückwärts mit dem alten System zu integrieren. Daher hat bis zum Abschluss des Deployments jede Komponente mit zwei verschiedenen Systemen gearbeitet: dem ursprünglichen und dem Ersatzsystem. Nichts ist wiederverwendbar, bis es wiederverwendet wurde – daher bedeutet schrittweises Deployment automatisch größere Wiederverwendbarkeit. In der Praxis führt es auch zu besserer Kohäsion und loserer Kopplung.

Umgekehrt gibt es wichtige Bereiche, in denen Analogien zum Ingenieurbau irreführend sind. Insbesondere drängt uns die Konkretheit der realen Welt zu einem Wasserfallprozess. Schließlich beginnt niemand mit dem Bau eines Wolkenkratzers, ohne zu wissen, wo er stehen oder wie hoch er sein soll. Das Hinzufügen weiterer Stockwerke zu einem bestehenden Gebäude ist kostspielig, störend und riskant – daher versuchen wir, es zu vermeiden. Nach der Planung soll der Wolkenkratzer weder seinen Standort noch seine Höhe ändern. **Wolkenkratzer sind nicht skalierbar.**

Wir können Straßen nicht einfach um Fahrspuren erweitern, aber wir haben gelernt, wie wir Software einfach um Funktionen erweitern können. Dies ist kein Fehler unserer Softwareprozesse, sondern eine Tugend des Mediums, in dem wir arbeiten. Es ist in Ordnung, eine Anwendung zu veröffentlichen, die nur wenige Dinge tut, solange Benutzer diese Dinge als wertvoll genug erachten, um dafür zu zahlen. Je früher Sie Ihre Anwendung veröffentlichen, desto größer ist der Nettobarwert des Gesamtprojekts.

„Frühe Veröffentlichung" mag im Widerspruch zu „schrittweisem Deployment" stehen, aber beides kann gut zusammenwirken. Die frühe Veröffentlichung einzelner Komponenten bedeutet, dass jede unabhängig iterieren kann. Tatsächlich wird es Sie zwingen, schwierige Fragen wie kontinuierliche Verfügbarkeit während Deployments und Protokoll-Versionierung zu klären.

Es ist selten, eine Technik zu finden, die gleichzeitig höheren kommerziellen Wert und bessere Architekturqualitäten bietet – aber das frühzeitige Deployment einzelner Komponenten bietet beides.

*Von Michael Nygard*

---

# 9. Sie verhandeln öfter, als Sie denken

Wir alle kennen „Budgetarchitektur". Das ist der Fall, wenn vernünftige technische Entscheidungen zugunsten von Kosteneinsparungen über Bord geworfen werden. Das Gespräch läuft etwa so:

„Brauchen wir X wirklich?", fragt der Projektauftraggeber.

Für „X" kann man fast alles einsetzen, was für den Betrieb des Systems unbedingt notwendig ist: Softwarelizenzen, redundante Server, externe Backups oder Stromversorgungen. Die Frage wird stets in einem paternalistischen Ton gestellt, als hätte der Erwachsene uns dabei erwischt, wie wir unser Taschengeld für Comics und Kaugummi ausgeben, während die ernsthaften Erwachsenen versuchen, mehr Eimer zu kaufen, um ihre Gewinne zu transportieren.

Die richtige Antwort lautet: „Ja. Wir brauchen es." Doch diese Antwort kommt fast nie.

Schließlich sind wir als Ingenieure ausgebildet, und Ingenieurwesen dreht sich um Kompromisse. Wir wissen genau, dass man auf Luxusgüter wie Stromversorgungen verzichten kann, solange es im Rechenzentrum genug Hamsterräder und günstige Praktikanten gibt. Statt „Ja, wir brauchen es" sagen wir also etwas wie: „Nun, man könnte auf einen zweiten Server verzichten, sofern man bereit ist, Ausfallzeiten bei Routinewartungen und bei Paritätsfehler-bedingten Abstürzen zu akzeptieren, aber wenn wir fehlerkorrigierenden Paritätsspeicher einsetzen, umgehen wir das, sodass wir uns nur noch Sorgen um Betriebssystemabstürze machen müssen, die etwa alle drei Komma neun Tage auftreten, weshalb wir nächtliche Neustarts einplanen müssen. Die Praktikanten können das tun, wenn sie Pause von den stromerzeugenden Hamsterrädern machen."

All das mag vollkommen wahr sein, ist aber völlig falsch. Der Auftraggeber hat nach dem Wort „nun" aufgehört zuzuhören.

Das Problem ist, dass Sie Ihre Rolle als Ingenieuraufgabe verstehen, während Ihr Auftraggeber klar erkennt, dass er in einer Verhandlung steckt. Wir suchen nach einer gemeinsamen Lösungsfindung; sie suchen nach einem Gewinn-Verlust-Manöver. Und in einer Verhandlung ist das Letzte, was Sie tun wollen, beim ersten Angebot Zugeständnisse zu machen. Die richtige Antwort auf die „Brauchen wir das wirklich?"-Frage lautet stattdessen:

*„Ohne einen zweiten Server wird das gesamte System mindestens dreimal täglich zusammenbrechen, insbesondere wenn es am stärksten ausgelastet ist oder wenn Sie eine Demo vor dem Vorstand durchführen. Tatsächlich brauchen wir vier Server, damit wir ein HA-Paar unabhängig abschalten können, während wir noch 100 % unserer Kapazität aufrechterhalten, selbst wenn eines der verbleibenden Paare unerwartet ausfällt."*

Natürlich wissen wir beide, dass Sie den dritten und vierten Server nicht wirklich brauchen. Dies ist ein Gegenverhandlungsmanöver, um den Auftraggeber dazu zu bringen, das Thema zu wechseln. Sie erhöhen den Einsatz und zeigen, dass Sie bereits auf der absolut minimalen, gefährlichen und fast unverantwortlichen Konfiguration arbeiten. Und außerdem: Wenn Sie die zusätzlichen Server tatsächlich bekommen, können Sie einen für die QA-Umgebung und den anderen als Build-Server nutzen.

*Von Michael Nygard*

---

# 10. Quantifizieren

„Schnell" ist keine Anforderung. „Reaktionsschnell" auch nicht. Und „erweiterbar" ebenso wenig. Der schlimmste Grund dafür ist, dass Sie keine objektive Möglichkeit haben festzustellen, ob diese Eigenschaften erfüllt sind. Aber Benutzer wollen sie dennoch. Die Rolle des Architekten besteht größtenteils darin, dem System diese Qualitäten zu verleihen und die unvermeidlichen Konflikte und Widersprüche zwischen ihnen auszubalancieren. Ohne objektive Kriterien sind Architekten dem Gutdünken launischer Benutzer ausgeliefert („Nein, ich akzeptiere es nicht, immer noch nicht schnell genug") und dem Perfektionismus obsessiver Programmierer („Nein, ich gebe es nicht frei, immer noch nicht schnell genug").

Wie bei allen Anforderungen versuchen wir, diese Wünsche schriftlich festzuhalten. Allzu oft werden dann vage Adjektive verwendet: „flexibel", „wartbar" und ähnliches. Es stellt sich heraus, dass diese Phänomene in jedem Fall (ja, sogar „benutzerfreundlich", mit etwas Aufwand) quantifiziert und Schwellenwerte festgelegt werden können. Wird dies nicht getan, gibt es keine Grundlage für die Abnahme des Systems durch die Benutzer, den Entwicklern wird wertvolle Orientierung entzogen, und die Vision derjenigen, die es entwerfen, wird verschwommen.

Einige einfache Fragen: Wie viele? In welchem Zeitraum? Wie oft? Wie bald? Steigend oder sinkend? Mit welcher Rate? Wenn diese Fragen nicht beantwortet werden können, ist der Bedarf nicht verstanden. Die Antworten sollten im Business Case des Systems enthalten sein – wenn nicht, muss ernsthaft nachgedacht werden. Wenn jemand sagt, ein System müsse „skalierbar" sein, fragen Sie: Woher kommen neue Benutzer und warum? Wie viele und bis wann? Lehnen Sie „viele" und „bald" als Antworten ab.

Unsichere quantitative Kriterien müssen als Bereich angegeben werden: das Minimum, der Normalwert und das Maximum. Kann dieser Bereich nicht angegeben werden, ist das erforderliche Verhalten nicht verstanden. Im Verlauf der Architekturentwicklung kann diese gegen diese Kriterien geprüft werden. Wenn die Leistung gegenüber bestimmten Kriterien im Laufe der Zeit abnimmt, erhält man wertvolles Feedback. Das Ermitteln dieser Bereiche und das Prüfen dagegen ist zeitaufwendig und kostspielig. Wenn niemand bereit ist, für Performance-Tests zu zahlen, ist Performance wahrscheinlich nicht wichtig – und Sie können Ihre architektonischen Bemühungen auf Aspekte konzentrieren, die es wert sind, bezahlt zu werden.

*„Muss auf Benutzereingaben in nicht mehr als 1.500 Millisekunden reagieren. Unter normaler Last (definiert als ...) muss die durchschnittliche Antwortzeit zwischen 750 und 1.250 Millisekunden liegen. Antwortzeiten unter 500 Millisekunden sind für den Benutzer nicht unterscheidbar, daher werden wir nicht dafür zahlen, darunter zu kommen."* Das ist eine Anforderung.

*Von Keith Braithwaite*

---

# 11. Eine Zeile funktionierender Code ist 500 Zeilen Spezifikation wert

Design ist eine wunderbare Sache. Eine systematische, detaillierte Darstellung und Überprüfung eines Problemraums und einer Lösung deckt Fehler und Verbesserungsmöglichkeiten auf – manchmal auf verblüffend dramatische Weise. Spezifikationen sind wichtig, weil sie das Muster für den Aufbau liefern. Die Zeit für das Nachdenken über die Architektur zu investieren ist wichtig – sowohl auf Makroebene mit Blick auf die Interaktionen zwischen Komponenten als auch auf Mikroebene mit Blick auf das Verhalten innerhalb einer Komponente.

Leider ist es allzu leicht, sich im Designprozess zu verlieren und von abstrakter Architektur fesseln zu lassen. Tatsache ist, dass Spezifikationen allein keinen Wert haben. Das ultimative Ziel eines Softwareprojekts ist ein produktives System. Ein Softwarearchitekt muss dieses Ziel stets im Blick behalten und daran denken, dass Design lediglich ein Mittel zum Zweck ist – kein Selbstzweck. Ein Architekt eines Wolkenkratzers, der die Gesetze der Physik ignoriert, um das Gebäude schöner zu machen, würde es schnell bereuen. Den Fokus auf funktionierenden Code zu verlieren bedeutet ernsthafte Schwierigkeiten für jedes Projekt.

Schätzen Sie die Teammitglieder, die Ihre Vision umsetzen. Hören Sie auf sie. Wenn sie Probleme mit dem Design haben, haben sie wahrscheinlich recht und das Design ist falsch oder zumindest unklar. In diesen Fällen ist es Ihre Aufgabe, das Design anzupassen, indem Sie mit Ihrem Team herausarbeiten, was funktioniert und was nicht. Kein Design ist von Anfang an perfekt – alle Designs müssen bei der Implementierung angepasst werden.

Wenn Sie auch Entwickler im Projekt sind, schätzen Sie die Zeit, die Sie mit dem Schreiben von Code verbringen, und glauben Sie niemandem, der Ihnen sagt, es lenke Sie von Ihrer Arbeit als Architekt ab. Ihr Verständnis sowohl der Makro- als auch der Mikroebene wird durch die Zeit, die Sie im Innenleben des Systems verbringen, enorm bereichert.

*Von Allison Randal*

---

# 12. Es gibt keine Einheitslösung

Architekten müssen kontinuierlich „kontextuellen Sinn" entwickeln und anwenden – denn es gibt keine Einheitslösung für Probleme, die sehr unterschiedlich sein können.

Der treffende Begriff „kontextueller Sinn" wurde von Eberhardt Rechtin in seinem Buch *Systems Architecting: Creating & Building Complex Systems* (1991) geprägt und beschrieben:

> *„[Die zentralen Ideen des ‚heuristischen Ansatzes' zur Architektur komplexer Systeme] entstammen der Frage, was erfahrene Architekten tun, wenn sie mit hochkomplexen Problemen konfrontiert werden. Der erfahrene Architekt würde wahrscheinlich antworten: ‚Verwende einfach gesunden Menschenverstand.' … [E]in besserer Ausdruck als ‚gesunder Menschenverstand' ist kontextueller Sinn – ein Wissen darüber, was in einem gegebenen Kontext vernünftig ist. Praktizierende Architekten sammeln durch Ausbildung, Erfahrung und Beispiele einen erheblichen Vorrat an kontextuellem Sinn, bevor ihnen die Lösung von Problemen auf Systemebene anvertraut wird – typischerweise nach 10 Jahren."*

Ein großes Problem in der Softwarebranche ist meiner Meinung nach, dass Menschen häufig für die Lösung von Problemen verantwortlich sind, die mehr kontextuellen Sinn erfordern, als sie angesammelt haben. Vielleicht liegt das daran, dass die Softwarebranche kaum zwei Generationen alt und explosionsartig gewachsen ist.

Zu den typischen Beispielen gehören: das Versäumnis, Domain-Driven Design anzuwenden, wenn es angebracht wäre; das Abweichen von einem pragmatischen Ansatz und das Überdesignen einer Lösung; sowie irrelevante oder unangemessene Vorschläge während Performance-Optimierungskrisen.

Das wichtigste Wissen über Software-Muster ist das Wissen darüber, wann man sie anwenden soll und wann nicht. Es ist axiomatisch: **Es gibt keine Einheitslösung.** Architekten müssen kontextuellen Sinn entwickeln und anwenden.

*Von Randy Stafford*

---

# 13. Es ist nie zu früh, über Performance nachzudenken

Geschäftsanwender spezifizieren ihre Bedürfnisse hauptsächlich durch funktionale Anforderungen. Die nicht-funktionalen Aspekte von Systemen – wie Performance, Resilienz, Verfügbarkeit und Supportbedarf – liegen im Verantwortungsbereich des Architekten. Häufig wird das erste Testen nicht-funktionaler Anforderungen jedoch sehr spät im Entwicklungszyklus durchgeführt und manchmal vollständig an das Betriebsteam delegiert. Das ist ein Fehler, der viel zu oft gemacht wird.

Die Gründe sind vielfältig: Es macht vermeintlich keinen Sinn, etwas schnell und resilient zu machen, wenn es die erforderliche Funktion noch nicht erfüllt. Die Umgebungen und Tests selbst sind komplex. Vielleicht werden die frühen Versionen des Produktivsystems nicht so stark genutzt.

Wenn Sie jedoch erst spät im Projektzyklus auf Performance achten, haben Sie wertvolle Informationen darüber verloren, wann sich die Performance verschlechtert hat. Wenn Performance ein wichtiges Architektur- und Designkriterium sein soll, sollte Performance-Testing so früh wie möglich beginnen. Bei einer agilen Methodik mit zweiwöchigen Iterationen sollte Performance-Testing spätestens in der dritten Iteration einbezogen werden.

Warum ist das so wichtig? Der wichtigste Grund ist, dass Sie zumindest wissen, welche Art von Änderungen die Performance einbrechen ließ. Anstatt bei Performance-Problemen die gesamte Architektur analysieren zu müssen, können Sie sich auf die neuesten Änderungen konzentrieren. Frühes und regelmäßiges Performance-Testing liefert Ihnen eine enge Bandbreite von Änderungen, auf die Sie sich konzentrieren können. In frühen Tests versuchen Sie möglicherweise noch nicht einmal, die Performance zu diagnostizieren, aber Sie haben eine Ausgangsbasis. Diese Trenddaten liefern wichtige Informationen bei der Diagnose und Behebung von Performance-Problemen.

Dieser Ansatz ermöglicht auch die Validierung von Architektur- und Designentscheidungen gegenüber den tatsächlichen Performance-Anforderungen. Besonders bei Systemen mit strengen Anforderungen ist eine frühzeitige Validierung entscheidend für die termingerechte Lieferung.

Technisches Testen ist bekanntermaßen schwierig in Gang zu bringen. Das Einrichten geeigneter Umgebungen, das Generieren der richtigen Datensätze und die Definition der notwendigen Testfälle erfordern viel Zeit. Indem Sie Performance-Testing frühzeitig angehen, können Sie Ihre Testumgebung schrittweise aufbauen und viel teurere Bemühungen vermeiden, nachdem Sie Performance-Probleme entdecken.

*Von Rebecca Parsons*

---

# 14. Anwendungsarchitektur bestimmt Anwendungsperformance

Anwendungsarchitektur bestimmt Anwendungsperformance. Das mag offensichtlich erscheinen, aber die Praxis zeigt, dass dem nicht so ist. Softwarearchitekten glauben beispielsweise häufig, dass ein bloßer Wechsel von einer Softwareinfrastruktur zu einer anderen ausreicht, um Performance-Probleme einer Anwendung zu lösen. Solche Überzeugungen mögen auf Benchmarks eines Anbieters beruhen, die zum Beispiel 25 % bessere Performance als der nächste Wettbewerber versprechen. Aber wenn das Produkt des Anbieters eine Operation in drei Millisekunden durchführt, während das des Wettbewerbers vier Millisekunden benötigt, spielt der Vorteil von 25 % bzw. einer Millisekunde inmitten einer hochgradig ineffizienten Architektur kaum eine Rolle.

Neben IT-Managern und Benchmark-Teams empfehlen auch Anbieter-Supportabteilungen und Autoren von Literatur zum Anwendungsperformance-Management einfach das „Tuning" der Softwareinfrastruktur – durch Anpassen von Speicherzuweisungen, Connection-Pool-Größen, Thread-Pool-Größen und ähnlichem. Wenn das Deployment einer Anwendung jedoch für die erwartete Last unzureichend architekturiert ist oder wenn die funktionale Architektur der Anwendung Rechenressourcen zu ineffizient nutzt, wird kein „Tuning" die gewünschten Performance- und Skalierbarkeitseigenschaften herbeiführen. Stattdessen ist eine Neuarchitektur der internen Logik, der Deployment-Strategie oder beider erforderlich.

Letztendlich sind alle Produkte und Anwendungsarchitekturen denselben grundlegenden Prinzipien des verteilten Rechnens und der zugrunde liegenden Physik unterworfen. Daher müssen alle verstehen: **Anwendungsarchitektur ist der primäre Bestimmungsfaktor für Anwendungsperformance und Skalierbarkeit.** Diese Qualitätsmerkmale können nicht durch einen einfachen Wechsel der Softwaremarke oder durch Infrastruktur-„Tuning" verbessert werden. Stattdessen erfordert eine Verbesserung die harte Arbeit sorgfältig durchdachter (Re-)Architektur.

*Von Randy Stafford*

---

# 15. Commit-and-Run ist ein Verbrechen

Es ist später Nachmittag. Das Team produziert die letzten Teile des neuen Funktionsumfangs für die Iteration, und man spürt fast den Rhythmus im Raum. John hat es jedoch eilig. Er ist spät dran für ein Date, schafft es aber noch, seinen Code fertigzustellen, zu kompilieren, einzuchecken – und weg ist er. Wenige Minuten später leuchtet das rote Licht auf. Der Build ist kaputt. John hatte keine Zeit, die automatisierten Tests auszuführen, also machte er ein „Commit-and-Run" und ließ alle anderen im Stich. Die Situation hat sich verändert, der Rhythmus ist verloren. Jeder weiß jetzt, dass er sich den kaputten Code auf seine lokale Maschine holen würde, wenn er ein Update gegen das Versionskontrollsystem durchführt – und da das Team noch viel zu integrieren hat, ist das eine erhebliche Störung. John hat den Teamfluss effektiv zum Erliegen gebracht, denn nun kann keine Integration stattfinden, bis jemand sich die Zeit nimmt, seine Änderungen rückgängig zu machen.

Dieses Szenario ist viel zu häufig. Commit-and-Run ist ein Verbrechen, weil es den Flow tötet. Es ist eine der häufigsten Methoden, mit denen ein Entwickler versucht, für sich selbst Zeit zu sparen – auf Kosten anderer. Und trotzdem passiert es überall. Warum? Normalerweise weil es zu lange dauert, das System ordnungsgemäß zu bauen oder die Tests auszuführen.

Hier kommen Sie ins Spiel, als Architekt. Wenn Sie viel Mühe in eine flexible Architektur investiert haben, in der Menschen leistungsfähig sein können, den Entwicklern agile Praktiken wie testgetriebene Entwicklung beigebracht haben und einen Continuous-Integration-Server eingerichtet haben, dann möchten Sie auch eine Kultur fördern, in der es nicht akzeptabel ist, die Zeit und den Flow anderer zu verschwenden. Um das zu erreichen, müssen Sie sicherstellen, dass das System unter anderem eine solide Architektur für automatisiertes Testen hat, da dies das Verhalten der Entwickler verändern wird. Wenn Tests schnell laufen, werden sie häufiger ausgeführt – was an sich schon gut ist, aber auch bedeutet, dass Entwickler ihre Kollegen nicht mit kaputtem Code zurücklassen. Wenn die Tests von externen Systemen abhängig sind oder die Datenbank treffen müssen, entwickeln Sie sie so um, dass sie lokal mit Mocks oder Stubs – oder zumindest mit einer In-Memory-Datenbank – ausgeführt werden können, und lassen Sie den Build-Server sie auf die langsame Weise ausführen. Menschen sollten nicht auf Computer warten müssen, denn wenn sie müssen, nehmen sie Abkürzungen, die oft Probleme für andere verursachen.

Investieren Sie Zeit, um das System schnell und angenehm zu arbeiten. Es erhöht den Flow, verringert die Gründe für das Arbeiten in Silos und ermöglicht letztendlich eine schnellere Entwicklung. Mocken Sie Dinge, erstellen Sie Simulatoren, reduzieren Sie Abhängigkeiten, unterteilen Sie das System in kleinere Module – oder tun Sie was auch immer nötig ist. Stellen Sie nur sicher, dass es keinen Grund gibt, auch nur an ein Commit-and-Run zu denken.

*Von Niclas Nilsson*

# 16. Es kann mehr als eine Lösung geben

Es scheint eine nie endende Quelle der Überraschung und des Frustration für Systementwickler zu sein, dass ein einziges Datenmodell, ein einziges Nachrichtenformat, ein einziger Nachrichtentransport – kurz gesagt: genau eine Lösung für jede wichtige Architekturkomponente, Richtlinie oder Position – nicht alle Teile des Unternehmens gleich gut bedienen kann. Natürlich: Ein Unternehmen (das Wort „Enterprise" ist schon Warnsignal Nr. 1), das groß genug ist, um sich Gedanken darüber zu machen, wie viele verschiedene „Account"-Tabellen den Systemaufbau im nächsten Jahrzehnt beeinflussen, ist höchstwahrscheinlich zu groß und zu vielfältig, als dass eine einzige „Account"-Tabelle ausreichen würde.

In technischen Domänen können wir Eindeutigkeit erzwingen – sehr praktisch für uns. In Geschäftsdomänen dringt die inkonsistente, vielschichtige, unscharfe und unordentliche Welt ein. Schlimmer noch: Das Geschäft befasst sich nicht einmal mit „der Welt", sondern mit den Meinungen der Menschen über Aspekte von Situationen in Teilen der Welt. Eine Reaktion darauf ist, die Domäne als technisch zu deklarieren und per Dekret eine einheitliche Lösung zu erzwingen. Aber die Realität ist das, was nicht verschwindet, wenn man aufhört, daran zu glauben – und die Unordnung kehrt stets zurück, wenn das Geschäft sich weiterentwickelt. So entstehen Enterprise-Data-Teams, die ihre (sehr teure) Zeit damit verbringen, existenzielle Angst durch DTD-Gezänk zu zähmen. Zahlende Kunden empfinden das Maß an Reaktionsfähigkeit, das dabei herauskommt, als eher unbefriedigend.

Warum nicht der Realität einer unordentlichen Welt ins Auge sehen und mehrere, inkonsistente, überlappende Darstellungen, Dienste und Lösungen zulassen? Als Technologen schrecken wir davor zurück. Wir stellen uns erschreckende Szenarien vor: inkonsistente Updates, Wartungsaufwand, ein Spaghetti-Geflecht von Abhängigkeiten. Aber nehmen wir uns einen Hinweis aus der Welt des Data Warehousing: Die Schemata von Data Marts sind oft (relational) denormalisiert, mischen importierte und berechnete Werte willkürlich und präsentieren eine sehr andere Sicht auf die Daten als die zugrunde liegenden Datenbanken. Und der Himmel fällt deshalb nicht ein. Der ETL-Prozess sitzt an der Grenze zweier sehr unterschiedlicher Welten – typischerweise transaktionale versus analytische Verarbeitung – mit sehr unterschiedlichen Update- und Abfragehäufigkeiten, unterschiedlichem Durchsatz, verschiedenen Änderungsraten im Design und möglicherweise sehr unterschiedlichen Datenmengen. Das ist der Schlüssel: Ausreichend unterschiedliche nicht-funktionale Eigenschaften eines Teilsystems schaffen eine Grenze, über die hinweg das Management inkonsistenter Darstellungen handhabbar wird.

Duplizieren Sie keine Darstellungen oder verwenden Sie nicht mehrere Transporte nur zum Vergnügen – aber erwägen Sie stets die Möglichkeit, dass eine Zerlegung Ihres Systems nach nicht-funktionalen Parametern Möglichkeiten aufzeigen kann, vielfältige Lösungen zum Vorteil Ihrer Kunden zuzulassen.

*Von Keith Braithwaite*

---

# 17. Das Business gibt den Takt vor

Im Kontext der Entwicklung von Unternehmensanwendungen muss ein Architekt als Brücke zwischen der Geschäfts- und der Technologiegemeinschaft einer Organisation agieren – die Interessen beider Seiten vertreten und schützen, oft zwischen beiden vermitteln, aber stets dem Business erlauben, die Richtung vorzugeben. Die Ziele und operativen Realitäten der Geschäftsorganisation sollten das Licht sein, in dem ein Architekt technologieorientierte Entscheidungen trifft.

Unternehmen planen in der Regel einen spezifischen, gewünschten Return on Investment (ROI), bevor sie eine Softwareentwicklungsinitiative starten. Der Architekt muss den angestrebten ROI und damit die Grenzen des Wertes der Softwareinitiative für das Unternehmen verstehen, um zu vermeiden, Technologieentscheidungen zu treffen, die das Budget übersteigen. Der ROI sollte als wichtiger objektiver Kontext in den Gesprächen mit dem Business über den Wert eines Features im Verhältnis zu dessen Kosten sowie mit dem Entwicklungsteam über technisches Design und Implementierung dienen.

Ein Teil der Herausforderung, dem Business das „Steuer" zu überlassen, besteht darin, dem Business ausreichend Qualitätsinformationen über den laufenden Softwareentwicklungsprozess bereitzustellen, um gute Geschäftsentscheidungen zu unterstützen. Hier wird Transparenz entscheidend. Der Architekt muss gemeinsam mit dem Entwicklungsmanagement Mittel für regelmäßige, kontinuierliche Informations-Feedback-Schleifen schaffen und pflegen. Dies kann durch verschiedene Lean-Software-Entwicklungstechniken erreicht werden, wie z. B. große sichtbare Diagramme (Big Visible Charts), Continuous Integration und häufige Releases funktionierender Software an das Business – beginnend früh im Projekt.

Softwareentwicklung ist grundlegend eine Designtätigkeit, da sie einen fortlaufenden Entscheidungsprozess bis zur Inbetriebnahme des Systems beinhaltet. Es ist angemessen, dass Softwareentwickler viele Entscheidungen treffen, aber normalerweise keine Geschäftsentscheidungen. Soweit die Geschäftsgemeinschaft es jedoch versäumt, ihrer Verantwortung zur Richtungsvorgabe nachzukommen, delegiert sie die Geschäftsentscheidungen de facto an die Softwareentwickler. Der Architekt muss den Makrokontext für diese fortlaufende Reihe von Mikroentscheidungen liefern, die Softwarearchitektur und Geschäftsziele kommunizieren und schützen sowie sicherstellen, dass Entwickler keine Geschäftsentscheidungen treffen. Technische Entscheidungen, die losgelöst von den Verpflichtungen, Erwartungen und Realitäten des Unternehmens getroffen werden, kommen kostspieligen Spekulationen gleich und führen oft zu einem nicht zu rechtfertigenden Einsatz knapper Ressourcen.

Die langfristigen Interessen des Softwareentwicklungsteams werden am besten bedient, wenn das Business den Takt vorgibt.

*Von Dave Muirhead*

---

# 18. Einfachheit vor Allgemeinheit, Nutzung vor Wiederverwendung

Ein häufiges Problem bei Komponentenframeworks, Klassenbibliotheken, Basisdiensten und anderem Infrastrukturcode ist, dass viele davon für den allgemeinen Gebrauch konzipiert werden, ohne Bezug auf konkrete Anwendungen. Dies führt zu einem schwindelerregenden Array von Optionen und Möglichkeiten, die oft ungenutzt, missbraucht oder schlicht nicht nützlich sind. Die meisten Entwickler arbeiten an spezifischen Systemen: Das Streben nach unbegrenzter Allgemeinheit dient ihnen selten gut. Der beste Weg zur Allgemeinheit führt über das Verstehen bekannter, konkreter Beispiele und die Konzentration auf deren Wesen, um eine wesentliche gemeinsame Lösung zu finden. **Einfachheit durch Erfahrung statt Allgemeinheit durch Raten.**

Einfachheit vor Allgemeinheit zu bevorzugen dient als Tiebreaker zwischen gleichwertigen Designalternativen. Wenn es zwei mögliche Lösungen gibt, bevorzugen Sie die einfachere, die auf einem konkreten Bedarf basiert, gegenüber der komplizierteren, die mit Allgemeinheit wirbt. Natürlich ist es durchaus möglich – und mehr als wahrscheinlich –, dass sich die einfachere Lösung in der Praxis als die allgemeinere herausstellt. Und wenn das nicht der Fall ist, wird es einfacher sein, die einfachere Lösung an das anzupassen, was Sie jetzt wissen, als die „allgemeine" zu ändern, die sich als nicht allgemein genug herausstellt.

Obwohl gut gemeint, enden viele Dinge, die nur für den allgemeinen Gebrauch konzipiert sind, oft damit, keinen Zweck zu erfüllen. Softwarekomponenten sollten in erster Linie für den Einsatz konzipiert werden und diesen gut erfüllen. Effektive Allgemeinheit entsteht durch Verstehen, und Verstehen führt zur Vereinfachung. Zu oft wird Generalisierung jedoch zu einem eigenständigen Arbeitspunkt, der in die entgegengesetzte Richtung zieht und die Komplexität erhöht statt verringert. Das Streben nach spekulativer Allgemeinheit führt oft zu Lösungen, die nicht in der Realität der tatsächlichen Entwicklung verankert sind.

Obwohl viele Architekten Allgemeinheit schätzen, sollte sie nicht bedingungslos sein. Menschen zahlen im Allgemeinen nicht für Allgemeinheit – sie haben eine spezifische Situation, und es ist die Lösung für diese spezifische Situation, die Wert hat. Wenn wir zu früh die Verankerung im Spezifischen aufgeben, treiben wir in einem Meer nebulöser Möglichkeiten – einer Welt kniffliger Konfigurationsoptionen, überladener Parameterlisten, weitschweifiger Schnittstellen und nicht-ganz-richtiger Abstraktionen.

*Von Kevlin Henney*

---

# 19. Architekten m��ssen praktisch tätig sein

Ein guter Architekt sollte durch Beispiel führen. Er (oder sie) sollte in der Lage sein, jede Position im Team zu übernehmen – vom Verkabeln des Netzwerks und Konfigurieren des Build-Prozesses bis zum Schreiben von Unit-Tests und Ausführen von Benchmarks. Ohne ein gutes Verständnis der gesamten Bandbreite der Technologie ist ein Architekt kaum mehr als ein Projektmanager. Es ist absolut akzeptabel, dass Teammitglieder tieferes Wissen in ihren spezifischen Bereichen haben – aber es ist schwer vorstellbar, wie Teammitglieder Vertrauen in ihren Architekten haben können, wenn dieser die Technologie nicht versteht.

Wie andernorts erwähnt, ist der Architekt die Schnittstelle zwischen dem Business und dem Technologieteam. Der Architekt muss jeden Aspekt der Technologie verstehen, um das Team gegenüber dem Business vertreten zu können, ohne ständig auf andere verweisen zu müssen. Ebenso muss der Architekt das Business verstehen, um das Team auf ihr Ziel auszurichten.

Ein Architekt ist wie ein Airline-Pilot: Er wirkt vielleicht nicht immer beschäftigt, nutzt aber jahrzehntelange Erfahrung, um die Situation kontinuierlich zu überwachen und sofort zu handeln, wenn er etwas Ungewöhnliches sieht oder hört. Der Projektmanager (Co-Pilot) übernimmt die täglichen Managementaufgaben und entlastet den Architekten von lästigen Routineaufgaben und Personalführung. Letztendlich sollte der Architekt die Verantwortung für die Lieferung und Qualität der Projekte gegenüber dem Business tragen – was ohne entsprechende Autorität schwer zu erreichen ist und entscheidend für den Erfolg jedes Projekts ist.

Menschen lernen am besten durch Beobachten anderer – so lernen wir als Kinder. Ein guter Architekt sollte in der Lage sein, ein Problem zu erkennen, das Team zusammenzurufen und – ohne jemanden zu beschuldigen – zu erklären, was das Problem ist oder sein könnte, und eine elegante Umgehungslösung oder Lösung bereitzustellen. Es ist völlig respektabel für einen Architekten, das Team um Hilfe zu bitten. Das Team sollte sich als Teil der Lösung fühlen, aber der Architekt sollte die Diskussion leiten und die richtigen Lösungen identifizieren.

Architekten sollten so früh wie möglich in das Team eingebunden werden. Sie sollten nicht in einem Elfenbeinturm sitzen und den Weg diktieren, sondern vor Ort mit dem Team arbeiten. Fragen zu Richtung oder Technologieauswahl sollten nicht in separate Untersuchungen oder neue Projekte ausgelagert werden, sondern pragmatisch durch praktische Untersuchungen oder den Rat von Architektenkollegen gelöst werden – alle guten Architekten sind gut vernetzt.

Ein guter Architekt sollte in mindestens einem Werkzeug seines Handwerks ein Experte sein – z. B. einer IDE. Ein Softwarearchitekt sollte die IDE kennen, ein Datenbankarchitekt das ER-Tool, ein Informationsarchitekt ein XML-Modellierungstool – aber ein technischer oder Enterprise-Architekt sollte auf allen Ebenen der Werkzeuge effektiv sein, vom Überwachen von Netzwerkverkehr mit Wireshark bis zum Modellieren einer komplexen Finanznachricht in XMLSpy. Keine Ebene ist zu niedrig oder zu hoch.

Ein Architekt kommt meist mit einem beeindruckenden Lebenslauf und kann sowohl das Business als auch Technologen beeindrucken – aber ohne die Fähigkeit, praktisch tätig zu sein, ist es schwer, den Respekt des Teams zu gewinnen, schwer für das Team zu lernen, und nahezu unmöglich, das zu liefern, wofür man ursprünglich eingestellt wurde.

*Von John Davies*

---

# 20. Kontinuierlich integrieren

Der Build als „Big-Bang"-Ereignis in der Projektentwicklung ist tot. Der Architekt – ob Anwendungs- oder Enterprise-Architekt – sollte die Nutzung von Continuous-Integration-Methoden und -Werkzeugen für jedes Projekt fördern und unterstützen.

Der Begriff Continuous Integration (CI) wurde erstmals von Martin Fowler in einem Design-Pattern geprägt. CI bezieht sich auf eine Reihe von Praktiken und Werkzeugen, die automatische Builds und Tests einer Anwendung in regelmäßigen Abständen sicherstellen – üblicherweise auf einem Integrationsserver, der speziell für diese Aufgaben konfiguriert ist. Das Zusammenwirken von Unit-Testing-Praktiken und -Werkzeugen mit automatisierten Build-Tools macht CI zu einem Muss für jedes Softwareprojekt heute.

Continuous Integration zielt auf ein universelles Merkmal des Softwareentwicklungsprozesses ab: den Integrationspunkt zwischen Quellcode und laufender Anwendung. An diesem Integrationspunkt kommen die vielen Teile der Entwicklungsarbeit zusammen und werden getestet. Sie haben wahrscheinlich den Satz „früh und oft bauen" gehört – eine Risikominderungstechnik, um sicherzustellen, dass es an diesem Punkt keine Überraschungen gibt. „Früh und oft bauen" wurde nun durch CI ersetzt, das den Build einschließt, aber auch Funktionen hinzufügt, die die Kommunikation und Koordination innerhalb des Entwicklungsteams verbessern.

Der prominenteste Teil einer CI-Implementierung ist der Build, der in der Regel automatisiert ist. Sie können einen manuellen Build durchführen, aber sie können auch nächtlich ausgelöst oder durch Quellcodeänderungen getriggert werden. Sobald der Build gestartet ist, wird die neueste Version des Quellcodes aus dem Repository gezogen, das CI-Tool versucht, das Projekt zu bauen und zu testen. Abschließend wird eine Benachrichtigung mit den Ergebnissen des Build-Prozesses versendet – per E-Mail oder Sofortnachricht.

Continuous Integration wird einen stabileren und zielgerichteteren Entwicklungsprozess ermöglichen. Als Architekt werden Sie es lieben – aber wichtiger noch: Ihre Organisation und Ihre Entwicklungsteams werden effektiver und effizienter sein.

*Von Dave Bartlett*

---

# 21. Terminausfälle vermeiden

Gescheiterte Projekte können aus einer Vielzahl von Gründen entstehen. Eine der häufigsten Ursachen ist die Änderung des Projektzeitplans mitten im Prozess ohne angemessene Planung. Diese Art von Misserfolg ist vermeidbar, kann jedoch erheblichen Aufwand von mehreren Personen erfordern. Das Anpassen des Zeitrahmens oder das Erhöhen von Ressourcen in einem Projekt ist normalerweise kein Problem. Probleme entstehen, wenn Sie gebeten werden, mehr in demselben Zeitrahmen zu leisten oder wenn der Zeitplan verkürzt wird, ohne die Arbeitslast zu reduzieren.

Die Idee, dass Zeitpläne verkürzt werden können, um Kosten zu senken oder die Lieferung zu beschleunigen, ist ein sehr verbreitetes Missverständnis. Häufig sieht man Versuche, Überstunden zu verlangen oder „weniger wichtige geplante Aufgaben" (wie Unit-Tests) zu opfern, um Liefertermine zu verkürzen oder die Funktionalität zu erhöhen, während die Liefertermine beibehalten werden. Vermeiden Sie dieses Szenario um jeden Preis. Erinnern Sie diejenigen, die Änderungen fordern, an folgende Tatsachen:

1. Ein überstürzter Designzeitplan führt zu schlechtem Design, schlechter Dokumentation und wahrscheinlichen Qualitätssicherungs- oder Benutzerakzeptanzproblemen.
2. Ein überstürzter Programmier- oder Lieferzeitplan steht in direktem Zusammenhang mit der Anzahl der Fehler, die an die Benutzer ausgeliefert werden.
3. Ein überstürzter Testzeitplan führt zu schlecht getestetem Code und steht in direktem Zusammenhang mit der Anzahl der gefundenen Testprobleme.
4. All das oben Genannte führt zu Produktionsproblemen, die weitaus teurer zu beheben sind.

Das Endergebnis ist eine Kostensteigerung statt einer Kostensenkung. Das ist normalerweise der Grund, warum die Misserfolge passieren.

Als Architekt werden Sie eines Tages in der Lage sein müssen, schnell zu handeln, um die Erfolgswahrscheinlichkeit zu erhöhen. **Sprechen Sie frühzeitig.** Versuchen Sie zunächst, die Qualität durch Verhandlung des ursprünglich geplanten Zeitrahmens zu erhalten. Wenn ein verkürzter Zeitplan notwendig ist, versuchen Sie, nicht-kritische Funktionalität in zukünftige Releases zu verschieben. Dies erfordert natürlich gute Vorbereitung, Verhandlungsgeschick und ein Talent dafür, Menschen zu überzeugen. Schärfen Sie diese Fähigkeiten noch heute – Sie werden es nicht bereuen.

*Von Norman Carnovale*

---

# 22. Architektonische Kompromisse

Jeder Softwarearchitekt sollte wissen und verstehen, dass man nicht alles haben kann. Es ist praktisch unmöglich, eine Architektur zu entwerfen, die gleichzeitig hohe Performance, hohe Verfügbarkeit, ein hohes Maß an Sicherheit und einen hohen Grad an Abstraktion aufweist. Es gibt eine wahre Geschichte, die Softwarearchitekten kennen, verstehen und ihren Kunden und Kollegen vermitteln können sollten. Es ist die Geschichte eines Schiffes namens **Vasa**.

In den 1620er Jahren befanden sich Schweden und Polen im Krieg. Um diesem kostspieligen Krieg schnell ein Ende zu setzen, beauftragte der König von Schweden den Bau eines Schiffes namens Vasa. Dieses war kein gewöhnliches Schiff. Die Anforderungen waren einzigartig: über 60 Meter lang, 64 Kanonen auf zwei Kanondecks und die Fähigkeit, 300 Soldaten sicher über das Wasser nach Polen zu transportieren. Zeit war ein kritischer Faktor, und das Budget war knapp. Der Schiffsarchitekt hatte zuvor noch nie ein solches Schiff entworfen. Trotzdem extrapolierte er auf Basis seiner bisherigen Erfahrung und begann mit dem Design und Bau der Vasa. Das Schiff wurde schließlich nach den Spezifikationen gebaut, und als der große Tag des Stapellaufs kam, segelte es stolz in den Hafen, feuerte seinen Kanonensalut – und sank prompt auf den Meeresgrund.

Das Problem mit der Vasa war offensichtlich: Jeder, der jemals das Deck eines großen Kriegsschiffes aus dem 17. oder 18. Jahrhundert gesehen hat, weiß, dass diese Decks überfüllt und gefährlich waren, besonders im Kampf. Ein Schiff zu bauen, das gleichzeitig Kampf- und Transportschiff war, war ein kostspieliger Fehler. Der Schiffsarchitekt hatte, in dem Versuch, alle Wünsche des Königs zu erfüllen, ein unausgewogenes und instabiles Schiff geschaffen.

Softwarearchitekten können aus dieser Geschichte viel lernen. Der Versuch, jede einzelne Anforderung zu erfüllen (wie bei der Vasa), schafft eine instabile Architektur, die im Grunde genommen nichts gut macht. Ein gutes Beispiel für einen Kompromiss ist die Anforderung, eine Service-Oriented Architecture (SOA) genauso performant wie eine Point-to-Point-Lösung zu machen. Dazu müssen normalerweise die verschiedenen Abstraktionsebenen einer SOA-Architektur umgangen werden, was zu einer Architektur führt, die wie eine typische Bestellung in einem italienischen Restaurant aussieht. Es gibt verschiedene Werkzeuge für Architekten, um die Kompromisse bei der Architekturgestaltung zu bestimmen, wie z. B. die **Architecture Tradeoff Analysis Method (ATAM)** und die **Cost Benefit Analysis Method (CBAM)**.

*Von Mark Richards*

---

# 23. Die Datenbank als Festung

Die Datenbank ist der Ort, an dem alle Daten gespeichert sind – sowohl die von Ihren Mitarbeitern eingegebenen als auch die von Ihren Kunden gesammelten. Benutzeroberflächen, Geschäfts- und Anwendungslogik sowie Mitarbeiter kommen und gehen, aber Ihre Daten bleiben für immer. Daher kann nicht genug über die Bedeutung des Aufbaus eines soliden Datenmodells von Anfang an gesagt werden.

Die Begeisterung für agile Techniken hat viele zu der Annahme verleitet, dass es in Ordnung – oder sogar vorzuziehen – ist, Anwendungen im laufenden Betrieb zu entwickeln. Vorbei sind die Tage, in denen komplexe, umfassende technische Designs im Voraus geschrieben wurden! Die neue Schule sagt: früh und oft deployen. Eine Codezeile in der Produktion ist besser als zehn in Ihrem Kopf. Das klingt fast zu gut, um wahr zu sein – und wo Ihre Daten betroffen sind, ist es das auch.

Während sich Geschäftsregeln und Benutzeroberflächen schnell weiterentwickeln, tun dies die Strukturen und Beziehungen innerhalb der gesammelten Daten oft nicht. Daher ist es entscheidend, Ihr Datenmodell von Anfang an richtig zu definieren – sowohl strukturell als auch analytisch. Die Migration von Daten von einem Schema zu einem anderen ist bestenfalls schwierig, immer zeitaufwendig und oft fehleranfällig. Während Sie vorübergehend mit Fehlern auf der Anwendungsebene leben können, können Fehler in der Datenbank katastrophal sein.

Ein solides Datenmodell ist eines, das die Sicherheit der heutigen Daten garantiert, aber auch für die Zukunft erweiterbar ist. Sicherheit garantieren bedeutet, gegen Fehler unempfindlich zu sein, referenzielle Integrität durchzusetzen, Domäneneinschränkungen zu integrieren, wo sie bekannt sind, und geeignete Schlüssel zu wählen. Erweiterbar für morgen zu sein bedeutet, Ihre Daten ordnungsgemäß zu normalisieren, keine Abkürzungen zu nehmen.

Die Datenbank ist der letzte Wächter Ihrer wertvollen Daten. Die Anwendungsschicht, die von Natur aus flüchtig ist, kann nicht ihre eigene Aufsicht übernehmen. Damit die Datenbank ihre Wächterfunktion erfüllen kann, muss das Datenmodell so gestaltet sein, dass es Daten ablehnt, die nicht hineingehören, und Beziehungen verhindert, die keinen Sinn ergeben. Schlüssel, Fremdschlüsselbeziehungen und Domäneneinschränkungen, wenn sie in einem Schema beschrieben sind, sind prägnant, leicht zu verstehen und zu überprüfen und letztendlich selbstdokumentierend.

**Behandeln Sie die Datenbank wie eine Festung** – wenn Sie ihr die schwere Verantwortung anvertrauen, Fehler aus anderen Schichten abzufangen, werden Sie nie enttäuscht sein.

*Von Dan Chak*

---

# 24. Unsicherheit als Treiber nutzen

Wenn man mit zwei Optionen konfrontiert wird, glauben die meisten Menschen, dass das Wichtigste eine Entscheidung zwischen ihnen ist. Im Design – ob Software oder anderes – ist das nicht so. Das Vorhandensein zweier Optionen ist ein Hinweis darauf, dass Sie Unsicherheit im Design berücksichtigen müssen. Nutzen Sie die Unsicherheit als Treiber, um zu bestimmen, wo Sie die Festlegung auf Details verzögern können und wo Sie durch Partitionierung und Abstraktion die Bedeutung von Designentscheidungen reduzieren können. Wenn Sie das Erstbeste verdrahten, werden Sie damit feststecken, sodass beiläufige Entscheidungen bedeutsam werden und die Weichheit der Software reduziert wird.

Eine der einfachsten und konstruktivsten Definitionen von Architektur stammt von Grady Booch: *„Alle Architektur ist Design, aber nicht alles Design ist Architektur. Architektur repräsentiert die wesentlichen Designentscheidungen, die ein System prägen, wobei Wesentlichkeit durch die Kosten der Änderung gemessen wird."* Daraus folgt, dass eine effektive Architektur die Bedeutung von Designentscheidungen generell reduziert. Eine ineffektive Architektur wird sie verstärken.

Wenn eine Designentscheidung vernünftigerweise in eine von zwei Richtungen gehen kann, muss ein Architekt einen Schritt zurücktreten. Statt zu versuchen, zwischen Option A und B zu entscheiden, lautet die Frage: „Wie designe ich so, dass die Wahl zwischen A und B weniger bedeutsam ist?" Das Interessanteste ist nicht die Wahl zwischen A und B selbst, sondern die Tatsache, dass es diese Wahl gibt.

Es gibt oft Druck, eine Entscheidung um der Entscheidung willen zu treffen. Hier kann Options-Denken helfen. Wo Unsicherheit über verschiedene Entwicklungspfade besteht, treffen Sie die Entscheidung, **keine Entscheidung zu treffen**. Verschieben Sie die eigentliche Entscheidung, bis sie verantwortungsbewusster getroffen werden kann – basierend auf tatsächlichem Wissen, aber nicht so spät, dass die Vorteile dieses Wissens nicht mehr genutzt werden können.

Architektur und Prozess sind miteinander verwoben, weshalb Architekten empirische Entwicklungslebenszyklen und Ansätze bevorzugen sollten, die Feedback hervorrufen und Unsicherheit konstruktiv nutzen.

*Von Kevlin Henney*

---

# 25. Umfang ist der Feind des Erfolgs

Umfang bezeichnet die Größe eines Projekts: Wie viel Zeit, Aufwand und Ressourcen? Welche Funktionalität in welcher Qualität? Wie schwierig ist die Lieferung? Wie viel Risiko? Welche Einschränkungen bestehen? Die Antworten definieren den Umfang eines Projekts. Softwarearchitekten lieben die Herausforderung großer, komplizierter Projekte. Die potenziellen Belohnungen können sogar dazu verleiten, den Umfang eines Projekts künstlich zu erweitern, um seine scheinbare Bedeutung zu erhöhen. **Die Erweiterung des Umfangs ist der Feind des Erfolgs**, weil die Wahrscheinlichkeit des Scheiterns schneller wächst als erwartet. Die Verdopplung des Projektumfangs erhöht die Wahrscheinlichkeit des Scheiterns oft um eine Größenordnung.

Warum funktioniert das so? Betrachten Sie einige Beispiele:

- Die Intuition sagt uns, Zeit oder Ressourcen zu verdoppeln, um doppelt so viel Arbeit zu erledigen. Die Geschichte zeigt, dass die Auswirkungen nicht so linear sind, wie die Intuition vermuten lässt. Ein vierköpfiges Team wird mehr als doppelt so viel Kommunikationsaufwand betreiben wie ein zweiköpfiges Team.
- Schätzung ist keine exakte Wissenschaft. Wer hat nicht schon Features erlebt, die viel schwieriger zu implementieren waren als erwartet?

Was sind die Strategien zur Reduzierung oder Verwaltung des Umfangs?

- **Den echten Bedarf verstehen** – Hinterfragen Sie Anforderungen, die nicht in messbarem Kundenwert erklärt werden.
- **Teile und herrsche** – Suchen Sie nach Möglichkeiten, die Arbeit in kleinere, unabhängige Teile aufzuteilen.
- **Priorisieren** – Die Welt des Business ändert sich schnell. Liefern Sie die wichtigsten Anforderungen zuerst.
- **Ergebnisse so früh wie möglich liefern** – Wenige Menschen wissen, was sie wollen, bevor sie es haben. Das frühe Liefern der wichtigsten Dinge bringt Ihnen das wichtigste Feedback früh, wenn Sie es am meisten brauchen.

Agile Befürworter fordern uns auf, **„das Einfachste zu bauen, das möglicherweise funktionieren könnte"**. Komplexe Architekturen scheitern weitaus häufiger als einfachere. Die Reduzierung des Projektumfangs ist eine der effektivsten Strategien, die ein Architekt anwenden kann, um die Erfolgschancen zu verbessern.

*Von Dave Quick*

---

# 26. Wiederverwendung dreht sich um Menschen und Bildung, nicht nur um Architektur

Möglicherweise verfolgen Sie den Ansatz, dass ein gut gestaltetes Framework oder eine sorgfältig durchdachte und clever implementierte Architektur zur Wiederverwendung in Ihrer Organisation beiträgt. Die Wahrheit ist, dass selbst die schönste, eleganteste und wiederverwendbarste Architektur, Framework oder System nur von Menschen wiederverwendet wird, die:

- **a) wissen, dass es existiert**
- **b) wissen, wie man es benutzt**
- **c) überzeugt sind, dass es besser ist, als es selbst zu tun**

**a) Wissen, dass es existiert**

Innerhalb Ihrer Organisation müssen Entwickler oder Designer wissen, dass ein Design, Framework, eine Bibliothek oder Codefragmente existieren und wo sie alle wichtigen Informationen darüber finden können. Es ist eine einfache, logische Wahrheit: Menschen suchen nicht nach Dingen, von denen sie nicht glauben, dass sie existieren. Sie haben mehr Erfolg mit wiederverwendbaren Elementen, wenn Informationen darüber „gepusht" werden. Die Methoden reichen von Wiki-Seiten mit RSS-Feeds über E-Mail-Ankündigungen bis hin zu persönlichen Gesprächen im kleinen Team. Stellen Sie sicher, dass Sie einen Prozess haben – überlassen Sie es nicht dem Zufall.

**b) Wissen, wie man es benutzt**

Das Verständnis zur Wiederverwendung eines Elements hängt von Fähigkeiten und Schulung ab. Es gibt talentierte Entwickler und Architekten, deren Geschwindigkeit und Tiefe des Verständnisses beeindruckend ist – aber diese Menschen sind selten. Der Rest Ihres Teams muss unterrichtet werden. Entwickler und Designer kennen möglicherweise nicht das spezifische Entwurfsmuster, das in einem Design verwendet wird. Sie müssen einfachen Zugang zu aktueller Dokumentation oder besser noch zu Schulungen haben. Eine kleine Schulung geht einen langen Weg, um sicherzustellen, dass alle auf derselben Seite sind.

**c) Überzeugt sein, dass es besser ist, als es selbst zu tun**

Menschen – und insbesondere Entwickler – neigen dazu, Probleme lieber selbst zu lösen. „Besser als es selbst zu tun" bedeutet für verschiedene Menschen verschiedene Dinge. Die „jungen Wilden" in Ihrem Team werden immer selbst schreiben wollen, weil es ihr Ego befriedigt, während Ihre erfahreneren Mitarbeiter eher akzeptieren, dass jemand anderes über das Problemfeld nachgedacht hat. Wenn Ihr Team nicht weiß, wo es wiederverwendbare Artefakte findet oder wie es sie benutzt, werden sie standardmäßig die natürliche, menschliche Position einnehmen: **sie werden es selbst bauen.** Und Sie werden dafür zahlen.

*Von Jeremy Meyer*

---

# 27. In „Architektur" steckt kein „Ich"

Ich weiß – technisch gesehen steckt doch ein „i" in „Architektur". Aber es ist kein großes „I", das auf sich aufmerksam macht und die Diskussion dominiert. Der Kleinbuchstabe fügt sich ordentlich in das Wort ein. Er ist nur da, weil er die Anforderungen für korrekte Schreibung und Aussprache erfüllt.

Was hat das mit uns als Softwarearchitekten zu tun? Unser Ego kann unser schlimmster Feind sein. Wer hat nicht schon Architekten erlebt, die:

- glauben, die Anforderungen besser zu verstehen als die Kunden?
- Entwickler als Ressourcen betrachten, die eingestellt wurden, um ihre Ideen umzusetzen?
- defensiv reagieren, wenn ihre Ideen hinterfragt werden, oder die Ideen anderer ignorieren?

Ich vermute, dass jeder erfahrene Architekt mindestens in eine dieser Fallen getappt ist. Ich bin in alle getappt und habe schmerzhafte Lektionen aus meinen Fehlern gelernt.

**Warum passiert das?**

- **Wir hatten Erfolg** – Erfolg und Erfahrung bauen Selbstvertrauen auf. Es gibt eine feine Linie zwischen Selbstvertrauen und Arroganz. Irgendwann ist das Projekt größer als unsere persönliche Fähigkeit – und Arroganz schleicht sich ein, bevor wir es merken.
- **Menschen respektieren uns** – Kritische Designfragen sind ein wichtiges Sicherheitsnetz. Unsere eigene Defensivität oder Arroganz kann dazu führen, dass diese Fragen übersehen werden.
- **Wir sind Menschen** – Architekten investieren sich in jedes Design. Kritik an Ihrem Werk fühlt sich wie Kritik an Ihrer Person an. Defensivität kommt leicht. Sie zu stoppen ist schwer.

**Wie vermeiden wir es?**

- **Anforderungen lügen nicht** – Mit korrekten, vollständigen Anforderungen ist jede Architektur, die sie erfüllt, eine gute. Arbeiten Sie eng mit dem Kunden zusammen. Die Anforderungen treiben die Architektur – nicht Sie.
- **Fokus auf das Team** – Das sind nicht nur Ressourcen; das sind Ihre Design-Mitarbeiter und Ihr Sicherheitsnetz. Es ist die Architektur des Teams, nicht nur Ihre. Sie geben die Richtung vor, aber alle heben gemeinsam die schweren Lasten.
- **Überprüfen Sie Ihre Arbeit** – Das Modell ist nicht die Architektur. Es ist nur Ihr Verständnis davon. Arbeiten Sie mit Ihrem Team daran, Tests zu identifizieren, die zeigen, wie die Architektur jede Anforderung unterstützt.
- **Beobachten Sie sich selbst** – Geben Sie den Ideen aller den Respekt und die Anerkennung, die sie verdienen? Reagieren Sie negativ auf gut gemeintes Feedback? Verstehen Sie wirklich, warum jemand mit Ihrem Ansatz nicht einverstanden war?

Das „I" aus der Architektur zu entfernen garantiert keinen Erfolg. Es beseitigt nur eine häufige Fehlerquelle, die vollständig in Ihrer Verantwortung liegt.

*Von Dave Quick*

---

# 28. Den 1000-Fuß-Blick gewinnen

Als Architekt wollen wir wissen, wie gut die Software ist, die wir entwickeln. Ihre Qualität hat einen offensichtlichen externen Aspekt – die Software sollte für ihre Benutzer wertvoll sein – aber es gibt auch einen schwerer fassbaren internen Aspekt: die Klarheit des Designs, die Leichtigkeit, mit der wir die Software verstehen, warten und erweitern können. Wenn wir nach einer Definition gedrückt werden, enden wir meist mit „Ich erkenne es, wenn ich es sehe." Aber wie können wir Qualität sehen?

In einem Architekturdiagramm repräsentieren kleine Kästchen ganze Systeme, und Linien zwischen ihnen können alles bedeuten: eine Abhängigkeit, den Datenfluss oder eine gemeinsame Ressource wie einen Bus. Diese Diagramme sind ein **30.000-Fuß-Blick** – wie eine Landschaft, die aus dem Flugzeug betrachtet wird. Typischerweise ist die einzige andere verfügbare Ansicht der Quellcode, der einem Blick auf Bodenniveau vergleichbar ist. Beide Ansichten vermitteln wenig über die Qualität der Software. Was fehlt, ist eine Ansicht dazwischen: ein **1000-Fuß-Blick**.

Dieser 1000-Fuß-Blick würde Informationen auf der richtigen Ebene liefern. Er aggregiert große Datenmengen und mehrere Metriken, wie Methodenanzahl, Class Fan-out oder zyklomatische Komplexität. Die eigentliche Ansicht hängt stark von einem spezifischen Qualitätsaspekt ab – sie kann eine visuelle Darstellung eines Abhängigkeitsgraphen, ein Balkendiagramm auf Klassenebene oder eine ausgeklügelte polymetrische Ansicht sein, die mehrere Eingabewerte korreliert.

Solche Ansichten manuell zu erstellen und sie mit der Software synchron zu halten ist ein hoffnungsloses Unterfangen. Wir brauchen Werkzeuge, die diese Ansichten aus der einzigen wahren Quelle erstellen: dem Quellcode. Werkzeuge wie **GraphViz** für komplexe Abhängigkeitsgraphen, **Checkstyle** für Metriken auf Klassen- und Methodenebene oder das **InfoViz-Toolkit** für Tree-Maps können dabei helfen.

Sobald eine geeignete Ansicht verfügbar ist, wird Softwarequalität etwas weniger subjektiv. Es ist möglich, die Software mit ähnlichen Systemen zu vergleichen, verschiedene Revisionen desselben Systems zu vergleichen, um Trends zu erkennen, und verschiedene Teilsysteme zu vergleichen, um Ausreißer zu identifizieren. Oft gilt eine einfache Beziehung: **Wenn es gut aussieht, ist es wahrscheinlich gut.**

*Von Erik Doernenburg*

---

# 29. Ausprobieren vor Entscheiden

Die Entwicklung einer Anwendung erfordert viele Entscheidungen. Einige beinhalten die Wahl eines Frameworks oder einer Bibliothek, andere drehen sich um die Verwendung spezifischer Designmuster. In beiden Fällen liegt die Verantwortung für die Entscheidung in der Regel beim Architekten im Team. Ein stereotypischer Architekt könnte alle verfügbaren Informationen sammeln, darüber nachdenken und dann die Lösung aus dem Elfenbeinturm verkünden. Wenig überraschend gibt es einen besseren Weg.

In ihrer Arbeit über Lean Development beschreiben Mary und Tom Poppendieck eine Technik zur Entscheidungsfindung: die Festlegung bis zum **letzten verantwortungsvollen Moment** hinauszuzögern – das ist der Moment, in dem, wenn das Team keine Entscheidung trifft, sie für sie getroffen wird. Je später eine Entscheidung getroffen wird, desto mehr Informationen stehen zur Verfügung. In vielen Fällen bedeutet jedoch mehr Informationen nicht genug Informationen, und die besten Entscheidungen werden im Nachhinein getroffen.

Der Architekt sollte ständig nach Entscheidungen Ausschau halten, die bald getroffen werden müssen. Wenn sich ein solcher Entscheidungspunkt nähert, kann der Architekt mehrere Entwickler bitten, eine Lösung für das Problem zu entwickeln und eine Weile damit zu arbeiten. Wenn der letzte verantwortungsvolle Moment kommt, trifft sich das Team und bewertet die Vor- und Nachteile der verschiedenen Lösungen. Normalerweise ist dann – mit dem Vorteil der Rückschau – die beste Lösung für alle offensichtlich. Der Architekt muss die Entscheidung nicht selbst treffen, er oder sie orchestriert lediglich den Entscheidungsprozess.

Dieser Ansatz funktioniert sowohl für kleine als auch für große Entscheidungen. Das Ausprobieren von zwei oder mehr Ansätzen für dasselbe Problem erfordert mehr Aufwand als eine Vorab-Entscheidung. Aber die Chancen stehen gut, dass eine Vorab-Entscheidung zu einer Lösung führt, die später als suboptimal erkannt wird – was den Architekten vor ein Dilemma stellt: Entweder wird die aktuelle Implementierung zurückgerollt, oder man lebt mit den Konsequenzen. Schlimmer noch: Wenn keine der Alternativen erkundet wurde, erkennt möglicherweise niemand im Team, dass der gewählte Ansatz nicht der beste ist. **Das Ausprobieren mehrerer Ansätze könnte letztendlich die günstigste Option sein.**

*Von Erik Doernenburg*

---

# 30. Die Geschäftsdomäne verstehen

Effektive Softwarearchitekten verstehen nicht nur Technologie, sondern auch die Geschäftsdomäne eines Problemraums. Ohne Kenntnisse der Geschäftsdomäne ist es schwierig, das Geschäftsproblem, die Ziele und Anforderungen zu verstehen – und damit schwierig, eine effektive Architektur zu entwerfen.

Es ist die Rolle des Softwarearchitekten, das Geschäftsproblem, die Geschäftsziele und die Geschäftsanforderungen zu verstehen und diese in eine technische Architekturlösung zu übersetzen. Die Kenntnis der Geschäftsdomäne hilft einem Architekten zu entscheiden, welche Muster anzuwenden sind, wie zukünftige Erweiterbarkeit geplant werden soll und wie man sich auf laufende Branchentrends vorbereitet. Beispielsweise eignen sich einige Geschäftsdomänen (z. B. Versicherungen) gut für einen Service-orientierten Architekturansatz, während andere (z. B. Finanzmärkte) eher zu einem workflow-basierten Architekturansatz tendieren.

Das Verständnis der Branchentrends einer bestimmten Domäne kann ebenfalls helfen. Zum Beispiel gibt es im Versicherungsbereich einen zunehmenden Trend zur „On-Demand"-Kfz-Versicherung, bei der Sie nur zahlen, wenn Sie tatsächlich fahren. Das Verständnis solcher Trends ermöglicht es Ihnen als Softwarearchitekt, diese in der Architektur einzuplanen, selbst wenn das Unternehmen sie noch nicht in sein Geschäftsmodell aufgenommen hat.

Das Verständnis der spezifischen Ziele des Unternehmens hilft Ihnen ebenfalls. Beinhalten die Ziele beispielsweise anorganisches Wachstum durch Fusionen und Übernahmen? Diese Antwort kann den Architekturtyp beeinflussen. Wenn ja, könnte die Architektur viele Abstraktionsebenen umfassen. Wenn die Ziele eine starke Online-Präsenz beinhalten, ist Hochverfügbarkeit wahrscheinlich ein sehr wichtiges Attribut.

Die erfolgreichsten Architekten, die ich kenne, sind diejenigen, die breites technisches Wissen mit einem starken Wissen über eine bestimmte Domäne verbinden. Diese Architekten können mit Führungskräften und Geschäftsanwendern in der Domänensprache kommunizieren, die diese kennen und verstehen – was wiederum ein starkes Vertrauen schafft, dass der Softwarearchitekt weiß, was er tut.

*Von Mark Richards*

---

# 31. Programmieren ist ein Designakt

Kristen Nygaard, Vater der objektorientierten Programmierung und der Programmiersprache Simula, pflegte zu sagen: **„Programmieren ist Lernen."** Die Tatsache zu akzeptieren, dass Programmieren – oder genauer gesagt Softwareentwicklung – ein Prozess der Entdeckung und des Lernens ist und kein Prozess des Engineerings und der Konstruktion, ist grundlegend für den Fortschritt der Softwarepraktiken. Die Anwendung der Konzepte des traditionellen Ingenieurwesens und der Konstruktion auf die Softwareentwicklung funktioniert nicht. Die Probleme wurden von führenden Softwareexperten seit mehr als 30 Jahren dokumentiert und kommentiert. Als Beispiel stellte Frederick Brooks Jr. 1987 im „Bericht der Verteidigungswissenschaftlichen Task Force über Militärsoftware" fest, dass der dokumentengesteuerte, „zuerst spezifizieren, dann bauen"-Ansatz im Kern so vieler Softwareprobleme liegt.

Wohin sollte die Softwarebranche also schauen, um ihre Praktiken zu verbessern? Was ist mit den Industrien, die an der Produktion anspruchsvoller Massenmarktprodukte wie Autos, Pharmaka oder Halbleiter beteiligt sind?

Schauen wir uns die Automobilindustrie an. Bei der Planung eines neuen Modells wird zunächst ein Konzept oder Archetyp gewählt – ein architektonischer Positionierungsmechanismus. Der BMW X6 ist ein Beispiel für ein neues Konzept, das die Eigenschaften eines SUV und eines Coupés in das verbindet, was BMW ein „Sports Activity Coupé" nennt. Aber bevor Sie einen neuen X6 kaufen können, hat BMW Tausende von Stunden und Millionen von Dollar in sein Fahrzeug- und Fertigungsdesign investiert. Wenn BMW Ihre Bestellung erhält, wird eine seiner Montagelinien anlaufen und Ihre maßgeschneiderte Version produzieren.

Was ist die Lektion aus diesem Szenario? Die Herstellung eines neuen Autos umfasst zwei Prozesse: den kreativen Designprozess – einschließlich der Einrichtung der erforderlichen Montagelinien – und die Fertigung von Autos nach Kundenvorgaben. In vielerlei Hinsicht finden sich diese Prozesse auch in der Softwarebranche. Die Herausforderung liegt darin, was wir in diese Begriffe einbringen.

In dem Artikel „What is Software Design?" schlug Jack Reeves vor, dass das einzige Artefakt des Software-Engineerings, das die Kriterien eines Designdokuments erfüllt – wie es in der klassischen Ingenieurtechnik verstanden und verwendet wird –, der Quellcode ist. Die Fertigung der Software ist automatisiert und wird vom Compiler sowie Build- und Test-Skripten übernommen.

Indem wir akzeptieren, dass das Schreiben von Quellcode ein Designakt und kein Konstruktionsakt ist, sind wir in der Lage, nützliche Managementpraktiken zu übernehmen, die nachweislich funktionieren: die Praktiken des agilen Produktmanagements und der Lean Production wie **SCRUM**. Diese Praktiken konzentrieren sich auf die Maximierung des Return-on-Investment in Bezug auf den Kundenwert.

Damit die Softwarebranche von diesen Praktiken profitieren kann, müssen wir uns erinnern: **Programmieren ist ein Designakt, kein Konstruktionsakt.**

*Von Einar Landre*

## 33. Entwicklern Autonomie geben

Die meisten Architekten beginnen ihre Karriere als Entwickler. Als Architekt trägt man neue Verantwortung und hat größere Befugnisse bei der Entscheidung, wie ein System gebaut wird. Es kann schwerfallen, loszulassen, was man als Entwickler getan hat, wenn man nun die Rolle des Architekten übernimmt. Schlimmer noch, man könnte meinen, dass es wichtig sei, viel Kontrolle darüber auszuüben, wie Entwickler ihre Arbeit umsetzen. Es wird für den eigenen Erfolg und den Erfolg des Teams entscheidend sein, allen Teammitgliedern genug Autonomie zu geben, damit sie ihre eigene Kreativität und ihre Fähigkeiten einbringen können.

Als Entwickler hat man selten die Zeit, innezuhalten und wirklich zu betrachten, wie das gesamte System zusammenpasst. Als Architekt ist genau das die Hauptaufgabe. Während Entwickler eifrig Klassen, Methoden, Tests, Benutzeroberflächen und Datenbanken bauen, sollte man sicherstellen, dass all diese Teile gut zusammenwirken. Man sollte auf Schmerzpunkte achten und versuchen, diese zu verbessern. Haben die Leute Schwierigkeiten beim Schreiben von Tests? Verbessere die Schnittstellen und reduziere Abhängigkeiten. Weißt du, wo du wirklich Abstraktion brauchst und wo nicht? Arbeite an Domänenklarheit. Weißt du, in welcher Reihenfolge die Dinge gebaut werden sollen? Erstelle deinen Projektplan. Machen Entwickler immer wieder die gleichen Fehler bei einer API, die du entworfen hast? Mache das Design offensichtlicher. Verstehen die Leute das Design wirklich? Kommuniziere und mache es klar. Weißt du wirklich, wo du skalieren musst und wo nicht? Arbeite mit deinem Kunden und lerne sein Geschäftsmodell kennen.

Wenn du einen guten Job als Architekt machst, solltest du eigentlich nicht genug Zeit haben, um Entwickler zu behindern. Du musst zwar genau genug beobachten, ob das Design wie beabsichtigt umgesetzt wird. Du musst jedoch nicht über die Schultern der Leute schauen, um dieses Ziel zu erreichen. Es ist vernünftig, Vorschläge zu machen, wenn man sieht, dass jemand kämpft – aber es ist noch besser, ein Umfeld zu schaffen, in dem die Leute von sich aus kommen und um Vorschläge bitten. Wenn du gut bist, wirst du geschickt den schmalen Grat zwischen der Sicherstellung einer erfolgreichen Architektur und der Einschränkung des kreativen und intellektuellen Lebens deiner Entwickler und Teammitglieder meistern.

Von Philip Nelson


## 34. Verantwortungsbewusstsein über Selbstdarstellung stellen

Wenn ein Architekt ein Projekt betritt, besteht ein verständlicher Wunsch, seinen Wert unter Beweis zu stellen. Die Zuweisung der Rolle des Software-Architekten deutet in der Regel auf implizites Vertrauen des Unternehmens in die technische Führungskompetenz des Architekten hin, und es liegt nahe, dass der Architekt diese Erwartung so schnell wie möglich erfüllen möchte. Leider gibt es diejenigen, die der irrigen Vorstellung nachhängen, ihren Wert durch Selbstdarstellung beweisen zu müssen – indem sie das Team mit ihrer technischen Brillanz beeindrucken, wenn nicht gar verwirren.

Selbstdarstellung, das Ansprechen des Publikums, ist im Marketing wichtig, ist aber für die Leitung eines Softwareentwicklungsprojekts kontraproduktiv. Architekten müssen den Respekt ihres Teams gewinnen, indem sie solide Führung zeigen und die technischen und geschäftlichen Domänen, in denen sie tätig sein sollen, wirklich verstehen.

Verantwortungsvolle Stewardship – die Übernahme von Verantwortung und Fürsorge für das Eigentum anderer – ist die angemessene Rolle eines Architekten. Ein Architekt muss im besten Interesse seines Kunden handeln und nicht den Bedürfnissen seines eigenen Egos nachgeben.

Software-Architektur dient den Bedürfnissen der eigenen Kunden, typischerweise durch die Richtung von denen, die über mehr Domänenkenntnisse verfügen als man selbst. Erfolgreich Software zu entwickeln bedeutet, Kompromisslösungen zu schaffen, die die Kosten und Komplexität der Implementierung gegen die verfügbare Zeit und den verfügbaren Aufwand abwägen. Diese Zeit und dieser Aufwand sind die Ressourcen des Unternehmens, die der Software-Architekt ohne eigennützige Hintergedanken verwalten muss. Übermäßig komplexe Systeme, die das neueste angesagte Framework oder den neuesten Technologie-Buzz-Begriff aufweisen, tun dies selten ohne Opfer auf Kosten des Unternehmens. Ähnlich wie ein Investmentbroker darf der Architekt mit dem Geld seines Kunden spielen, basierend auf der Prämisse, dass seine Tätigkeit eine akzeptable Rendite erbringt.

Stelle Verantwortungsbewusstsein über Selbstdarstellung; vergiss nie, dass du mit dem Geld anderer Menschen spielst.

Von Barry Hawkins


## 35. Achtung: Probleme im Rückspiegel sind größer als sie erscheinen

Ich habe an Hunderten von Softwareprojekten gearbeitet. Jedes hatte Probleme, die mehr Schwierigkeiten verursachten, als das Team erwartet hatte. Oft erkannte ein kleiner Teil des Teams das Problem frühzeitig, und die Mehrheit ignorierte es oder tat es ab, weil sie nicht verstanden, wie wichtig es wirklich war – bis es zu spät war.

Die wirkenden Kräfte umfassen:
Probleme, die am Anfang des Projekts trivial erschienen, werden kritisch, nachdem es zu spät ist, sie zu beheben. Obwohl das Experiment mit dem kochenden Frosch möglicherweise ein Volksirrtum ist, ist es eine nützliche Analogie für das, was in vielen Projekten passiert.
Einzelpersonen stoßen oft auf Widerstand, wenn der Rest des Teams ihre Erfahrung oder ihr Wissen nicht teilt. Diesen Widerstand zu überwinden erfordert ungewöhnlichen Mut, Selbstvertrauen und Überzeugungskraft. Das passiert selten, selbst bei hochbezahlten, erfahrenen Beratern, die speziell eingestellt wurden, um solche Probleme zu vermeiden.
Die meisten Softwareentwickler sind Optimisten. Schmerzhafte Erfahrungen lehren uns, unseren Optimismus zu mäßigen, aber ohne spezifische Erfahrung neigen wir zum Optimismus. Natürliche Pessimisten in Entwicklungsteams sind oft unbeliebt, auch wenn sie konstant recht haben. Nur wenige Menschen riskieren diesen Ruf und stellen sich gegen die Mehrheit ohne einen sehr soliden Fall. Die meisten von uns kennen das Gefühl „Das macht mir Unbehagen, aber ich kann nicht erklären warum", aber es selten zu teilen gewinnt keine Argumente.
Jedes Teammitglied hat eine andere Ansicht darüber, was mehr oder weniger wichtig ist. Ihre Sorgen sind oft auf ihre persönlichen Verantwortlichkeiten fokussiert, nicht auf die Ziele des Projekts.
Wir alle haben blinde Flecken; Schwächen, die für uns schwer zu erkennen oder zu akzeptieren sind.

Einige mögliche Strategien, um diesen Kräften entgegenzuwirken:
Etabliere einen organisierten Ansatz zur Risikoverwaltung. Ein einfacher Ansatz besteht darin, Risiken genauso zu verfolgen wie Fehler. Jeder kann ein Risiko identifizieren, und jedes Risiko wird verfolgt, bis es kein Risiko mehr ist. Risiken werden priorisiert und überprüft, wenn sich ihr Status ändert oder wenn es neue Informationen gibt. Das hilft, Emotionen aus der Diskussion zu entfernen, und macht es einfacher, daran zu denken, sie regelmäßig neu zu bewerten.
Wenn man gegen die Mehrheit geht, suche nach Wegen, dem Rest des Teams das Verständnis zu erleichtern. Ermutige jedes Team, dem du angehörst, den Wert abweichender Meinungen zu erkennen, und suche nach neutralen Wegen, diese zu besprechen.
„Üble Gerüche" (Bad Smells) sind es wert, erkannt zu werden. Wenn die Fakten noch nicht vorhanden sind, suche nach den einfachsten Tests, die die Fakten liefern würden.
Überprüfe dein Verständnis ständig mit dem Team und dem Kunden. Werkzeuge wie eine priorisierte Liste von User Stories können helfen, sind aber kein Ersatz für regelmäßige Kommunikation mit dem Kunden und einen offenen Geist.
Blinde Flecken sind per Definition schwer zu erkennen. Menschen, denen du vertraust, dir die harte Wahrheit zu sagen, wenn du sie brauchst, sind ein wertvolles Gut.

Von Dave Quick


## 36. Der Titel Software-Architekt hat nur Kleinbuchstaben; damit muss man leben

Seit einiger Zeit ist innerhalb der Softwareentwicklung ein enttäuschender Trend zu beobachten: der Versuch, die Praxis der Software-Architektur als Profession auf Augenhöhe mit der klassischen Architektur zu professionalisieren. Dies scheint aus einem Bedürfnis nach weiterer Legitimierung der eigenen Leistung über die Anerkennung durch Kollegen und Arbeitgeber hinaus zu stammen. Im Vergleich dazu wurde die Architektur selbst erst Ende des 19. Jahrhunderts professionalisiert, mindestens einige Jahrtausende nachdem die Praxis bereits existierte. Es wäre keine große Übertreibung zu sagen, dass einige Software-Architekten im Vergleich dazu etwas ungeduldig erscheinen.

Software-Architektur ist ein Handwerk, und es braucht sicherlich Übung und Disziplin, um in diesem Bereich erfolgreich zu sein. Dennoch ist die Softwareentwicklung noch ein relativ junges Unterfangen. Wir wissen noch nicht genug über diese Praxis, um sie angemessen zu professionalisieren. Trotz ihrer Jugend ist das Produkt der Softwareentwicklung zu einem hoch geschätzten Werkzeug geworden, und entsprechend haben die erfahrenen Personen (sowie diejenigen, die als erfahren wahrgenommen werden möchten) Vergütungsniveaus erlangt, die mit den führenden Berufsfeldern wie Medizin, Buchhaltung und Recht vergleichbar sind.

Softwareentwickler genießen beträchtliche Vergütung für eine Arbeit, die hochkreativ und explorativ ist. Die Früchte unserer Arbeit wurden genutzt, um viele bedeutende Meilensteine zu erreichen, von denen einige der gesamten Menschheit zugutekommen. Die Eintrittsbarrieren basieren größtenteils auf eigenem Verdienst und Gelegenheit; die vollständig professionalisierten Berufsfelder durchlaufen Studien- und Praktikumsprogramme, die unsere bei weitem übertreffen. Denke einen Moment darüber nach und überlege, wie viel Grund wir haben, zufrieden zu sein – und wie dreist es ist, darauf zu bestehen, dass Software-Architekt als Titel betrachtet wird, der gleichwertig mit Anwalt, Arzt und Architekt ist.

Der Titel Software-Architekt hat nur Kleinbuchstaben; damit muss man leben.

Von Barry Hawkins


## 37. Software-Architektur hat ethische Konsequenzen

Die ethische Dimension in der Software ist offensichtlich, wenn wir über Bürgerrechte, Identitätsdiebstahl oder schädliche Software sprechen. Aber sie taucht auch in weniger exotischen Umständen auf. Wenn Programme erfolgreich sind, beeinflussen sie das Leben von Tausenden oder Millionen von Menschen. Dieser Einfluss kann positiv oder negativ sein. Das Programm kann das Leben der Menschen besser oder schlechter machen – selbst wenn nur in geringem Maße.

Jedes Mal, wenn ich eine Entscheidung darüber treffe, wie sich ein Programm verhält, entscheide ich eigentlich, was meine Benutzer tun können und was nicht – auf eine Weise, die unflexibler als Gesetze ist. Für Pflichtfelder oder obligatorische Arbeitsabläufe gibt es kein Berufungsgericht.

Eine andere Weise, darüber nachzudenken, sind Multiplikatoren. Denke an den letzten großen Internet-Wurm, oder als ein großer Geek-Film herauskam. Zweifellos hast du eine Geschichte darüber gehört oder gelesen, wie viel Produktivität das dem Land kosten würde. Man findet immer irgendein Analyst mit einer Schätzung ungeheuerlicher Schäden, der alles beschuldigt, was Menschen von ihren Schreibtischen wegbringt. Die eigentliche Moral dieser Geschichte handelt nicht von mangelnder Zahlenkompetenz in der Presse oder selbstverherrlichenden Buchhaltern. Es geht um Multiplikatoren und den Effekt, den sie haben können.

Angenommen, du musst eine Entscheidung über eine bestimmte Funktion treffen. Du kannst es einfach in etwa einem Tag machen oder schwierig in etwa einer Woche. Wie solltest du es machen? Angenommen, der einfache Weg macht vier neue Felder zu Pflichtfeldern, während die schwierige Methode das Programm so intelligent macht, dass es mit unvollständigen Daten umgehen kann. Wie solltest du es machen?

Pflichtfelder erscheinen harmlos, aber sie sind immer eine Aufzwingung deines Willens auf die Benutzer. Sie zwingen Benutzer, mehr Informationen zu sammeln, bevor sie ihre Arbeit beginnen können. Dies bedeutet oft, dass sie ihre Daten auf Post-it-Zetteln aufbewahren müssen, bis sie alles gleichzeitig zusammen haben, was zu Datenverlust, Verzögerungen und allgemeiner Frustration führt.

Als Analogie: Angenommen, ich bringe ein Schild an meinem Gebäude an. Ist es in Ordnung, das Schild nur zwei Meter hoch an der Wand zu montieren und Fußgänger zu zwingen, sich zu ducken oder drum herum zu gehen? Es ist für mich einfacher, das Schild anzubringen, wenn ich keine Leiter und kein Gerüst brauche, und das Schild würde den Gehweg nicht einmal blockieren. Ich spare eine Stunde beim Aufhängen des Schildes, auf Kosten von zwei Sekunden für jeden Fußgänger, der an meinem Geschäft vorbeigeht. Langfristig werden all diese Zwei-Sekunden-Umwege ein Vielfaches der Stunde ausmachen, die ich gespart habe.

Es ist nicht ethisch, das Leben anderer zu verschlechtern, auch nur ein wenig, nur um es sich selbst einfacher zu machen. Erfolgreiche Software betrifft Millionen von Menschen. Jede Entscheidung, die du triffst, zwingt deinen Benutzern deinen Willen auf. Sei dir immer der Auswirkungen deiner Entscheidungen auf diese Menschen bewusst. Du solltest bereit sein, große Lasten zu tragen, um ihre Lasten zu erleichtern.

Von Michael Nygard


## 38. Alles wird letztendlich versagen

Hardware ist fehleranfällig, also fügen wir Redundanz hinzu. Dies ermöglicht uns, einzelne Hardware-Ausfälle zu überleben, erhöht aber die Wahrscheinlichkeit, zu einem gegebenen Zeitpunkt mindestens einen Fehler zu haben.

Software ist fehleranfällig. Unsere Anwendungen bestehen aus Software und sind daher anfällig für Fehler. Wir fügen Monitoring hinzu, um uns zu informieren, wenn die Anwendungen ausfallen, aber dieses Monitoring besteht aus mehr Software und ist daher ebenfalls fehleranfällig.

Menschen machen Fehler; auch wir sind fehleranfällig. Also automatisieren wir Aktionen, Diagnosen und Prozesse. Automatisierung beseitigt die Chance für einen Begehungsfehler, erhöht aber die Chance für einen Unterlassungsfehler. Kein automatisches System kann auf die gleiche Bandbreite von Situationen reagieren wie ein Mensch.

Daher fügen wir der Automatisierung Monitoring hinzu. Mehr Software, mehr Möglichkeiten für Fehler.

Netzwerke bestehen aus Hardware, Software und sehr langen Kabeln. Daher sind Netzwerke fehleranfällig. Selbst wenn sie funktionieren, sind sie unvorhersehbar, weil der Zustandsraum eines großen Netzwerks für alle praktischen Zwecke unendlich ist. Einzelne Komponenten können deterministisch handeln und dennoch im Wesentlichen chaotisches Verhalten produzieren.

Jeder Sicherheitsmechanismus, den wir einsetzen, um eine Art von Fehler zu mildern, fügt neue Fehlermodi hinzu. Wir fügen Clustering-Software hinzu, um Anwendungen von einem ausgefallenen Server auf einen gesunden zu verschieben, riskieren aber nun das „Split-Brain-Syndrom", wenn das Netzwerk des Clusters Probleme hat.

Es lohnt sich zu erinnern, dass der Unfall von Three Mile Island größtenteils durch ein Druckentlastungsventil verursacht wurde – ein Sicherheitsmechanismus, der bestimmte Arten von Überdruckfehlern verhindern sollte.

Was können wir also angesichts der Gewissheit von Fehlern in unseren Systemen tun?

Akzeptiere, dass dein System egal was passiert eine Vielzahl von Fehlermodi haben wird. Leugne diese Unvermeidlichkeit, und du verlierst deine Fähigkeit, sie zu kontrollieren und einzudämmen. Sobald du akzeptierst, dass Fehler auftreten werden, hast du die Möglichkeit, die Reaktion deines Systems auf spezifische Fehler zu entwerfen. So wie Automobilingenieure Knautschzonen schaffen – Bereiche, die Passagiere schützen sollen, indem sie zuerst versagen – kannst du sichere Fehlermodi schaffen, die den Schaden eindämmen und den Rest des Systems schützen.

Wenn du deine Fehlermodi nicht entwirfst, wirst du das bekommen, was auch immer unvorhersehbare – und meist gefährliche – Fehlermodi zufällig entstehen.

Von Michael Nygard


## 39. Kontext ist König

Ich empfinde eine gewisse Ironie darin, zu versuchen, etwas über architektonische Ideale zu vermitteln, wenn die Prämisse, mit der ich beginnen möchte, ist, dass es effektiv keine Ideale gibt. Wenn das tatsächlich der Fall ist, gibt es dann nichts zu schreiben – ich bin ein Widerspruch, und indem ich dies tue, riskiere ich, dass das Universum implodiert oder so etwas ähnliches.

Aber dennoch: ceci n'est pas une pipe.

Eine der wertvollsten Lektionen, die ich als Software-Architekt gelernt habe, ist, dass Kontext König ist und Einfachheit sein bescheidener Diener. Was das in der Praxis bedeutet, ist, dass Kontext die einzige Kraft ist, die Einfachheit bei architektonischen Entscheidungen übertrumpft.

Wenn ich von Kontext spreche, meine ich nicht nur hochrangige, unmittelbare Kräfte wie wesentliche Geschäftstreiber, sondern auch Elemente in der Peripherie, wie aufkommende Technologien und Vordenkerschaft zu verschiedenen Themen. Gute Architekten behalten tatsächlich mehrere sich schnell bewegende Ziele im Auge.

Was ist gute Architektur? Sie ist das Produkt von Entscheidungen, die in einem Kontext getroffen werden, der in der Regel von mehreren konkurrierenden Prioritäten geprägt ist. Diese konkurrierenden Prioritäten bedeuten, dass manchmal die wichtigsten Entscheidungen nicht darüber sind, was du hineinlegst, sondern was du weglässt. Die Währung guter Architektur ist schlicht kluge Entscheidungsfindung (während die Produkte alle nur darum gehen, deine Absicht zu kommunizieren).

Historisch gesehen gab es einige faszinierende Beispiele für den Einfluss, den Kontext auf die Architektur haben kann. Ein bevorzugtes Beispiel betrifft die Datenbank, die zur Unterstützung eines ambitionierten neuen Softwaresystems für einen modernen Kampfpanzer ausgewählt wurde [1]. (Die Entscheidung, welche Datenbank zu verwenden ist, ist in der Regel nicht architektonisch bedeutsam; dieses Beispiel dient lediglich der Veranschaulichung eines Punktes.)

Als es Zeit war, die Datenbank auszuwählen, bewertete das Team viele. Sie stellten fest, dass während sich der Panzer schnell über unebenes Gelände bewegte und ein Ziel verfolgte, die meisten der Datenbanken in der Lage waren, den für die Navigations- und Zielsysteme erforderlichen maximalen Durchsatz zu unterstützen. Aber sie wurden überrascht, als sie entdeckten, dass das Abfeuern der Hauptwaffe des Panzers einen so starken elektromagnetischen Impuls erzeugte, dass er die Bordsysteme und natürlich auch die Datenbank zum Absturz brachte! Auf einem modernen Schlachtfeld ist ein Panzer ohne seine laufende Software buchstäblich im Dunkeln. In diesem Kontext war die Wiederherstellungszeit der überwiegende Faktor bei der Wahl der Datenbank, und keine Datenbank tat das damals besser als InterBase [2], weshalb sie für den M1 Abrams-Panzer ausgewählt wurde.

Während also Newsgroups mit den Flammen von Technologiedebatten über X vs. Y rasen, ist das eine müßige Belustigung. Der Grund, warum diese Debatten toben, liegt oft nicht an riesigen Unterschieden in ihren technischen Vorzügen, sondern daran, dass es subtilere Unterschiede zwischen ihnen gibt, und welche Funktionen Einzelpersonen mehr schätzen als andere, wenn kein leitender Kontext als Trumpfkarte dient.

Dein Team sollte frei von Idealen sein, zunächst über den Kontext nachdenken und von dort aus nach den einfachsten Lösungen greifen.

Von Edward Garson

Dieses Werk ist unter einer Creative Commons Attribution 3-Lizenz lizenziert.

Fußnoten

[1] - Ein Panzer ist trotz seines äußerst zweifelhaften Zwecks noch immer ein technisches Wunderwerk.

[2] - Interessanterweise hatte InterBase eine Architektur, die dazu führte, dass Disk-Schreibvorgänge die Datenbank in einem immer konsistenten Zustand hinterließen. Das ist einer der Gründe, der zu seiner Fähigkeit beiträgt, sich so schnell von schweren Fehlern zu erholen.


## 40. Es dreht sich alles um Leistung

Stell dir ein persönliches Fahrzeug vor, das geräumig, komfortabel, kraftstoffeffizient, günstig herzustellen und zu 98% recycelbar ist. Willst du eines? Sicher. Jeder will eines. Nur ein Problem: Seine Höchstgeschwindigkeit beträgt 10 km/h. Willst du es immer noch? Dieses kleine Beispiel zeigt, dass Leistung genauso wichtig ist wie jedes andere Kriterium.

Der Grund, warum viele Designer Leistung ans Ende ihrer Liste setzen, könnte sein, dass Computer bei Berechnungen so viel schneller sind als ihre menschlichen Gegenstücke, dass sie davon ausgehen, die Geschwindigkeit des Systems werde akzeptabel sein. Und wenn die heutigen Systeme nicht schnell genug sind, wird das Mooresche Gesetz sich um alles kümmern. Aber Hardware-Geschwindigkeit ist nur ein Teil des Systems.

Leistung wird manchmal als eine einfache Messung der Zeit betrachtet, die ein System benötigt, um auf Benutzereingaben zu reagieren. Aber Systemdesigner müssen viele Aspekte der Leistung berücksichtigen, einschließlich der Leistung der Analysten und Programmierer, die das Design implementieren; der Leistung der menschlichen Interaktionen des Systems; und der Leistung der nicht-interaktiven Komponenten.

Die Leistung der Menschen, die das System bauen, wird oft als Produktivität bezeichnet und ist wichtig, weil sie die Kosten und den Zeitplan des Projekts direkt beeinflusst. Ein Team, das ein Projekt zu spät und über Budget abliefert, hat viel zu erklären. Die Verwendung von Werkzeugen und vorgefertigten Komponenten kann dramatisch beeinflussen, wie schnell das System gebaut werden und Wert zurückgeben kann.

Die Leistung der menschlichen Interaktionen ist entscheidend für die Akzeptanz des Systems. Viele Faktoren des Systemdesigns tragen zu diesem Aspekt der Leistung bei, wobei die Reaktionszeit vielleicht der offensichtlichste ist. Aber die Reaktionszeit ist nicht der einzige Faktor. Ebenso wichtig sind die Intuitivität der Schnittstelle und die Anzahl der Gesten, die zum Erreichen eines Ziels erforderlich sind, die beide die Leistung direkt beeinflussen.

Mehr als die Reaktionszeit an sich wird eine gute Systemspezifikation die Aufgabenzeit messen, definiert als die Zeit, die zur Erledigung einer domänenspezifischen Aufgabe erforderlich ist, einschließlich aller menschlichen Interaktionen mit dem System. Zusätzlich zur Systemreaktionszeit umfasst diese Messung die Denkzeit des Bedieners und die Dateneingabezeit des Bedieners, die nicht unter der Kontrolle des Systems stehen. Aber die Einbeziehung dieser Zeiten motiviert zum richtigen Design der menschlichen Schnittstelle. Die angemessene Aufmerksamkeit für die Art und Weise, wie Informationen präsentiert werden, und die Anzahl der Gesten, die zur Erledigung der Aufgabe erforderlich sind, wird zu einer besseren menschlichen Betriebsleistung führen.

Die Leistung der nicht-interaktiven Komponenten ist ebenso wichtig für den Erfolg des Systems. Zum Beispiel wird ein „nächtlicher" Batch-Lauf, der mehr als 24 Stunden dauert, zu einem unbrauchbaren System führen. Die Leistung der Disaster-Recovery-Komponente ist ebenfalls eine kritische Überlegung. Im Falle einer vollständigen Zerstörung eines Teils des Systems: Wie schnell kann der Betriebsstatus wiederhergestellt werden, um die Wiederaufnahme des normalen Geschäftsbetriebs zu ermöglichen?

Bei der Überlegung zur Implementierung und zum Betrieb eines erfolgreichen Systems sollten Architekten und Designer stets sorgfältig auf die Leistung achten.

Von Craig L. Russell


## 41. Im Weißraum konstruieren

Ein System besteht aus voneinander abhängigen Programmen. Wir nennen die Anordnung dieser Programme und ihrer Beziehungen „Architektur". Wenn wir diese Systeme darstellen, stellen wir einzelne Programme oder Server oft als vereinfachte kleine Rechtecke dar, die durch Pfeile verbunden sind.

Ein kleiner Pfeil könnte bedeuten: „Synchrone Anfrage/Antwort mit SOAP-XML über HTTP." Das sind ziemlich viele Informationen für ein einziges Zeichen. Normalerweise ist nicht genug Platz, um das alles zu schreiben, also beschriften wir den Pfeil entweder mit „XML über HTTP" – aus einer internen Perspektive – oder „SKU-Abfrage" – für die externe Perspektive.

Dieser Pfeil, der Programme zu verbinden scheint, sieht wie ein direkter Kontakt aus, ist es aber nicht. Der Weißraum zwischen den Boxen ist mit Hardware- und Softwarekomponenten gefüllt. Dieses Substrat kann enthalten:

* Netzwerkkarten
* Netzwerk-Switches
* Firewalls
* IDS und IPS
* Nachrichtenwarteschlangen oder -broker
* XML-Transformations-Engines
* FTP-Server
* „Landing-Zone"-Tabellen
* Metro-Bereich SONET-Ringe
* MPLS-Gateways
* Stammleitungen
* Ozeane
* Kabel-suchende Fischtrawler

Es wird immer vier oder fünf Computer zwischen Programm A und B geben, die ihre Software für Paketvermittlung, Verkehrsanalyse, Routing, Bedrohungsanalyse usw. ausführen. Als Architekt, der diese Programme überbrückt, musst du dieses Substrat berücksichtigen.

Ich habe einen Pfeil mit der Aufschrift „Fulfillment" gesehen. Ein Server befand sich innerhalb des Unternehmens meines Kunden, der andere Server in einem anderen Unternehmen. Dieser Pfeil, der entscheidend für die Kundenzufriedenheit war, entfaltete sich zu einer Ereigniskette, die eher einem Spiel „Mausefalle" als einer einzigen Schnittstelle ähnelte. Nachrichten gingen zu Nachrichtenbrokern, die in Dateien geschrieben wurden, welche von einem periodischen FTP-Job aufgegriffen wurden, und so weiter. Diese eine „Schnittstelle" hatte mehr als zwanzig Schritte.

Es ist wesentlich, die statischen und dynamischen Lasten zu verstehen, die dieser Pfeil tragen muss. Anstatt nur „SOAP-XML über HTTP" sollte dieser kleine Pfeil auch sagen: „Erwarte eine Anfrage pro HTTP-Request und sende eine Antwort pro HTTP-Antwort zurück. Erwarte bis zu 100 Anfragen pro Sekunde und liefere Antworten in weniger als 250 Millisekunden zu 99,999% der Zeit."

Es gibt mehr, was wir über diesen Pfeil wissen müssen:

* Was, wenn der Aufrufer ihn zu oft ansteuert? Sollte der Empfänger Anfragen ignorieren, höflich ablehnen oder sein Bestes tun?
* Was sollte der Aufrufer tun, wenn Antworten länger als 250 Millisekunden dauern? Sollte er den Aufruf wiederholen? Sollte er warten oder davon ausgehen, dass der Empfänger ausgefallen ist, und ohne diese Funktion weitermachen?
* Was passiert, wenn der Aufrufer eine Anfrage mit Version 1.0 des Protokolls sendet und eine Antwort in Version 1.1 zurückbekommt? Was, wenn er HTML statt XML zurückbekommt? Oder eine MP3-Datei statt XML?
* Was passiert, wenn ein Ende der Schnittstelle eine Weile verschwindet?

Diese Fragen zu beantworten ist das Wesen des Konstruierens im Weißraum.

Von Michael Nygard


## 42. Die Sprache sprechen

Wie in jedem Berufsfeld wird Fachjargon verwendet, damit Fachleute effektiv miteinander kommunizieren können. Juristen sprechen miteinander über Habeas Corpus, Voir Dire und Venire; Zimmerleute sprechen miteinander über Stumpfverbindungen, Überlappungsverbindungen und Fluss; Software-Architekten sprechen miteinander über ROA, Two Step View und Layer Supertype. Warte, was war das?

Es ist unerlässlich, dass Software-Architekten, unabhängig von der Plattform, auf der sie arbeiten, ein effektives Kommunikationsmittel untereinander haben. Eines dieser Kommunikationsmittel sind Architektur- und Designmuster. Um ein effektiver Software-Architekt zu sein, muss man die grundlegenden Architektur- und Designmuster verstehen, erkennen, wann diese Muster verwendet werden, wissen, wann man die Muster anwenden soll, und in der Lage sein, mit anderen Architekten und Entwicklern unter Verwendung dieser Muster zu kommunizieren.

Architektur- und Designmuster können in vier grundlegende Kategorien eingeteilt werden: Enterprise-Architekturmuster, Anwendungsarchitekturmuster, Integrationsmuster und Designmuster. Diese Kategorien basieren im Allgemeinen auf dem Umfang innerhalb der Gesamtarchitektur. Enterprise-Architekturmuster befassen sich mit der übergeordneten Architektur, während Designmuster sich damit befassen, wie einzelne Komponenten innerhalb der Architektur strukturiert sind und sich verhalten.

Enterprise-Architekturmuster definieren den Rahmen für die übergeordnete Architektur. Zu den gängigeren Architekturmustern gehören Event Driven Architecture (EDA), Service Oriented Architecture (SOA), Resource Oriented Architecture (ROA) und Pipeline Architecture.

Anwendungsarchitekturmuster legen fest, wie Anwendungen oder Subsysteme im Rahmen einer größeren Unternehmensarchitektur entworfen werden sollen. Einige gängige Musterkataloge in dieser Kategorie umfassen die bekannten J2EE-Designmuster (z. B. Session Façade und Transfer Object) und die Anwendungsarchitekturmuster, die in Martin Fowlers Buch „Patterns of Enterprise Application Architecture" beschrieben werden.

Integrationsmuster sind wichtig für das Entwerfen und Kommunizieren von Konzepten rund um die gemeinsame Nutzung von Informationen und Funktionalität zwischen Komponenten, Anwendungen und Subsystemen. Einige Beispiele für Integrationsmuster sind Dateifreigabe, Remoteprozeduraufrufe und zahlreiche Nachrichtenmuster. Diese Muster sind zu finden unter [http://www.enterpriseintegrationpatterns.com/eaipatterns.html.](http://www.enterpriseintegrationpatterns.com/eaipatterns.html.)

Die grundlegenden Designmuster zu kennen, wie sie im Buch der Gang of Four „Design Patterns: Elements of Reusable Object-Oriented Software" beschrieben werden, ist für jeden Software-Architekten ein Muss. Obwohl diese Muster für einen Software-Architekten zu niedrig angesiedelt erscheinen mögen, sind sie Teil eines Standardvokabulars, das eine effektive Kommunikation zwischen Architekten und Entwicklern ermöglicht.

Es ist auch wichtig, die verschiedenen Anti-Patterns zu kennen und zu verstehen. Anti-Patterns, ein von Andrew Koenig geprägter Begriff, sind wiederholbare Prozesse, die ineffektive Ergebnisse produzieren. Zu den bekannteren Anti-Patterns gehören Analysis Paralysis, Design By Committee, Mushroom Management und Death March. Diese Muster zu kennen wird dir helfen, die vielen Fallstricke zu vermeiden, auf die du höchstwahrscheinlich stoßen wirst. Eine Liste der gängigen Anti-Patterns findest du unter [http://en.wikipedia.org/wiki/Anti-patterns.](http://en.wikipedia.org/wiki/Anti-patterns.)

Software-Architekten brauchen die Fähigkeit, effektiv, klar, prägnant und wirkungsvoll miteinander zu kommunizieren. Die Muster sind vorhanden; es liegt an uns als Software-Architekten, diese Muster zu erlernen und zu verstehen, damit wir „den Worten Taten folgen lassen können".

Von Mark Richards


## 43. Heterogenität gewinnt

Die natürliche Evolution der Computertechnologie hat wichtige Veränderungen hinsichtlich der Werkzeuge gebracht, die Architekten zum Aufbau von Softwaresystemen verwenden können. Diese Veränderungen haben ein erneuertes Interesse an polyglotter Programmierung hervorgerufen, was sich auf die Verwendung von mehr als einer Kernsprache bei der Bereitstellung eines Softwaresystems bezieht.

Polyglotte Programmierung ist kein neues Konzept: Ein prominentes Beispiel aus der Vergangenheit sind Visual-Basic-Clients, die durch COM-Objekte unterstützt werden, die in C++ auf dem Back-End erstellt wurden. Im Wesentlichen nutzte diese Architektur, worin diese Sprachen zu ihrer Hochzeit gut waren.

Was hat sich also verändert, um dieses erneuerte Interesse an polyglotter Programmierung zu befeuern?

Die Veränderung besteht darin, dass technische Standards zusammen mit ständig wachsender Bandbreite und Rechenressourcen zusammenkamen, um textbasierte Protokolle praktikabel zu machen: Vorbei sind die Zeiten der kryptischen Binärprotokolle als Voraussetzung für effiziente verteilte Systeme. Textbasierte Remote-Interoperabilität begann größtenteils mit XML/SOAP-basierten Webservices und entwickelt sich weiter mit RESTful-Architekturstilen und anderen unterstützenden (aber nicht weniger wichtigen) Protokollen wie Atom und XMPP.

Diese neue Art von Technologien schafft weitaus breitere Möglichkeiten für heterogene Entwicklung als je zuvor, einfach weil die Nutzlast formatierter Text ist, der universell erzeugt und verarbeitet wird. Heterogene Entwicklung ermöglicht die Verwendung des richtigen Werkzeugs für die Aufgabe, und textbasierte Interoperabilität hat die Türen zu dem aufgestoßen, was bisher möglich war.

Architekten können nun spezifische, leistungsstarke Werkzeuge kombinieren, die die Latte von der vorherigen Möglichkeit, die richtige Sprache einzusetzen, auf die nun mögliche Nutzung des richtigen Paradigmas verschieben. Programmiersprachen unterstützen verschiedene Paradigmen, wobei einige objektorientiert sind, während andere funktional sind oder sich durch gleichzeitige Programmierung auszeichnen. Einige dieser Paradigmen passen perfekt zu bestimmten Problemen oder Domänen, während andere schlecht geeignet sind. Heute ist es jedoch möglich, einige recht unkonventionelle und scheinbar dissonante Werkzeuge zu eleganten Lösungen zu kombinieren, viel einfacher als in der Vergangenheit.

Die Auswirkungen dieser Veränderung haben begonnen und manifestieren sich als kombinatorische Zunahme der Architekturtopologie moderner Softwaresysteme. Dies ist nicht nur ein Spiegelbild ihrer inhärenten Vielfalt, sondern ein Zeugnis neuer Möglichkeiten.

Während Auswahl nicht immer eine gute Sache ist, ist sie im Kontext moderner Software-Architektur „weniger schlimm" als die Alternative. Als Branche stehen wir vor sehr ernsthaften Problemen [1], und wir brauchen jede Interoperabilität, die wir bekommen können, insbesondere da die etablierten Plattformen nicht gut gerüstet sind, diese zu lösen [2].

Deine Aufgabe als Architekt ist noch herausfordernder geworden, weil technologische Silos angesichts neuer Möglichkeiten ins Wanken geraten: Begrüße dies, denke außerhalb des Stacks und nutze die neue Vielfalt: Heterogenität gewinnt.

[1] - Die bevorstehende Mehrkern-Ära könnte sich als das bislang bedeutendste Problem erweisen, dem die Softwareentwicklungsgemeinschaft gegenübersteht.
[2] - The Free Lunch Is Over – Herb Sutter, [http://www.gotw.ca/publications/concurrency-ddj.htm](http://www.gotw.ca/publications/concurrency-ddj.htm)

Von Edward Garson

## 44. Zwerge, Elfen, Zauberer und Könige

In Cryptonomicon erklärt Randy Waterhouse sein Klassifikationssystem für die verschiedenen Typen von Menschen, denen er begegnet. Zwerge sind Arbeiter, die stetig schöne Artefakte in der dunklen Einsamkeit ihrer Höhlen produzieren. Sie entfesseln gewaltige Kräfte, bewegen Berge und formen die Erde, und sind für ihr Handwerk bekannt. Elfen sind elegant, kultiviert und verbringen ihre Tage damit, neue und wunderschöne magische Dinge zu erschaffen. Sie sind so begabt, dass sie gar nicht bemerken, dass andere Rassen diese Dinge als geradezu übernatürlich wahrnehmen. Die Zauberer sind immens mächtige Wesen, die sich fast vollständig von allen anderen unterscheiden – doch im Gegensatz zu den Elfen wissen sie um die Magie, ihre Kraft und ihr Wesen, und setzen sie mit höchster Wirkung ein. Aber es gibt eine vierte Art von Charakter, auf die Waterhouse anspielt, ohne sie ausdrücklich zu nennen. Die Könige sind die Visionäre, die wissen, was mit all diesen verschiedenen Charakteren getan werden muss.

Ein Architekt ist gewissermaßen ein König. Der Architekt muss mit all diesen Charakteren vertraut sein und sicherstellen, dass die Architektur Rollen für all diese Charaktere bereithält. Eine Architektur, die nur für einen entworfen wurde, wird auch nur diesen einen Charakter zum Projekt anziehen – und selbst mit den besten Zwergen, Elfen oder Zauberern wird das Team in seiner Reichweite stark eingeschränkt sein, wenn es Probleme nur auf eine Art und Weise angehen kann.

Ein guter König führt alle Typen durch ein Abenteuer und hilft ihnen, zusammenzuarbeiten, um es zu vollenden. Ohne das Abenteuer gibt es keine Vision für das Team, und es wird letztendlich zu einem parteiischen Durcheinander. Ohne alle Charaktere kann das Team nur eine Klasse von Problemen lösen und scheitert an der ersten Hürde, die mit dieser Lösung nicht zu überwinden ist.

Der Architekt schafft das Abenteuer mit Blick auf alle Charaktere. Die Architektur wird dann zu einem Leitfaden, um Aufgaben für die verschiedenen Charaktere zu finden, während sie voneinander lernen. Wenn ein Projekt auf Schwierigkeiten stößt, weiß das Team bereits, wie es diese angehen soll, weil die Architektur ihnen die Möglichkeiten gegeben hat, zu einem Team heranzuwachsen.

Von Evan Cofsky


## 45. Von Architekten der Gebäude lernen

_„Architektur ist ein sozialer Akt und das materielle Theater menschlicher Aktivität."_ – Spiro Kostof

Wie viele Software-Architekten sehen ihre Rolle als ausschließlich oder vorrangig technisch? Sind sie nicht vielmehr die Vermittler, Mittelsleute und Schiedsrichter der streitenden Fraktionen unter den Stakeholdern? Wie viele gehen ihre Arbeit in einem rein intellektuellen Geist an, ohne den menschlichen Faktoren ihrer Tätigkeit angemessenes Gewicht beizumessen?

_„Ein großer Architekt wird nicht so sehr durch ein Gehirn geformt, sondern vielmehr durch ein kultiviertes, bereichtes Herz."_ – Frank Lloyd Wright

Was zeichnet die Architekten in deiner Organisation stärker aus: rohe intellektuelle Kapazität und ein enormes Gedächtnis für technische Details – oder Geschmack, Verfeinerung und Großzügigkeit des Geistes? Unter welcher Tendenz würdest du lieber arbeiten?

_„Ein Arzt kann seine Fehler begraben, aber ein Architekt kann seinem Klienten nur raten, Weinreben zu pflanzen."_ – ebenda

Ist die „Wartung" von „Legacy"-Systemen mehr als das Beschneiden dieser Weinreben? Hättest du als Architekt den Mut, ein Stück Arbeit aufzugeben, das gescheitert ist? Oder würdest du es verdecken? Wright sagte auch, dass der beste Freund des Architekten der Vorschlaghammer sei. Was hast du zuletzt abgerissen?

_„Architekten glauben nicht nur, dass sie zur Rechten Gottes sitzen, sondern dass sie den Stuhl übernehmen, wenn Gott aufsteht."_ – Karen Moyer

Für „Gott" lese „Kunde".

_„In der Architektur wie in allen anderen operativen Künsten muss das Ziel den Vorgang bestimmen. Das Ziel ist es, gut zu bauen. Gutes Bauen hat drei Bedingungen: Nützlichkeit, Festigkeit und Freude."_ – Henry Watton

Wann haben Sie zuletzt ein Stück Software gesehen, dessen Architektur Ihnen irgendeine Freude bereitet hat? Streben Sie danach, mit Ihrer Arbeit Freude zu bereiten?

„Niemand, der kein großer Bildhauer oder Maler ist, kann Architekt sein. Wenn er kein Bildhauer oder Maler ist, kann er nur ein Baumeister sein." – John Ruskin

Spielt Kunstfertigkeit in deiner Architektur die ihr gebührende Rolle? Ist das Zusammenfügen von Komponenten zu Systemen von einem malerischen Gespür für Form und Textur geprägt, mit einem skulpturalen Sinn für Balance und implizierte Bewegung, für die Bedeutung des negativen Raums?

Und schließlich bedarf dieser Kommentar keines Kommentars – er ist ein sicheres Heilmittel für das schädlichste Syndrom des Software-Architekten:

„Es erscheint als ein phantastisches Paradoxon, aber es ist dennoch eine äußerst wichtige Wahrheit, dass keine Architektur wirklich edel sein kann, die nicht unvollkommen ist." – ebenda

Von Keith Braithwaite


## 46. Wiederholung bekämpfen

Führen deine Entwickler wiederkehrende Aufgaben aus, die wenig Nachdenken erfordern? Findest du wiederkehrende Muster im Code? Erkennst du Code, der im Copy-Paste-Modify-Stil geschrieben wurde? Wenn das der Fall ist, arbeitet dein Team langsamer als nötig – und seltsamerweise könntest du selbst die Ursache sein.

Bevor ich erkläre warum, lass uns ein paar Wahrheiten über die Softwareentwicklung vereinbaren:

1) Duplikation ist das Böse.

2) Repetitive Arbeit verlangsamt die Entwicklung.

Als Architekt gibst du den Ton an. Du hast den besten Gesamtüberblick über das System und hast wahrscheinlich einen richtungsweisenden, end-to-end vertikalen Schnitt des Systems geschrieben, der als Beispiel für das Team dient – ein Beispiel, das inzwischen viele Male kopiert wurde. Wann immer ein Entwickler etwas kopiert – sei es ein paar Zeilen Code, eine XML-Datei oder eine Klasse – ist das ein klares Indiz dafür, dass etwas vereinfacht oder sogar vollständig abstrahiert werden könnte. Meist ist es nicht die Domänenlogik, die kopiert wird; es ist der Infrastruktur-Code, der einfach da sein muss, damit es funktioniert. Deshalb ist es entscheidend, dass du die Auswirkungen deiner Beispiele erkennen kannst. Jeder Code und jede Konfiguration in deinen Beispielen wird die Basis für Dutzende, Hunderte oder vielleicht Tausende anderer Schnitte des Systems sein. Das bedeutet, du musst sicherstellen, dass dein Code sauber, aussagekräftig ist und nichts enthält außer dem, was nicht abstrahiert werden kann – das Domänenproblem selbst. Als Architekt musst du sehr sensibel für jede Art von wiederkehrenden Mustern sein, da alles, was du schreibst, (ironischerweise) wiederholt werden wird.

Aber das passiert in deinem System nicht, oder? Schau dir die Konfigurationsdatei an. Was muss anders sein, wenn sie auf einen anderen Schnitt des Systems angewendet wird, und was bleibt gleich? Schau dir eine typische Business-Layer-Methode an. Gibt es ein Muster, das in anderen Methoden ebenfalls auftaucht und Dinge wie Transaktionsbehandlung, Logging, Authentifizierung oder Auditing enthält? Wie sieht es mit dem Data-Access-Layer aus? Gibt es dort Code, der abgesehen von den Namen der Entitäten und Felder gleich ist? Schau weiter. Findest du zwei oder drei Zeilen Code, die häufig zusammen vorkommen und die sich zwar auf verschiedene Objekte beziehen, sich aber wie dasselbe anfühlen? Das sind alles Beispiele für Wiederholung. Wiederholung im Code ist etwas, das Entwickler schließlich lernen auszublenden und beim Lesen des Codes zu ignorieren, sobald sie herausgefunden haben, wo die interessanten Variabilitäten liegen – aber selbst wenn die Entwickler sich daran gewöhnen, verlangsamt es sie. Solcher Code ist eindeutig für Computer geschrieben, die ihn ausführen sollen, nicht für Entwickler, die ihn lesen sollen.

Deine Verantwortung ist es, ihn zu beseitigen. Dazu musst du vielleicht Frameworks entwickeln, bessere Abstraktionen schaffen, vielleicht den Toolsmith bitten, ein Aspekt-Framework einzurichten oder ein paar kleine Code-Generatoren zu schreiben – aber die Wiederholung wird nicht verschwinden, wenn niemand etwas dagegen tut.

Dieser jemand bist du.

Von Niclas Nilsson


## 47. Willkommen in der realen Welt

Ingenieure lieben Präzision, besonders Software-Ingenieure, die in der Welt der Einsen und Nullen leben. Sie sind es gewohnt, mit binären Entscheidungen zu arbeiten: eins oder null, wahr oder falsch, ja oder nein. Alles ist klar und konsistent, garantiert durch Fremdschlüssel-Constraints, atomare Transaktionen und Prüfsummen.

Leider ist die reale Welt nicht ganz so binär. Kunden geben Bestellungen auf, nur um sie einen Moment später zu stornieren. Schecks platzen, Briefe gehen verloren, Zahlungen verzögern sich und Versprechen werden gebrochen. Dateneingabefehler passieren gelegentlich zwangsläufig. Benutzer bevorzugen „flache" Benutzeroberflächen, die ihnen Zugang zu vielen Funktionen auf einmal geben, ohne sie in einen langen, eindimensionalen „Prozess" zu sperren, der zwar einfacher zu programmieren ist und vielen Entwicklern „logischer" erscheint. Anstatt dass der Call-Stack den Programmfluss steuert, hat der Benutzer das Sagen.

Noch schlimmer: Weit verteilte Systeme bringen eine ganz neue Reihe von Inkonsistenzen ins Spiel. Dienste können nicht erreichbar sein, sich ohne Vorankündigung ändern oder keine transaktionalen Garantien bieten. Wenn du Anwendungen auf Tausenden von Maschinen betreibst, ist ein Ausfall keine Frage des „Ob", sondern des „Wann". Diese Systeme sind lose gekoppelt, asynchron, nebenläufig und halten sich nicht an traditionelle Transaktionssemantiken. Du hättest die blaue Pille nehmen sollen!

Da die schöne neue Welt der Informatiker gerade zusammenbricht – was tun wir? Wie so oft ist Bewusstsein ein erster wichtiger Schritt zur Lösung. Verabschiede dich von der guten alten vorhersehbaren Call-Stack-Architektur, bei der du bestimmen kannst, was wann und in welcher Reihenfolge geschieht. Sei stattdessen bereit, jederzeit auf Ereignisse in beliebiger Reihenfolge zu reagieren und deinen Kontext bei Bedarf wiederherzustellen. Stelle asynchrone Anfragen gleichzeitig, anstatt Methoden nacheinander aufzurufen. Vermeide vollständiges Chaos, indem du deine Anwendung mithilfe von ereignisgesteuerten Prozessketten oder Zustandsmodellen modellierst. Gleiche Fehler durch Kompensation, Wiederholung oder vorläufige Operationen aus.

Klingt das beängstigend und nach mehr, als du erwartet hast? Zum Glück hatte die reale Welt schon lange mit denselben Problemen zu kämpfen: verzögerte Briefe, gebrochene Versprechen, sich kreuzende Nachrichten, Zahlungen, die auf das falsche Konto gebucht wurden – die Beispiele sind zahllos. Entsprechend mussten die Menschen Briefe erneut senden, schlechte Bestellungen abschreiben oder dir mitteilen, die Zahlungserinnerung zu ignorieren, falls du bereits eine Zahlung gesendet hast. Mache also nicht nur die reale Welt für deine Kopfschmerzen verantwortlich, sondern nutze sie auch als Ort, um nach Lösungen zu suchen. Schließlich verwendet auch Starbucks kein Two-Phase-Commit [1]. Willkommen in der realen Welt.

[1] [http://www.eaipatterns.com/ramblings/18_starbucks.html](http://www.eaipatterns.com/ramblings/18_starbucks.html)


## 48. Nicht kontrollieren, sondern beobachten

Heutige Systeme sind verteilt und lose gekoppelt. Den Aufbau lose gekoppelter Systeme empfindet man als mühsam – warum tun wir uns das also an? Weil wir wollen, dass unsere Systeme flexibel sind und bei kleinsten Änderungen nicht auseinanderfallen. Das ist eine entscheidende Eigenschaft in heutigen Umgebungen, in denen wir möglicherweise nur einen kleinen Teil unserer Anwendung kontrollieren, während der Rest in verteilten Diensten oder Drittanbieter-Paketen lebt, die von anderen Abteilungen oder externen Lieferanten kontrolliert werden.

Es scheint also eine gute Idee zu sein, den Aufwand zu betreiben, ein System zu bauen, das flexibel ist und sich im Laufe der Zeit weiterentwickeln kann. Aber das bedeutet auch, dass sich unser System mit der Zeit verändert. Im Sinne von: „Das System von heute ist nicht mehr das von gestern." Leider macht das die Dokumentation des Systems zu einer Herausforderung. Es ist allgemein bekannt, dass Dokumentation in dem Moment veraltet ist, in dem sie gedruckt wird – aber in einem System, das sich ständig verändert, kann es nur schlimmer werden. Darüber hinaus bedeutet der Aufbau eines flexiblen Systems in der Regel, dass die Architektur komplexer ist und es schwieriger ist, das sprichwörtliche „Gesamtbild" zu erfassen. Wenn beispielsweise alle Systemkomponenten über logische, konfigurierbare Kanäle miteinander kommunizieren, sollte man besser einen Blick auf die Kanalkonfiguration werfen, um überhaupt eine Vorstellung davon zu bekommen, was vor sich geht. Nachrichten ins logische Nirgendwo zu senden wird wahrscheinlich keinen Compiler-Fehler auslösen, wird aber sicher den Benutzer enttäuschen, dessen Aktion in dieser Nachricht verkapselt war.

Ein kontrollbesessener Architekt zu sein ist von gestern und führt zu eng gekoppelten und brüchigen Lösungen. Aber die Software unkontrolliert laufen zu lassen, bringt mit Sicherheit Chaos hervor. Du musst den Mangel an Kontrolle durch andere Mechanismen ausgleichen, um keinen Instrumentenflug ohne Instrumente zu machen. Aber welche Instrumente stehen uns zur Verfügung? Jede Menge, tatsächlich. Heutige Programmiersprachen unterstützen Reflexion, und fast alle Laufzeitplattformen liefern Laufzeitmetriken. Da dein System konfigurierbarer wird, ist die aktuelle Systemkonfiguration eine weitere großartige Informationsquelle.

Da so viele Rohdaten schwer zu verstehen sind, extrahiere daraus ein Modell. Sobald du zum Beispiel herausgefunden hast, welche Komponenten Nachrichten an welche logischen Kanäle senden und welche Komponenten auf diese Kanäle hören, kannst du ein Graphenmodell der tatsächlichen Kommunikation zwischen den Komponenten erstellen. Das kannst du alle paar Minuten oder Stunden tun und damit ein genaues und aktuelles Bild des Systems liefern, wie es sich entwickelt. Denke daran als „Reverse MDA [1]": Anstatt dass ein Modell die Architektur vorantreibt, baust du eine flexible Architektur und extrahierst das Modell aus dem tatsächlichen Systemzustand.

In vielen Fällen ist es einfach, dieses Modell zu visualisieren und das buchstäbliche Gesamtbild zu erstellen. Widerstehe jedoch der Versuchung, das 3 mal 5 Meter große Plakat mit Kästchen und Linien zu zeichnen, das jede Klasse in deinem System enthält. Dieses Bild mag als zeitgenössische Kunst durchgehen, ist aber kein nützliches Softwaremodell. Verwende stattdessen eine 1000-Fuß-Ansicht, wie von Erik Doernenburg beschrieben – eine Abstraktionsebene, die dir tatsächlich etwas sagt. Darüber hinaus kannst du sicherstellen, dass dein Modell grundlegende Validierungsregeln besteht, wie z. B. das Fehlen von Kreisabhängigkeiten in einem Abhängigkeitsgraphen oder keine Nachrichten, die an einen logischen Kanal gesendet werden, dem niemand zuhört.

Die Kontrolle loszulassen ist erschreckend, selbst wenn es um Systemarchitektur geht. Aber ergänzt durch Beobachtung, Modellextraktion und Validierung ist es wahrscheinlich der einzige Weg, für das 21. Jahrhundert zu architekturieren.

[1] MDA = Model Driven Architecture


## 49. Janus, der Architekt

In der römischen Welt war Janus der Gott der Anfänge und Enden, der Türen und Durchgänge. Janus wird üblicherweise mit zwei Köpfen dargestellt, die in verschiedene Richtungen schauen – ein Symbol, das man vielleicht auf Münzen oder aus Filmen kennt. Janus steht für Übergänge und Veränderungen im Leben, von Vergangenheit zu Zukunft, von Jung zu Alt, Heirat, Geburten und das Erwachsenwerden.

Für jeden Architekten – ob Software oder Bauwerk – ist die Fähigkeit des Janus, vorwärts und rückwärts, von Vergangenheit zu Zukunft zu sehen, eine hoch geschätzte Eigenschaft. Ein Architekt strebt danach, Realitäten mit Visionen zu verbinden; vergangene Erfolge mit zukünftigen Richtungen; Erwartungen von Geschäft und Management mit Entwicklungsbeschränkungen. Diese Brücken zu schaffen ist ein wesentlicher Teil des Architekten-Daseins. Oft fühlt sich ein Architekt so, als müsse er Abgründe überbrücken, um ein Projekt zum Abschluss zu bringen, weil verschiedene Kräfte auf ein Projekt einwirken. Zum Beispiel: einfacher Zugang versus Sicherheit, oder die Befriedigung aktueller Geschäftsprozesse bei gleichzeitigem Design für die zukünftige Vision des Managements. Ein guter Architekt muss diese zwei Köpfe haben, die in der Lage sind, zwei verschiedene Ideen oder Gedanken, unterschiedliche Ziele oder Visionen zu tragen, um ein Produkt zu schaffen, das die verschiedenen Projekt-Stakeholder zufriedenstellt.

Man sollte beachten, dass Janus zwei Köpfe hat, nicht nur zwei Gesichter. Das ermöglicht Janus, die zusätzlichen Ohren und Augen für das Bewusstsein zu haben. Ein exzellenter IT-Architekt wird ein überragender Zuhörer und Bewerter sein. Den Grund für eine Kapitalausgabe zu verstehen ist entscheidend für die Bestimmung der Ziele und Visionen, die ein Managementteam für die Zukunft seiner Organisation hat. Die Fähigkeit, die technischen Fähigkeiten des Personals im Verhältnis zum Design und der Technologie zu bewerten, die im Projekt eingesetzt werden sollen, hilft dabei, die richtigen Trainings- und Programmierpaare zu schaffen, um ein erfolgreiches Projekt zu gewährleisten. Zu wissen, welche Open-Source-Lösungen in Kombination mit handelsüblicher Software eingesetzt werden sollten, kann die Zeitpläne und Budgets eines Projekts erheblich straffen. Ein exzellenter Architekt wird sich vieler dieser disparaten Teile des Entwicklungsprozesses bewusst sein und sie nutzen, um im Projektlebenszyklus erfolgreich zu sein.

Es gibt Manager, die gott-ähnliche Qualitäten von ihren Architekten fordern und erwarten, aber das ist nicht der Zweck dieses Vergleichs. Ein guter Architekt ist offen für neue Ideen, Werkzeuge und Designs, die das Projekt, das Team oder den Berufsstand voranbringen; sie möchte nicht die meiste Zeit in Management-Meetings verbringen oder die ganze Programmierung übernehmen; er sollte guten Ideen nachgeben und eine Atmosphäre pflegen, in der Ideen wachsen können. Es ist ein offener Geist, der als Architekt erfolgreich sein wird; ein Geist, der die vielen widersprüchlichen Kräfte in Projekten ausbalancieren kann. Alle Architekten streben danach, ihre Projekte abzuschließen und den Erfolg ihrer Entwicklungsteams zu sichern. Die besten Architekten schaffen Systeme, die den Test der Zeit bestehen, weil diese Systeme gewartet und in die Zukunft hinein erweitert werden können, wenn die Organisation wächst und sich die Technologie verändert. Diese Architekten haben zugehört, bewertet und ihre Prozesse, Designs und Methoden überarbeitet, um den Erfolg ihrer Arbeit und Projekte zu gewährleisten; sie haben sich bemüht, sicherzustellen, dass ihre Produkte den sicheren Übergängen und Veränderungen standhalten werden.

Das ist die Denkweise, nach der wir als Architekten streben sollten. Sie ist einfach und doch schwer umzusetzen. Wie Janus muss ein Software-Architekt ein Hüter von Türen und Durchgängen sein, der das Alte und das Neue überbrückt, Kreativität mit solider Ingenieursarbeit verbindet, um die heutigen Anforderungen zu erfüllen und gleichzeitig die Erwartungen von morgen zu planen.

Von Dave Bartlett


## 50. Der Fokus des Architekten liegt auf Grenzen und Schnittstellen

Seit Lord Nelson 1805 bei Trafalgar die französische und spanische Flotte vernichtete, ist „Teile und herrsche" das Mantra für den Umgang mit komplexen und schwierigen Problemen. Ein vertrauterer Begriff mit derselben Absicht ist die Trennung von Belangen (Separation of Concern). Aus der Trennung von Belangen ergibt sich Kapselung, und aus der Kapselung ergeben sich Grenzen und Schnittstellen.

Aus der Sicht eines Architekten liegt die schwierige Aufgabe darin, die natürlichen Stellen zu finden, an denen Grenzen platziert werden sollen, und die geeigneten Schnittstellen zu definieren, die zum Aufbau eines funktionierenden Systems benötigt werden. Das ist besonders schwierig bei großen Unternehmenssystemen, die oft durch wenige natürliche Grenzen und verflochtene Domänen gekennzeichnet sind. In dieser Situation geben alte Weisheiten wie: Kopplung minimieren, Kohäsion maximieren und Keine Schnitte durch Bereiche mit hohem Informationsaustausch vornehmen eine gewisse Orientierung, sagen aber nichts darüber aus, wie man die Probleme und möglichen Lösungen auf einfache Weise den Stakeholdern kommuniziert.

Hier kommen das Konzept der Bounded Contexts und das Context Mapping zu Hilfe, wie von Eric Evans in seinem Buch „Domain-Driven Design" beschrieben. Ein Bounded Context ist ein Bereich, in dem ein Modell oder ein Konzept eindeutig definiert ist. Wir stellen ihn als Wolke oder Blase mit einem beschreibenden Namen dar, der seine Rolle und Verantwortung in der jeweiligen Domäne definiert. Als Beispiel könnte ein Versandsystem Kontexte enthalten wie: Frachtbetrieb, Frachtplanung und Hafenbewegung. In anderen Domänen werden andere Bezeichnungen angemessen sein.

Nachdem die Bounded Contexts identifiziert und auf dem Whiteboard eingezeichnet sind, ist es an der Zeit, die Beziehungen zwischen den Kontexten zu zeichnen. Diese Beziehungen können organisatorische, funktionale oder technische Abhängigkeiten adressieren. Das Ergebnis dieser Übung ist eine Context Map: eine Sammlung von Bounded Contexts und den Schnittstellen zwischen ihnen.

Eine solche Context Map bietet Architekten ein mächtiges Werkzeug, das es ihnen ermöglicht, sich darauf zu konzentrieren, was zusammengehört und was getrennt bleiben sollte – und ermöglicht es ihnen, klug und kommunikativ zu teilen und zu herrschen. Die Technik lässt sich leicht einsetzen, um die Ist-Situation zu dokumentieren und zu analysieren, und von dort aus das Redesign in Richtung eines besseren Systems mit geringer Kopplung, hoher Kohäsion und klar definierten Schnittstellen zu leiten.

Von Einar Landre


## 51. Annahmen hinterfragen – besonders die eigenen

Wetherns Gesetz des aufgeschobenen Urteils besagt (auf etwas augenzwinkernde Weise), dass „Annahme die Mutter aller Fehlschläge ist." Eine populärere Version wäre: „Nehme nichts an – es macht aus dir einen Esel." Aber wenn es um Annahmen geht, die Tausende, wenn nicht Millionen von Dollar kosten könnten, ist das nicht immer zum Lachen.

Bewährte Praktiken in der Software-Architektur besagen, dass man die Begründung hinter jeder Entscheidung dokumentieren sollte, insbesondere wenn diese Entscheidung einen Kompromiss beinhaltet (Leistung vs. Wartbarkeit, Kosten vs. Time-to-Market usw.). Bei formaleren Ansätzen ist es üblich, zusammen mit jeder Entscheidung den Kontext dieser Entscheidung zu erfassen, einschließlich der „Faktoren", die zum endgültigen Urteil beigetragen haben. Faktoren können funktionale oder nicht-funktionale Anforderungen sein, aber sie können auch einfach „Fakten" (oder Faktoid-Gerüchte...) sein, die die Entscheidungsträger für wichtig hielten (Technologiebeschränkungen, verfügbare Fähigkeiten, das politische Umfeld usw.).

Diese Praxis ist wertvoll, weil sie durch das Auflisten dieser Faktoren dabei hilft, Annahmen der Architekten hervorzuheben, die wichtige Entscheidungen bezüglich der zu entwerfenden Software beeinflussen. Sehr oft basieren diese Annahmen auf „historischen Gründen", Meinungen, Entwickler-Folklore, FUDs oder sogar „etwas, das ich auf dem Flur gehört habe":

```
„Open Source ist nicht zuverlässig"
„Bitmap-Indizes machen mehr Probleme als sie wert sind"
„Der Kunde würde NIEMALS eine Seite akzeptieren, die 5 Sekunden zum Laden braucht"
„Der CIO würde alles ablehnen, das nicht von einem großen Anbieter verkauft wird"
```

Es ist wichtig, diese Annahmen für die Nachwelt und für zukünftige Neubewertungen sichtbar und explizit zu machen. Noch wichtiger ist es jedoch sicherzustellen, dass alle Annahmen, die nicht auf relevanten empirischen Belegen (oder einer Bestätigung der betroffenen Personen bei politischen Faktoren) basieren, vor der Finalisierung einer Entscheidung validiert werden. Was, wenn Kunden 5 Sekunden auf kritische Berichte warten können, wenn du einen Fortschrittsanzeiger bereitstellst? Auf welche genau Art ist welches Open-Source-Projekt genau unzuverlässig? Hast du die Bitmap-Indizes auf deinen Daten getestet, mit den Transaktionen und Abfragen deiner Anwendung?

Und übersehe nicht das Wort „relevant". Etwas, das in einer älteren Version deiner Software wahr war, muss heute nicht mehr wahr sein. Die Leistung von Bitmap-Indizes in einer Version von Oracle ist möglicherweise nicht die gleiche wie in einer anderen. Eine ältere Version einer Bibliothek könnte Sicherheitslücken gehabt haben, die bereits behoben wurden. Dein alter zuverlässiger Software-Anbieter könnte finanziell auf dem letzten Loch pfeifen. Die Technologielandschaft ändert sich täglich, und Menschen auch. Wer weiß? Vielleicht ist dein CIO inzwischen heimlich ein Linux-Fan geworden.

Fakten und Annahmen sind die Pfeiler, auf denen deine Software aufgebaut wird. Was auch immer sie sind – stelle sicher, dass die Fundamente solide sind.

Von Timothy High


## 52. Begründungen dokumentieren

In der Softwareentwicklungsgemeinschaft wird viel über den Wert von Dokumentation diskutiert, insbesondere in Bezug auf das Design der Software selbst. Die Meinungsverschiedenheiten drehen sich im Allgemeinen um den wahrgenommenen Wert eines „großen Vorab-Designs" und die Schwierigkeiten, Design-Dokumentation synchron mit einer sich ständig ändernden Codebasis zu halten.

Eine Art von Dokumentation, die gut altert, nicht viel Aufwand erfordert und sich fast immer auszahlt, ist eine Aufzeichnung der Begründungen hinter Entscheidungen, die die Software-Architektur betreffen. Wie im Axiom „Architektonische Kompromisse" erläutert, geht es bei der Definition einer Software-Architektur darum, die richtigen Kompromisse zwischen verschiedenen Qualitätsattributen, Kosten, Zeit und anderen Faktoren zu wählen. Es sollte für dich, deine Manager, Entwickler und andere Software-Stakeholder klar sein, warum eine Lösung gegenüber einer anderen gewählt wurde und welche Kompromisse das mit sich brachte (hast du die horizontale Skalierbarkeit im Namen der Reduzierung von Hardware- und Lizenzkosten geopfert? War Sicherheit so ein wichtiges Anliegen, dass es akzeptabel war, die Gesamtantwortzeit gegen Datenverschlüsselung einzutauschen?).

Das genaue Format dieser Dokumentation kann je nach dem, was für dein Projekt geeignet ist, variieren – von schnellen Notizen in einem Textdokument, Wiki oder Blog bis hin zur Verwendung einer formelleren Vorlage zur Erfassung aller Aspekte jeder Architekturentscheidung. Unabhängig von Form und Format sollte die Dokumentation die grundlegenden Fragen beantworten: „Was war die Entscheidung, die wir getroffen haben?" und „Warum haben wir diese Entscheidung getroffen?" Eine häufig gestellte Zusatzfrage, die ebenfalls dokumentiert werden sollte, ist: „Welche anderen Lösungen wurden in Betracht gezogen, und warum wurden sie abgelehnt?" (Die eigentlich gestellte Frage ist meist: „Warum können wir es nicht AUF MEINE Art machen?") Die Dokumentation sollte auch durchsuchbar sein, damit du sie bei Bedarf leicht finden kannst.

Diese Dokumentation kann in einer Reihe von Situationen nützlich sein:

```
Als Kommunikationsmittel an Entwickler bezüglich wichtiger architektonischer Prinzipien, die befolgt werden sollten
Um das Team „auf denselben Nenner zu bringen" oder sogar eine Meuterei abzuwenden, wenn Entwickler die Logik hinter der Architektur in Frage stellen (oder auch um demütig Kritik anzunehmen, wenn sich herausstellt, dass eine Entscheidung der Überprüfung nicht standhält)
Um Managern und Stakeholdern genau zu zeigen, warum die Software so gebaut wird, wie sie es wird (zum Beispiel warum ein teures Hardware- oder Software-Stück notwendig ist)
Bei der Übergabe des Projekts an einen neuen Architekten (wie oft hast du eine Software geerbt und dich gewundert, warum die Designer es GENAU SO gemacht haben?)
```

Die wichtigsten Vorteile dieser Praxis sind jedoch:

```
Sie zwingt dich, deine Überlegungen explizit zu machen, um zu überprüfen, ob deine Grundlagen solide sind (siehe das Axiom „Annahmen hinterfragen – besonders die eigenen")
Sie kann als Ausgangspunkt für die Neubewertung einer Entscheidung verwendet werden, wenn sich die Bedingungen, die die endgültige Entscheidung beeinflusst haben, verändert haben
```

Der Aufwand für die Erstellung dieser Dokumentation entspricht dem Aufschreiben einiger Notizen, wann immer du ein Meeting oder eine Diskussion zu dem Thema hast. Was auch immer das Format, das du wählst: Das ist eine Art von Dokumentation, die die Investition wert ist.

Von Timothy High


## 53. Entwickler befähigen

Dinge sind meistens leichter gesagt als getan, und Software-Architekten sind berüchtigt dafür, Dinge zu sagen. Damit deine Worte nicht zu heißer Luft werden (im Allgemeinen die wichtigste Zutat bei der Herstellung von Vaporware), brauchst du ein gutes Team von Entwicklern, um es zu verwirklichen. Die Rolle eines Architekten besteht in der Regel darin, Einschränkungen aufzuerlegen, aber du hast auch die Möglichkeit, ein Ermöglicher zu sein. Soweit deine Verantwortlichkeiten es erlauben, solltest du alles tun, um deine Entwickler zu befähigen.

Stelle sicher, dass Entwickler die Werkzeuge haben, die sie brauchen. Werkzeuge sollten nicht den Entwicklern aufgezwungen werden, sondern sorgfältig ausgewählt werden, um sicherzustellen, dass sie die richtigen Werkzeuge für die jeweilige Aufgabe sind. Repetitive und gedankenlose Arbeit sollte wo immer möglich automatisiert werden. Es lohnt sich auch, dafür zu sorgen, dass Entwickler erstklassige Maschinen haben, ausreichende Netzwerkbandbreite und Zugang zu Software, Daten und Informationen, die für ihre Arbeit notwendig sind.

Stelle sicher, dass sie die Fähigkeiten haben, die sie brauchen. Wenn Training erforderlich ist, stelle sicher, dass sie es bekommen. Investiere in Bücher und fördere aktive Diskussionen über Technologie. Das Arbeitsleben eines Entwicklers sollte praktisch und anwendungsorientiert sein, aber auch aktiv akademisch. Wenn du das Budget dafür hast, schicke dein Team zu technischen Präsentationen und Konferenzen. Wenn nicht, binde sie in technische Mailinglisten ein und suche nach kostenlosen Veranstaltungen in deiner Stadt. Beteilige dich so weit wie möglich auch am Entwicklerauswahlprozess. Suche nach Entwicklern, die wissensdurstig sind, die diesen kleinen „Funken" haben, der zeigt, dass sie wirklich Technik lieben (stelle auch sicher, dass sie gut im Team spielen können...). Es ist schwer, einen großen Knall aus einem Team von Null-Bock-Typen herauszuholen.

Lass Entwickler ihre eigenen Entscheidungen treffen, wo immer es nicht dem Gesamtziel des Software-Designs widerspricht. Setze Einschränkungen dort, wo sie zählen – nicht nur um Qualität zu garantieren, sondern auch um Entwickler weiter zu befähigen. Erstelle Standards um der Konsistenz willen, aber auch um die Anzahl der lästigen, unbedeutenden Entscheidungen zu reduzieren, die nicht Teil des wesentlichen Problems sind, das Entwickler lösen. Erstelle eine klare Roadmap, wo ihre Quelldateien abgelegt werden sollen, wie sie benannt werden sollen, wann neue erstellt werden sollen, und so weiter. Das wird ihnen Zeit sparen.

Schütze Entwickler schließlich vor unwesentlichen Teilen ihrer Arbeit. Zu viel Papierkram und zu viele Büropflichten erhöhen den Overhead und verringern ihre Effektivität. Du bist (normalerweise) kein Manager, aber du kannst Einfluss auf die Prozesse rund um die Softwareentwicklung haben. Welche Prozesse auch immer verwendet werden – stelle sicher, dass sie darauf ausgelegt sind, Hindernisse zu beseitigen, nicht zu erhöhen.

Von Timothy High


## 5## 54. Es dreht sich alles um die Daten

Als Software-Entwickler verstehen wir Software zunächst als ein System von Befehlen, Funktionen und Algorithmen. Diese instruktionsorientierte Sichtweise auf Software hilft uns dabei zu lernen, wie man Software baut, aber genau diese Perspektive beginnt uns zu behindern, wenn wir versuchen, größere Systeme zu bauen.

Wenn man einen Schritt zurücktritt, ist ein Computer nichts weiter als ein ausgefeiltes Werkzeug, das uns hilft, auf Datenhaufen zuzugreifen und diese zu manipulieren. Es ist die Struktur dieser Daten, die im Kern des Verständnisses liegt, wie man Komplexität in einem riesigen System bewältigt. Millionen von Anweisungen sind an sich schon kompliziert, aber darunter können wir uns leicht eine kleinere Menge grundlegender Datenstrukturen vorstellen.

Wenn du zum Beispiel das UNIX-Betriebssystem verstehen möchtest, hilft es wahrscheinlich nicht, den Quellcode Zeile für Zeile durchzugehen. Wenn du jedoch ein Buch liest, das die primären internen Datenstrukturen für Dinge wie Prozesse und das Dateisystem beschreibt, hast du eine bessere Chance zu verstehen, wie UNIX im Kern funktioniert. Die Daten sind konzeptionell kleiner als der Code und erheblich weniger kompliziert.

Während Code in einem Computer läuft, verändert sich der zugrundeliegende Zustand der Daten ständig. In einem abstrakten Sinne können wir jeden Algorithmus als eine einfache Transformation von einer Version der Daten zu einer anderen betrachten. Wir können alle Funktionalität als eine größere Menge von klar definierten Transformationen sehen, die die Daten durch verschiedene Revisionen schieben.

Diese datenorientierte Perspektive – das System vollständig durch die Struktur seiner zugrundeliegenden Informationen zu betrachten – kann selbst das komplexeste System auf eine greifbare Sammlung von Details reduzieren. Eine Reduzierung der Komplexität, die notwendig ist, um zu verstehen, wie komplexe Systeme gebaut und betrieben werden.

Daten stehen im Kern der meisten Probleme. Geschäftsdomänen-Probleme schleichen sich über die Daten in den Code. Die meisten wichtigen Algorithmen sind beispielsweise oft gut verstanden – es ist die Struktur und die Beziehungen der Daten, die sich häufig ändern. Operative Probleme wie Upgrades sind auch erheblich schwieriger, wenn sie Daten betreffen. Das liegt daran, dass das Ändern von Code oder Verhalten kein großes Problem ist – er muss nur veröffentlicht werden –, aber die Überarbeitung von Datenstrukturen kann einen enormen Aufwand bei der Transformation der alten Version in eine neuere erfordern.

Und natürlich sind viele der Grundprobleme in der Software-Architektur wirklich Fragen der Daten. Erfasst das System die richtigen Daten zur richtigen Zeit, und wer soll sie sehen oder ändern können? Wenn die Daten vorhanden sind, wie ist ihre Qualität und wie schnell wachsen sie? Wenn nicht, was ist ihre Struktur, und woher kommen sie zuverlässig? In diesem Licht stellt sich, sobald die Daten im System sind, nur noch die Frage, ob es bereits eine Möglichkeit gibt, die spezifischen Daten anzuzeigen und/oder zu bearbeiten, oder ob das noch hinzugefügt werden muss.

Aus einer Design-Perspektive ist die kritische Frage für die meisten Systeme, die richtigen Daten zur richtigen Zeit ins System zu bekommen. Von dort aus ist das Anwenden verschiedener Transformationen auf die Daten eine Frage, sie verfügbar zu machen, die Funktionalität auszuführen und dann die Ergebnisse zu speichern. Die meisten Systeme müssen im Kern nicht besonders komplex sein, damit sie funktionieren – sie müssen einfach immer größere Datenhaufen aufbauen. Funktionalität ist das, was wir zuerst sehen, aber Daten bilden den Kern jedes Systems.

Von Paul W. Homer


## 55. Die Daten kontrollieren, nicht nur den Code

Quellcodeverwaltung und Continuous Integration sind ausgezeichnete Werkzeuge zur Verwaltung des Anwendungs-Build- und Deployment-Prozesses. Neben dem Quellcode sind Schema- und Datenänderungen oft ein wesentlicher Teil dieses Prozesses und verdienen daher ähnliche Kontrollmechanismen. Wenn dein Build- und Deployment-Prozess eine Liste aufwendiger Schritte für Datenupdates enthält, sei vorsichtig. Diese Listen sind die, bei denen man immer die Daumen drückt. Sie sehen etwa so aus:

1) Erstelle eine Liste der Skripte, die ausgeführt werden müssen, in der richtigen Reihenfolge

2) Skripte per E-Mail an eine spezielle Datenbankperson senden

3) Datenbankperson kopiert die Skripte an einen Ort, wo sie von einem Cron-Job ausgeführt werden

4) Ausführungsprotokoll des Skripts prüfen und hoffen, dass alle Skripte erfolgreich ausgeführt wurden, da du dir nicht sicher bist, was passiert, wenn du sie erneut ausführst

5) Validierungsskripte ausführen und die Daten stichprobenartig prüfen

6) Regressionstests der Anwendung und schauen, was zusammenbricht

7) Skripte schreiben, um fehlende Daten einzufügen und Zusammenbrüche zu beheben

8) Wiederholen

Gut, das mag eine leichte Übertreibung sein, aber es ist nicht weit hergeholt. Viele Projekte erfordern diese Art von akrobatischem Workflow für eine erfolgreiche Datenbankmigration. Aus irgendeinem Grund scheint der Datenteil des Migrationsplans bei der Architekturplanung leicht übersehen zu werden. Als Folge davon kann er zu einem brüchigen, manuellen Prozess werden, der nachträglich aufgepfropft wird.

Dieses komplexe Geflecht schafft viele Möglichkeiten für Prozessausfälle. Was die Sache noch schlimmer macht: Fehler, die durch Schema- und Datenänderungen verursacht werden, werden nicht immer von Unit-Tests im Rahmen des nächtlichen Build-Berichts abgefangen. Sie zeigen sich gerne lautstark und aufsehenerregend, unmittelbar nachdem ein Build migriert wurde. Datenbankprobleme sind in der Regel mühsam manuell rückgängig zu machen, und ihre Lösungen tendieren dazu, schwieriger zu validieren zu sein. Der Wert eines vollständig automatisierten Build-Prozesses, der in der Lage ist, die Datenbank in einen bekannten Zustand zurückzusetzen, wird nie deutlicher sein als wenn man ihn verwendet, um ein extrem sichtbares Problem zu beheben. Wenn du nicht die Möglichkeit hast, die Datenbank zu löschen und sie in einen Zustand wiederherzustellen, der mit einem bestimmten Build der Anwendung kompatibel ist, bist du denselben Arten von Problemen ausgesetzt, die du hättest, wenn du eine Code-Änderung nicht schnell rückgängig machen könntest.

Datenbankänderungen sollten keine Wellen in deinem Build-Zeit-Raum-Kontinuum schlagen. Du musst in der Lage sein, die gesamte Anwendung, einschließlich der Datenbank, als eine Einheit zu bauen. Mache Daten- und Schema-Management frühzeitig zu einem nahtlosen Teil deines automatisierten Build- und Testprozesses und füge einen „Rückgängig-Button" hinzu; es wird sich großartig auszahlen. Im besten Fall wird es Stunden schmerzhafter, hochgespannter Problemlösung nach einem Fehler spät in der Nacht ersparen. Im schlechtesten Fall wird es deinem Team die Fähigkeit geben, die Refaktorierung der Datenzugriffsschicht mit Zuversicht voranzutreiben.

Von Chad LaVigne


## 56. Die Architektur-Metaphern nicht überdehnen

Architekten mögen Metaphern. Sie bieten schöne, greifbare Handhaben für Themen, die oft abstrakt, komplex und sich ständig weiterentwickelnde Ziele sind. Ob bei der Kommunikation mit dem Rest des Teams oder beim Besprechen der Architektur mit dem Endbenutzer – es ist so verlockend, etwas Greifbares oder Physisches als Metapher für das zu finden, was man zu bauen versucht.

Das beginnt in der Regel gut, da sich eine gemeinsame Sprache entwickeln kann, bei der die Menschen das Gefühl haben, dass die Dinge in die richtige Richtung gehen. Die Metapher entwickelt und wächst im Laufe der Zeit, bis sie ein Eigenleben entwickelt. Die Menschen fühlen sich gut bei der Metapher – wir machen Fortschritte!

Was in der Regel passiert, ist, dass die Metapher für die Architektur nun gefährlich wird. Hier ist, wie sie sich gegen ihre Architekten-Schöpfer wenden kann:

```
Der Kunde aus der Geschäftsdomäne beginnt deine Metapher mehr zu mögen als dein vorgeschlagenes System, da jetzt von allen Beteiligten die optimistischste mögliche Interpretation angenommen wird und keine echten Einschränkungen aufgedeckt werden.
```
Beispiel: Wir bauen ein „Transportsystem wie ein Schiff, das zwischen einer Reihe von Docks fährt".

Du denkst an Containerschiffe, die den Pazifik überqueren. Ich dachte eigentlich an ein Ruderboot in einem Schwimmbad, möglicherweise mit nur einem Ruder.

```
Das Entwicklungsteam beginnt zu denken, dass die Metapher wichtiger ist als das eigentliche Geschäftsproblem. Du fängst an, merkwürdige Entscheidungen wegen einer Vorliebe für die Metapher zu rechtfertigen.
```
Beispiel: Wir haben gesagt, es ist wie ein Aktenschrank, also müssen wir es dem Benutzer natürlich alphabetisch anzeigen. Ich weiß, es ist ein Aktenschrank mit sechs Dimensionen und unendlicher Länge und einer eingebauten Uhr, aber wir haben jetzt das Symbol gemacht – also muss es ein Aktenschrank sein...

```
Das ausgelieferte System enthält Relikte von Namen alter, längst vergangener Metaphern; archäologische Zeugnisse von Konzepten, die längst umstrukturiert und übergegraben wurden.
```
Beispiel: Warum erstellt das Billing-Factory-Objekt einen Port-Channel für das Ruderboot-System? Sicherlich sollte es eine Pomegranate-View für den Hub-Bus zurückgeben? Was meinst du, dass du hier neu bist?

Also denke daran: Verliebe dich nicht in deine Systemmetapher – verwende sie nur zu explorativen Kommunikationszwecken und lass sie nicht gegen dich arbeiten.

Von David Ing


## 57. Auf Anwendungssupport und -wartung vorbereiten

Der Support und die Wartung einer Anwendung sollten niemals als Nachgedanke behandelt werden. Da über 80 % des Lebenszyklus einer Anwendung in der Wartung verbracht werden, solltest du bei deinem Design viel Aufmerksamkeit auf die Probleme von Support und Wartung legen. Vernachlässigst du das, wirst du mit Entsetzen zusehen, wie deine Anwendung aufhört, der Traum des Architekten zu sein, und zu einem abscheulichen Ungetüm wird, das einen schrecklichen Tod stirbt und für immer als Misserfolg in Erinnerung bleibt.

Wenn die meisten Architekten Anwendungen entwerfen, denken sie hauptsächlich an Entwickler, die IDEs und Debugger zur Verfügung haben. Wenn etwas schief geht, debuggen hochqualifizierte Software-Ingenieure das Problem und der Fehler wird entdeckt. Es ist leicht, so zu denken, weil die meisten Architekten den Großteil ihrer Karriere als Entwickler verbracht haben und nicht als Administratoren. Leider haben der Entwickler und der Support-Mitarbeiter unterschiedliche Qualifikationen, genau wie die Entwicklungs-/Testumgebung und die Produktionsumgebung unterschiedliche Zwecke haben.

Hier sind einige der Nachteile, mit denen ein Administrator konfrontiert ist:

* Ein Administrator kann eine Anfragenachricht nicht erneut senden, um das Problem zu reproduzieren. Wenn du in der Produktion bist, kannst du eine Finanztransaktion nicht erneut gegen die „Live"-Datenbank ausstellen, um zu sehen, was schief gelaufen ist.
* Sobald die Anwendung in der Produktion ist, kommt der Druck zur Fehlerbehebung von Kunden und Führungskräften, nicht vom Projektmanager und dem Testteam. Und ein wütender CEO kann wesentlich bedrohlicher sein.
* Sobald du in der Produktion bist, gibt es keinen Debugger.
* Sobald du in der Produktion bist, muss der Einsatz geplant und koordiniert werden. Du kannst eine Produktionsanwendung nicht für ein paar Minuten herunternehmen, um eine Fehlerbehebung zu testen.
* Das Protokollierungsniveau ist in der Entwicklungsumgebung viel höher als in der Produktion.

Einige Symptome dieses Versagens bei der Planung für den Support sind:
* Die meisten Probleme erfordern die Beteiligung eines Entwicklers.
* Die Beziehung zwischen dem Entwicklungsteam und dem Support-Team ist schlecht; die Entwickler halten das Support-Team für Idioten.
* Das Support-Team hasst die neue Anwendung.
* Der Architekt und die Entwicklungsteams verbringen viel Zeit in der Produktion.
* Die Anwendung wird oft neu gestartet, um Probleme zu lösen.
* Die Administratoren haben nie Zeit, das System ordentlich zu optimieren, weil sie ständig Feuer bekämpfen.

Um sicherzustellen, dass deine Anwendung erfolgreich ist, sobald sie aus den Händen der Entwickler ist, solltest du:
* verstehen, dass Entwicklung und Support unterschiedliche Qualifikationen erfordern;
* so früh wie möglich im Projekt einen Support-Lead hinzuziehen;
* den Support-Lead zu einem zentralen Teil des Teams machen;
* den Support-Lead an der Planung für den Anwendungssupport beteiligen.

Entwirf so, dass die Lernkurve für das Support-Personal minimal ist. Rückverfolgbarkeit, Auditing und Protokollierung sind entscheidend. Wenn die Administratoren zufrieden sind, sind alle zufrieden (besonders dein Chef).

Von Mncedisi Mawabo Kasper


## 58. Bereite dich darauf vor, zwei zu wählen

Manchmal kann das Akzeptieren einer Einschränkung oder das Aufgeben einer Eigenschaft zu einer besseren Architektur führen – einer, die einfacher und kostengünstiger zu bauen und zu betreiben ist. Wie Busse tendieren wünschenswerte Eigenschaften dazu, in Dreiergruppen aufzutreten, und der Versuch, ein System zu definieren und zu bauen, das alle drei unterstützt, kann zu einem System führen, das nichts besonders gut macht.

Ein bekanntes Beispiel ist Brewers Vermutung, auch bekannt als Konsistenz, Verfügbarkeit und Partitionierung (CAP), die besagt, dass es drei Eigenschaften gibt, die in einem verteilten System üblicherweise gewünscht werden – Konsistenz, Verfügbarkeit und Partitionstoleranz – und dass es unmöglich ist, alle drei zu erreichen. Der Versuch, alle drei zu haben, wird die Entwicklungskosten drastisch erhöhen und in der Regel die Komplexität steigern, ohne tatsächlich den gewünschten Effekt oder das Geschäftsziel zu erreichen. Wenn die Daten verfügbar und verteilt sein müssen, wird das Erreichen von Konsistenz zunehmend teurer und letztendlich unmöglich. Ebenso wird, wenn das System verteilt und konsistent sein muss, das Gewährleisten von Konsistenz zunächst zu Latenz- und Leistungsproblemen und schließlich zur Nichtverfügbarkeit führen, da das System nicht zugänglich gemacht werden kann, während es versucht, eine Einigung zu erzielen.

Oft werden eine oder mehrere Eigenschaften als unverletzlich betrachtet – Daten dürfen nicht dupliziert werden, alle Schreibvorgänge müssen transaktional sein, das System muss zu 100 % verfügbar sein, Aufrufe müssen asynchron sein, es darf keinen Single Point of Failure geben, alles muss erweiterbar sein und so weiter. Abgesehen davon, dass das naiv ist, hindert dich das Behandeln von Eigenschaften als religiöse Artefakte daran, über das eigentliche Problem nachzudenken. Wir beginnen über architektonische Abweichungen zu sprechen, anstatt über prinzipiengeleitetes Design, und wir verwechseln Dogmatismus mit guter Governance. Stattdessen sollten wir fragen: Warum müssen diese Eigenschaften gelten? Welchen Nutzen bringt das? Wann sind diese Eigenschaften wünschenswert? Wie können wir das System aufteilen, um ein besseres Ergebnis zu erzielen? Sei immer skeptisch, denn architektonisches Dogma tendiert dazu, die Auslieferung zu untergraben. Die Unvermeidlichkeit solcher Kompromisse ist eine der schwierigsten Dinge, die in der Softwareentwicklung akzeptiert werden müssen – nicht nur als Architekt, sondern auch als Entwickler und Stakeholder. Aber wir sollten sie schätzen, da es weit besser ist, als grenzenlose Wahlmöglichkeiten zu haben; und das Akzeptieren von Kompromissen führt oft zu einem kreativen und erfinderischen Ergebnis.

Von Bill de hÓra


## 59. Prinzipien, Axiome und Analogien Meinungen und Geschmack vorziehen

Bei der Erstellung deiner Architektur solltest du explizit Prinzipien, Axiome und Analogien als Leitfaden verwenden. Das gibt der Architektur eine Reihe von Vorteilen, die nicht vorhanden sind, wenn du einfach implizit auf deine Erfahrung, Meinungen und deinen Geschmack zurückgreifst.

Die Dokumentation deiner Architektur wird einfacher. Du kannst damit beginnen, die Prinzipien zu beschreiben, denen gefolgt wurde. Das ist wesentlich einfacher, als zu versuchen, deine Meinungen und Erfahrungen zu kommunizieren. Die Prinzipien werden dann einen praktischen Anknüpfungspunkt für diejenigen bieten, die mit dem Verständnis und der Implementierung der Architektur beauftragt sind. Es wird auch für nachfolgende oder unerfahrene Architekten, die mit der Architektur arbeiten müssen, von unschätzbarem Wert sein.

Eine Architektur mit klaren Prinzipien ist eine Architektur, die ihren Architekten davon befreit, alles zu überprüfen und überall präsent zu sein. Sie gibt Architekten größere Hebelwirkung und Einfluss. Du wirst kein allwissender Workaholic sein müssen, um sicherzustellen, dass andere konsistent:

```
die Architektur implementieren und anpassen können;
```
```
die Architektur auf verwandte Domänen erweitern können;
```
```
die Architektur mit neueren Technologien neu implementieren können;
```
```
die detaillierten Randfälle ausarbeiten können.
```

Meinungsverschiedenheiten über Ansichten und Geschmack werden unweigerlich zu politischen Auseinandersetzungen, bei denen Autorität eingesetzt wird, um zu gewinnen. Meinungsverschiedenheiten, bei denen die Grundprinzipien klar sind, bieten jedoch eine Möglichkeit für eine sachlichere Diskussion, ohne dass Fragen personalisiert werden. Das ermöglicht es auch, Meinungsverschiedenheiten zu lösen, ohne überhaupt auf den Architekten verweisen zu müssen.

Prinzipien und Axiome verleihen einer Architektur auch Konsistenz in ihrer gesamten Implementierung und über die Zeit hinweg. Konsistenz ist oft ein Problem, besonders in großen Systemen, die mehrere Technologien umfassen und viele Jahre existieren werden. Klare Architekturprinzipien ermöglichen es denjenigen, die mit einer bestimmten Technologie oder Komponente nicht vertraut sind, über die unbekannte Technologie nachzudenken und sie leichter zu verstehen.

Von Michael Harmer


## 60. Mit einem gehenden Skelett beginnen

Eine sehr nützliche Strategie zur Implementierung, Verifizierung und Weiterentwicklung einer Anwendungsarchitektur ist es, mit dem zu beginnen, was Alistair Cockburn ein „Walking Skeleton" nennt. Ein Walking Skeleton ist eine minimale End-to-End-Implementierung des Systems, die alle wichtigen Architekturkomponenten miteinander verbindet. Klein anzufangen, mit einem funktionierenden System, das alle Kommunikationspfade nutzt, gibt dir die Gewissheit, dass du in die richtige Richtung gehst.

Sobald das Skelett vorhanden ist, ist es Zeit, es einem Trainingsprogramm zu unterziehen. Fülle es mit Ganzkörper-Workouts. Das bedeutet: inkrementell implementieren und End-to-End-Funktionalität hinzufügen. Das Ziel ist es, das System am Laufen zu halten und dabei das Skelett wachsen zu lassen.

Änderungen an einer Architektur vorzunehmen ist umso schwieriger und teurer, je länger sie existiert und je größer sie wird. Wir wollen Fehler frühzeitig finden. Dieser Ansatz gibt uns einen kurzen Feedback-Zyklus, aus dem wir uns schneller anpassen und iterativ arbeiten können, um die priorisierten Laufzeit-Qualitätsattribute des Unternehmens zu erfüllen. Annahmen über die Architektur werden früher validiert. Die Architektur lässt sich leichter weiterentwickeln, weil Probleme in einem früheren Stadium gefunden werden, wenn weniger in ihre Implementierung investiert wurde.

Je größer das System, desto wichtiger ist es, diese Strategie zu verwenden. In einer kleinen Anwendung kann ein Entwickler eine Funktion relativ schnell von oben nach unten implementieren, aber das wird bei größeren Systemen unpraktisch. Es ist durchaus üblich, dass mehrere Entwickler in einem einzelnen Team oder sogar in mehreren, möglicherweise verteilten Teams an der End-to-End-Implementierung beteiligt sind. Folglich ist mehr Koordination notwendig. Und natürlich implementieren Entwickler in unterschiedlichem Tempo. Einige Entwickler können viel in kurzer Zeit erreichen, während andere viel Zeit damit verbringen können, sehr wenig umzusetzen. Schwierigere und zeitaufwändigere Aufgaben sollten früher im Projekt erledigt werden.

Beginne mit einem Walking Skeleton, halte es am Laufen und lass es inkrementell wachsen.

Von Clint Shank


## 61. Dein Wissen und deine Erfahrungen teilen

Aus all unseren Erfahrungen, sowohl aus Erfolgen als auch aus Misserfolgen, lernen wir sehr viel. In einer jungen Industrie wie der Softwareentwicklung ist die Verbreitung dieser Erfahrungen und dieses Wissens entscheidend für die Aufrechterhaltung des Fortschritts. Was jedes Team in seiner eigenen kleinen Ecke der Welt lernt, kann möglicherweise weltweit Einfluss haben.

Realistisch gesehen ist unsere grundlegende Wissensbasis für die Softwareentwicklung – also das Wissen, das absolut und theoretisch korrekt ist – im Vergleich zu dem, was für die erfolgreiche Entwicklung eines Projekts notwendig ist, gering. Als Ausgleich raten wir, verlassen uns auf intuitive Urteile oder wählen sogar zufällig. Dabei erzeugt jedes größere Entwicklungsprojekt empirische Belege dafür, was funktioniert und was nicht. Wir arbeiten uns schrittweise durch die Permutationen, die wir auf die gesamte Industrie anwenden wollen.

Auf individueller Ebene versuchen wir alle zu wachsen und zu verstehen, wie man immer größere Systeme baut. Der Verlauf unserer Karrieren wird uns vor immer größere Herausforderungen stellen, für die wir wollen, dass unsere vergangenen Erfahrungen uns als Leitfaden dienen. Dabei zu sein ist eine Sache, aber um das Meiste aus der Erfahrung herauszuholen, müssen wir sie oft rationalisieren. Der beste und einfachste Weg, das zu verarbeiten, ist der Versuch, es einer anderen Person zu erklären.

Der Akt des Diskutierens hilft immer, Schwächen aufzuzeigen. Man versteht etwas nicht wirklich, bis man es leicht erklären kann. Erst durch das Vorlegen unserer Erklärungen und das Diskutieren darüber festigen wir die Erfahrung in Wissen.

Ein weiterer Punkt ist, dass wir zwar spezifische Erfahrungen gemacht haben, die Schlussfolgerungen, die wir daraus ziehen, im Gesamtkontext möglicherweise nicht ganz korrekt sind. Wir waren vielleicht nicht so erfolgreich, wie wir dachten, oder nicht so klug, wie wir sein wollten. Natürlich ist es erschreckend, sein Wissen an der realen Welt zu testen, besonders wenn man herausfindet, dass etwas Liebgewonnenes ein Mythos ist, falsch ist oder nie wahr war; es ist schwer, Unrecht zu haben.

Letztendlich sind wir Menschen, also ist nicht alles in unseren Köpfen korrekt; nicht jeder Gedanke, den wir haben, ist vernünftig. Erst wenn wir unsere Fehler akzeptieren, öffnen wir die Möglichkeit zur Verbesserung. Die alte Weisheit, dass man mehr aus Misserfolgen lernt, gilt immer. Wenn unsere Ideen und Überzeugungen dem Test einer Debatte nicht standhalten, ist es besser, das jetzt herauszufinden, als später darauf aufzubauen.

Wir wollen wirklich unser Wissen und unsere Erfahrungen teilen, um den Fortschritt der Industrie zu fördern; wir erkennen auch, dass es uns selbst hilft, es zu verstehen und zu korrigieren. Angesichts des Zustands so vieler unserer Software ist es klar, dass es für uns wichtig ist, jede Gelegenheit zu nutzen, um die Dinge zu teilen, die wir wissen, was wir zu wissen glauben und was wir gesehen haben. Wenn wir denen um uns herum helfen, sich zu verbessern, werden sie uns helfen, unser volles Potenzial zu erreichen.

Von Paul W. Homer


## 62. Sicherstellen, dass das Einfache einfach bleibt

Software-Architekten lösen viele sehr schwierige Probleme, aber wir lösen auch einige relativ einfache. Was wir nicht wollen, ist eine komplizierte Lösung auf ein einfaches Problem anzuwenden. So offensichtlich dieser Rat auch klingt – er kann schwer zu befolgen sein. Menschen, die Software entwerfen, sind klug, wirklich klug. Die Falle „einfaches Problem – komplexe Lösung" kann leicht zuschnappen, weil wir unser Wissen gerne unter Beweis stellen. Wenn du feststellst, dass du eine Lösung entwirfst, die so klug ist, dass sie möglicherweise ein Eigenbewusstsein entwickeln könnte, halte inne und denke nach. Passt die Lösung zum Problem? Wenn die Antwort Nein ist, überdenke deine Designoptionen. Halte das Einfache einfach. Du wirst genug Gelegenheiten bekommen, dein Talent zu zeigen, wenn die schwierigen Probleme auftauchen – und das werden sie.

Das bedeutet nicht, dass wir keine eleganten Lösungen implementieren sollten. Es bedeutet, dass wenn wir damit beauftragt sind, ein System zu entwerfen, das nur den Verkauf eines einzigen Typs von SKU-basierten Widgets unterstützen muss, es wahrscheinlich eine schlechte Idee ist, für Hierarchien von dynamisch konfigurierbaren Produkten zu entwerfen.

Die Kosten einer komplizierten Lösung mögen gering erscheinen, aber die Chance ist groß, dass sie größer sind, als du ihnen zuschreibst. Over-Engineering auf der Architekturebene verursacht viele der gleichen Probleme wie auf der Entwicklungsebene, aber die negativen Auswirkungen tendieren dazu, verstärkt zu werden. Schlechte Entscheidungen auf der Designebene sind schwieriger zu implementieren, zu warten und vor allem rückgängig zu machen. Bevor du mit einer Architekturentscheidung vorangehst, die die Systemanforderungen übersteigt, frage dich, wie schwierig es wäre, sie wieder zu entfernen, sobald sie einmal eingebaut ist.

Die Kosten hören nicht bei der Implementierung und Wartung der betreffenden Lösung auf. Mehr Zeit als notwendig auf ein einfaches Problem zu verwenden, lässt weniger Zeit für die komplizierten Probleme. Plötzlich verursachen deine Architekturentscheidungen Scope Creep und fügen dem Projekt unnötige Risiken hinzu. Deine Zeit könnte viel effizienter damit verbracht werden, sicherzustellen, dass niemand anderes das tut.

Oft besteht ein starker Wunsch, Lösungen mit einem wahrgenommenen Nutzen oder implizierten Anforderungen zu rechtfertigen. Denke daran: Wenn du versuchst, zukünftige Anforderungen zu erraten, liegst du 50 % der Zeit falsch und 49 % der Zeit sehr, sehr falsch. Löse das heutige Problem heute. Bringe die Anwendung rechtzeitig heraus und warte auf Feedback, um echte Anforderungen zu generieren. Das einfache Design, das du erstellst, wird es viel einfacher machen, diese neuen Anforderungen zu integrieren, wenn sie eintreffen. Wenn du gegen die Wahrscheinlichkeit ankämpfst und deine implizierte Anforderung beim nächsten Release zu einer echten wird, hast du bereits eine Lösung im Sinn. Der Unterschied ist, dass du nun in der Lage sein wirst, dafür in der Schätzung eine angemessene Zeit zu reservieren, weil sie wirklich erforderlich ist. Bevor du es weißt, hast du den Ruf eines Teams, das gute Schätzungen macht und die Arbeit pünktlich erledigt.

Von Chad LaVigne


## 63. Wenn du es entwirfst, solltest du es auch programmieren können

Als Architekt ist es verlockend, aufwendige Designs und Abstraktionen zu erstellen, die das vorliegende Problem elegant lösen. Noch verlockender ist es, neue Technologien in das Projekt zu streuen. Am Ende des Tages muss jemand dein Design implementieren, und die architektonischen Kunststücke, die du die Entwickler ausführen lässt, haben Auswirkungen auf das Projekt.

Beim Entwerfen der Architektur für dein Projekt musst du ein Gespür für den Aufwand haben, der zur Implementierung jedes Elements deines Designs erforderlich ist – wenn du ein Element bereits früher entwickelt hast, wird es viel einfacher sein, den erforderlichen Aufwand zu schätzen.

Verwende kein Muster in deinem Design, das du noch nicht persönlich implementiert hast. Verlasse dich nicht auf ein Framework, gegen das du noch nicht programmiert hast. Verwende keinen Server, den du noch nicht konfiguriert hast. Wenn deine Architektur von Design-Elementen abhängt, die du noch nicht persönlich verwendet hast, gibt es eine Reihe von negativen Nebeneffekten:

1. Du wirst die Lernkurve nicht erlebt haben, der deine Entwickler begegnen werden. Wenn du nicht weißt, wie lange es dauert, eine neue Technologie zu erlernen, wirst du keine gute Schätzung der Implementierungszeit geben können.
2. Du wirst die Fallstricke nicht kennen, die du bei der Verwendung der Elemente vermeiden musst. Zwangsläufig werden die Dinge nicht so gut laufen wie die Demo, die der ausgebildete Experte für die Technologie gezeigt hat. Wenn du die Technologie noch nicht eingesetzt hast, wirst du überrascht sein, wenn das passiert.
3. Du wirst das Vertrauen deiner Entwickler verlieren. Wenn die Entwickler Fragen zum Design stellen und du keine fundierten Antworten geben kannst, werden sie schnell das Vertrauen in dich und dein Design verlieren.
4. Du wirst unnötige Risiken einführen. Diese Dinge nicht zu kennen kann ein großes Fragezeichen hinter wichtige Elemente der Lösung setzen. Niemand möchte ein Projekt mit großen, unnötigen Risiken beginnen.

Wie lernt man also neue Frameworks, Muster und Server-Plattformen? Nun, das ist an sich schon ein eigenes Axiom: Vor allem anderen ist ein Architekt ein Entwickler.

Von Mike Brown


## 64. Die ROI-Variable

Jede Entscheidung, die wir für unsere Projekte treffen, sei es technologie-, prozess- oder personenbezogen, kann als eine Form von Investition betrachtet werden. Investitionen sind mit Kosten verbunden, die monetär sein können oder auch nicht, und bringen die Erwartung mit sich, dass sie sich letztendlich auszahlen. Unsere Arbeitgeber entscheiden sich, uns Gehälter anzubieten, in der Hoffnung, dass diese Investition das Ergebnis ihres Unternehmens positiv beeinflusst. Wir entscheiden uns, einer bestimmten Entwicklungsmethodik zu folgen, in der Hoffnung, dass sie das Team produktiver macht. Wir entscheiden uns, einen Monat damit zu verbringen, die physische Architektur einer Anwendung neu zu gestalten, in der Überzeugung, dass es langfristig vorteilhaft sein wird.

Eine der Möglichkeiten, den Erfolg von Investitionen zu messen, ist die Rendite, auch bekannt als Return on Investment (ROI). Zum Beispiel: „Wir gehen davon aus, dass wir durch mehr Zeit beim Schreiben von Tests weniger Fehler in unserem nächsten Produktions-Release haben werden." Die Kosten der Investition ergeben sich in diesem Fall aus der Zeit, die für das Schreiben von Tests aufgewendet wird. Was wir gewinnen, ist die Zeit, die wir in Zukunft beim Beheben von Fehlern sparen, plus die zufriedenen Kunden, die eine besser funktionierende Software erleben. Nehmen wir an, dass derzeit 10 von 40 Arbeitsstunden pro Woche für die Behebung von Fehlern aufgewendet werden. Wir schätzen, dass wir durch die Widmung von 4 Stunden pro Woche für Tests die Zeit für die Fehlerbehebung auf 2 Stunden pro Woche reduzieren und effektiv 8 Stunden für etwas anderes freisetzen. Der erwartete ROI beträgt 200 %, entspricht den 8 Stunden, die wir bei der Fehlerbehebung einsparen, dividiert durch die 4 Stunden, die wir in Tests investieren.

Nicht alles muss sich direkt in Geldgewinnen niederschlagen, aber unsere Investitionen sollten zu einem Mehrwert führen. Wenn für das aktuelle Projekt die Time-to-Market für die Stakeholder entscheidend ist, bietet eine kugelsichere Architektur, die eine langwierige Vorab-Designphase erfordert, möglicherweise keinen so interessanten ROI wie ein schnelles Alpha-Release. Durch einen schnellen Live-Gang gewinnen wir die Fähigkeit, uns an Zielgruppenreaktionen anzupassen, die das entscheidende Element für die zukünftige Ausrichtung und den Erfolg des Projekts sein können. Hingegen kann unzureichende Planung die Kosten verursachen, die Anwendung bei Bedarf nicht einfach genug skalieren zu können. Der ROI jeder Option kann durch die Untersuchung ihrer Kosten und prognostizierten Gewinne ermittelt werden und kann als Grundlage für die Auswahl zwischen den verfügbaren Optionen dienen.

Betrachte Architekturentscheidungen als Investitionen und berücksichtige die damit verbundene Rendite – es ist ein nützlicher Ansatz, um herauszufinden, wie pragmatisch oder zweckmäßig jede Option auf dem Tisch ist.

Von George Malamidis
## 65. Dein System ist Legacy – Gestalte es entsprechend

Auch wenn dein System hochmodern ist und mit der neuesten Technologie entwickelt wurde, wird es für den Nächsten bereits Legacy sein. Damit musst du klarkommen! Die Natur heutiger Software bedeutet, dass Dinge schnell veralten. Wenn du erwartest, dass dein System in Produktion geht und überlebt, selbst nur für ein paar Monate, dann musst du akzeptieren, dass Wartungsentwickler Dinge reparieren müssen. Das bedeutet Folgendes:

Klarheit – Es sollte offensichtlich sein, welche Rolle Komponenten und Klassen spielen.

Testbarkeit – Ist dein System leicht zu verifizieren?

Korrektheit – Funktionieren die Dinge wie entworfen oder wie sie sollten? Eliminiere schnelle und unsaubere Fixes.

Nachverfolgbarkeit – Kann „Ernie der Notfall-Bugfixer", der den Code noch nie gesehen hat, in die Produktion einsteigen, einen Fehler diagnostizieren und einen Fix einbauen? Oder braucht er eine achtwöchige Einarbeitung?

Versuche, dir vorzustellen, dass ein anderes Team die Codebasis öffnet und herausfindet, was passiert. Das ist grundlegend für eine großartige Architektur. Sie muss nicht übermäßig vereinfacht oder bis ins letzte Detail dokumentiert sein – ein gutes Design dokumentiert sich in vielerlei Hinsicht selbst. Auch die Art und Weise, wie sich ein System in der Produktion verhält, kann das Design offenbaren. Zum Beispiel verhält sich eine ausufernde Architektur mit hässlichen Abhängigkeiten in der Produktion oft wie ein eingesperrtes Tier. Denke an (meist jüngere) Entwickler, die Fehler debuggen müssen.

Legacy ist in Software-Kreisen oft ein schlechtes Wort, aber in Wirklichkeit sollten alle Softwaresysteme dieses Etikett tragen. Es ist keine schlechte Sache, da es darauf hinweisen kann, dass dein System dauerhaft ist, die Erwartungen erfüllt und einen Geschäftswert hat. Jedes Softwaresystem, das nie als Legacy bezeichnet wurde, wurde wahrscheinlich vor dem Launch eingestellt – was kein Zeichen einer erfolgreichen Architektur ist.

*von Dave Anderson*


## 66. Wenn es nur eine Lösung gibt, hol dir eine zweite Meinung

Das hast du wahrscheinlich schon einmal gehört. Wenn du ein erfahrener Architekt bist, weißt du, dass es stimmt: Wenn du nur an eine Lösung für ein Problem denken kannst, bist du in Schwierigkeiten.

Software-Architektur dreht sich darum, die bestmögliche Lösung für ein Problem unter Berücksichtigung einer beliebigen Anzahl von Einschränkungen zu finden. Es ist selten möglich, alle Anforderungen und Einschränkungen mit der ersten Lösung zu erfüllen, die einem in den Sinn kommt. Im Allgemeinen müssen Kompromisse eingegangen werden, indem man die Lösung wählt, die die Anforderungen gemäß den wichtigsten Prioritäten am besten erfüllt.

Wenn du nur eine Lösung für das vorliegende Problem hast, hast du keinen Spielraum, um diese Kompromisse auszuhandeln. Es ist sehr gut möglich, dass diese eine Lösung für die Stakeholder deines Systems unbefriedigend ist. Es bedeutet auch, dass dein System möglicherweise keinen Raum hat, sich an neue Anforderungen anzupassen, wenn sich die Prioritäten aufgrund eines sich verändernden Geschäftsumfelds verschieben.

Diese Situation wird selten durch einen echten Mangel an Optionen verursacht. Viel wahrscheinlicher liegt sie an der Unerfahrenheit des Architekten in diesem speziellen Problembereich. Wenn du weißt, dass das der Fall ist, tu dir selbst einen Gefallen und bitte jemanden mit mehr Erfahrung, dir zu helfen.

Eine noch heimtückischere Ausprägung dieses Problems tritt auf, wenn eine Architektur aus Gewohnheit entworfen wird. Ein Architekt kann mit einem einzigen Architekturstil erfahren sein (z. B. einem 3-Schichten-Client-Server-System), aber nicht genug wissen, um zu erkennen, wann dieser Stil nicht passt. Wenn du dich in einer Situation befindest, in der du die Lösung automatisch KENNST, ohne irgendeinen Vergleich mit anderen Ansätzen angestellt zu haben, halte inne, tritt einen Schritt zurück und frag dich, ob du dir einen anderen Weg vorstellen kannst. Wenn du das nicht kannst, brauchst du vielleicht etwas Hilfe.

Ein Freund von mir war einmal die technisch verantwortliche Person in einem kleinen, aber wachsenden Internet-Startup. Als ihre Nutzerbasis zu wachsen begann, wuchsen auch die Lastanforderungen an ihr System. Die Leistung ging den Bach runter, und sie begannen, einige ihrer hart erkämpften Nutzer zu verlieren.

Also fragte der Chef ihn: „Was können wir tun, um die Leistung zu verbessern?"

Mein Freund hatte die Antwort: „Kauf eine größere Maschine!"

„Was können wir sonst noch tun?"

„Ähm... soweit ich weiß, das war's."

Mein Freund wurde auf der Stelle gefeuert. Natürlich hatte der Chef Recht.

*von Timothy High*


## 67. Verstehe die Auswirkungen von Veränderungen

Ein guter Architekt reduziert die Komplexität auf ein Minimum und kann eine Lösung entwerfen, deren Abstraktionen solide Grundlagen bieten, auf denen man aufbauen kann, die aber pragmatisch genug sind, um Veränderungen standzuhalten.

Der großartige Architekt versteht die Auswirkungen von Veränderungen – nicht nur in isolierten Softwaremodulen, sondern auch zwischen Menschen und zwischen Systemen.

Veränderungen können sich in verschiedenen Formen manifestieren:

```
Funktionale Anforderungen ändern sich
Skalierbarkeitsanforderungen entwickeln sich weiter
Systemschnittstellen werden modifiziert
Teammitglieder kommen und gehen
und die Liste geht weiter...
```

Die Breite und Komplexität von Veränderungen in einem Softwareprojekt ist im Voraus unmöglich zu erfassen, und es ist eine fruchtlose Aufgabe, jede potenzielle Unebenheit vor ihrem Auftreten zu berücksichtigen. Aber der Architekt kann eine entscheidende Rolle dabei spielen, ob die Unebenheiten auf dem Weg ein Projekt machen oder brechen.

Die Rolle des Architekten besteht nicht unbedingt darin, Veränderungen zu managen, sondern sicherzustellen, dass Veränderungen handhabbar sind.

Nimm zum Beispiel eine stark verteilte Lösung, die viele Anwendungen umfasst und auf eine Vielzahl von Middleware angewiesen ist, um die Teile zusammenzukleben. Eine Änderung in einem Geschäftsprozess kann Chaos verursachen, wenn die Abhängigkeiten nicht korrekt verfolgt oder in einem visuellen Modell präzise dargestellt werden. Die Auswirkungen auf nachgelagerte Systeme sind besonders erheblich, wenn die Änderung das Datenmodell betrifft, bestehende Schnittstellen bricht und die vorhandenen lang laufenden, zustandsbehafteten Transaktionen erfolgreich unter der alten Version des Prozesses abgeschlossen werden müssen.

Dieses Beispiel mag extrem erscheinen, aber hochintegrierte Lösungen sind heute Mainstream. Das zeigt sich in der Auswahl an verfügbaren Integrationsstandards, Frameworks und Mustern. Die Auswirkungen von Veränderungen in diesen weitreichenden Systemen zu verstehen ist entscheidend, um ein nachhaltiges Niveau der Unterstützung für deine Kunden zu gewährleisten.

Glücklicherweise gibt es viele Werkzeuge und Techniken, um die Auswirkungen von Veränderungen zu mildern:

```
Kleine, schrittweise Änderungen vornehmen
Wiederholbare Testfälle erstellen – sie häufig ausführen
Das Erstellen von Testfällen einfacher machen
Abhängigkeiten verfolgen
Systematisch handeln und reagieren
Wiederkehrende Aufgaben automatisieren
```

Der Architekt muss das Risiko von Veränderungen auf verschiedene Aspekte des Umfangs, der Zeit und des Budgets des Projekts abschätzen und bereit sein, mehr Zeit in jene Bereiche zu investieren, deren Auswirkungen bei einem „Hindernis auf dem Weg" am größten wären. Das Messen von Risiken ist ein nützliches Werkzeug, um zu wissen, wo deine wertvolle Zeit am besten eingesetzt werden sollte.

Komplexität zu reduzieren ist wichtig, aber reduzierte Komplexität ist nicht gleichbedeutend mit Einfachheit. Die Auszahlung dafür, die Art und Auswirkungen von Veränderungen auf deine Lösungen zu verstehen, ist mittel- bis langfristig unermesslich.

*von Doug Crawford*


## 68. Du musst auch Hardware verstehen

Für viele Software-Architekten ist die Hardware-Kapazitätsplanung ein Thema, das außerhalb ihrer Komfortzone liegt, und dennoch bleibt es ein wichtiger Teil der Arbeit eines Architekten. Es gibt eine Reihe von Gründen, warum Software-Architekten Hardware-Überlegungen oft nicht ausreichend berücksichtigen, aber sie hängen meistens mit mangelndem Verständnis und unklaren Anforderungen zusammen.

Der Hauptgrund, warum wir Hardware-Überlegungen vernachlässigen, ist, dass wir uns auf Software konzentrieren und dazu neigen, Hardware-Anforderungen zu ignorieren. Darüber hinaus sind wir durch hochrangige Sprachen und Software-Frameworks natürlich von der Hardware isoliert.

Unklare Anforderungen sind ebenfalls ein Faktor, da sie sich ändern oder schlecht verstanden werden können. Da sich die Architektur weiterentwickelt, werden sich auch die Hardware-Überlegungen ändern. Darüber hinaus verstehen oder können unsere Kunden die Größe ihrer eigenen Nutzerbasis oder die Systemnutzungsdynamik möglicherweise nicht vorhersagen. Schließlich entwickelt sich Hardware ständig weiter. Was wir in der Vergangenheit über Hardware wussten, gilt heute nicht mehr.

Ohne Hardware-Fachkenntnisse ist das Vorhersagen von Hardware-Konfigurationen für zu entwickelnde Systeme sehr fehleranfällig. Um dies zu kompensieren, verwenden einige Software-Architekten große Sicherheitsfaktoren. Solche Sicherheitsfaktoren basieren im Allgemeinen nicht auf objektiven Bewertungen oder einer fundierten Methodik. In den meisten Fällen führt dies zu übermäßigen Infrastrukturkapazitäten, die selbst in Zeiten von Spitzennachfrage nicht genutzt werden. Als Ergebnis wird das Geld der Kunden für mehr Hardware ausgegeben, als ein System jemals brauchen wird.

Die beste Absicherung gegen schlechte Hardware-Planung ist die enge Zusammenarbeit mit einem Infrastruktur-Architekten. Infrastruktur-Architekten sind – im Gegensatz zu Software-Architekten – Spezialisten für Hardware-Kapazitätsplanung und sollten Teil deines Teams sein. Allerdings hat nicht jeder Software-Architekt den Luxus, mit einem Infrastruktur-Architekten zusammenzuarbeiten. In solchen Fällen gibt es einige Dinge, die ein Software-Architekt tun kann, um Fehler bei der Hardware-Planung zu verringern.

Das Nutzen eigener Erfahrungen aus der Vergangenheit kann helfen. Du hast in der Vergangenheit Systeme implementiert und hast daher einige Kenntnisse über Hardware-Kapazitätsplanung – auch wenn es damals ein nachträglicher Gedanke war. Du kannst das Thema auch mit deinem Kunden besprechen und ihn überzeugen, Mittel für die Hardware-Kapazitätsplanung beiseite zu legen. Das Budgetieren für Kapazitätsplanung kann weitaus kosteneffektiver sein als mehr Hardware zu kaufen als nötig. In diesem Fall ist horizontale Skalierbarkeit der Schlüssel – Hardware nach Bedarf hinzufügen, anstatt zu Beginn zu viel zu kaufen. Um eine horizontale Strategie umzusetzen, müssen Software-Architekten die Kapazität ständig messen und Software-Komponenten so isolieren, dass sie in leistungsvorhersehbaren Umgebungen ausgeführt werden.

Hardware-Kapazitätsplanung ist genauso wichtig wie Software-Architektur und muss als Priorität erster Ordnung behandelt werden, egal ob ein Infrastruktur-Architekt zur Hand ist oder nicht. Genau wie ein Architekt dafür verantwortlich ist, die Verbindungen zwischen Geschäftsanforderungen und einer Softwarelösung herzustellen, ist er verantwortlich, die Verbindungen zwischen Hardware und Software zu visualisieren.

*von Kamal Wickramanayake*


## 69. Abkürzungen von heute werden morgen mit Zinsen zurückgezahlt

Es ist wichtig, sich beim Entwurf eines Systems daran zu erinnern, dass die Wartung auf lange Sicht mehr Ressourcen verbrauchen wird als die ursprüngliche Entwicklung des Projekts. Abkürzungen, die während der anfänglichen Entwicklungsphase eines Projekts genommen werden, können später zu erheblichen Wartungskosten führen.

Zum Beispiel könntest du informiert worden sein, dass Unit-Tests keinen direkten Wert liefern, und sagst daher deinen Entwicklern, sie sollen die rigorose Anwendung davon überspringen. Das macht das gelieferte System viel schwieriger zu ändern in der Zukunft, und verringert das Vertrauen beim Vornehmen dieser Änderungen. Das System wird für eine kleinere Menge von Änderungen weitaus mehr manuelles Testen erfordern, was zu Brüchigkeit und erhöhten Wartungskosten führt, sowie zu einem Design, das nicht so angemessen ist wie ein vollständig getestetes Design (von einem Test-First-Design ganz zu schweigen).

Ein schwerwiegender Architekturfehler, der manchmal gemacht wird, ist die Anpassung eines bestehenden Systems für einen Zweck, für den es nicht geeignet ist, mit der Begründung, dass die Verwendung eines bestehenden Systems irgendwie die Kosten reduziert. Zum Beispiel könntest du dich dabei wiederfinden, BPEL-Architekturkomponenten in Verbindung mit Datenbank-Triggern zu verwenden, um ein asynchrones Messaging-System zu liefern. Das könnte aus Gründen der Bequemlichkeit oder weil das die Architektur ist, die dir oder dem Kunden bekannt ist, getan oder darauf bestanden werden. Aber eine Messaging-Architektur hätte von Anfang an ausgewählt werden sollen, nachdem die Anforderungen klar gemacht haben, dass sie eine notwendige Komponente ist. Schlechte Entscheidungen zu Beginn eines Projekts machen es wesentlich teurer, das System für neue Anforderungen neu zu gestalten.

Neben dem Vermeiden von Abkürzungen während der anfänglichen Entwicklungsphase ist es auch wichtig, schlechte Designentscheidungen so schnell wie möglich zu korrigieren, sobald sie entdeckt werden. Schlecht gestaltete Funktionen können zur Grundlage für zukünftige Funktionen werden, was korrigierende Maßnahmen später noch kostspieliger macht.

Wenn du beispielsweise entdeckst, dass unangemessene Bibliotheken für einige zugrunde liegende Funktionalitäten ausgewählt wurden, sollten sie so schnell wie möglich ersetzt werden. Andernfalls wird der Aufwand, sie an sich entwickelnde Anforderungen anzupassen, zusätzliche Abstraktionsschichten erzeugen, von denen jede dazu dient, die schlechte Passung der vorherigen Schicht zu verbergen. Du baust dir selbst einen Knäuel aus verwirrtem Garn, Heftzwecken und Klebeband, und mit jeder Schicht, die du hinzufügst, wird es schwieriger, ihn aufzulösen. Das führt leicht zu einem System, das sich Veränderungen widersetzt.

Als Architekt, wenn du auf ein Architekturproblem oder einen Designfehler stößt, bestehe darauf, dass es jetzt behoben wird, wenn es am günstigsten zu beheben ist. Je länger du es hinausziehst, desto höher wird die Zinszahlung.

*von Scot Mcphee*


## 70. „Perfekt" ist der Feind von „Gut genug"

Software-Designer, und insbesondere Architekten, neigen dazu, Lösungen danach zu bewerten, wie elegant und optimal sie für ein gegebenes Problem sind. Wie Juroren bei einem Schönheitswettbewerb sehen wir ein Design oder eine Implementierung und erkennen sofort kleine Mängel oder Warzen, die mit nur wenigen weiteren Änderungen oder Refactoring-Iterationen beseitigt werden könnten. Domänenmodelle betteln geradezu um einen weiteren Durchgang, um zu sehen, ob es gemeinsame Attribute oder Funktionen gibt, die in Basisklassen verschoben werden könnten. Dienste, die in mehreren Implementierungen dupliziert sind, schreien nach ihrer Notwendigkeit, Web-Services zu werden. Abfragen beschweren sich über „Buffer Gets" und nicht-eindeutige Indizes und fordern Aufmerksamkeit.

Mein Rat: Gib nicht der Versuchung nach, dein Design oder deine Implementierung perfekt zu machen! Strebe nach „gut genug" und höre auf, sobald du es erreicht hast.

Was genau ist „gut genug", fragst du? Gut genug bedeutet, dass die verbleibenden Unvollkommenheiten die Systemfunktionalität, Wartbarkeit oder Leistung in keiner bedeutsamen Weise beeinträchtigen. Die Architektur und das Design hängen zusammen. Die Implementierung funktioniert und erfüllt die Leistungsanforderungen. Der Code ist klar, prägnant und gut dokumentiert. Könnte er besser sein? Sicher, aber er ist gut genug, also hör auf. Erkläre dich zum Sieger und geh zur nächsten Aufgabe über.

Die Suche nach Perfektion in Design und Implementierung führt meiner Meinung nach zu überentwickelten und verschleierten Lösungen, die am Ende schwerer zu warten sind.

Eine Reihe der Axiome in diesem Buch mahnen Designer, unnötige Abstraktion oder Komplexität zu vermeiden. Warum haben wir Probleme, die Dinge einfach zu halten? Weil wir die perfekte Lösung suchen! Warum sonst würde ein Architekt Komplexität in eine funktionierende Lösung einführen, außer um eine wahrgenommene Unvollkommenheit im einfacheren Design zu beheben?

Denke daran, dass die Anwendungsentwicklung kein Schönheitswettbewerb ist, also hör auf, nach Fehlern zu suchen und Zeit mit der Jagd nach Perfektion zu verschwenden.

*von Greg Nyberg*


## 71. Vermeide „Gute Ideen"

Gute Ideen töten Projekte. Manchmal ist es ein schneller Tod, aber oft ist es ein langsamer, schleichender Tod, verursacht durch verpasste Meilensteine und eine spiralförmig anwachsende Bug-Anzahl.

Du kennst die Art von guten Ideen, über die ich spreche: Verlockende, selbstverständliche, harmlos aussehende, „könnte-nicht-schaden-es-auszuprobieren"-Ideen. Sie fallen gewöhnlich jemandem im Team etwa auf halbem Weg durch ein Projekt ein, wenn alles gut zu laufen scheint. Stories und Aufgaben werden in einem guten Tempo erledigt, erste Tests laufen gut, und das Rollout-Datum sieht solide aus. Das Leben ist schön.

Jemand hat eine „gute Idee", du gibst nach, und plötzlich baust du eine neue Version von Hibernate in dein Projekt ein, um die neuesten Funktionen zu nutzen, oder du implementierst AJAX in einigen deiner Webseiten, weil der Entwickler dem Benutzer gezeigt hat, wie cool das ist, oder du überarbeitest sogar das Datenbankdesign, um XML-Funktionen des RDBMS zu nutzen. Du sagst dem Projektmanager, dass du ein paar Wochen brauchst, um diese „gute Idee" zu implementieren, aber es beeinflusst am Ende mehr Code als ursprünglich erwartet, und dein Zeitplan beginnt zu rutschen. Außerdem hast du, indem du die erste „gute Idee" hereingelassen hast, sprichwörtlich die Nase des Kamels im Zelt, und bald kommen die guten Ideen aus allen Ecken und es wird schwieriger, nein zu sagen (und das Kamel schläft bald in deinem Bett).

Das wirklich Heimtückische an „guten Ideen" ist, dass sie „gut" sind. Jeder kann „schlechte" Ideen erkennen und von vornherein ablehnen – es sind die guten, die durchschlüpfen und Probleme mit Umfang, Komplexität und schlichtem verschwendetem Aufwand verursachen, indem etwas in die Anwendung integriert wird, das nicht notwendig ist, um den Geschäftsbedarf zu erfüllen.

Hier sind einige Schlüsselphrasen, auf die du achten solltest:

```
„Wäre es nicht cool, wenn ..." – Wirklich, jeder Satz mit dem Wort „cool" darin ist ein Gefahrensignal.

„Hey, sie haben gerade Version XXX des YYY-Frameworks veröffentlicht. Wir sollten upgraden!"

„Weißt du, wir sollten wirklich XXX refaktorieren, solange wir an ZZZ arbeiten ..."

„Diese XXX-Technologie ist wirklich mächtig! Vielleicht könnten wir sie für ... verwenden"

„Hey, <dein-name-hier>, ich habe über das Design nachgedacht und habe eine Idee!"
```

Okay, okay, vielleicht bin ich mit dem letzten etwas zu zynisch. Aber pass weiterhin auf „gute Ideen" auf, die dein Projekt töten können.

*von Greg Nyberg*


## 72. Großartige Inhalte schaffen großartige Systeme

Ich habe meinen gerechten Anteil an Initiativen gesehen, die sich endlos auf Anforderungen, Design, Entwicklung, Sicherheit und Wartung konzentrieren, aber nicht auf den eigentlichen Punkt des Systems – die Daten. Das gilt besonders für inhaltsbasierte Systeme, bei denen die Daten Informationen sind, die als unstrukturierter oder halbstrukturierter Inhalt geliefert werden. Großartige Inhalte machen den Unterschied zwischen einem hohlen System und einem, das relevant ist.

Inhalt ist König. Inhalt ist das Netzwerk. Inhalt ist die Schnittstelle. In einer zunehmend vernetzten Welt wird die Qualität der Inhalte schnell zum Unterschied zwischen Erfolg und Misserfolg. FaceBook vs. Orkut / Google vs. Cuil / NetFlix vs. BlockbusterOnline... die Liste ist endlos, wo Schlachten auf dem Schlachtfeld der Inhalte gewonnen und verloren wurden. Man könnte argumentieren, dass inhaltsrelevante Aspekte nicht das Problem des Software-Architekten sind – aber ich denke, das nächste Jahrzehnt wird das mit Sicherheit widerlegen.

Ein Teil des Designprozesses für ein neues System sollte der Bewertung des Inhaltsbestands gewidmet sein. Ein effektives Domänen-/Objekt-/Datenmodell zu entwerfen ist nicht genug.

Analysiere alle verfügbaren Inhalte und bewerte ihren Wert anhand der folgenden Kriterien:

- Gibt es genug Inhalte? Falls nicht, wie erreichen wir kritische Masse?
- Sind die Inhalte frisch genug? Falls nicht, wie verbessern wir die Lieferraten?
- Wurden alle möglichen Inhaltskanäle erkundet? RSS-Feeds, E-Mail, Papierformulare sind alles Kanäle.
- Gibt es effektive Eingangsströme, die die kontinuierliche Lieferung dieser Inhalte in das System ermöglichen? Es ist eine Sache, wertvolle Inhalte zu identifizieren, aber eine ganz andere, sie regelmäßig zu ernten.

Verwechsle das nicht: Der Erfolg eines Systems hängt von seinen Inhalten ab. Verwende einen gesunden Teil des Designprozesses darauf, den Wert deiner Inhalte zu bewerten. Wenn deine Ergebnisse unbefriedigend sind, ist das ein rotes Flag, und die Stakeholder müssen darüber informiert werden. Ich habe viele Systeme gesehen, die alle vertraglichen Verpflichtungen erfüllen, jede Anforderung erfüllen und dennoch scheitern, weil dieser ziemlich offensichtliche Aspekt ignoriert wurde. Großartige Inhalte schaffen großartige Systeme.

*von Zubin R. Wadia*


## 73. Das Unternehmen vs. der wütende Architekt

Es kommt in unserer Karriere als Architekt ein Zeitpunkt, an dem wir erkennen, dass viele der Probleme, auf die wir stoßen, wiederkehrend sind. Obwohl das Projekt und die Branche sich ändern mögen, sind viele der Probleme ähnlich. Zu diesem Zeitpunkt können wir auf unsere Erfahrung zurückgreifen, um viele Lösungen schnell bereitzustellen, was mehr Zeit lässt, die herausfordernden Probleme zu genießen. Wir sind zuversichtlich in unsere Lösungen und liefern wie versprochen. Wir haben Homöostase erreicht. Das ist der perfekte Zeitpunkt, einen kolossalen Fehler zu machen – wie zu entscheiden, dass man so viel weiß, dass es Zeit ist, mehr zu reden als zuzuhören. Diese schlechte Entscheidung kommt gewöhnlich mit einer Beilage von Zynismus, Ungeduld und allgemeiner Wut gegenüber minderwertigen Geistern, die es wagen, dein überlegenes Verständnis von allem Technischen und anderem zu widersprechen.

In seiner schlimmsten Form sickert dieses Übervertrauen in den Geschäftsbereich. Das ist ein ausgezeichneter Weg, deine Karriere auf einer Liste irgendwo neben dem Schwarzen Nashorn zu landen. Das Unternehmen ist unser Existenzgrund. Diese Aussage schmerzt vielleicht ein wenig, aber wir dürfen das nicht aus den Augen verlieren. Wir leben, um ihnen zu dienen, nicht umgekehrt. Dem Unternehmen, das uns zur Problemlösung engagiert, zuzuhören und es zu verstehen ist die kritischste Fähigkeit, die wir besitzen. Hast du dich jemals dabei erwischt, ungeduldig darauf zu warten, dass ein Business-Analyst aufhört zu reden, damit du deinen Punkt machen konntest? Wahrscheinlich hast du seinen nicht verstanden. Zeige den Fachexperten des Unternehmens den Respekt, den du selbst erwartest zu empfangen. Das ist die letzte Gruppe von Menschen, die du als unnahbar wahrnehmen lassen möchtest. Wenn sie beginnen, dich zu meiden, bist du ein Katalysator für Kommunikationsbrüche und sabotierst dein eigenes Projekt. Denke daran: Wenn du redest, kannst du nur etwas hören, das du bereits weißt. Fang nie an zu denken, du seist so klug, dass niemand anderes etwas Wertvolles zu sagen hätte.

Wenn wir zuhören, werden wir oft mit dem, was wir über den Geschäftsbetrieb hören, nicht einverstanden sein. Das ist in Ordnung. Wir können Verbesserungsvorschläge machen und sollten das definitiv tun. Wenn du jedoch am Ende des Tages nicht einverstanden bist, wie das Unternehmen geführt wird, und das sich nicht ändern wird, ist das einfach Pech. Erlaube dir nicht, ein unzufriedener Genius zu werden, der seine ganze Zeit damit verbringt, andere zu beeindrucken, indem er witzige, herablassende Aussagen darüber macht, wie schlecht das Unternehmen geführt wird. Sie werden nicht beeindruckt sein. Sie haben diesen Typen vorher getroffen und mögen ihn nicht wirklich. Eine der Schlüsselzutaten im Rezept für einen großartigen Architekten ist Leidenschaft für deine Arbeit, aber du willst nicht zu viel Leidenschaft der wütenden Sorte. Lerne, Meinungsverschiedenheiten zu akzeptieren und weiterzumachen. Wenn die Unterschiede zu groß sind und du dich ständig im Widerspruch zum Unternehmen befindest, finde ein Unternehmen, das leichter für dich zu unterstützen ist, und entwerfe Lösungen für dieses. Finde auf jeden Fall einen Weg, eine gute Beziehung zum Unternehmen aufzubauen, und lass deinen Ego sie nicht beschädigen. Das wird dich glücklicher und produktiver machen.

*von Chad LaVigne*


## 74. Dehne Schlüsseldimensionen, um zu sehen, was bricht

Das Design einer Anwendung wird zunächst auf der Grundlage der festgelegten Geschäftsanforderungen, ausgewählter oder bestehender Technologien, des Leistungsrahmens, der erwarteten Datenmengen und der verfügbaren finanziellen Ressourcen zum Bauen, Bereitstellen und Betreiben umrissen. Die Lösung, was immer sie ist, wird das erfüllen oder übertreffen, was in der zeitgenössischen Umgebung von ihr gefordert wird, und wird erwartet, erfolgreich zu laufen (oder sie ist noch keine Lösung).

Nimm nun diese Lösung und dehne die Schlüsseldimensionen, um zu sehen, was bricht.

Diese Untersuchung sucht nach Grenzen im Design, die auftreten werden, wenn beispielsweise das System wildly popular wird und mehr Kunden es nutzen, die verarbeiteten Produkte ihre Transaktionszahlen pro Tag erhöhen, oder sechs Monate lang Daten gespeichert werden müssen, statt der ursprünglich festgelegten Woche. Die Dimensionen werden einzeln und dann in Kombination gedehnt, um die unsichtbaren Grenzen aufzudecken, die im ursprünglichen Design verborgen liegen könnten.

Das Dehnen von Schlüsseldimensionen ermöglicht es einem Architekten, eine Lösung zu validieren durch:

```
Verständnis, ob die geplante Infrastruktur diese Zuwächse aufnehmen kann und wo die Grenzen liegen.
Wenn die Infrastruktur brechen wird, wird identifiziert, wo sie brechen wird, was dem Eigentümer der Anwendung hervorgehoben werden kann, oder die geplante Infrastruktur kann mit spezifischen Upgrade-Pfaden im Sinn erworben werden.
Bestätigung, dass genügend Stunden im Tag vorhanden sind, um die Verarbeitung bei erwartetem Durchsatz durchzuführen, mit Spielraum, um „geschäftige Tage" oder „Aufholen" nach einem Ausfall zu bewältigen. Eine Lösung, die die Verarbeitung eines Tages nicht an einem Tag bewältigen kann und sich auf das Wochenende verlässt, wenn es ruhiger ist, hat keine langfristige Zukunft.
Validierung, dass die getroffenen Datenzugriffsentscheidungen immer noch gültig sind, wenn das System skaliert. Was für die Haltung von Daten einer Woche funktionieren könnte, kann mit sechs Monaten geladener Daten unbrauchbar sein.
Bestätigung, wie die erhöhte Arbeitslast der Anwendung auf zusätzliche Hardware skaliert wird (falls erforderlich), und des Übergangswegs, wenn die Last zunimmt. Das Durcharbeiten des Übergangs, bevor die Anwendung bereitgestellt wird, kann die gespeicherten Daten und ihre Struktur beeinflussen.
Bestätigung, dass die Anwendung immer noch wiederhergestellt werden kann, wenn die Datenmengen zunehmen und/oder die Daten jetzt auf eine erhöhte Infrastruktur aufgeteilt sind.
```

Basierend auf dieser Untersuchung können Elemente des Designs als Probleme erkannt werden, die eine Neugestaltung erfordern. Die Neugestaltung wird günstiger sein, während das Design noch virtuell ist, technische Entscheidungen noch nicht festgelegt sind und die Geschäftsdaten noch nicht in den Repositorien gespeichert wurden.

*von Stephen Jones*


## 75. Vor allem ist ein Architekt ein Entwickler

Hast du schon einmal von einem Richter gehört, der kein Anwalt war, oder von einem Chefchirurgen, der kein Chirurg war? Auch nachdem sie das erreicht haben, was manche als den Gipfel ihrer Karriere bezeichnen würden, wird von den Inhabern dieser Berufe immer noch erwartet, dass sie weiterhin die neuen Entwicklungen in ihren jeweiligen Bereichen erlernen. Als Software-Architekten sollten wir an denselben Standards gemessen werden.

Egal wie gut eine Lösung entworfen ist, einer der wichtigsten Faktoren für den Erfolg einer Implementierung ist es, die Entwickler für den Spielplan zu gewinnen. Der schnellste Weg, die Entwickler für sich zu gewinnen, ist ihr Vertrauen und ihren Respekt zu gewinnen. Wir alle kennen den schnellsten Weg, das Vertrauen eines Entwicklers zu gewinnen: dein Code ist deine Währung. Wenn du deinen Entwicklern zeigen kannst, dass du nicht nur ein wolkenverlorener Tagträumer bist, der sich nicht aus einer Papiertüte herauscodieren kann, wirst du weniger Gemurre hören über die Reifen, durch die du sie „lässt" springen, um Daten auf der Seite anzuzeigen, wenn „ich es in weniger Zeit erledigen kann, indem ich einfach ein Dataset an ein Grid binde."

Obwohl ich es nicht als Teil meiner Arbeit muss, nehme ich häufig einige der komplizierteren Aufgaben auf mich. Das dient zwei Zwecken: Erstens macht es Spaß und hilft mir, meine Entwicklungsfähigkeiten scharf zu halten; zweitens hilft es mir, meinen Entwicklern zu demonstrieren, dass ich nicht nur heiße Luft produziere, wo die Sonne nicht scheint.

Als Architekt sollte dein primäres Ziel sein, eine Lösung zu schaffen, die machbar, wartbar und natürlich auf das vorliegende Problem ausgerichtet ist. Teil des Wissens, was in einer Lösung machbar ist, ist das Wissen um den Aufwand, der für die Entwicklung der Elemente der Lösung erforderlich ist. Daher schlage ich vor: Wenn du es entwirfst, solltest du es auch codieren können.

*von Mike Brown*


## 76. Eine Rose unter einem anderen Namen endet als Kohl

Ich hörte, wie einige Leute entschieden, dass sie mehr Schichten in ihrer Architektur brauchen. Sie hatten Recht, wie es sich herausstellte, aber sie gingen dabei etwas rückwärts vor. Sie versuchten, ein Framework zu erstellen, das die Geschäftslogik enthalten würde. Anstatt einige spezifische Probleme zu lösen, begannen sie mit der Idee, ein Framework zu wollen, das die Datenbank umhüllt und Objekte produziert. Und es sollte Object-Relational Mapping verwenden. Und Nachrichten. Und Web Services. Und es sollte alle möglichen coolen Sachen machen.

Leider, da sie nicht genau wussten, welche coolen Sachen es tun würde, wussten sie nicht, wie sie es nennen sollten. Also veranstalteten sie einen kleinen Wettbewerb, um einen Namen vorzuschlagen. Und das ist der Punkt, an dem du erkennen musst, dass du ein Problem hast: Wenn du nicht weißt, wie man eine Sache nennen soll, kannst du nicht wissen, was sie ist. Wenn du nicht weißt, was sie ist, kannst du dich nicht hinsetzen und den Code schreiben.

In diesem speziellen Fall enthüllte ein schneller Blick in die Quellcode-Verwaltungshistorie die Tiefe des Problems. Natürlich gab es viele leere Interface-„Implementierungen"! Und das wirklich Lustige ist, dass sie den Namen bereits dreimal geändert hatten, ohne tatsächlichen Code. Als sie anfingen, nannten sie es ClientAPI – wobei „Client" sich auf die Kunden des Unternehmens bezieht, nicht auf Client wie in „Client-Server" – und die endgültige Version wurde ClientBusinessObjects genannt. Großartiger Name: vage, breit und irreführend.

Natürlich ist ein Name am Ende nur ein Zeiger. Sobald jeder Beteiligte weiß, dass der Name nur ein Name ist und keine Design-Metapher, können alle weitermachen. Wenn du jedoch keinen Namen finden kannst, der spezifisch genug ist, dass du weißt, wann er falsch ist, könntest du Schwierigkeiten haben, überhaupt anzufangen. Design dreht sich alles darum, Absichten zu erfüllen – z. B. schnell, günstig, flexibel – und Namen vermitteln Absichten.

Wenn du es nicht benennen kannst, kannst du es nicht schreiben. Wenn du den Namen 3 Mal änderst, dann halte an, bis du weißt, was du zu bauen versuchst.

*von Sam Gardiner*


## 77. Stabile Probleme führen zu qualitativ hochwertigen Lösungen

Reales Programmieren dreht sich nicht darum, das Problem zu lösen, das jemand dir gibt. Im Informatik-Unterricht musst du das gegebene Binary-Sort-Problem lösen. In der realen Welt lösen die besten Architekten keine schwierigen Probleme – sie umgehen sie. Die Fähigkeit liegt darin, Grenzen um diffuse und vielfältige Software-Probleme zu ziehen, sodass sie stabil und in sich abgeschlossen sind.

Ein Architekt sollte in der Lage sein, eine ganze Menge von Konzepten, Daten und Prozessen zu betrachten und sie in kleinere Stücke oder „Brocken" zu trennen. Das Wichtige an diesen Problembrocken ist, dass sie stabil sind, was es ermöglicht, sie durch einen Systembrocken zu lösen, der endlich und stabil im Umfang ist. Die Problembrocken sollten sein:

* Intern kohäsiv: Der Brocken ist konzeptionell vereint, sodass alle Aufgaben, Daten und Funktionen miteinander verbunden sind.
* Gut von anderen Brocken getrennt: Die Brocken sind konzeptionell normalisiert; es gibt wenig oder keine Überschneidungen zwischen ihnen.

Die Person, die übermäßig gut darin ist, weiß vielleicht nicht einmal, dass sie es tut, genau wie eine Person mit einem guten Orientierungssinn weiß, wo sie sich befindet. Es scheint ihnen einfach sinnvoll zu sein, die Aufgaben, Daten und Funktionen auf eine Weise aufzuteilen, die eine schöne Kante oder Schnittstelle zum System bietet. Ich spreche nicht von den tatsächlichen Schnittstellen einer objektorientierten Sprache, sondern von Systemgrenzen.

Zum Beispiel hat ein relationales Datenbankverwaltungssystem eine sehr schöne Systemgrenze. Es verwaltet buchstäblich jeden Datentyp, der in einen Byte-Stream serialisiert werden kann, und es kann diese Daten organisieren, suchen und abrufen. Einfach.

Was interessant ist: Wenn das Problem stabil ist, dann ist es, wenn es einmal gelöst ist, dauerhaft gelöst. In fünf oder fünfzig Jahren möchtest du vielleicht eine Web- oder telepathische Schnittstelle darüber legen, aber dein Kernsystem muss sich nicht ändern. Das System ist dauerhaft, weil das Problem dauerhaft ist.

Natürlich muss der Code ziemlich sauber sein, aber wenn das Problem sauber ist, kann der Code sauber sein, da es keine Sonderfälle gibt. Und sauberer Code ist gut, weil er leicht zu testen und leicht zu überprüfen ist, was bedeutet, dass die Implementierungsqualität sehr hoch sein kann. Da du keinen unordentlichen Code hast, kannst du dich auf Dinge konzentrieren, die außerhalb des Bereichs der für den Benutzer sichtbaren Funktionen liegen, wie die Verwendung von zuverlässigem Messaging, verteilten Transaktionen oder das Steigern der Leistung durch Multithreading oder sogar Sprachen auf niedrigem Niveau wie Assembler; weil sich das Problem nicht ändert, kannst du dich darauf konzentrieren, die Qualität so weit zu steigern, dass Qualität ein Merkmal ist.

Ein stabiles Problem ermöglicht es dir, ein System mit einem stabilen Design zu erstellen; stabiles Design ermöglicht es dir, dich darauf zu konzentrieren, eine Anwendung zu erstellen, die sehr hohe Qualität aufweist.

*von Sam Gardiner*


## 78. Es erfordert Sorgfalt

Die Arbeit eines Architekten wird oft als eine Tätigkeit beschrieben, die sich auf Einfallsreichtum und Problemlösung konzentriert. Einfallsreichtum ist ein Schlüsselmerkmal erfolgreicher Architekten. Eine ebenso wichtige Charakterisierung der Aktivitäten eines erfolgreichen Architekten ist jedoch „Sorgfalt". Sorgfalt kann sich auf viele Weisen manifestieren, aber letztendlich ist es eine Übung in Ausdauer und darin, jedem Ziel die richtige Aufmerksamkeit zu widmen.

Sorgfalt geht Hand in Hand mit dem Alltäglichen. Erfolgreiche Architekturpraktiken sind in vielerlei Hinsicht alltäglich. Effektive Architekten folgen oft alltäglichen täglichen und wöchentlichen Checklisten, um sie an das zu erinnern, was sie bereits akademisch wissen, aber nicht aus Gewohnheit praktizieren. Ohne solche alltäglichen Checklisten und Erinnerungen können Architekten schnell in die Software-Zeit verfallen, in der kein messbarer Fortschritt erzielt wird, weil ein Mangel an Sorgfalt es der Architektur ermöglichte, zu mäandern und bekannte akademische Prinzipien zu verletzen. Es ist wichtig, in diesen Rückblicken auf gescheiterte Projekte zu erkennen, dass es in den meisten Fällen nicht Inkompetenz war, die das Scheitern antrieb, sondern vielmehr der Mangel an Sorgfalt und einem Gefühl der Dringlichkeit.

Sorgfalt erfordert auch, dass ein Architekt die scheinbar einfache Aufgabe meistert, Verpflichtungen einzugehen und einzuhalten. Diese Verpflichtungen sind oft unterschiedlich und können eine breite Palette von Einschränkungen und Erwartungen umfassen. Beispiele umfassen:

```
Die Budget- und Zeitvorgaben des Kunden einhalten
Alle Arbeit erledigen, die den Architekten effektiv macht, nicht nur die Arbeit, die der Architekt genießt.
Verpflichtung gegenüber dem Prozess/der Methodik
Verantwortung übernehmen
```

Atul Gawande, in seinem hervorragenden Buch „Better: A Surgeon's Notes on Performance", spricht von Sorgfalt in der Medizin:

„Echter Erfolg in der Medizin ist nicht einfach. Er erfordert Willen, Aufmerksamkeit für Details und Kreativität. Aber die Lektion, die ich aus Indien mitnahm, war, dass es überall und von jedem möglich ist. Ich kann mir kaum einen Ort mit schwierigeren Bedingungen vorstellen. Und doch konnte man erstaunlichen Erfolg finden... was ich sah, war: Besser ist möglich. Es erfordert kein Genie. Es erfordert Sorgfalt. Es erfordert moralische Klarheit. Es erfordert Einfallsreichtum. Und vor allem erfordert es die Bereitschaft, es zu versuchen."

*von Brian Hart*


## 79. Übernimm Verantwortung für deine Entscheidungen

Software-Architekten müssen Verantwortung für ihre Entscheidungen übernehmen, da sie in Software-Projekten weitaus mehr Einfluss haben als die meisten Menschen in Organisationen. Studien über Software-Projekte zeigen, dass über zwei Drittel von ihnen entweder direkt scheitern oder erfolglos abgeliefert werden (Fristverschiebung, Budgetüberschreitungen oder geringe Kundenzufriedenheit). Viele der Grundursachen weisen auf unangemessene Entscheidungen hin, die Software-Architekten getroffen haben, oder auf Versäumnisse, die richtigen Architekturentscheidungen durchzusetzen.

Wie kannst du ein verantwortungsvoller Software-Architekt werden, der effektive Architekturentscheidungen trifft?

Zunächst musst du dir deines Entscheidungsprozesses voll bewusst sein, ob er agil oder zeremoniell ist. Du solltest NICHT behaupten, dass eine Architekturentscheidung getroffen wurde, bis die folgenden zwei Bedingungen erfüllt sind:

* Eine Entscheidung wurde schriftlich festgehalten, weil Architekturentscheidungen selten trivial sind. Sie müssen substantiiert und nachverfolgbar sein.
* Eine Entscheidung wurde den Personen mitgeteilt, die sie ausführen, und den Personen, die direkt oder indirekt betroffen sein werden. Kommunikation dreht sich alles darum, gemeinsames Verständnis zu schaffen.

Zweitens überprüfe deine Architekturentscheidungen regelmäßig. Untersuche die Ergebnisse deiner Entscheidungen im Vergleich zu den Erwartungen. Identifiziere Architekturentscheidungen, die gültig bleiben, und solche, die es nicht tun.

Drittens setze deine Architekturentscheidungen durch. Viele Software-Projekte beziehen Software-Architekten nur in die Designphase ein, dann wechseln sie zu anderen Projekten oder der Beratungsvertrag endet. Wie können sie sicherstellen, dass ihre durchdachten Architekturentscheidungen korrekt implementiert wurden? Ihre Entscheidungen werden bestenfalls gute Absichten bleiben, sofern sie nicht mit ihnen nachfolgen.

Schließlich delegiere einige Entscheidungen an andere, die in einem Problembereich Experten sind. Viele Architekten nehmen fälschlicherweise an, dass sie jede Architekturentscheidung treffen müssen. Daher positionieren sie sich als Allwissende Experten. In Wirklichkeit gibt es so etwas wie einen universellen technischen Genius nicht. Architekten haben Bereiche, in denen sie sehr kompetent sind, Bereiche, in denen sie sachkundig sind, und Bereiche, in denen sie schlicht inkompetent sind. Geschickte Architekten delegieren Entscheidungen über Domänenprobleme, in denen sie nicht kompetent sind.

*von Yi Zhou*


## 80. Sei kein Problemlöser

Mit einigen Ausnahmen waren Architekten früher Entwickler. Entwickler werden dafür belohnt, Programmierprobleme zu lösen, die in ihrem Umfang lokaler sind als Architekturprobleme. Viele Programmierprobleme sind kleine, knifflige, algorithmische Probleme. Solche Probleme werden häufig in Programmierinterviews, Büchern und Universitätskursen so präsentiert, als ob die Probleme in einem Vakuum existieren. Die Kniffligkeit ist verlockend und verführerisch. Mit der Zeit beginnen wir, solche Probleme widerspruchslos anzunehmen. Wir fragen nicht, ob dieses Problem sinnvoll, oder interessant, oder nützlich, oder ethisch ist. Wir werden nicht dafür belohnt, die Beziehung dieses Problems zu einer größeren Landschaft zu berücksichtigen. Wir sind darauf trainiert, uns nur auf unsere Lösung zu konzentrieren, was dadurch verschärft wird, dass das Lösen schwieriger Probleme schwer ist. Wir stürzen uns in Programmierinterviews, die oft damit beginnen, uns eine Anzahl von Gummibärchen zu präsentieren, die wir gemäß einer willkürlichen Reihe von Einschränkungen sortieren sollen. Wir lernen, die Einschränkungen nicht in Frage zu stellen; sie sind ein pädagogisches Werkzeug, das uns dazu bringen soll, das zu entdecken, was der Lehrer oder Interviewer oder Mentor bereits weiß.

Architekten und Entwickler lernen, sofort in den Problemlösungsmodus einzusteigen. Aber manchmal ist die beste Lösung keine Lösung. Viele Software-Probleme müssen überhaupt nicht gelöst werden. Sie erscheinen nur als Probleme, weil wir uns nur die Symptome anschauen.

Betrachte verwalteten Speicher. Entwickler auf verwalteten Plattformen haben keine Speicherprobleme gelöst, noch könnten viele von ihnen dies tun, wenn es erforderlich wäre; Teil ihrer Lösung bedeutet, dass sie dieses Problem meistens einfach nicht haben.

Betrachte komplexe Builds, die viele miteinander verbundene Skripte erfordern, die die Durchsetzung vieler Standards und Konventionen erfordern. Du könntest das Problem lösen, und es würde sich großartig anfühlen, es zum Funktionieren zu bringen, indem du deine besten Scripting-Fähigkeiten und Best Practices einsetzt. Unsere Kollegen werden beeindruckt sein. Niemand ist beeindruckt davon, dass wir ein Problem nicht lösen. Aber wenn wir zurücktreten und herausfinden können, dass wir kein Build-Problem lösen, sondern ein Automatisierungs- und Portabilitätsproblem, könnte das dich zu einem Werkzeug führen, das es abstrahiert.

Da Architekten dazu neigen, sofort in den Problemlösungsmodus einzusteigen, vergessen wir, oder haben nie gelernt, wie man das Problem selbst befragt. Wir müssen lernen, wie ein Teleobjektiv, hinein- und herauszuzoomen, um sicherzustellen, dass die Frage wirklich richtig formuliert ist, und dass wir nicht nur das annehmen, was uns gegeben wird. Wir dürfen keine passiven Empfänger von Anforderungen sein, fröhlich an unserem Posten bereit, unsere klügsten Lösungen auf die Art eines Pez-Spenders auszugeben.

Anstatt sofort daran zu arbeiten, das Problem wie dargestellt zu lösen, sieh zu, ob du das Problem ändern kannst. Frag dich selbst: Wie würde die Architektur aussehen, wenn ich dieses Problem einfach nicht hätte? Das kann letztendlich zu eleganteren und nachhaltigeren Lösungen führen. Das Geschäftsproblem muss immer noch gelöst werden, aber vielleicht nicht so unmittelbar wie vorgeschlagen.

Wir müssen unsere Sucht nach „Problemen" überwinden. Wir lieben es, sie zu bekommen, und sehen uns selbst auf einer europäischen Brücke, als ob wir Geheimagenten wären, denen gerade ein sich selbst zerstörender brauner Umschlag mit unserer Mission übergeben wurde. Bevor du deine Antwort auf ein Problem überlegst, denke darüber nach, wie die Welt aussehen würde, wenn du dieses Problem einfach nicht hättest.

*von Eben Hewitt*


## 81. Wähle deine Waffen sorgfältig, gib sie widerwillig auf

Als erfahrener Veteran des Software-Designs und der Implementierung ist jeder Architekt mit einer Reihe von Waffen ausgestattet, die er mit wiederholtem Erfolg eingesetzt hat. Aus dem einen oder anderen Grund haben diese Technologien Gefallen gefunden und sind an die Spitze unserer Liste bevorzugter Lösungen gestiegen. Höchstwahrscheinlich haben sie sich ihren rechtmäßigen Platz in deinem Arsenal verdient, indem sie einen erbitterten Wettbewerb besiegt haben. Trotzdem bedroht eine Lawine neuer Technologien ständig ihre Position. Wir werden oft dazu verleitet, unsere bevorzugten Waffen für diese neuen Alternativen niederzulegen, aber sei nicht zu schnell damit, deine bewährten Rüstzeuge beiseite zu werfen. Sie für Alternativen aufzugeben, die durch ähnliche Prüfungen nicht erprobt wurden, ist ein riskantes Unterfangen.

Das bedeutet nicht, dass eine Technologie, sobald sie auf unserer Favoritenliste steht, unendliche Amtszeit erhält, und es bedeutet sicherlich nicht, dass du deinen Kopf in den Sand stecken und Fortschritte in der Software-Entwicklung ignorieren kannst. Für jede Technologie wird die Zeit kommen, in der sie ersetzt werden muss. Technologie bewegt sich schnell und überlegene Lösungen sind unterwegs. Als Architekten müssen wir über Branchentrends auf dem Laufenden bleiben, wir müssen nur nicht die Ersten sein, die aufkeimende Technologie annehmen. Es gibt gewöhnlich keinen großen Vorteil darin, die Ersten zu sein, die neue Technologie übernehmen, aber es kann mehrere Nachteile geben.

Um das Risiko zu rechtfertigen, das mit der Auswahl neuer Technologie verbunden ist, sollten ihre Vorteile einen Quantensprung nach vorne darstellen. Viele neue Technologien behaupten solche Fortschritte, aber nur wenige liefern sie. Es ist leicht, neue Technologie anzuschauen und technische Vorteile zu sehen, aber diese Vorteile sind oft schwer an Stakeholder zu verkaufen. Bevor du entscheidest, mit neuer Technologie einen Weg zu bahnen, frag dich, wie das Unternehmen von dieser Entscheidung profitieren wird. Wenn das beste Ergebnis aus Geschäftsperspektive ist, dass niemand es bemerken wird, überdenke deine Entscheidung.

Eine weitere wichtige Sache, die es anzuerkennen gilt, ist der Kostenbeitrag der Mängel neuer Technologie. Diese Kosten können hoch sein und sind schwer zu berechnen. Wenn du mit vertrauter Technologie arbeitest, bist du dir ihrer Eigenarten bewusst. Es ist naiv zu denken, dass eine neue Technologie nicht mit ihrer eigenen Sammlung von Fallstricken kommt. Das Hinzufügen von Problemen, die du noch nicht gelöst hast, wird deine Schätzungen zunichte machen. Du bist dir der Kosten, die bei der Implementierung von Lösungen mit vertrauter Technologie anfallen, weitaus besser bewusst.

Eine letzte Sache, die es zu bedenken gilt, ist die zukünftige Relevanz. Es wäre schön, wenn wir einfach überlegene Technologien identifizieren und auswählen könnten, aber die Dinge sind nicht ganz so einfach. Großartige Technologien gewinnen nicht immer. Zu versuchen, die Gewinner früh vorherzusagen, ist ein Glücksspiel, das keine große Auszahlung ergibt. Warte, bis der Hype abklingt, und sieh, ob sich die Technologie in einem nützlichen Bereich etabliert. Du wirst feststellen, dass viele einfach verschwinden. Gefährde dein Projekt nicht für eine Technologie, die keine Zukunft hat.

Die Auswahl der Technologien, die wir zur Lösung von Problemen einsetzen, ist ein großer Teil der Arbeit des Software-Architekten. Wähle deine Waffen sorgfältig und gib sie widerwillig auf. Lass deinen vergangenen Erfolg dazu beitragen, zukünftigen Erfolg zu sichern, und entwickle deinen Technologie-Stack vorsichtig.

*von Chad LaVigne*


## 82. Dein Kunde ist nicht dein Kunde

Wenn du in Anforderungsbesprechungen daran arbeitest, Software zu entwerfen, tue so, als ob dein Kunde nicht dein Kunde wäre. Es stellt sich heraus, dass das eine sehr einfache Sache ist zu tun, weil es wahr ist.

Dein Kunde ist nicht dein Kunde. Der Kunde deines Kunden ist dein Kunde. Wenn der Kunde deines Kunden gewinnt, gewinnt dein Kunde. Was bedeutet, dass du gewinnst.

Wenn du eine E-Commerce-Anwendung schreibst, kümmere dich um die Dinge, von denen du weißt, dass Menschen, die in diesem Shop einkaufen, sie benötigen werden. Sie werden Transportsicherheit benötigen. Sie werden eine Verschlüsselung der gespeicherten Daten benötigen. Dein Kunde erwähnt diese Anforderungen möglicherweise nicht. Wenn du weißt, dass dein Kunde Dinge auslässt, die der Kunde deines Kunden benötigen wird, sprich sie an und erkläre, warum.

Wenn dein Kunde wissentlich und willentlich bestimmte wichtige Dinge nicht berücksichtigt, um die sich der Kunde deines Kunden kümmert – wie es von Zeit zu Zeit vorkommt –, erwäge, von dem Projekt zurückzutreten. Nur weil Sally Kunde nicht für SSL jedes Jahr bezahlen möchte und Kreditkarten im Klartext speichern möchte, weil es weniger kostet zu bauen, ist es nicht in Ordnung, einfach zuzustimmen. Du tötest den Kunden deines Kunden, wenn du zustimmst, Arbeit zu leisten, von der du weißt, dass sie eine schlechte Idee ist.

Anforderungserfassungsbesprechungen sind keine Implementierungsbesprechungen. Verbiete dem Kunden die Verwendung implementierungsspezifischer Begriffe, es sei denn, es handelt sich um ein absolutes oder wohlverstandenes Problem. Erlaube deinem Kunden nur das Platonische Ideal auszudrücken, sein Konzept und seine Ziele, anstatt eine Lösung zu diktieren oder sogar technische Begriffe zu verwenden.

Wie behältst du also eine solche Disziplin in diesen Besprechungen bei, die täuschend schwierig sein können? Denke daran, dich um den Kunden deines Kunden zu kümmern. Denke daran, dass, obwohl dein Kunde deinen Scheck schreibt, du klar sein musst, dass du Best Practices einhalten musst, damit du das machen kannst, was der Kunde wirklich braucht, nicht nur das, was er sagt, dass er es braucht. Natürlich erfordert das viele Diskussionen und Klarheit darüber, was genau du tust und warum.

Vielleicht, wie bei so vielen Dingen im Leben, wird das am besten durch ein Gedicht verdeutlicht. Im Jahr 1649 schrieb Richard Lovelace „To Lucasta, on Going to the Wars". Es endet mit der Zeile: „I could not love thee, dear, so much, / Loved I not honor more."

Wir können unsere Kunden nicht so sehr lieben, wenn wir nicht ihre Kunden noch mehr lieben.

*von Eben Hewitt*


## 83. Es wird nie so aussehen

Es wird nie so aussehen. Es ist allzu leicht, in die Falle zu tappen, viel Zeit in ein Design zu investieren und zuversichtlich zu sein, dass die Implementierung genauso aussehen wird. Ein detailliertes Design kann dich leicht dazu verleiten zu glauben, dass du jeden Winkel abgedeckt hast. Je mehr Detail und je tiefgründiger die Forschung, desto größer dein Vertrauen darin. Aber es ist eine Illusion: Es wird nie so aussehen.

Die Wahrheit ist, egal wie tiefgründig, wie gut recherchiert und wie gut durchdacht dein Design ist, es wird nie genauso aussehen wie in deinem Kopf. Etwas wird passieren, ein externer Faktor kann das Design beeinflussen: falsche Informationen, eine Einschränkung, ein seltsames Verhalten im Code von jemand anderem. Oder du hast etwas falsch gemacht: eine Übersicht, eine falsche Annahme, ein subtiles Konzept übersehen. Oder etwas wird sich ändern; die Anforderungen, die Technologie, oder jemand findet vielleicht einfach einen besseren Weg™.

Diese kleinen Veränderungen im Design summieren sich schnell, und viele kleine Veränderungen erfordern bald, dass eine große gemacht werden muss. Bevor lange dein ursprüngliches Konzept in Stücken auf dem Boden liegt und es zurück zum Reißbrett geht. Du entscheidest, dass du mehr Design, mehr Detail gebraucht hättest, also gehst du zurück und die nächste Architekturvision ist klarer, radikaler, perfekter als die letzte. Aber bevor lange passiert dasselbe, diese Veränderungen beginnen aufzutauchen und dein Design zu verschieben und die Entwickler stopfen immer mehr Zeug hinein, um das kaputte Design zu umgehen, es aber nur noch mehr zu zerbrechen, und du endest damit zu schreien „Natürlich hat es Bugs; es war nie so konzipiert, das zu tun!".

Design ist ein Entdeckungsprozess, da wir bei der Implementierung neue Informationen entdecken, die oft im Voraus nicht bekannt sein können. Indem wir akzeptieren, dass Design ein fortlaufender und empirischer Prozess in einer sich ständig verändernden Welt ist, lernen wir, dass der Designprozess auch flexibel und fortlaufend sein muss. An deinen ursprünglichen Designs festzuhalten und zu versuchen, sie durchzuzwingen, wird nur mit einem Ergebnis enden, also musst du lernen zu verstehen, dass es nie so aussehen wird.

*von Peter Gillard-Moss*


## 84. Wähle Frameworks, die gut mit anderen zusammenarbeiten

Bei der Auswahl von Software-Frameworks als Basis deines Systems musst du nicht nur die individuelle Qualität und die Funktionen jedes Frameworks berücksichtigen, sondern auch, wie gut die Frameworks, aus denen dein System besteht, zusammenarbeiten werden, und wie leicht es sein wird, sie an neue Software anzupassen, die du möglicherweise hinzufügen musst, wenn dein System sich weiterentwickelt. Das bedeutet, dass du Frameworks wählen musst, die sich nicht überschneiden und die bescheiden, einfach und spezialisiert sind.

Es ist am besten, wenn jedes Framework oder jede Drittanbieter-Bibliothek einen separaten logischen Bereich oder eine separate Zuständigkeit anspricht und nicht in den Bereich oder die Zuständigkeit eines anderen Frameworks eingreift, das du verwenden musst.

Stelle sicher, dass du verstehst, wie die logischen Bereiche und Zuständigkeiten, die deine Kandidaten-Frameworks ansprechen, überlappen. Zeichne ein Venn-Diagramm, wenn du musst. Zwei Datenmodelle, die sich im Bereich erheblich überschneiden, oder zwei Implementierungen, die sehr ähnliche Zuständigkeiten aber auf leicht unterschiedliche Weise ansprechen, werden unnötige Komplexität verursachen: die geringen Unterschiede in der Konzeptualisierung oder Darstellung müssen mit klobigem Klebecode abgebildet oder gepatcht werden. Du wirst wahrscheinlich nicht nur mit komplexem Klebcode enden, sondern auch mit dem kleinsten gemeinsamen Nenner der Funktionalität oder des Darstellungsvermögens der beiden Frameworks.

Um die Chance zu minimieren, dass ein bestimmtes Framework sich mit einem anderen überschneidet, wähle Frameworks, die ein hohes Verhältnis von Nutzen zu Ballast im Kontext deiner Systemanforderungen haben. Nutzen ist die Funktionalität oder Datendarstellung, die dein Projekt vom Framework benötigt. Ballast ist die weitreichende, alles umfassende, „Ich-bin-verantwortlich"-Sichtweise des Frameworks auf die Welt. Besteht es darauf, Datendarstellung und Steuerung zu vermischen? Erstreckt sich sein Datenmodell oder sein Satz von Paketen und Klassen weit über das hinaus, was dein System benötigt? Musst du ein Fundamentalist in der Religion des Frameworks werden und deine Auswahl anderer Frameworks auf solche der richtigen Denomination beschränken? Begrenzt seine übermäßige Komplexität die Arten von Dingen, die du damit mischen kannst? Wenn ein Framework mit viel Ballast kommt, dann sollte es auch 75 % des Funktionswertes in deinem Projekt liefern.

Dein System sollte aus sich gegenseitig ausschließenden Frameworks bestehen, von denen jedes ein Meister seines Bereichs sein kann, das aber auch einfach, bescheiden und flexibel ist.

*von Eric Hawthorne*


## 85. Mach ein starkes Geschäftsargument

Als Software-Architekt hattest du Schwierigkeiten, dein Architekturprojekt gut finanziert zu bekommen? Die Vorteile der Software-Architektur sind für Architekten offensichtlich, aber für viele Stakeholder mythisch. Die Massenpsychologie sagt uns, dass „Sehen ist Glauben" der stärkste Glaube für die meisten Menschen ist. In der frühen Phase der Projekte gibt es jedoch wenig zu demonstrieren, um Stakeholder vom Wert einer soliden Software-Architektur zu überzeugen. Es ist noch herausfordernder in Nicht-Software-Industrien, wo die meisten Stakeholder wenig Software-Engineering-Wissen haben.

Die Massenpsychologie zeigt auch, dass die meisten Menschen glauben, dass „Wahrnehmung Realität ist." Daher kannst du, wenn du kontrollieren kannst, wie Menschen den Architekturansatz wahrnehmen, den du vorschlägst, praktisch garantiert kontrollieren, wie sie auf deinen Vorschlag reagieren werden. Wie kannst du die Wahrnehmungen der Stakeholder managen? Mach ein starkes Geschäftsargument für deine Architektur. Menschen, die die Budgetbefugnis haben, deine Ideen zu sponsern, sind fast immer geschäftsorientiert.

Ich habe die folgenden fünf Schritte eingesetzt, um solide Geschäftsargumente zu erstellen, um meinen Architekturansatz viele Male in meiner Karriere erfolgreich zu verkaufen:

```
Stelle den Wertvorschlag auf. Der Wertvorschlag ist deine Zusammenfassung, warum das Geschäft deiner Organisation eine bestimmte Software-Architektur rechtfertigt. Der Schlüssel ist es, deinen Architekturansatz mit bestehenden Lösungen oder anderen Alternativen zu vergleichen. Der Fokus sollte auf seine Fähigkeit gelegt werden, die Produktivität und Effizienz des Unternehmens zu steigern, und nicht darauf, wie brillant die Technologien sind.
Erstelle Kennzahlen zur Quantifizierung. Die Werte, die du zu liefern versprichst, müssen in einem vernünftigen Maß quantifiziert werden. Je mehr du misst, desto mehr kannst du deinen Fall stärken, dass eine solide Architektur zu einem erheblichen Return führen wird. Je früher du Kennzahlen festlegst, desto besser managst du die Wahrnehmungen der Menschen, die dir helfen, verantwortungsvolle Architektur zu verkaufen.
Verknüpfe mit traditionellen Geschäftskennzahlen. Es wäre ideal, wenn du deine technische Analyse in Dollarzahlen übersetzen könntest. Schließlich ist der einzige konstante Parameter in den traditionellen Geschäftskennzahlen Geld. Finde Business-Analysten als deine Partner, wenn du dich mit Finanzarbeit nicht wohl fühlst.
Wisse, wann du aufhören sollst. Bevor du weißt, wann du aufhören sollst, musst du eine Roadmap vorbereiten, die eine Vision erfasst, bei der jeder Meilenstein direkt mit Geschäftswerten verknüpft ist. Lass die Stakeholder entscheiden, wann sie aufhören wollen. Wenn der Geschäftswert für jeden Impuls erheblich ist, wirst du höchstwahrscheinlich weiterhin finanziert werden.
Finde den richtigen Zeitpunkt. Selbst wenn du die obigen vier Schritte befolgst, um ein solides Geschäftsargument zu erstellen, könntest du deine Ideen immer noch nicht verkaufen können, wenn du einen schlechten Zeitpunkt wählst. Ich erinnere mich, dass einer meiner Vorschläge lange Zeit nicht genehmigt wurde, bis ein anderes Projekt sich als totaler Misserfolg wegen schlechten Architektur-Designs herausstellte. Sei klug beim Timing.
```

*von Yi Zhou*


## 86. Muster-Pathologie

Entwurfsmuster sind eines der wertvollsten Werkzeuge, die einem Software-Architekten zur Verfügung stehen. Die Verwendung von Mustern ermöglicht es uns, gemeinsame Lösungen zu erstellen, die leichter zu kommunizieren und zu verstehen sind. Sie sind Konzepte, die direkt mit gutem Design verbunden sind. Diese Tatsache kann es sehr verlockend machen, unsere Architekturkompetenz zu demonstrieren, indem wir einem Projekt viele Muster aufzwingen. Wenn du dich dabei findest, deine Lieblingsmuster in einen Problemraum zu pressen, in dem sie nicht passen, leidest du möglicherweise an Muster-Pathologie.

Viele Projekte leiden unter diesem Zustand. Das sind die Projekte, bei denen du dir vorstellst, wie der ursprüngliche Architekt von der letzten Seite seines Musterbuchs aufblickt, sich die Hände reibt und sagt: „Nun, welches werde ich zuerst verwenden!?". Diese Denkweise ähnelt ein wenig der eines Entwicklers, der beginnt, eine Klasse mit dem Gedanken zu schreiben: „Hmm, welche Klasse sollte ich erweitern?". Entwurfsmuster sind ausgezeichnete Werkzeuge zur Minderung notwendiger Komplexität, aber wie alle Werkzeuge können sie missbraucht werden. Entwurfsmuster werden zu einem Problem, wenn wir sie zum sprichwörtlichen Hammer machen, mit dem wir jeden Nagel schlagen müssen. Sei vorsichtig, dass deine Wertschätzung für Muster nicht zu einer Faszination wird, die dich dazu bringt, Lösungen einzuführen, die komplizierter sind als nötig.

Muster überall auf ein Projekt zu drücken, ohne Notwendigkeit, ist Über-Engineering. Entwurfsmuster sind keine Magie, und ihre Verwendung qualifiziert eine Lösung nicht automatisch als gutes Design. Sie sind wiederverwendbare Lösungen für wiederkehrende Probleme. Sie wurden von anderen entdeckt und dokumentiert, um uns zu helfen, zu erkennen, wenn wir uns ein Rad anschauen, das bereits erfunden wurde. Es ist unsere Aufgabe, Probleme zu identifizieren, die durch diese Lösungen gelöst werden, wenn sie auftreten, und Entwurfsmuster angemessen anzuwenden. Lass deinen Wunsch, Muster-Wissen zu zeigen, nicht deinen pragmatischen Blick trüben. Halte deine Sicht darauf fokussiert, Systeme zu entwerfen, die effektive Geschäftslösungen liefern, und verwende Muster, um die Probleme zu lösen, die sie ansprechen.

*von Chad LaVigne*


## 87. Lerne eine neue Sprache

Um als Architekt erfolgreich zu sein, musst du dich von Menschen verstanden machen, die nicht deine Muttersprache sprechen. Nein. Ich schlage nicht vor, Esperanto oder sogar Klingonisch zu lernen, aber du solltest zumindest grundlegendes Business- und Test-Englisch sprechen können. Und wenn du nicht fließend in Entwickler-Sprache bist, solltest du das zur obersten Priorität machen.

Wenn du den Wert des Lernens anderer Sprachen nicht siehst, betrachte das folgende Szenario. Die Geschäftsleute wollen eine Änderung an einem bestehenden System vornehmen, also rufen sie ein Meeting mit dem Architekten und Entwicklern ein, um es zu besprechen. Leider spricht keiner aus dem technischen Team Business-Sprache und keiner der Geschäftsleute spricht Entwickler-Sprache. Das Meeting wird wahrscheinlich ungefähr so verlaufen:

```
Eine Geschäftsperson spricht eine Minute über den Bedarf nach einer relativ einfachen Erweiterung eines bestehenden Produkts und erklärt, wie die Änderung dem Verkaufsteam ermöglichen wird, sowohl Markt- als auch Gedankenanteil zu steigern.

Während die Geschäftsperson noch spricht, beginnt der Architekt, einige okkulte Symbole auf einem Notizblock zu skizzieren, und tritt in ein leises Argument mit einem der Entwickler in ihrer seltsamen mehrsilbigen Sprache ein.

Schließlich hört die Geschäftsperson auf und schaut den Architekten erwartungsvoll an.

Nach dem geflüsterten Argument abgeschlossen ist, geht der Architekt an die Tafel und beginnt, mehrere komplexe Diagramme zu zeichnen, die angeblich mehrere Ansichten des bestehenden Systems darstellen sollen, während er (in komplexen technischen Begriffen) erklärt, warum die angeforderte Erweiterung ohne wesentliche Änderungen praktisch unmöglich ist und möglicherweise sogar eine vollständige Neugestaltung/Neuprogrammierung des gesamten Systems erfordert.

Die Geschäftsleute (die wenig von dem Diagramm und noch weniger von der Erklärung verstanden haben) sind offen verblüfft und finden es schwer zu glauben, dass etwas so Einfaches solche massiven Änderungen erfordern würde. Sie beginnen sich zu fragen, ob der Architekt es ernst meint oder sich nur etwas ausdenkt, um die Änderung zu vermeiden.

Inzwischen sind der Architekt und die Entwickler genauso überrascht, dass die Geschäftsleute nicht sehen, wie die „geringfügige" Änderung wesentliche Modifikationen an der Kernfunktionalität des Systems erfordern wird.
```

Und darin liegt das Problem. Keine der beiden Gruppen versteht, wie die andere denkt, oder was die Hälfte der Worte, die sie verwenden, bedeutet. Das führt zu Misstrauen und Missverständnissen.

Stell dir vor, wie das obige Szenario sich verändern könnte, wenn der Architekt in der Lage wäre, die Probleme den Geschäftsleuten in Begriffen zu erklären, die sie verstehen, und die Geschäftsprobleme den Entwicklern in Begriffen zu vermitteln, die sie verstehen. Anstatt Überraschung und Misstrauen wäre das Ergebnis Einigkeit und Zustimmung.

Ich sage nicht, dass das Lernen mehrerer Sprachen alle deine Probleme lösen wird, aber es wird helfen, die Missverständnisse und Missverständnisse zu verhindern, die zu Problemen führen.

Für diejenigen von euch, die entscheiden, dass das Sinn macht, wünsche ich euch Erfolg auf eurer Reise. Oder, wie die Klingonen sagen, Qapla!

*von Burk Hufnagel*


## 88. Sei nicht clever

Allgemeine Intelligenz, Einfallsreichtum, Nachdenklichkeit, eine Breite und Tiefe des Wissens und eine Affinität für Präzision sind lobenswerte Qualitäten bei jedem, besonders geschätzt bei Architekten.

Cleverness trägt jedoch eine bestimmte zusätzliche Konnotation. Sie impliziert die Fähigkeit, schnell eine Lösung zu erdenken, die dich aus einer Klemme befreien kann, die aber letztendlich auf einem Gimmick, einem Taschenspielertrick oder einem Schwindel beruht. Wir erinnern uns an clevere Debattierer aus der Oberschule – immer in der Lage, Semantik zu spielen oder logische Trugschlüsse einzusetzen, um den Punkt zu gewinnen.

Clevere Software ist teuer, schwer zu warten und brüchig. Sei nicht clever. Sei so dumm wie möglich und erstelle immer noch das angemessene Design. Das angemessene Design wird niemals clever sein. Wenn Cleverness absolut erforderlich erscheint, ist das Problem falsch formuliert; setze das Problem zurück. Formuliere es neu, bis du wieder dumm sein kannst. Arbeite in groben Kreidezeichnungen; bleibe allgemein. Lass den Geschmack des Tages los. Es braucht einen klugen Architekten, um dumm zu sein.

Es ist unsere Cleverness, die es uns ermöglicht, Software dazu zu bringen, zu funktionieren. Sei nicht der Anwalt, der deine Software aufgrund einer Formalität freibekommt. Wir sind nicht Rube Goldberg. Wir sind nicht MacGyver, immer bereit, ein kompliziertes Design aus dem Hut zu ziehen, nachdem wir nur eine Büroklammer, einen Feuerwerkskörper und ein Stück Kaugummi bekommen haben. Leere deinen Kopf und gehe das Problem ohne dein umfangreiches Wissen über Closures und Generics und wie man die Objektpromotion im Heap manipuliert an. Manchmal natürlich ist genau solches Zeug das, was wir brauchen. Aber seltener als wir denken könnten.

Mehr Entwickler können dumme Lösungen implementieren und warten. Bei dummen Lösungen kann jede Komponente nur eine Sache tun. Sie werden weniger Zeit zur Erstellung benötigen und weniger Zeit zur späteren Änderung. Sie erben Optimierungen von den Bausteinen, die du verwendest. Sie entstehen aus der Seite als lebendiger Prozess, und du kannst ihre Eleganz und Einfachheit fühlen. Clevere Designs bleiben hartnäckig verwurzelt; ihre Details sind zu sehr in das Gesamtbild verwickelt. Sie zerbröckeln, wenn du sie anfasst.

*von Eben Hewitt*


## 89. Baue Systeme, um Zuhanden zu sein

Wir bauen Werkzeuge. Die Systeme, die wir erstellen, haben keinen anderen Existenzgrund (noch wir, um bezahlt zu werden), als jemandem zu helfen, meist jemand anderem, etwas zu tun.

Martin Heidegger, ein einflussreicher deutscher Philosoph des 20. Jahrhunderts, erforschte die Arten, wie Menschen Werkzeuge (und allgemeiner „Zeug") in ihrem Leben erleben. Menschen verwenden Werkzeuge, um auf ein Ziel hinzuarbeiten, und das Werkzeug ist lediglich ein Mittel zum Zweck.

Während des erfolgreichen Einsatzes ist ein Werkzeug zuhanden („ready-to-hand", mit der Eigenschaft der „Handlichkeit"). Das Werkzeug wird direkt erlebt, es wird ohne Überlegung, ohne Theoretisieren verwendet. Wir greifen das Werkzeug und verwenden es, um uns auf unser Ziel zuzubewegen. Im Einsatz verschwindet es! Das Werkzeug wird zu einer Erweiterung des Körpers des Benutzers und wird nicht in eigenem Recht erlebt. Ein Zeichen dafür, dass ein Werkzeug zuhanden ist, ist, dass es unsichtbar, unfühlbar, bedeutungslos wird.

Überlege, wie es sich anfühlt, einen Nagel zu hämmern oder mit einem Stift zu schreiben. Denke an diese Unmittelbarkeit. Denke an die Art, wie das Werkzeug eine nahtlose Erweiterung deines Körpers zu sein scheint.

Alternativ, und meist wenn etwas damit schiefgelaufen ist, kann der Benutzer ein Werkzeug als vorhanden („present-at-hand") erleben. Das Werkzeug ist vom Ziel isoliert, es liegt vor uns und fordert Aufmerksamkeit. Es wird zu einem eigenständigen Untersuchungsgegenstand. Der Benutzer kann nicht mehr auf sein Ziel hinarbeiten, sondern muss sich zuerst mit dem Werkzeug befassen, ohne dass es etwas tut, um ihn seinem Ziel näherzubringen. Als Technologen neigen wir dazu, die Systeme, die wir für Benutzer bauen, als vorhanden zu erleben, während wir sie bauen, und wieder, wenn wir Fehlerberichte erhalten. Für uns ist das Werkzeug ganz richtig ein Gegenstand der Untersuchung, des Theoretisierens, der Erforschung. Es ist ein Ding, das studiert werden soll.

Es ist jedoch entscheidend für ihren Erfolg, dass die Benutzer die Werkzeuge, die wir für sie bauen, als zuhanden erleben. Sind deine Systeme so architektiert, dass sie im Einsatz unsichtbar sind? Fällt die Benutzeroberfläche natürlich zur Hand? Oder fordern deine Systeme ständig Aufmerksamkeit, die Benutzer von ihrem Ziel ablenkt?

*von Keith Braithwaite*


## 90. Finde und behalte leidenschaftliche Problemlöser

Ein Team aus herausragenden Entwicklern zusammenzustellen ist eines der wichtigsten Dinge, die du tun kannst, um den Erfolg eines Software-Projekts zu sichern. Während das Konzept, dieses Team zusammenzuhalten, nicht so viel Aufmerksamkeit zu bekommen scheint, ist es gleichermaßen wichtig. Daher musst du dein Entwicklungsteam sorgfältig auswählen und es, einmal zusammengestellt, gewissenhaft schützen.

Die meisten Menschen werden wohl zustimmen, dass das Finden erstklassiger Entwickler gründliche technische Interviews erfordert. Aber was bedeutet gründlich genau? Es bedeutet nicht, von Kandidaten zu verlangen, schwierige Fragen über obskure technische Details zu beantworten. Nach spezifischen technischen Kenntnissen zu suchen ist definitiv Teil des Prozesses, aber ein Interview in einen Zertifizierungstest zu verwandeln, wird keinen Erfolg garantieren. Du suchst nach Entwicklern mit Problemlösungsfähigkeiten und Leidenschaft. Die Werkzeuge, die du verwendest, werden sich sicher ändern; du brauchst Menschen, die gut darin sind, Probleme anzugehen, unabhängig von den beteiligten Technologien. Zu beweisen, dass jemand jede Methode in einer API aufzählen kann, sagt dir sehr wenig über seine Eignung oder Leidenschaft zur Problemlösung aus.

Jedoch gibt das Bitten um die Erklärung des Ansatzes zur Diagnose eines Leistungsproblems dir einen großartigen Einblick in seine Methoden zur Problemlösung. Wenn du mehr über die Fähigkeit eines Entwicklers erfahren möchtest, gelernte Lektionen anzuwenden, frage, was er ändern würde, wenn er die Chance hätte, sein jüngstes Projekt von vorne zu beginnen. Gute Entwickler sind leidenschaftlich in ihrer Arbeit. Das Fragen nach vergangenen Erfahrungen wird diese Leidenschaft hervorrufen und dir sagen, was korrekte Antworten auf technische Trivialfragen nicht können.

Wenn du fleißig dabei warst, ein starkes Team zusammenzustellen, möchtest du alles in deiner Macht Stehende tun, um das Team zusammenzuhalten. Bindungsfaktoren wie Vergütung mögen außerhalb deiner Hände liegen, aber stelle sicher, dass du die kleinen Dinge erledigst, die dazu beitragen, ein gesundes Arbeitsumfeld zu fördern. Gute Entwickler werden oft stark durch Anerkennung motiviert. Nutze diese Tatsache zu deinem Vorteil und erkenne herausragende Leistungen an. Großartige Entwickler zu finden ist schwierig. Zu wissen, dass Menschen wertgeschätzt werden, ist es nicht. Verpasse keine einfachen Chancen, die Moral zu stärken und die Produktivität zu steigern.

Sei vorsichtig mit negativer Verstärkung. Zu viel davon könnte die Kreativität eines Entwicklers unterdrücken und die Produktivität verringern. Schlimmer noch, es kann Zwietracht im Team säen. Gute Entwickler sind klug; sie wissen, dass sie nicht immer falsch liegen. Wenn du die Kleinigkeiten ihrer Arbeit auseinandernimmst, wirst du ihren Respekt verlieren. Halte Kritik konstruktiv und verlange nicht, dass jede Lösung so aussieht, als wäre sie von dir gekommen.

Die Bedeutung, dein Entwicklungsteam richtig zu besetzen, kann nicht übertrieben werden. Das sind die Menschen, die die schwere Arbeit leisten. Wenn es um Schätzungen geht, werden alle als gleich produktiv behandelt. Stelle sicher, dass es schwer ist, in die Startaufstellung zu kommen, und wenn du einmal ein Gewinnerteam hast, geh die extra Meile, um es zusammenzuhalten.

*von Chad LaVigne*


## 91. Software existiert eigentlich nicht

Software Engineering wird oft mit gut etablierten Disziplinen wie dem Bauingenieurwesen verglichen. Es gibt ein Problem mit diesen Analogien; im Gegensatz zu den sehr greifbaren Produkten, die durch diese traditionellen Praktiken entstehen, existiert Software nicht wirklich. Nicht im traditionellen Sinne jedenfalls. Diejenigen von uns in der Welt der Einsen und Nullen sind nicht durch dieselben physischen Regeln eingeschränkt, die klassische Ingenieursparadigmen binden. Während die Anwendung von Ingenieursprinzipien auf die Software-Designphase gut funktioniert, ist die Annahme, dass man das Design auf dieselbe Weise umsetzen kann, die von traditionelleren Ingenieursansätzen verwendet wird, unrealistisch.

Sowohl Unternehmen als auch Software sind lebende, sich bewegende Entitäten. Geschäftsanforderungen ändern sich schnell aufgrund von Dingen wie neu erworbenen Geschäftspartnern und Marketingstrategien. Das macht es sehr schwierig, ein Software-Projekt auf dieselbe Weise anzugehen wie ein traditionelles Ingenieursprojekt wie den Brückenbau. Es ist sehr unwahrscheinlich, dass du gebeten wirst, die Position einer Brücke auf halbem Weg durch ein Bauprojekt zu verschieben. Es ist jedoch sehr wahrscheinlich, dass die Übernahme eines Geschäftspartners dich dazu zwingt, Unterstützung für organisationsbasiertes Content Management zu einer Anwendung hinzuzufügen. Dieser Vergleich sollte die Dinge in Perspektive setzen. Wir sagen oft, dass Software-Architekturentscheidungen schwer zu ändern sind, aber nicht annähernd so sehr wie Dinge, die buchstäblich und übertragen in Stein gemeißelt sind.

Das Wissen, dass die Produkte, die wir bauen, formbar sind und dass sich die Anforderungen darum wahrscheinlich ändern werden, versetzt uns in eine andere Position als jemanden, der ein unbewegliches Objekt baut. Ingenieursbemühungen der physischen Art sind viel einfacher auf eine „Plan die Arbeit, arbeite den Plan"-Art umzusetzen. Bei Software müssen die Dinge eher auf eine „Plan die Arbeit, massiere den Plan"-Art angegangen werden.

Diese Unterschiede sind nicht immer schlechte Nachrichten, manchmal können sie vorteilhaft sein. Zum Beispiel bist du nicht unbedingt darauf beschränkt, die Komponenten eines Softwaresystems in einer bestimmten Reihenfolge zu bauen, sodass du zuerst hochriskante Themen angehen kannst. Das steht im direkten Gegensatz zu etwas wie dem Brückenbau, wo es viele physische Beschränkungen gibt, die die Reihenfolge betreffen, in der Aufgaben ausgeführt werden.

Die Flexibilität des Software Engineerings bringt jedoch einige Probleme mit sich, von denen viele selbstverursacht sind. Als Architekten sind wir uns der „weichen" Natur unseres Handwerks sehr bewusst und wir mögen Probleme lösen. Schlimmer noch, die Geschäftsinhaber sind sich dieser Tatsachen vage bewusst. Das erleichtert es ihnen, große Änderungen durchzusetzen. Sei nicht zu bestrebt, große Architekturänderungen zu berücksichtigen, nur weil es deiner Natur als Lösungsanbieter entspricht. Solche Entscheidungen können ein sonst gesundes Projekt brechen.

Denke daran, dass ein Anforderungsdokument kein Blueprint ist und Software nicht wirklich existiert. Die virtuellen Objekte, die wir erstellen, sind leichter zu ändern als ihre physischen Weltgegenstücke, was eine gute Sache ist, weil sie viele Male dazu aufgefordert werden. Es ist in Ordnung, zu planen, als würden wir ein unbewegliches Objekt bauen; wir können nur nicht überrascht oder unvorbereitet sein, wenn wir aufgefordert werden, das Objekt zu verschieben.

*von Chad LaVigne*


## 92. Zahle deine technischen Schulden ab

In jedem Projekt, das sich in der Produktion befindet (d. h. es hat Kunden, die es verwenden), wird eine Zeit kommen, in der eine Änderung vorgenommen werden muss; entweder muss ein Bug behoben oder eine neue Funktion hinzugefügt werden. An diesem Punkt gibt es zwei mögliche Entscheidungen; du kannst dir die Zeit nehmen, es „richtig zu machen", oder du kannst eine oder mehrere „Abkürzungen" nehmen und versuchen, die Änderung früher abzuliefern.

Im Allgemeinen werden die Geschäftsleute (Vertrieb/Marketing und Kunden) die Änderung so schnell wie möglich haben wollen, während die Entwickler und Tester mehr daran interessiert sein werden, sich die Zeit zu nehmen, die Änderung ordnungsgemäß zu entwerfen, zu implementieren und zu testen, bevor sie an die Kunden geliefert wird.

Als Architekt des Projekts musst du entscheiden, was sinnvoller ist, und dann die Entscheidungsträger davon überzeugen, deinen Rat zu befolgen; und wie bei den meisten Architekturthemen gibt es einen Kompromiss. Wenn du glaubst, dass das System einigermaßen stabil ist, könnte es sinnvoll sein, den „schnellen und unsauberen" Weg zu gehen und die Änderung schnell in die Produktion zu bringen. Das ist in Ordnung, aber du musst wissen, dass dein Projekt damit einige „technische Schulden" aufnimmt, die später zurückgezahlt werden müssen. Rückzahlung bedeutet in diesem Fall, zurückzugehen und die Änderung so vorzunehmen, wie du es getan hättest, wenn du die Zeit und die Ressourcen gehabt hättest, es beim ersten Mal richtig zu machen.

Warum also die Besorgnis, Änderungen jetzt statt später richtig vorzunehmen? Weil es versteckte Kosten für diese schnellen und unsauberen Fixes gibt. Bei Finanzschulden werden diese versteckten Kosten „Zinsen" genannt, und die meisten Menschen mit einer Kreditkarte wissen, wie teuer es sein kann, nur die Zinsen einer Schuld zu zahlen. Bei technischen Schulden manifestieren sich Zinsen in Form von Systeminstabilität und erhöhten Wartungskosten aufgrund der eingehackten Änderungen, dem Mangel an angemessenem Design, Dokumentation und/oder Tests. Und wie finanzielle Zinsen müssen regelmäßige Zahlungen geleistet werden, bis die ursprüngliche Schuld zurückgezahlt ist.

Jetzt, da du etwas mehr über die wahren Kosten technischer Schulden weißt, könntest du entscheiden, dass der Preis zu hoch ist und du dir die Kosten nicht leisten kannst. Aber wenn es eine Wahl zwischen den Entwicklern ist, den Fix so schnell wie möglich rauszubringen, oder einen erheblichen finanziellen Schlag einzustecken, macht es im Allgemeinen Sinn, den Fix so schnell wie möglich rauszubringen. Also nimm den Schlag und bringe die Änderung so schnell wie möglich in die Produktion, aber höre dort nicht auf.

Sobald der Fix in der Produktion ist, lass die Entwickler zurückgehen und ihn ordnungsgemäß beheben, damit er in die nächste geplante Version aufgenommen werden kann. Das ist das Äquivalent davon, etwas auf deine Kreditkarte zu laden und dann das Guthaben am Ende des Monats abzuzahlen, damit dir keine Zinsen berechnet werden. So kannst du die schnellen Änderungen liefern, die das Unternehmen benötigt, während du dein Projekt aus dem Schuldengefängnis heraushalten kannst.

*von Burk Hufnagel*


## 93. Du kannst Lösungen nicht zukunftssicher machen

### Die Lösung von heute ist das Problem von morgen

Niemand kann die Zukunft vorhersagen. Wenn du das als universelle Wahrheit akzeptierst, dann wird die Frage: Wie weit liegt die Zukunft entfernt? Eine Dekade? Zwei Jahre? Zwanzig Minuten? Wenn du die Zukunft nicht vorhersagen kannst, kannst du nichts über den aktuellen Moment hinaus vorhersagen. Dieser Moment und die Momente, die ihm vorangingen, sind alles, was du weißt, bis der nächste Moment eintritt. Das ist der Grund, warum wir Autounfälle haben – wenn du wüsstest, dass du am Donnerstag einen Unfall haben wirst, würdest du wahrscheinlich zuhause bleiben.

Und doch sehen wir Software-Architekten immer wieder versuchen, Systeme zu entwerfen, die, um einen besseren Begriff zu verwenden, „zukunftssicher" sind. Es ist schlicht nicht möglich, eine Architektur zukunftssicher zu machen. Egal welche Architekturentscheidung du jetzt triffst, diese Wahl wird irgendwann obsolet werden. Die coole Programmiersprache, die du verwendet hast, wird schließlich zum COBOL von morgen. Das heutige verteilte Framework wird zum DCOM von morgen. Kurz gesagt, die Lösung von heute wird immer das Problem von morgen sein.

Wenn du diese Tatsache akzeptierst – dass die Entscheidungen, die du heute triffst, in der Zukunft mit ziemlicher Sicherheit falsch sein werden –, dann befreit dich das von der Last, deine Architekturen zukunftssicher zu machen. Wenn jede Wahl, die du heute triffst, in der Zukunft eine schlechte Wahl sein wird, dann mach dir keine Sorgen um das, was die Zukunft bringen wird, wähle die beste Lösung, die deinen Bedürfnissen heute entspricht.

Eines der Probleme, die Architekten heute haben, ist Analyse-Lähmung, und ein großer Beitrag dazu ist der Versuch, die beste Technologie für die Zukunft zu erraten. Eine gute Technologie für jetzt zu wählen ist schon schwer genug, eine zu wählen, die in der Zukunft relevant sein wird, ist sinnlos. Schau, was dein Unternehmen jetzt braucht. Schau, was der Technologiemarkt jetzt bietet. Wähle die beste Lösung, die deinen Bedürfnissen jetzt entspricht, weil alles andere nicht nur morgen die falsche Wahl sein wird, sondern auch die falsche Wahl heute.

*von Richard Monson-Haefel*


## 94. Das Problem der Benutzerakzeptanz

Menschen sind nicht immer glücklich über neue Systeme oder größere Upgrades. Das kann eine Bedrohung für den erfolgreichen Abschluss eines Projekts darstellen.

Es ist nicht ungewöhnlich, dass Menschen der Entscheidung widersprechen, ein neues System einzuführen – besonders am Anfang. Das sollte erwartet werden und die Gründe sollten notiert werden. Jedoch sind erste Reaktionen auf ein neues System weniger beunruhigend als eine anhaltend negative Reaktion.

Dein Ziel als Architekt ist es, die Bedrohung durch Akzeptanzprobleme zu erkennen und zu messen und daran zu arbeiten, diese Bedrohungen zu entschärfen. Dazu musst du dir ihrer bewusst sein und die Gründe dafür berücksichtigen. Einige der häufigsten Gründe sind:

1. Menschen haben möglicherweise Bedenken hinsichtlich der Notwendigkeit eines neuen Systems (und der anschließenden Einstellung eines alten Systems). Das kann auch die Angst vor dem Verlust von Funktionalität oder dem Verlust von Einfluss oder Macht umfassen, wenn sich Rollen ändern.
2. Menschen fürchten neue (unerprobte) Technologien.
3. Menschen haben Kosten-/Budgetbedenken.
4. Menschen mögen einfach keine Veränderungen.

Jeder dieser Gründe erfordert verschiedene mögliche Lösungen. Einige davon kannst du ansprechen und andere nicht. Du musst den Unterschied erkennen und schnell mit denen umgehen, die du kannst. Beginne früh, Gespräche mit deinen Endbenutzern über das neue System und seine realen und wahrgenommenen Vor- und Nachteile zu führen. Die effektivste langfristige Lösung ist, das Design des Systems selbst zu verwenden, um die Bedenken anzusprechen. Andere effektive Lösungen umfassen Training, geplante System-Demonstrationen (früh im Projektlebenszyklus) und das Teilen des Wissens darüber, was Benutzer mit einem neuen System bekommen werden.

Ein „Projekt-Champion" kann helfen, Benutzerakzeptanzprobleme zu vermeiden. Idealerweise sollte das eine Person sein, die die Benutzergruppe oder Stakeholder repräsentiert. Manchmal müssen sie selbst überzeugt werden. Wenn es keinen gibt, dann dränge von Anfang an auf einen. Sobald du einen Projekt-Champion gewonnen hast, gib ihm deine Unterstützung in jeder möglichen Weise.

*von Norman Carnovale*


## 95. Die Bedeutung von Consommé

Ein Consommé ist eine extrem geklärte Brühe, meistens aus Rind- oder Kalbfleisch, die als delikate Suppe serviert wird. Ein gut gemachtes Consommé ist vollkommen klar. Es gilt als herausfordernd und zeitaufwändig herzustellen, weil es nur einen Weg gibt, das Fett und andere Feststoffe zu entfernen, die die Brühe trüben, und die absolute Klarheit zu gewinnen, die das Gericht erfordert: wiederholtes, einfaches, feinmaschiges Abseihen. Dieses immer wiederholte Abseihen, diese hyperbewusste Verfeinerung der Mischung, schafft einen intensiv reichhaltigen Geschmack. Es ist so, als ob man beim Genuss eines Consommés die Essenz einer Sache selbst kostet. Das ist tatsächlich der Sinn des Gerichts.

In Kochschulen in Amerika wird ein einfacher Test für Schüler durchgeführt, die Consommé zubereiten: Der Lehrer lässt ein Zehncentstück in deine bernsteinfarbene Brühe fallen; wenn du das Datum auf dem Geldstück, das auf dem Boden der Schüssel liegt, lesen kannst, bestehst du. Wenn du es nicht kannst, fällst du durch.

Software-Architektur erfordert eine kontinuierliche Verfeinerung des Denkens, ein wiederholtes Abseihen von Ideen, bis wir die Essenz jeder Anforderung im System bestimmt haben. Wir fragen, wie Hamlet, der Yoricks Schädel hält, was ist dieses Ding? Was sind seine Eigenschaften? Seine Beziehungen? Wir klären unsere Konzepte, um die Beziehungen innerhalb der Architektur nachweislich wahr und intern konsistent zu machen.

Viele fehlende Anforderungen und Bugs in Software lassen sich auf mehrdeutige, allgemeine Sprache zurückführen. Stelle Kunden, Entwicklern, Analysten und Benutzern dieselben Fragen wiederholt, bis sie vor Langeweile schläfrig werden. Nun verkleidest du deine Frage, um sie auf eine andere Weise zu stellen, wie ein Anwalt, der nach einer Schwachstelle im Alibi sucht, um etwas Neues, irgendwelche Unterschiede oder Widersprüche herauszukitzeln. Abseihen und immer wieder abseihen.

Konzentriere dich darauf, was aus den in der Architektur präsentierten Konzepten, den Substantiven, die sie bilden, entfernt werden kann, um ihre Essenz zu bestimmen. Bringe chirurgische Präzision in die Sprache, die du in deinen Anforderungen findest, und lehne Mehrdeutigkeit, Allgemeinheit, ungerechtfertigte Annahmen oder überflüssige Formulierungen ab. Das dient dazu, deine Konzepte reicher und robuster zu machen. Reduzieren und immer wieder reduzieren.

Teste Aussagen, indem du fragst: „Würdest du dieselbe Aussage machen, wenn ich ‚immer und ewig und unter allen Umständen' daran anhänge?" Menschen zögern, sich auf solche Absoluta festzulegen, und müssen ihre Worte verfeinern. Zwinge Darstellungen von Konzepten durch ein sprachliches Sieb, um sie zu klären. Tu das wieder, bis du nur noch mit der erschöpfenden Liste einfacher und nachweislich wahrer Aussagen übrig bleibst, die die wesentliche Natur des Systems beschreiben.

Du wirst wissen, wann die Architektur fertig ist: wenn du durch sie hindurchschauen und das Datum auf einem Zehncentstück lesen kannst.

*von Eben Hewitt*


## 96. Für den Endbenutzer ist die Benutzeroberfläche das System

Es gibt zu viele gute Produkte, die hinter schlechten Benutzeroberflächen versteckt sind. Der Endbenutzer wird über die Benutzeroberfläche auf das System zugreifen. Wenn die Qualität der Erfahrung des Benutzers bei der Interaktion mit deinem Produkt leidet, dann leidet auch sein Eindruck von deinem Produkt, egal wie technologisch fortschrittlich und bahnbrechend dein Produkt sein mag.

Die Benutzeroberfläche ist eine wichtige Komponente der Architektur und eine, die oft vernachlässigt wird. Der Architekt sollte die Dienste von Spezialisten wie User-Experience-Designern und Usability-Experten in Anspruch nehmen. Die Experten für Benutzerinteraktion können zusammen mit dem Architekten das Interface-Design sowie seine Kopplung mit den internen Mechanismen vorantreiben. Die Einbeziehung von Experten für Benutzeroberflächen in einem frühen Stadium und während der gesamten Produktentwicklungsphasen stellt sicher, dass das Endprodukt ausgereift ist und die Integration der Benutzeroberfläche mit dem Produkt nahtlos verläuft. Der Architekt sollte auch darauf achten, Benutzerinteraktionstests durchzuführen, während sich das Produkt noch in der Beta-Phase befindet, und zwar mit echten Endbenutzern, und deren Feedback in das finale Produkt einfließen zu lassen.

Oft verändert sich die Nutzung eines Produkts im Laufe der Zeit, wenn sich die Technologie wandelt und Funktionen hinzugefügt werden. Der Architekt sollte sicherstellen, dass sich die Benutzeroberfläche mit der Architektur verändert und die Erwartungen der Benutzer widerspiegelt.

Benutzerinteraktionen sollten eines der Ziele der gesamten Produktarchitektur sein. Tatsächlich sollte die Benutzerinteraktion ein integraler Bestandteil des Entscheidungsprozesses für Architektur-Kompromisse und interne Produktdokumentation sein – genauso wie Robustheit und Performance. Änderungen im Benutzerinteraktionsdesign sollten im Laufe der Zeit festgehalten werden, genau wie Code. Dies gilt insbesondere für Produkte, bei denen die Benutzeroberfläche in einer anderen Programmiersprache geschrieben ist als der Rest des Produkts.

Es liegt in der Verantwortung des Architekten, die häufigsten Interaktionen für den Endbenutzer nicht nur einfach, sondern auch lohnend zu gestalten. Bessere Benutzeroberflächen führen zu zufriedeneren Kunden, was dazu beiträgt, die Produktivität der Kunden zu steigern. Wenn dein Produkt dazu beiträgt, dass Menschen produktiver werden, wird es zum Geschäftsergebnis des Unternehmens beitragen.

Von Vinayak Hegde


## 97. Großartige Software wird nicht gebaut, sie wächst

Als Architekt bist du damit beauftragt, die anfängliche Struktur und Anordnung von Softwaresystemen bereitzustellen, die wachsen und sich über die Zeit verändern werden, die überarbeitet werden müssen, die mit anderen Systemen kommunizieren müssen, und dies fast immer auf eine Weise, die du und deine Stakeholder nicht vorhergesehen haben. Auch wenn wir Architekten genannt werden und wir viele Metaphern aus dem Bauwesen und der Ingenieurwissenschaft entlehnen, wird großartige Software nicht gebaut, sie wächst.

Der einzelne größte Prädiktor für das Scheitern von Software ist die Größe; bei näherer Betrachtung gibt es kaum einen Vorteil darin, mit einem großen Systemdesign zu beginnen. Dennoch werden wir alle irgendwann versucht sein, genau das zu tun. Abgesehen davon, dass es anfällig für zufällige Komplexität und Trägheit ist, bedeutet das Entwerfen großer Systeme im Vorfeld größere Projekte, die mit größerer Wahrscheinlichkeit scheitern, mit größerer Wahrscheinlichkeit nicht testbar sind, mit größerer Wahrscheinlichkeit fragil sind, mit größerer Wahrscheinlichkeit unnötige und ungenutzte Teile haben, mit größerer Wahrscheinlichkeit teuer sind und mit größerer Wahrscheinlichkeit eine negative politische Dimension haben.

Widerstehe daher dem Versuch, ein großes, vollständiges System zu entwerfen, das die bekannten Anforderungen und gewünschten Eigenschaften „erfüllt oder übertrifft", egal wie verlockend das auch sein mag. Habe eine große Vision, aber kein großes Design. Lass dich und dein System anpassen, wenn sich die Situation und die Anforderungen zwangsläufig ändern.

Wie geht das? Der beste Weg, um sicherzustellen, dass ein Softwaresystem sich entwickeln und anpassen kann, ist, es von Anfang an weiterzuentwickeln und anzupassen. Ein System zur Weiterentwicklung zu bringen bedeutet, mit einem kleinen, laufenden System zu beginnen, einem funktionierenden Teilsystem der beabsichtigten Architektur – der einfachsten Sache, die möglicherweise funktionieren könnte. Dieses entstehende System wird viele wünschenswerte Eigenschaften haben und uns viel über die Architektur lehren können, was ein großes System oder, schlimmer noch, eine Sammlung von Architekturdokumenten niemals kann. Du wirst mit größerer Wahrscheinlichkeit an seiner Implementierung beteiligt gewesen sein. Seine geringe Oberfläche wird einfacher zu testen und daher weniger anfällig für Kopplung sein. Es wird ein kleineres Team erfordern, was die Koordinationskosten des Projekts reduziert. Seine Eigenschaften werden leichter zu beobachten sein. Es wird einfacher bereitzustellen sein. Es wird dich und dein Team zum frühestmöglichen Zeitpunkt lehren, was funktioniert und was nicht. Es wird dir zeigen, wo sich das System nicht leicht weiterentwickeln wird, wo es wahrscheinlich kristallisieren wird, wo es fragil ist. Wo es brechen könnte. Vielleicht am wichtigsten: Es wird für seine Stakeholder von Anfang an verständlich und greifbar sein und es ihnen ermöglichen, ebenfalls in das Gesamtdesign hineinzuwachsen.

Entwirf das kleinste System, das du kannst, hilf es auszuliefern und lass es sich in Richtung der großen Vision entwickeln. Auch wenn sich das vielleicht so anfühlt, als würde man die Kontrolle aufgeben oder sogar seine Verantwortung vernachlässigen, werden dir deine Stakeholder letztendlich dafür danken. Verwechsle einen evolutionären Ansatz nicht damit, Anforderungen wegzuwerfen, das gefürchtete Phasing oder damit, eines zu bauen, um es wegzuwerfen.

von Bill de hÓra

## Related
<!-- openclaw:wiki:related:start -->
### Referenced By

- [[concepts/80-20 Leitfragen|80/20 Leitfragen für Planung & Entscheidungen]]
- [[concepts/80-20 Leitfragen Frontend|80/20 Leitfragen für Software (Frontend)]]
<!-- openclaw:wiki:related:end -->
