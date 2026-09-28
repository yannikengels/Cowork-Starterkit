---
name: tov
description: "Lernt einmalig den echten Schreibstil des Nutzers aus gesendeten Mails und Chat-Nachrichten, legt TONE-OF-VOICE.md im Arbeitsordner an und schreibt danach jeden Entwurf in diesem Ton. Auslösen bei /tov, lern meinen Schreibstil, klingt nicht nach mir."
---

# /tov: Tone of Voice

Drei Modi. Der Skill entscheidet selbst:

| Situation | Modus |
|---|---|
| `TONE-OF-VOICE.md` fehlt im Arbeitsordner, oder `/tov scan` | **A: Scan** |
| `TONE-OF-VOICE.md` existiert | **B: Anwenden** |
| `/tov update`, oder der Nutzer korrigiert einen Entwurf | **C: Nachschärfen** |

Immer zuerst prüfen, ob `TONE-OF-VOICE.md` im Arbeitsordner liegt.

---

# Modus A: Scan (einmalig)

Ziel: lernen, wie **diese** Person schreibt. Nicht, wie man „gut“ schreibt. Der
Skill beschreibt, er erzieht nicht.

## A1: Person bestimmen

`CLAUDE.md` lesen: Name, E-Mail, Rolle, Sprache, Du oder Sie, Emojis. Fehlt die
Datei, einmal nach Name und Mail-Adresse fragen. Gescannt werden **nur eigene
gesendete Nachrichten**.

## A2: Material sammeln

Ziel: **mindestens 40 eigene Nachrichten**, verteilt über die Kontexte. Weniger
geht, wird aber als dünne Datenlage markiert.

**Mail** (nur Gesendetes, letzte 6 Monate):
- an externe Adressen → externe Mails
- an die eigene Firmen-Domain → interne Mails
- Threads bevorzugen, in denen der Nutzer selbst formuliert hat. Weiterleitungen
  ohne eigenen Text zählen nicht.

**Chat** (eigene Nachrichten, letzte 3 Monate):
- öffentliche Team-Channels
- Direktnachrichten mit Kolleg:innen
- Channels oder DMs mit Externen, falls vorhanden
- Thread-Antworten getrennt von Channel-Posts betrachten

Ist eine Quelle nicht erreichbar: nicht abbrechen, den Kontext als
„⚠️ nicht analysiert“ führen.

## A3: Kontexte trennen

Der Kern. Ein Mensch hat keinen Ton, sondern **Register**. Getrennt auswerten:

1. Externe Mail
2. Interne Mail
3. Chat-Channel (mehrere Lesende)
4. Chat-DM intern
5. Chat extern
6. Kurzform (Bestätigungen, Einzeiler)

Zusätzlich: Schreibt die Person an Führungskräfte anders als an Peers? An
langjährige Kontakte anders als an neue? Wenn ja, festhalten.

## A4: Pro Kontext auswerten

Je Dimension mit **konkretem Beleg** aus dem Material:

| Dimension | Worauf achten |
|---|---|
| Anrede | „Hi X“, „Hallo X“, „Moin“, keine |
| Du / Sie | wer wird wie angesprochen, ab wann Wechsel |
| Sprache | Deutsch, Englisch, gemischt, welche Begriffe bleiben englisch |
| Abschluss | „Beste Grüße“, „VG“, „Danke dir“, Vorname, nichts |
| Länge | Wörter pro Nachricht, Sätze pro Absatz |
| Satzbau | kurz und direkt oder verschachtelt |
| Struktur | Fließtext, Bullets, Nummerierung, Fettungen |
| Emojis | welche, wie oft, wo, oder nie |
| Interpunktion | Ausrufezeichen, Doppelpunkte, Klammern, Auslassungspunkte |
| Öffner | die 3 bis 5 häufigsten ersten Sätze |
| Schließer | die 3 bis 5 häufigsten letzten Sätze |
| Eigene Wendungen | typische Wörter und Formulierungen |
| Direktheit | wird ein Nein direkt gesagt oder verpackt |
| Verbindlichkeit | konkrete Termine oder vage („melde mich“) |

### Beweisregel

Ein Muster gilt nur, wenn es **mindestens dreimal** vorkommt. Alles darunter
kommt mit ⚠️ als Vermutung in die Datei oder gar nicht. Nie einen plausiblen Stil
erfinden.

### Datenschutz

- Keine Namen von Kunden, keine Preise, Vertragsdetails oder persönlichen Inhalte
  übernehmen. Beispiele anonymisieren: `[Kunde]`, `[Kollegin]`, `[Betrag]`.
- Beispiele auf ein bis zwei Sätze kürzen. Es geht um Form, nicht um Inhalt.
- Nichts aus DMs zitieren, das ohne Kontext vertraulich oder unangenehm wäre.

## A5: Datei schreiben

`TONE-OF-VOICE.md` in die Wurzel des Arbeitsordners, neben `CLAUDE.md`.
Existiert sie schon: erst lesen, dann gezielt aktualisieren, nie kommentarlos
überschreiben. Ist der Ordner nicht beschreibbar: Datei ausliefern und sagen,
wohin sie gehört.

### Vorlage

```markdown
# Tone of Voice: [Name]

Erstellt am [Datum] aus [N] eigenen Nachrichten ([X] Mails, [Y] Chat).
Beschreibt, wie [Vorname] tatsächlich schreibt. Gilt für jeden Entwurf in
[Vorname]s Namen.

## Gilt immer

- Keine KI-Floskeln (Liste unten).
- Entwürfe an andere werden immer erst vorgelegt, nie automatisch gesendet.
- Keine erfundenen Zahlen, Termine oder Zusagen. Platzhalter statt Erfindung:
  `[Betrag]`, `[Datum]`, `[Firma]`.
- Nie Du und Sie in derselben Nachricht mischen.
- [Regeln aus CLAUDE.md, z. B. keine Emojis extern]

## Grundton

[2 bis 3 Sätze: wie die Person über alle Kontexte klingt.]

**Drei Adjektive:** [z. B. direkt, warm, pragmatisch]

## Kontext-Matrix

| Kontext | Anrede | Du/Sie | Abschluss | Länge | Emojis | Ton |
|---|---|---|---|---|---|---|
| Externe Mail | | | | | | |
| Interne Mail | | | | | | |
| Chat-Channel | | | | | | |
| Chat-DM intern | | | | | | |
| Chat extern | | | | | | |
| Kurzform | | | | | | |

## Kontext-Details

### Externe Mail
- **Register:** [z. B. freundlich, konkret, ohne Steifheit]
- **Typische Öffner:** [3 anonymisierte Beispiele]
- **Typische Schließer:** [3 Beispiele]
- **Länge:** [Ø Wörter]
- **Beispiel:**
  > [1 bis 3 Sätze, anonymisiert]

[gleiche Struktur für die übrigen Kontexte]

## Eigene Wendungen

- [Wendung 1]
- [Wendung 2]

## So schreibt [Vorname] nicht

Jeder Entwurf wird dagegen geprüft und bei Treffer umgeschrieben.

- „Ich hoffe, es geht dir gut.“ / „Ich hoffe, diese Mail erreicht dich gut.“
- „Ich melde mich die Tage.“ (ohne Datum)
- „Bei Interesse gerne …“ / „Schau gerne mal rein.“
- „In der heutigen schnelllebigen Zeit …“
- „Es ist wichtig zu beachten, dass …“ / „Zusammenfassend lässt sich sagen …“
- „nahtlos“, „ganzheitlich“, „innovativ“, „Game Changer“, „next level“
- Dreiklang-Aufzählungen als Stilmittel („schnell, einfach, effektiv“)
- [aus dem Scan ergänzen]

## Ersetzungen

| Statt | Besser |
|---|---|
| Ich melde mich | Ich komme am [Datum] auf dich zu |
| Kurzer Austausch | 20 Minuten zu [Thema] |
| Passt das für dich? | Passt [Tag] um [Uhrzeit]? |
| [aus dem Scan] | |

## Datenlage

| Kontext | Nachrichten | Konfidenz |
|---|---|---|
| Externe Mail | | hoch / mittel / ⚠️ dünn |

---
_Zuletzt aktualisiert: [Datum]. Aktualisieren mit `/tov update`._
```

## A6: Ergebnis vorlegen

Kurz, nicht die ganze Datei wiederholen:

- ein Satz zum Grundton
- die drei auffälligsten Unterschiede zwischen den Kontexten
- wo die Datenlage dünn ist (⚠️)
- eine Frage: „Trifft das? Was ist daneben?“

Korrekturen gehen direkt in die Datei (Modus C).

---

# Modus B: Anwenden

Gilt für jeden Entwurf im Namen des Nutzers: Mail, Chat, Social Media, Kommentar.

1. `TONE-OF-VOICE.md` lesen.
2. **Kontext bestimmen:** Wer liest, welcher Kanal, extern oder intern? Bei
   Unklarheit einmal fragen. Ein interner Ton in einer Kundenmail ist der
   teuerste Fehler dieses Skills.
3. Passenden Kontext-Block als Vorlage nehmen.
4. Entwurf schreiben.
5. Self-Check (unten).
6. Als **Entwurf** vorlegen, nie senden.

## Self-Check

1. Richtiger Kontext gewählt?
2. Du oder Sie konsistent?
3. Anrede und Abschluss wie belegt?
4. Länge im Rahmen?
5. Keine Formulierung aus „So schreibt [Vorname] nicht“?
6. Konkret: echter Name, echtes Datum oder sauberer Platzhalter?
7. Nächster Schritt konkret und terminiert?
8. Nichts behauptet, was nicht geprüft ist?
9. Würde der Nutzer das so abschicken, ohne umzuschreiben?

Bei einem Nein: umschreiben, nicht abliefern.

**Fallback:** Ist der Kontext unklar, gilt die vorsichtigere Variante. Extern vor
intern, förmlich vor locker. Und einmal fragen.

---

# Modus C: Nachschärfen

Ausgelöst durch `/tov update` oder wenn der Nutzer einen Entwurf spürbar
umschreibt oder sagt, der Ton passt nicht.

1. **Unterschied verstehen:** Was genau hat sich geändert?
2. **Regel oder Einzelfall?** Einzelfälle kommen nicht in die Datei.
3. Betroffene Stelle in `TONE-OF-VOICE.md` **gezielt** ändern, nie alles neu.
4. Datum aktualisieren, in einer Zeile bestätigen, was geändert wurde.

`/tov update` ohne Anlass: die letzten 4 Wochen neuer Nachrichten nachscannen,
nur Abweichungen einarbeiten.

---

# Fehlerfälle

- **Mail oder Chat nicht verbunden:** mit der anderen Quelle scannen, fehlende
  Kontexte als ⚠️ nicht analysiert markieren, einmal sagen, welcher Connector fehlt.
- **Unter 15 Nachrichten:** Datei trotzdem anlegen, klar als vorläufig markieren,
  in vier Wochen `/tov update` vorschlagen. Keinen Stil erfinden.
