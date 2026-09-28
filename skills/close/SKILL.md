---
name: close
description: "Speichert am Ende eines Gesprächs eine kompakte Zusammenfassung in memory.md im Arbeitsordner, damit die nächste Session weiß, was besprochen und entschieden wurde. Auslösen bei /close, merk dir das, halt das Gespräch fest, sichere den Chat."
---

# /close: Gesprächs-Gedächtnis

Fasst das **aktuelle Gespräch** kompakt zusammen und hängt es an eine fortlaufende
Datei `memory.md` im Arbeitsordner an. Der Nutzer tippt nur `/close` und hat das
Wichtigste dauerhaft gesichert, ohne selbst zu formulieren.

## Grundprinzip

- **Eine zentrale Datei:** alles landet in `memory.md`, chronologisch angehängt.
- **Kompakt, aber vollständig:** Thema, Kernpunkte, Ergebnisse, offene Punkte.
  Kein Roman, aber nichts Zentrales weglassen.
- **Sprache:** wie in `CLAUDE.md` festgelegt. Sachlich und knapp.
- **Nicht nachfragen.** Zusammenfassung bauen, speichern, kurz bestätigen. Nur
  nachfragen, wenn der Arbeitsordner nicht erreichbar ist.

## Schritt 1: Zusammenfassung bauen

Das bisherige Gespräch durchgehen und auf das Wesentliche verdichten. Genau
dieses Format:

```
## JJJJ-MM-TT · <kurzer, aussagekräftiger Titel>

**Worum ging's:** 1 bis 2 Sätze, die das Gespräch einordnen.
**Wichtigste Punkte:** die zentralen Inhalte, kompakt.
**Ergebnisse / Entscheidungen:** was konkret rauskam oder entschieden wurde.
**Offene Punkte / nächste Schritte:** nur, wenn es welche gibt.
```

- Datum = heutiges Datum. Nie raten.
- Der Titel macht das Gespräch später auf einen Blick wiedererkennbar, nicht
  generisch („Chat“).
- Details, die man später nachschlagen will (eine Zahl, ein Dateiname, ein
  Beschluss), kommen rein.
- Keine Meta-Sätze wie „In diesem Gespräch haben wir …“.
- Nichts behaupten, was im Gespräch nicht belegt wurde. Annahmen mit ⚠️.

## Schritt 2: Speichern

- Die Datei heißt immer `memory.md` und liegt in der Wurzel des Arbeitsordners,
  neben `CLAUDE.md`.
- Existiert sie: erst lesen, dann den neuen Eintrag mit einer Leerzeile Abstand
  **ans Ende** anhängen.
- Existiert sie nicht: neu anlegen, beginnend mit diesem Kopf:

```
# Gesprächs-Gedächtnis

Kompakte Zusammenfassungen wichtiger Gespräche. Neueste Einträge unten.
```

- Aufgaben aus dem Gespräch zusätzlich in `TASKS.md`, Projektstand nach
  `Projects/`, wie in `CLAUDE.md` beschrieben.
- Ist der Arbeitsordner nicht erreichbar: Datei ausliefern und in einem Satz
  sagen, wohin sie gehört.

## Schritt 3: Bestätigen

Eine kurze Zeile, zum Beispiel:

> Gespeichert in `memory.md`: „Titel“ (heute).

Keine Wiederholung des Inhalts.

## Wichtig

- **Bestehende Einträge nie überschreiben oder kürzen.** Immer nur anhängen.
  Schlägt das Lesen der alten Datei fehl: stoppen und nachfragen, statt sie mit
  nur dem neuen Eintrag zu überschreiben.
- Nur das aktuelle Gespräch zusammenfassen, frühere Einträge nicht neu bewerten.
