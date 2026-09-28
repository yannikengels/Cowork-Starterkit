# Meetings/

Notizen aus Meetings.

## Struktur

- `Recurring/{Name}/` für wiederkehrende Termine (1:1s, Weeklies), eine Datei pro Termin
- `One-off/` für einmalige Meetings, Dateiname `JJJJ-MM-TT-name-thema.md`

## Vorlage

```markdown
# [Meeting] [Name / Thema] · JJJJ-MM-TT

## Agenda
- ...

## Notizen
- ...

## Entscheidungen
- ...

## Aufgaben
- [ ] [Wer]: [Was] bis [Wann]

## Offen für nächstes Mal
- ...
```

## Routing

Aufgaben wandern nach `../TASKS.md`, Entscheidungen zu einem Projekt nach `../Projects/`.
