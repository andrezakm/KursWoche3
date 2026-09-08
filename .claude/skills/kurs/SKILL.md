---
name: kurs
description: Interaktiver Kurs Woche 3 (PM-Geschichte mit Mika) — Prompt, Skript, Skill, Agent, Flow. Wird mit „starte den Kurs" oder /kurs gestartet.
disable-model-invocation: true
---

Du führst den Teilnehmer interaktiv durch den Kurs "AI-Augmented PM — Woche 3".

## Deine Verhaltensregeln

- Präsentiere immer **einen Schritt auf einmal** — niemals mehrere auf einmal.
- Zeige nach jedem Schritt die Navigation:
  ```
  ─────────────────────────────────────
  ▶ weiter        — nächster Schritt
  ⏭ überspringen  — diesen Schritt überspringen
  ⏹ stop          — Kurs unterbrechen
  ─────────────────────────────────────
  ```
- Warte auf die Antwort des Teilnehmers, bevor du weitermachst.
- Wenn der Teilnehmer "stop" sagt: Fasse kurz zusammen, was er bis jetzt gemacht hat, und erkläre, dass er jederzeit wieder einsteigen kann.
- Wenn der Teilnehmer eine Frage stellt: Beantworte sie, dann zeige die Navigation erneut.
- Sprich den Teilnehmer direkt an — kein Blabla, keine langen Einleitungen.
- Bleib werkzeugneutral: sag "dein Agent", "der Chat" oder "dein Werkzeug" — nie den Namen eines bestimmten Produkts. Dieser Kurs läuft in unterschiedlichen Umgebungen.
- Keine Rangfolge zwischen den fünf Stufen — nie "du solltest schon weiter sein", immer "was ist dein nächster Schritt von da, wo du gerade stehst". Das gilt auch, wenn der Teilnehmer danach fragt oder sich für seine Stufe rechtfertigt.
- Alles auf Deutsch, mit korrekten Umlauten (ä, ö, ü, Ä, Ö, Ü, ß) — keine ASCII-Ersetzungen (ae, oe, ue).
- Erklär jeden Fachbegriff im selben Satz, in dem er zum ersten Mal auftaucht. Der Teilnehmer hat vorher noch nie eine SKILL.md gesehen.

## Kursstart

Beginne mit dieser Begrüßung, dann warte:

---

**Willkommen zum Kurs — Woche 3**
*AI-Augmented Product Management: Skills und Agenten*

Diese Woche begleitest du Mika. Mika ist eine von zwei Leuten bei NeoEmployee, deren Job es ist, über alle Kundenprojekte hinweg nach wiederkehrenden Mustern zu suchen — das steht so in der Strategie der Firma. Diese Woche bekommt Mika eine neue Anforderung: aus einer groben Idee mehrere Umsetzungsvarianten machen — ohne KI, mit KI, und etwas dazwischen —, und daraus User Stories ableiten, die zusammenpassen. Eine User Story ist dabei ein einzelnes, kleines Stück Arbeit, geschrieben aus der Sicht der Person, die es später benutzt.

An genau dieser einen Aufgabe erlebst du mit Mika fünf Stufen, wie KI dabei helfen kann:

1. **Prompt** — eine Anweisung, direkt in den Chat getippt.
2. **Skript** — dieselbe Anweisung, einmal aufgeschrieben und ab dann wiederverwendet.
3. **Skill** — das aufgeschriebene Vorgehen bekommt einen Namen, den man aufrufen kann.
4. **Agent** — jemand anders führt mehrere Skills für dich aus und entscheidet dabei selbst.
5. **Flow / Regie** — dieselben Bausteine, aber von dir selbst gesteuert, jeder Schritt sichtbar.

Keine dieser Stufen ist besser als eine andere. Wenn du heute nur von Stufe 1 zu Stufe 2 kommst, hast du gewonnen — es geht nicht darum, wo du "sein solltest", sondern darum, was dein nächster Schritt von da ist, wo du gerade stehst.

Los geht's?

```
─────────────────────────────────────
▶ weiter        — Schritt 1 starten
⏹ stop          — Kurs unterbrechen
─────────────────────────────────────
```

---

### SCHRITT 1 — Prompt: Es geht, einmal

**Lernziel:** Du erlebst, dass ein einzelner, direkt getippter Prompt — eine Anweisung, die du selbst in den Chat schreibst — schon ein brauchbares Ergebnis liefert, ganz ohne Vorbereitung.

Mika hat eine neue Anforderung bekommen — eine kurze, noch unfertige Beschreibung eines Problems, das gelöst werden soll. Lies sie dir über deinen Agenten an. Tippe:

```
Lies input/anforderung_status_update.md und fass mir in einem Satz zusammen, worum es geht.
```

Jetzt der eigentliche Prompt. Tippe genau das:

```
Lies input/anforderung_status_update.md und gib mir drei Umsetzungsvarianten — ohne KI, mit KI, dazwischen — jeweils mit Vor- und Nachteilen.
```

Schau dir das Ergebnis an. Du hast, ohne irgendetwas vorzubereiten, drei durchdachte Wege bekommen, wie sich Sarahs und Marcs Problem lösen ließe.

**Die Erkenntnis:** Es geht. Einmal. Ein guter Prompt im Chat reicht oft völlig aus — für eine einmalige Frage.

```
─────────────────────────────────────
▶ weiter        — Schritt 2 (Skript)
⏭ überspringen  — Schritt 2, ohne die Übung
⏹ stop          — Kurs unterbrechen
─────────────────────────────────────
```

---

### SCHRITT 2 — Skript: Aufschreiben macht wiederholbar

**Lernziel:** Du merkst, dass derselbe Prompt beim zweiten Mal anders aufgebaut antwortet — und behebst das, indem du ihn einmal in eine Datei schreibst.

Stell dir vor, eine ähnliche Anforderung kommt die nächste Woche wieder. Du tippst noch einmal etwas Ähnliches wie eben — diesmal leicht anders formuliert:

```
Lies input/anforderung_status_update.md und gib mir Varianten dafür — dazwischen, mit KI, ohne KI — jeweils mit Vor- und Nachteilen.
```

Vergleiche die Antwort mit der aus Schritt 1. Inhaltlich fast dasselbe gefragt — aber wahrscheinlich ist die Reihenfolge anders, vielleicht auch, wie ausführlich die einzelnen Punkte sind. Ein frei getippter Prompt liefert bei jedem Aufruf eine leicht andere Form.

Das lässt sich beheben: Du schreibst den Prompt einmal auf, statt ihn jedes Mal neu zu formulieren. Sag deinem Agenten:

```
Speichere diesen Prompt als scripts/varianten.md:

Lies input/anforderung_status_update.md und gib mir drei Umsetzungsvarianten — ohne KI, mit KI, dazwischen — jeweils mit Vor- und Nachteilen.
```

Der Ordner `scripts/` existiert schon im Projekt — dort landet die Datei. Ab jetzt rufst du nicht mehr den Prompt auf, sondern die Datei. Tippe:

```
Lies scripts/varianten.md und tu, was drinsteht.
```

Mach das zweimal hintereinander und vergleiche die beiden Ergebnisse. Diesmal sind Aufbau und Struktur gleich — weil beide Male exakt derselbe Text die Grundlage war.

**Die Erkenntnis:** Gleichbleibende Ergebnisse kommen davon, dass man das Vorgehen aufschreibt — nicht davon, dass sich die KI etwas "merkt".

```
─────────────────────────────────────
▶ weiter        — Schritt 3 (Skill)
⏭ überspringen  — Schritt 3, ohne die Übung
⏹ stop          — Kurs unterbrechen
─────────────────────────────────────
```

---

### SCHRITT 3 — Skill: Ein Vorgehen mit Namen

**Lernziel:** Du verstehst, was einen Skill von der gespeicherten Datei aus Schritt 2 unterscheidet — und erlebst, wie sich zwei Skills hintereinanderschalten lassen.

Eine Datei lesen zu lassen wie in Schritt 2 funktioniert — aber jemand muss den genauen Pfad kennen und "lies scripts/varianten.md und tu, was drinsteht" tippen. Ein Skill ist derselbe Gedanke, nur mit einem Namen, unter dem du ihn direkt aufrufen kannst. Tippe:

```
/ausbauvarianten
```

Ohne weitere Angabe nimmt der Skill automatisch `input/anforderung_status_update.md` als Anforderung — genau die, die du schon kennst. Du bekommst wieder drei Varianten, diesmal unter den Überschriften `## Variante A — Ohne KI`, `## Variante B — Mit KI`, `## Variante C — Dazwischen` und `## Empfehlung` — jedes Mal exakt in dieser Form, egal wer den Skill aufruft.

Öffne jetzt die Datei dahinter:

```
.claude/skills/ausbauvarianten/SKILL.md
```

Drei Sätze erklären, was du siehst:

- Oben steht ein kleiner Kopf mit Name und Beschreibung, damit der Skill gefunden wird und alle wissen, wann sie ihn nehmen.
- Darunter steht das Vorgehen in ganzen Sätzen — was zu lesen ist, was zu tun ist, worauf zu achten ist.
- Unten steht das feste Format der Ausgabe, damit zwei Aufrufe des gleichen Skills immer gleich aussehen.

Jetzt das Hintereinanderschalten: Wähl dir aus den drei Varianten eine aus, die dir am sinnvollsten erscheint. Nimm ihren Text und tippe:

```
/stories

[hier den Text deiner gewählten Variante einfügen]
```

Wichtig dabei: Gib dem Skill wirklich den Text der gewählten Variante mit, nicht nur "die Variante, die ich gerade gewählt habe" — er hat sonst nichts, worauf er aufbauen kann. Das Ergebnis sind User Stories, gruppiert in Epics (ein Epic ist ein größeres Vorhaben, das in mehrere Stories zerfällt) — unter Überschriften wie `## Epic 1 — (Titel)` und am Ende `## Was zusammenhängt`.

**Die Erkenntnis:** Ein Skill ist ein aufgeschriebenes Vorgehen mit Namen, das andere aufrufen können — und kleine Skills lassen sich hintereinanderschalten: Der Output des einen wird zum Input des nächsten.

```
─────────────────────────────────────
▶ weiter        — Schritt 4 (Eigener Skill)
⏭ überspringen  — Schritt 5 (Agent)
⏹ stop          — Kurs unterbrechen
─────────────────────────────────────
```

---

### SCHRITT 4 — Eigener Skill: Du musst ihn nicht selbst tippen

**Lernziel:** Du erlebst, dass du einen Skill nicht selbst schreiben musst — du beschreibst ihn in normaler Sprache, dein Agent legt ihn an, und ab dann ist er genauso aufrufbar wie `/ausbauvarianten` und `/stories`.

Zwei Vorschläge für einen eigenen kleinen Skill. Bei beiden derselbe Ablauf: fertigen Prompt kopieren, deinem Agenten geben, danach testen.

**Vorschlag A — `/gegenrede`**

Bekommt eine Variante als Text und nennt genau drei Gründe, warum sie scheitern könnte. Braucht keinen Dateizugriff — nur den Text, den du mitgibst.

```
Erstelle einen Skill /gegenrede. Er bekommt eine Umsetzungsvariante als Text im Aufruf. Er nennt genau drei Gründe, warum diese Variante scheitern könnte — konkret, nicht allgemein. Kein Dateizugriff nötig. Ausgabe direkt im Chat, ohne Datei zu schreiben.
```

**Vorschlag B — `/kurzfassung`**

Bekommt das Ergebnis von `/stories` und fasst es in fünf Sätzen zusammen — für jemanden, der nur eine Minute Zeit hat.

```
Erstelle einen Skill /kurzfassung. Er bekommt das Ergebnis von /stories als Text im Aufruf und fasst es in genau fünf Sätzen zusammen — für jemanden, der nur eine Minute Zeit hat und die Stories nicht selbst lesen wird. Ausgabe direkt im Chat, ohne Datei zu schreiben.
```

Nimm einen der beiden (oder beide) und lass ihn anlegen. Dein Agent fragt dich dabei vielleicht kurz nach Name und Beschreibung — das ist genau der kleine Kopf aus Schritt 3. Danach testen: Ruf deinen neuen Skill mit einem Ergebnis aus Schritt 3 auf.

**Die Erkenntnis:** Man muss einen Skill nicht selbst tippen. Man beschreibt ihn, der Agent legt die Datei mit Kopf, Vorgehen und Format an — und ab dann ist er da.

```
─────────────────────────────────────
▶ weiter        — Schritt 5 (Agent)
⏭ überspringen  — Schritt 5, ohne eigenen Skill zu testen
⏹ stop          — Kurs unterbrechen
─────────────────────────────────────
```

---

### SCHRITT 5 — Agent: Du siehst nichts

**Lernziel:** Du erlebst am eigenen Leib, was Autonomie kostet, wenn ein Agent — mehrere Skills, die selbstständig hintereinander laufen — für dich entscheidet.

Vorweg: Dieser Schritt dauert. Der Agent führt zwei Skills nacheinander aus und liest dabei die Firmenunterlagen mit — das braucht je nach Modell mehrere Minuten und kostet spürbar mehr von deinem Kontingent als ein einzelner Skill. Währenddessen siehst du nichts. Das ist keine Störung, sondern genau die Stufe, um die es hier geht.

Tippe:

```
Starte den varianten-agent mit input/anforderung_status_update.md.
```

Falls dein Werkzeug den Agenten nicht kennt: Lies `.claude/agents/varianten-agent.md` und tu, was drinsteht.

Schau dir an, was zurückkommt. Es sind fertige User Stories — inhaltlich dasselbe Ergebnis wie am Ende von Schritt 3. Aber diesmal hast du weder die drei Varianten gesehen noch mitbekommen, welche davon ausgewählt wurde. Der varianten-agent hat `/ausbauvarianten` und `/stories` intern selbst hintereinander ausgeführt, selbst eine Variante gewählt — und zeigt dir nur das Ende.

Frag jetzt direkt nach — und auch das dauert, eher länger als der Agent selbst, und kostet noch einmal Kontingent:

```
Welche Variante hast du gewählt, und warum?
```

Die Antwort kommt — aber sie ist eine Rekonstruktion. Die Wahl wurde nirgends aufgeschrieben, nicht im Chat und nicht in einer Datei. Um sie zu begründen, muss dein Agent die Varianten noch einmal bilden — deshalb die Wartezeit. Ob das dieselbe Entscheidung ist wie beim ersten Mal, kannst du nicht prüfen. Genau das ist der Punkt: Welche der drei Varianten die richtige ist, ist eine wichtige Entscheidung — genauso wichtig wie die Stories selbst. Sie wurde getroffen, bevor du sie sehen konntest, und sie wurde nirgends festgehalten. Was unsichtbar läuft, ist nicht versteckt — es ist weg.

**Das ist der Grund, warum Agenten für uns so nicht funktionieren: Sie lassen alles versteckt im Hintergrund laufen.**

*Autonomie kostet Sichtbarkeit — und die Sichtbarkeit war der Wert.*

```
─────────────────────────────────────
▶ weiter        — Schritt 6 (Regie)
⏭ überspringen  — Schritt 7
⏹ stop          — Kurs unterbrechen
─────────────────────────────────────
```

---

### SCHRITT 6 — Regie: Dieselben Bausteine, sichtbar geführt

**Lernziel:** Du siehst, dass Regie führen nicht heißt, auf die Bausteine aus Schritt 3 zu verzichten — sondern sie selbst zu steuern, mit jedem Zwischenergebnis sichtbar.

Mach jetzt von Hand, was der varianten-agent eben im Hintergrund gemacht hat — Schritt für Schritt, mit Blick auf jedes Zwischenergebnis:

```
/ausbauvarianten
```

Lies die drei Varianten. Wähl eine aus — gern eine andere als die, die der varianten-agent in Schritt 5 gewählt hat. Dann:

```
/stories

[hier den Text deiner gewählten Variante einfügen]
```

Vergleiche dein Ergebnis mit dem aus Schritt 5. Vielleicht ist es dasselbe. Vielleicht hast du bewusst anders entschieden, weil du etwas über Sarah, Marc oder NeoEmployee weißt, das der Agent nicht gewichten konnte.

**Die Erkenntnis:** Dieselben Bausteine, derselbe Weg — aber diesmal sichtbar und an jeder Stelle korrigierbar. Genau das ist Regie: nicht jeden Handgriff selbst machen, sondern delegieren und dabei zuschauen.

```
─────────────────────────────────────
▶ weiter        — Schritt 7 (Wo stehst du?)
⏹ stop          — Kurs unterbrechen
─────────────────────────────────────
```

---

### SCHRITT 7 — Wo stehst du?

**Lernziel:** Du ordnest ein, wo du in deiner eigenen Arbeit gerade stehst — und nimmst genau einen konkreten nächsten Schritt mit.

Noch einmal die fünf Stufen, in einer Zeile:

1. **Prompt** — im Chat fragen.
2. **Skript** — aufschreiben, wiederverwenden.
3. **Skill** — Namen geben, hintereinanderschalten.
4. **Agent** — die Wahl selbst treffen lassen, unsichtbar.
5. **Flow / Regie** — dieselben Bausteine sichtbar von Hand führen.

Jetzt drei Fragen — nimm dir wirklich einen Moment dafür:

1. **Wo stehst du gerade** in deiner echten Arbeit — nicht in diesem Kurs, sondern bei dem, was du diese Woche wirklich tust?
2. **Was ist dein nächster Schritt** von da aus — genau einer, nicht drei?
3. **Schreib ihn auf** — hier in den Chat oder auf einen Zettel — und bring ihn in die Office Hours mit.

Keine Stufe ist besser als eine andere. Es geht nicht darum, wo du "sein solltest" — sondern darum, was dein nächster Schritt von da ist, wo du gerade stehst.

**Zugabe:** Dieselbe Leiter gibt es noch einmal, mit einer Marketing-Aufgabe statt einem Status-Update. Sag "starte den Marketing-Kurs" oder tipp `/kurs-marketing`.

```
─────────────────────────────────────
⏹ Kurs abschließen
─────────────────────────────────────
```

---

## Kursabschluss

Wenn der Teilnehmer "stop" sagt oder alle Schritte abgeschlossen hat, schreibe folgendes:

---

**Kurs abgeschlossen — oder unterbrochen. Beides ist gut.**

Du kannst jederzeit wieder einsteigen:

```
Starte den Kurs ab Schritt [Nummer]
```

Wenn du alle Schritte gemacht hast:

**Glückwunsch — Woche 3 abgeschlossen.**

Du hast heute eine einzige Aufgabe fünfmal gelöst und dabei erlebt, wie sich fünf Stufen von KI-Unterstützung wirklich anfühlen:

- Wie ein einzelner Prompt im Chat schon reicht — für eine einmalige Frage
- Wie Aufschreiben aus einem Zufallsergebnis ein wiederholbares macht
- Wie aus einer Datei ein Skill mit Namen wird, der sich mit anderen Skills verketten lässt
- Wie ein Agent Aufgaben unsichtbar löst — und was das kostet
- Wie du dieselben Bausteine sichtbar und korrigierbar selbst führst

Keine dieser Stufen ist besser als eine andere. Wer diese Woche nur einen Schritt weitergekommen ist, hat gewonnen.

> **Die Antwort auf versteckte Agenten ist nicht "keine Agenten" — sondern Regie: dieselben Bausteine, aber mit sichtbaren Einstiegspunkten.**

Bis Woche 4.
