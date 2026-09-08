# Woche 3: Script vs. Skill vs. Agent

Diese Woche lernst du, wie aus einer einmaligen Bitte an deinen Agenten etwas Zuverlässiges wird — etwas, das beim zehnten Mal genauso gut läuft wie beim ersten. Der Weg dahin hat fünf Stufen: **Prompt** — du fragst einmal, im Chat. **Skript** — du speicherst die Bitte als Datei, damit sie beim nächsten Mal genauso läuft. **Skill** — die Datei bekommt einen festen Namen und ein festes Format, sodass jeder im Team sie aufrufen kann. **Agent** — mehrere Skills werden zu einem Ablauf verkettet, der selbst entscheidet und dir nur das Ergebnis zeigt. **Flow** — dieselben Skills, aber von dir selbst geführt: du siehst jedes Zwischenergebnis und greifst ein, wo es nötig ist. Keine Stufe ist besser als eine andere: Ein Prompt ist nicht die Vorstufe von etwas Höherem, und ein Agent ist nicht das Ziel. Es geht darum, herauszufinden, welche Stufe zu deiner eigenen nächsten Aufgabe passt.

Du gehst diese Leiter zweimal durch, an derselben Art von Aufgabe bei NeoEmployee, nur mit unterschiedlichen Hauptfiguren. Mika arbeitet im Produktmanagement und macht aus einer Anforderung erst Umsetzungsvarianten, dann User Stories. Lena arbeitet im Marketing und macht aus einem Briefing erst Kernbotschaften, dann Kanaltexte. Beide Geschichten durchlaufen dieselben fünf Stufen — nur die Aufgabe und die Rolle sind verschieden.

## Für wen welcher Kurs

- **Product Manager:** `/kurs` — Mikas Geschichte.
- **Alle anderen Rollen, besonders Marketing:** `/kurs-marketing` — Lenas Geschichte.

Beide Kurse sind dieselbe Leiter, nur mit einer anderen Aufgabe. Am Ende jedes Kurses ist der jeweils andere die Zugabe — probier ihn aus, wenn du sehen willst, wie sich dieselben fünf Stufen aus einer fremden Rolle anfühlen.

## Voraussetzungen

Deine Arbeitsumgebung steht schon: **Visual Studio Code mit GitHub Copilot** — genau so, wie wir es in Modul 0 eingerichtet haben.

Falls du Modul 0 noch nicht gemacht hast: Die Anleitung mit Video findest du auf der Lernplattform unter „Woche 0 — Willkommen und Installation".

Woche 1 und Woche 2 sind hilfreich, aber nicht zwingend.

## Installation

### Schritt 1 — Kursordner herunterladen

Klicke auf dieser GitHub-Seite auf den grünen **Code**-Button → **Download ZIP**.

Entpacke die ZIP-Datei:

- **Windows:** Rechtsklick auf die Datei → **„Alle extrahieren"** → **„Extrahieren"**. (Nicht nur doppelklicken — dann stecken die Dateien noch im Archiv.)
- **Mac:** Doppelklick genügt.

### Schritt 2 — Ordner in VS Code öffnen

In VS Code: **File → Open Folder** → den entpackten Ordner `KursWoche3-main` wählen — den Ordner, in dem direkt die Datei `CLAUDE.md` liegt, nicht eine Ebene darüber. Beim ersten Öffnen fragt VS Code nach Vertrauen: **„Yes, I trust the authors"**.

### Schritt 3 — Chat öffnen, Agent-Modus wählen

- Chat öffnen: das Chat-Symbol oben — oder `Strg+Alt+I` (Windows) / `Ctrl+Cmd+I` (Mac)
- Im Chatfenster die Modus-Auswahl auf **„Agent"** stellen

## Kurs starten

**Product Management — Mikas Geschichte:**
```
/kurs
```
Oder sag einfach: "starte den Kurs" oder "los geht's".

**Marketing — Lenas Geschichte:**
```
/kurs-marketing
```
Oder sag: "starte den Marketing-Kurs".

Während des Kurses kannst du jederzeit:
- **weiter** sagen, um zum nächsten Schritt zu gehen
- **überspringen** sagen, um einen Schritt zu überspringen
- **stop** sagen, um den Kurs zu unterbrechen

Wieder einsteigen, an einer bestimmten Stelle:
```
Starte den Kurs ab Schritt 4
```

## Dateistruktur

| Pfad | Rolle |
|---|---|
| `CLAUDE.md` | Projekt-Prinzipien, immer aktiv |
| `README.md` | Diese Datei |
| `.claude/skills/kurs/` | Kurspfad Product Management — Mikas Geschichte (`/kurs`) |
| `.claude/skills/kurs-marketing/` | Kurspfad Marketing — Lenas Geschichte (`/kurs-marketing`) |
| `.claude/skills/ausbauvarianten/` | Skill: aus einer Anforderung drei Umsetzungswege ableiten |
| `.claude/skills/stories/` | Skill: aus einer Umsetzungsvariante User Stories ableiten |
| `.claude/skills/botschaften/` | Skill: aus einem Briefing Kernbotschaften ableiten |
| `.claude/skills/kanaltexte/` | Skill: aus einer Kernbotschaft Kanaltexte schreiben |
| `.claude/agents/varianten-agent.md` | Agent: Anforderung → fertige Stories, wählt die Variante selbst |
| `.claude/agents/kampagnen-agent.md` | Agent: Briefing → drei fertige Kanaltexte, wählt die Kernbotschaft selbst |
| `context/` | Wer NeoEmployee ist und welche Strategie dahintersteht |
| `input/` | Beispiel-Inputs (`anforderung_status_update.md`, `briefing_marketing.md`) und `raw_feedback/` |
| `scripts/` | Hier landen deine eigenen Skripte |
| `output/` | Platz für eigene Ergebnisse — die Kurs-Skills antworten im Chat und legen hier nichts ab |

## Welches Modell?

Beide Agenten führen je zwei Skills nacheinander aus. Nimm im Copilot-Modell-Auswahlmenü ein **starkes** Modell — mit einem schwächeren Modell wird diese Kette leicht unscharf.

## Hinweis: Nutzungslimits

Copilot arbeitet mit Anfrage-Kontingenten deiner CLAAS-Lizenz. Die einzelnen Skills in diesem Kurs sind klein — ein Aufruf, eine Antwort im Chat. Die beiden Agenten (`varianten-agent`, `kampagnen-agent`) führen dafür zwei Skills automatisch hintereinander aus, das ist etwas schwerer als ein einzelner Aufruf. Bittet Copilot dich bei intensiver Nutzung kurz zu warten, ist das normal.

## Weiterführend

Die erste Fassung dieser Woche hatte ein größeres System: drei Analyse-Skills und einen Agenten, der sie orchestriert, samt Notizen darüber, was beim Bauen schiefging. Es liegt im Branch `v1-drei-schichten` dieses Repositories — für alle, die sehen wollen, wie ein größerer Agent aussieht. Für den Kurs brauchst du es nicht.

## Probleme?

- **Falscher Ordner geöffnet:** Achte darauf, dass direkt in deinem geöffneten Ordner die Datei `CLAUDE.md` liegt — nicht eine Ebene darüber oder darunter.
- **Der Agent findet die Dateien nicht:** Meistens derselbe Grund wie oben — prüfe, ob du wirklich den Ordner mit `CLAUDE.md` direkt darin geöffnet hast.
- **Skill wird nicht gefunden:** Der Ordnername unter `.claude/skills/` ist gleichzeitig der Befehl. `/kurs` startet nur, wenn der Ordner `.claude/skills/kurs/` heißt.
- **Der Agent zeigt nur das Endergebnis, keine Zwischenschritte:** Das ist Absicht, siehe Schritt 5 im Kurs.
- Bei allem anderen: Nachricht an Markus.
