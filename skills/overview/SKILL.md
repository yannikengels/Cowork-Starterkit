---
name: overview
description: "Morning Briefing auf Abruf: scannt Kalender, Mail, Chat und TASKS.md und sagt in 60 Sekunden, was heute zählt. Auslösen bei /overview, Tagesüberblick, was steht heute an, Morning Briefing."
---

# /overview: Morning Briefing

Ein Befehl, ein Überblick. Nach 60 Sekunden Lesen weiß der Nutzer, was heute
zählt, was liegen bleiben kann und wo etwas hängt.

**Stil:** in der Sprache aus `CLAUDE.md`, kompakt, Antwort zuerst, keine Floskeln.

**Nur lesen.** Dieser Skill sendet nichts, beantwortet nichts, verschiebt keine
Termine. Will der Nutzer danach etwas senden, ist das ein eigener Auftrag.

## Schritt 0: Rahmen setzen

1. Aktuelles Datum und Uhrzeit holen. Nie raten.
2. `CLAUDE.md` im Arbeitsordner lesen: Name, Rolle, Team, Tools, wichtige Channels,
   Präferenzen. Daraus ergibt sich, was für diese Person „wichtig“ heißt.
3. Zeitfenster:
   - Standard: **heute** plus alles Unbeantwortete der **letzten 3 Tage**.
   - `/overview morgen` → morgen. `/overview woche` → die nächsten 7 Tage.
   - Nach 15 Uhr zusätzlich die ersten Termine von morgen als Einzeiler.

**Nicht zurückfragen.** Einfach scannen und liefern.

## Schritt 1: Quellen scannen (parallel)

Alle verbundenen Quellen in einem Zug abfragen. Fehlt ein Connector oder schlägt
eine Abfrage fehl: nicht abbrechen, sondern am Ende unter „Nicht gescannt“ vermerken.

### Kalender

- Alle Termine im Zeitfenster, inklusive Ganztägigem und Abwesenheiten.
- Pro Termin: Zeit, Titel, Teilnehmende (intern oder extern), Zusagestatus,
  Agenda vorhanden ja oder nein.
- Flaggen: **Überschneidungen**, externe Termine **ohne Agenda**, Blöcke **ohne
  Puffer** (unter 10 Minuten), **nicht beantwortete** Einladungen.

### Mail

1. **Neu und ungelesen** im Posteingang, letzte 2 Tage.
2. **Wartet auf mich:** Threads der letzten 3 Tage, deren letzte Nachricht nicht
   vom Nutzer ist.
3. **Wartet auf andere:** Threads, in denen der Nutzer zuletzt geschrieben hat und
   seit mehr als 3 Werktagen keine Antwort kam. Die stillen Hänger.

Newsletter, Benachrichtigungen und automatische Mails nicht einzeln listen, nur
als Sammelzeile: „12 Newsletter und Automatische ignoriert.“

### Chat (z. B. Slack, Teams)

- Erwähnungen des Nutzers seit dem letzten Werktag.
- Direktnachrichten ohne Antwort des Nutzers.
- Threads, in denen der Nutzer geschrieben und danach jemand geantwortet hat.
- Die in `CLAUDE.md` genannten wichtigen Channels überfliegen: nur Entscheidungen,
  Fragen, Blocker, Deadlines.

### TASKS.md

- Offene Einträge (`- [ ]`) aus „In Arbeit“ und „Diese Woche“.
- Backlog nur, wenn oben weniger als 5 offene Einträge stehen.
- Erledigte Einträge (`- [x]`) sind Ground Truth und werden nie als offen gemeldet.

### Weitere Tools

Steht in `CLAUDE.md`, dass Aufgaben in einem anderen Tool liegen (Projektmanagement,
CRM), dort nur offene Aufgaben mit Fälligkeit heute oder überfällig ziehen.

## Schritt 2: Priorisieren

Reihenfolge, von oben nach unten:

1. **Harte Zeitbindung heute:** Termine, Deadlines, Zusagen für heute.
2. **Jemand wartet auf den Nutzer:** je älter, desto höher. Extern vor intern.
3. **Der Nutzer wartet und es hängt:** Nachfassen nötig.
4. **Vorbereitung nötig:** Termin heute, der Prep braucht.
5. **Eigene Aufgaben** aus `TASKS.md`.

**Genau drei Top-Punkte.** Gibt es nur zwei, dann zwei. Nie zehn.

## Schritt 3: Ausgeben

Nur im Chat, keine Datei. Format:

```
**Di, 6. Okt** · 3 Termine · 4 offene Antworten · 2 Aufgaben fällig

### Top 3 heute
1. [Was] · [warum jetzt, max. 10 Wörter]
2. …
3. …

### Kalender
- 09:30 bis 10:00 · Team-Weekly · intern
- 14:00 bis 15:00 · [Firma] Kickoff · extern · ⚠️ keine Agenda

### Wartet auf dich
- [Absender] · [Thema in 5 Wörtern] · seit 2 Tagen · Mail

### Hängt (du hast zuletzt geschrieben)
- [Empfänger] · [Thema] · seit 6 Tagen keine Antwort

### Offene Aufgaben
- [Eintrag aus TASKS.md]

### Freie Zeit
11:00 bis 13:00 (2 h) · 15:30 bis 17:00 (1,5 h)

_Rest: 12 Newsletter, 9 Channel-Nachrichten ohne Handlungsbedarf._
⚠️ Nicht gescannt: [Quelle]
```

- Leere Blöcke weglassen.
- Eine Zeile pro Eintrag: wer, was, wie alt.
- Namen ausschreiben, nicht „ein Kunde“.
- Bei unsicherer Zuordnung ⚠️ statt raten.

## Schritt 4: Proaktiv flaggen

Maximal drei kurze Hinweise unter den Top 3, wenn zutreffend:

- Externer Termin heute ohne Agenda oder Vorbereitung.
- Termine überlappen oder haben keinen Puffer.
- Externe Mail seit über 48 Stunden unbeantwortet.
- Aufgabe in `TASKS.md` seit über 14 Tagen offen.
- Termin mit jemandem, zu dem es Notizen in `Meetings/` gibt.
- Tag zu über 80 Prozent verplant, keine Fokuszeit.

## Varianten

| Aufruf | Verhalten |
|---|---|
| `/overview` | Heute |
| `/overview morgen` | Morgen |
| `/overview woche` | Nächste 7 Tage, Termine und Deadlines |
| `/overview mail` | Nur Mail |
| `/overview chat` | Nur Chat |
| `/overview kurz` | Nur Top 3 und Kalender |

## Als geplante Aufgabe

Läuft der Skill zeitgesteuert statt im Live-Chat: keine Rückfragen, Annahmen in
einer Zeile oben nennen, Rest normal liefern.

## Danach

Nicht ungefragt weiterarbeiten. Eine Zeile anbieten, was der nächste Schritt wäre:

> Einen Schritt weiter: Soll ich Antworten auf die drei ältesten Mails vorbereiten?

Entwürfe nur zeigen, nie senden.

## Fehlerfälle

- **Connector fehlt:** Quelle unter „Nicht gescannt“, einmal erwähnen, wie man
  sie verbindet.
- **Nichts gefunden:** gültiges Ergebnis. Ein Satz: „Heute ist wenig los:
  [Termine]. Nichts wartet auf dich.“ Nichts erfinden.
