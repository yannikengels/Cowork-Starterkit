# Skills

Drei fertige Skills, die mit dem Starterkit zusammenspielen:

| Skill | Was er macht | Braucht |
|---|---|---|
| `/overview` | Morning Briefing: Kalender, Mail, Chat und `TASKS.md` in 60 Sekunden, mit den Top 3 für heute. | Kalender, Mail, optional Chat |
| `/tov` | Lernt einmalig deinen Schreibstil aus gesendeten Nachrichten. Danach klingt jeder Entwurf nach dir. | Mail, optional Chat |
| `/close` | Hält am Ende eines Gesprächs das Wichtigste in `memory.md` fest. Die nächste Session weiß, was besprochen wurde. | nichts |

## Installieren

_Stand September 2026. Die Oberfläche von Claude ändert sich öfter. Wenn ein
Menüpunkt anders heißt, frag einfach Claude selbst._

1. In den Einstellungen die **Code-Ausführung** aktivieren (Voraussetzung für Skills).
2. In Claude zu **Customize → Skills** gehen.
3. Auf **+** klicken, dann **Create skill** → **Upload a skill**.
4. `overview.zip` hochladen. Dasselbe für `tov.zip` und `close.zip`.
5. Fertig. Die Skills tauchen in deiner Liste auf und lassen sich ein- und ausschalten.

Die ZIPs liegen in diesem Ordner. Wer lieber selbst packt: den Ordner
(`overview/`, `tov/` bzw. `close/`) als ZIP komprimieren. Der Ordnername muss zum Skill-Namen passen.

## Loslegen

- `/overview` tippen. Oder einfach: „Was steht heute an?“
- `/tov` einmal laufen lassen. Danach gilt der Stil automatisch für jeden Entwurf.
  Sagst du „klingt nicht nach mir“, schärft der Skill nach.
- `/close` am Ende eines längeren Gesprächs. `memory.md` legt sich beim ersten Mal selbst an.

## Anpassen

Die Skills sind einfache Textdateien (`SKILL.md`). Öffnen, ändern, neu hochladen.
Oder Claude bitten: „Pass den overview-Skill so an, dass er auch mein
Projektmanagement-Tool scannt.“
