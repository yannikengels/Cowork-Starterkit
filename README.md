# Cowork Starterkit

Ein Arbeitsordner für Claude Cowork, der Claude in 15 Minuten zu einem Kollegen
macht, der dein Unternehmen, deine Rolle und deine Tools kennt. Und der ein paar
feste Werte mitbringt: Er denkt einen Schritt weiter, widerspricht, wenn etwas
nicht passt, und behauptet nichts, was er nicht geprüft hat.

## So funktioniert's

Claude liest bei jeder Aufgabe die `CLAUDE.md` in diesem Ordner. Dort steht, wer
du bist, wie dein Unternehmen tickt, welche Tools du nutzt und nach welchen
Regeln Claude arbeitet. Die Datei musst du nicht selbst schreiben: Der
Setup-Prompt interviewt dich und füllt sie aus.

Dazu kommt eine einfache Gedächtnis-Struktur. Aufgaben, Projekte und
Meeting-Notizen landen in Dateien, damit Claude in der nächsten Session weiß,
wo ihr stehen geblieben seid.

## In 4 Schritten startklar

1. **Ordner herunterladen.** Oben rechts auf `Code` → `Download ZIP`, entpacken
   und an einen festen Ort legen, zum Beispiel `Dokumente/Cowork`.
2. **Ordner in Cowork verbinden.** Claude Desktop öffnen, zu Cowork wechseln und
   den Ordner als Arbeitsordner auswählen.
3. **Setup starten.** Den Prompt aus `SETUP-PROMPT.md` kopieren und als erste
   Nachricht einfügen. Claude interviewt dich in kurzen Runden (ca. 15 Minuten).
4. **Skills installieren (optional).** Zwei fertige Skills liegen unter `skills/`.
   Anleitung in `skills/README.md`.

Danach einfach arbeiten. Claude kennt ab jetzt deinen Kontext.

## Was drin ist

| Datei / Ordner | Wofür |
|---|---|
| `CLAUDE.md` | Dein Kontext und Claudes Werte. Wird beim Setup ausgefüllt. |
| `SETUP-PROMPT.md` | Das Interview, das `CLAUDE.md` füllt. |
| `TASKS.md` | Deine To-do-Liste. Claude pflegt sie mit. |
| `PROMPTS.md` | Fertige Prompts für wiederkehrende Aufgaben. |
| `Meetings/` | Meeting-Notizen. |
| `Projects/` | Ein File pro Projekt: Stand, Entscheidungen, offene Fragen. |
| `Completed/` | Fertige Ergebnisse, nach Datum sortiert. |
| `skills/` | Zwei Skills: `/overview` (Morning Briefing) und `/tov` (dein Schreibstil). |

## Die Werte

Fest in `CLAUDE.md` verankert und für jede Rolle gleich:

1. **Einen Schritt weiter denken.** Frage beantworten, dann den nächsten sinnvollen
   Schritt nennen, an den du noch nicht gedacht hast. Was das in deiner Rolle
   heißt, legst du im Setup fest.
2. **Nie behaupten, was nicht geprüft ist.** Dokumentation ist ein Stand, kein
   Beweis. Was Claude nicht prüfen kann, sagt er.
3. **Widersprechen statt zustimmen.** Kein Abnicken. Lücken werden benannt.
4. **Nichts ohne Freigabe senden.** Mails und Nachrichten an andere sind immer
   erst ein Entwurf.
5. **Gedächtnis pflegen.** Entscheidungen und Aufgaben landen sofort in der
   richtigen Datei.

Du kannst die Werte anpassen. Überleg dir nur gut, welchen du streichst.

## Voraussetzungen

- Claude Desktop mit Cowork (bezahlter Plan)
- Für Skills muss in den Einstellungen die Code-Ausführung aktiviert sein
- Empfohlen: Connectors zu deinen Tools (Mail, Kalender, Chat, CRM, Ablage).
  Welche sich lohnen, schlägt Claude im Setup vor.

## Wichtig, bevor du etwas teilst

Nach dem Setup stehen in `CLAUDE.md`, `TASKS.md` und den Unterordnern Interna
aus deinem Unternehmen. **Deine ausgefüllte Version nie öffentlich hochladen**,
auch nicht als Fork. Dieses Repo ist die leere Vorlage.

## Feedback

Fragen, Ideen oder Fehler gern als Issue. Eine englische Version gibt es auf
Anfrage.

---

Lizenz: [CC BY 4.0](LICENSE). Frei nutzen und anpassen, mit Namensnennung.
