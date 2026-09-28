# Setup-Prompt

**So geht's:** Diesen Ordner in Cowork als Arbeitsordner verbinden. Dann alles
zwischen den beiden Linien kopieren und als erste Nachricht einfügen. Dauer: ca.
15 Minuten. Du kannst jederzeit „weiter“ oder „überspring das“ sagen.

---

Du richtest mich als deinen Cowork-Kollegen ein. In diesem Ordner liegt eine
`CLAUDE.md` mit zwei Teilen: Teil A (Werte und Arbeitsregeln) ist fest, Teil B
(mein Kontext) ist voller Platzhalter `[[ … ]]`. Deine Aufgabe: mich interviewen
und Teil B ausfüllen, plus die Rollen-Variante von Wert 1 in Teil A.

**Regeln für das Interview:**

- Lies zuerst `CLAUDE.md` komplett. Halte dich schon während des Interviews an
  die Werte aus Teil A.
- Frag in Runden von 2 bis 4 Fragen, nie alles auf einmal. Nummeriere die
  Runden („Runde 2 von 6“), damit ich weiß, wo wir stehen.
- Was ich nicht weiß oder überspringe: `⚠️ offen` eintragen, nicht raten.
- Was du selbst recherchierst, kennzeichnest du als recherchiert und lässt es
  mich bestätigen.
- Kurze Fragen, keine Erklärtexte. Wenn eine Frage Beispiele braucht, gib 2 bis 3.

**Ablauf:**

**Runde 1: Start**
Stell dich in zwei Sätzen vor und erklär, was gleich passiert. Dann frag nach:
meinem Namen, meiner Rolle und der Website meines Unternehmens.

**Runde 2: Unternehmen**
Recherchiere die Website selbst (Startseite, Produkte, Über uns, Impressum).
Zeig mir eine kurze Zusammenfassung: was, für wen, Produkte, Positionierung,
Größe. Frag mich dann nur noch, was falsch ist oder fehlt, und nach dem, was
auf keiner Website steht: wichtigste Wettbewerber aus Kundensicht, Werte und
Kultur, wie Entscheidungen getroffen werden. Kannst du die Website nicht lesen,
sag das und frag stattdessen direkt.

**Runde 3: Rolle und Team**
Mission in 1 bis 2 Sätzen, 3 bis 6 Kernverantwortlichkeiten, Manager:in,
Teamgröße, Arbeitsmodell, und die 3 bis 5 Menschen, mit denen ich am engsten
arbeite (Name, Rolle, wofür).

**Runde 4: Tools**
Frag, welche Tools ich und mein Unternehmen im Alltag nutzen. Gib Kategorien als
Gedankenstütze: Mail, Kalender, Chat, Ablage/Dokumente, CRM, Projektmanagement,
Wissensdatenbank, Meeting-Aufnahmen, Buchhaltung, Automatisierung, eigene Systeme.

Dann für jedes genannte Tool:
1. **Prüf, ob es dafür einen Connector gibt.** Nutze dafür, was dir zur
   Verfügung steht (Connector-Verzeichnis, verbundene Tools). Kannst du es nicht
   prüfen, sag das ehrlich. Erfinde keine Integration.
2. **Ordne ein:** schon verbunden · verfügbar, noch nicht verbunden · kein
   Connector. Bei „kein Connector“: realistische Alternative nennen
   (Automatisierungs-Tool, Export, Copy-Paste).
3. **Mach 1 bis 2 konkrete Vorschläge, wie ich es mit dir im Alltag nutze.**
   Nicht generisch („E-Mails verwalten“), sondern ein Satz, den ich morgen so
   eintippen könnte. Beispiel Kalender: „Bereite meine externen Termine von
   morgen vor und sag mir, wo die Agenda fehlt.“

Zeig das Ergebnis als Tabelle: Tool · Connector-Status · Vorschlag für den Alltag.
Frag, welche drei ich zuerst verbinden will, und empfiehl selbst drei, mit
einem Satz Begründung. Erklär bei Bedarf kurz, wo man Connectors verbindet.

Frag außerdem: Wo liegt bei euch die Wahrheit? Welches System ist verbindlich
für Kundendaten, Prozesse, Zahlen? Das kommt als „Verbindliche Quellen“ in die Datei.

**Runde 5: Arbeitsweise und Ton**
Sprache, Du oder Sie (intern und extern), wie knapp, wie direkt ich widersprochen
haben will, Emojis ja oder nein, Wörter und Formulierungen, die ich nicht mag.
Plus: meine wichtigsten Abkürzungen und internen Begriffe.

**Runde 6: Einen Schritt weiter**
Erklär Wert 1 in einem Satz. Schlag dann 2 bis 3 Varianten vor, was „einen
Schritt weiter“ in meiner Rolle konkret heißen könnte, passend zu dem, was du
über Rolle und Unternehmen weißt. Ein Beispiel für Sales: „Wenn ich ein Produkt
verkaufe, schlag mir das passende Zusatzprodukt oder das größere Paket vor.“
Ich wähle oder formuliere um. Frag auch, ob ich an einem der anderen Werte etwas
ändern will. Wenn ja: Push back, wenn die Änderung einen Wert aushöhlt.

**Abschluss**
1. `CLAUDE.md` ausfüllen: Teil B komplett, in Teil A nur die Zeile „In meiner
   Rolle heißt das“. Den Rest von Teil A nicht verändern, außer ich habe es in
   Runde 6 ausdrücklich so gewollt.
2. Wenn ich Aufgaben oder Projekte erwähnt habe: in `TASKS.md` bzw. als Datei in
   `Projects/` anlegen.
3. Zeig mir eine Zusammenfassung in maximal 8 Zeilen und die Liste aller
   `⚠️ offen`-Punkte.
4. Schlag drei erste Aufgaben vor, die ich direkt mit dir erledigen kann, passend
   zu Rolle und verbundenen Tools.
5. Weise auf die zwei Skills im Ordner `skills/` hin: `/overview` für ein
   Morning Briefing, `/tov`, damit Entwürfe nach mir klingen.

Los geht's mit Runde 1.

---

_Tipp: Den Prompt jederzeit erneut nutzen, wenn sich Rolle, Team oder Tools
ändern. Claude aktualisiert dann nur, was sich geändert hat._
