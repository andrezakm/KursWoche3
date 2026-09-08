# Kursumgebung: AI-Augmented PM — Woche 3

## Wer wir sind

NeoEmployee baut custom AI Agenten, die Mitarbeiterfähigkeiten in Unternehmen ersetzen. Wir arbeiten als Beratung auf Time-&-Material-Basis. Wir sind bootstrapped — Revenue ist Runway. Unser langfristiges Ziel sind produktisierbare Agenten, die branchenübergreifend einsetzbar sind. Details in `context/company.md` und `context/strategy.md`.

## Pfadkonventionen

- Beispiel-Inputs liegen in `input/`
- Rohes Feedback liegt in `input/raw_feedback/`
- Kontext-Dateien liegen in `context/`
- Eigene Skripte liegen in `scripts/`
- Skills liegen in `.claude/skills/`, Agenten in `.claude/agents/`
- Alle Outputs landen in `output/`

## Sprache

Alle Outputs immer mit korrekten deutschen Umlauten: ä, ö, ü, Ä, Ö, Ü, ß. Keine ASCII-Ersetzungen (ae, oe, ue).

## Qualitätsstandard

Keine Spekulation. Nur was in den Daten steht. Jede Aussage muss auf eine Quelldatei rückverfolgbar sein. Widersprüche werden dokumentiert, nicht geglättet.

## Kurs starten

Sobald der Nutzer "starte den Kurs", "los geht's" oder ähnliches sagt — führe `/kurs` aus. Starte ohne Vorrede.

Sobald der Nutzer "starte den Marketing-Kurs", "Marketing-Kurs" oder ähnliches sagt — führe `/kurs-marketing` aus. Starte ohne Vorrede.

Sagt der Nutzer nur "weiter", führe den zuletzt gestarteten Kurs fort.
