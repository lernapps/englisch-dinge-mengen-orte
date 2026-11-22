---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

„Dinge, Mengen und Orte“ (Repository `englisch-dinge-mengen-orte`): Explainer (Strang-App `englisch/grammatik`, Format 2, Sprache Deutsch, englische Beispiele) über Artikel, Plural, Genitiv, this/that, much/many, some/any, there is/are und die Präpositionen des Ortes und der Zeit. Auftrag: Issue lernapps/apps#475 (Epic lernapps/apps#489, Konventionen dort). Die erste Version baut nur Stufe 5-6 (Kapitel 1 bis 3); Kapitel 4 „Ohne Etikett und Sonderfälle“ (Stufe 7-8: `artikel-gebrauch`, `nomen-kongruenz`) kommt später als Inkrement `increment/<NN>-<name>`.

## Curriculum

Englisch als erste Fremdsprache, Klasse 5-6 (Stufe 5-6 der Karte). Kein Lehrplan: Reihenfolge und Bausteine kommen aus der Lernlandkarte `https://lernapps.net/apps/map/englisch.json` (Fokus `competency`; Strang-App des Strangs `grammatik`). Vorwissen: Hello, Millbrook! (#470), Pronomen (#471), Zeiten und to be (#472). Nicht hier: Possessivbegleiter my/your (#471), Adjektive und das Stützwort one (#476), Phrasal verbs (#485), Kapitel 4 (Inkrement).

## Competencies

Alle elf sind Lücken der Karte, Band 5-6. Eine Seite je Baustein, Reihenfolge nach `requires`. Von außen braucht die Karte nur `to-be` (#472), `datum` und `uhrzeit` (#470), alle in Kapitel 3 (eine Sammel-Wiederholung).

1. Kapitel `ein-ding-viele-dinge` („Ein Ding, viele Dinge“)
   - `artikel` → `ein-ding-viele-dinge/artikel` (Musterseite)
   - `plural` → `…/plural`
   - `genitiv` → `…/genitiv`
   - `demonstrativ` → `…/demonstrativ`
2. Kapitel `wie-viel-wie-viele` („Wie viel und wie viele?“)
   - `much-many` → `…/much-many`
   - `mengen-mit-of` → `…/mengen-mit-of`
   - `some-any` → `…/some-any`
   - `somebody-anything` → `…/somebody-anything`
3. Kapitel `wo-und-wann` („Wo und wann?“)
   - Wiederholung `recap: [englisch/to-be, englisch/datum, englisch/uhrzeit]` → `wo-und-wann/das-brauchst-du` (ohne Übung, ohne `competencies`)
   - `praepositionen-ort` → `…/praepositionen-ort`
   - `there-is-are` → `…/there-is-are`
   - `praepositionen-zeit` → `…/praepositionen-zeit`

Jede Seite nennt `competencies: [<id>]` mit der Karten-Id; die „Ich kann“-Sätze stehen wie in der Karte (nicht umformulieren). Übungs-IDs: Präfix = Seite (`artikel-…`; für die Seiten `much-many` und `there-is-are` abgekürzt zu `much-…` und `there-…`, `praepositionen-ort` zu `ort-…`, `praepositionen-zeit` zu `zeit-…`, `mengen-mit-of` zu `mengen-…`, `some-any` zu `some-…`, `somebody-anything` zu `somebody-…`, `demonstrativ` zu `demonstrativ-…`), Einstieg `<seite>-start`, Diktat `<seite>-hoeren`, Nachsprechen `<seite>-nachsprechen`, freie Aufgabe `<seite>-<thema>`.

## Content structure

- Pfad: `src/<kapitel>/chapter.yaml`, Seiten `src/<kapitel>/<seite>.yaml`.
- Jede Seite hat dieselben Abschnitts-IDs in dieser Reihenfolge: `einstieg` (Szene, kurzer Text, „Das kannst du danach“, Tabelle „Klassenzimmer-Poster · Neue Wörter“, erste leichte Aufgabe), `neu` (Zeichnung der Kiste, des Glases, des Regals oder des Zeit-Behälters, wachsende Poster-Tabelle, Kasten „Merke“), `uebung` (mindestens vier Übungen, leicht → schwer, Diktat), `anwenden` (`speaking-task`, `open-task`), `weiter` (nächster Schritt der Geschichte; am Kapitelende ein Rückblick). Titel sagen, was der Abschnitt tut. Die Wiederholungsseite hat nur Text und Tabellen.
- Länge: höchstens 350 Wörter Text, höchstens 4 Textblöcke hintereinander, Bild oder Übung in den ersten vier Blöcken. Jede Seite bringt einen neuen Schritt (`explainer-one-step`).
- Geschichte: Mr Hill lässt die Klasse den **Lagerraum** der Millbrook School (ein Raum im Erdgeschoss neben dem Klassenzimmer) für das **Schulfest** ordnen: Zählbares kommt in **Kisten**, Nicht-Zählbares in **Gläser**, alles bekommt **Etiketten** (a, an, the, some, much …) und einen Platz im Regal. Das Schulfest ist am ersten Samstag im Dezember um 10 Uhr; der Schulkalender hängt neben der Lagerraumtür. Mrs Parker backt Kuchen fürs Fest (keine weiteren neuen Figuren). Figuren und Orte sonst wie in #470 (nicht ändern): Sophie (blond, Zöpfe, grüne Jacke, aus Deutschland, wohnt bei den Parkers, 11 bis 12), Ellie Parker (11, roter Pferdeschwanz, rote Jacke), Peter Parker (9, kurze braune Haare, gelbe Jacke), Amir (11, schwarze Locken, Brille, blaue Jacke), Mr Hill (graue Haare, braune Jacke). Millbrook School, Schultag ab 8:45. Geburtstage: Peter 5. Mai, Ellie 10. Juli, Amir 12. Oktober, Sophie 14. Oktober. Lagerraum und Schulfest sind gesetzte Fakten der Reihe (`konventionen.md`).
- Tabellen: „Klassenzimmer-Poster · Neue Wörter“ (Wort, Bedeutung; alle Wörter, die die Seite abfragt, vor der ersten Übung, außer dem, was die Einstiegsaufgabe selbst prüft), „Klassenzimmer-Poster · Kisten und Etiketten“ (wächst in Kapitel 1 und 2), „Klassenzimmer-Poster · Orte“ und „Schulkalender · Zeitangaben“ (Kapitel 3).
- Anrede „du“.

## Terminology

- „Ausdruck“ (fester Ausdruck), nie „Wendung“. Fachbegriffe noun, verb, adjective, sentence, tense (aus #470).
- Bildwörter, immer gleich: **Kiste** (zählbares Nomen), **Glas** (nicht zählbares Nomen), **Etikett** (Begleiter: a, an, the, this, some, much …), **Überraschungskiste** (unregelmäßiger Plural), **Mengenwort** (a cup of, a bottle of, a piece of, a bag of, a pair of: macht Nicht-Zählbares zählbar; nie „Behälter“ nennen), **Zeit-Behälter** (in, on, at bei Zeitangaben; nur dieses Wort mit „Behälter“), **Regal** (Ort). Das Wort Glas (Bild für Nicht-Zählbares) und das englische glass (Trinkglas, ein Mengenwort) werden auf der Seite `mengen-mit-of` ausdrücklich unterschieden. Kein „Artikelwort“, kein „Zählwort“ ohne Erklärung; „zählbar / nicht zählbar“ steht daneben.
- Menschen sind keine „Dinge“: Bei ’s und bei Beziehungen zwischen Personen (her brother, his sister) heißt es „wem gehört es?“ oder „die Person, zu der es gehört“, nie „Besitzer“ und „Ding“; „Gegenstand“ und „Ding“ nur für Sachen.
- Britisches Englisch (colour, favourite). Englische Aufgaben enthalten kein deutsches Wort; englische Wörter immer mit deutscher Bedeutung, wo sie neu sind.
- Aussprache: Lesehilfe in deutscher Annäherung, betonte Silbe in Großbuchstaben, nur wo sie nötig ist (zum Beispiel „the“ vor Vokal); keine Lautschrift (IPA gehört zu #482). Hörtexte nur als ganze Sätze.

## Exercise patterns

Aufbau leicht → schwer: zuordnen/wählen → Lücke → Tabelle ableiten → schreiben mit Cue → Diktat und Nachsprechen → freie Aufgabe. Je Übung `mistakes` mit eigener Rückmeldung, die die Regel nennt, und `hint`; gleichwertige Antworten mit `(a|b)`.

- (a) Zuordnen: `matching` Ding ↔ Etikett, Kiste ↔ Glas.
- (b) Etikett wählen: `language-task` mode `choice` mit `distractors` (`target: "[a] ball"`).
- (c) Lücke: mode `gap`. (d) Form bilden: mode `write` mit `cue` (`cue: "ball · 2"`). (e) Tabelle ableiten: mode `table`.
- (f) Reihenfolge: `ordering` (Satzbau mit there is/are, Zeitangabe). (g) Entscheiden mit Begründung: `true-false`, `single-choice`; die Rückmeldung nennt die Kiste, das Glas oder den Zeit-Behälter.
- (h) Hören und schreiben: `language-task` mit `audio` (je Seite drei ganze Sätze, nie wiederholt); Nachsprechen: `speaking-task` (drei weitere Sätze).
- (i) Freies Schreiben: `open-task` (eigenes Etikett, eigenes Regal, eigener Kalendereintrag).
- Typische Fehler (jeweils `mistakes`): a vor Vokal (a egg), an vor Konsonant, an university / a hour (Laut, nicht Buchstabe), childs / mans / apple’s, the Sophie’s bike, Peters’s, this books, much books / many water, some in der Frage und any in der Aussage, there is two boxes, in Monday / at July / on 8 o’clock.
- Selbsteinschätzung: je Kapitel zwei Übungen je Seite (Skill `lernapps-explainer-self-assessment`).
- Aufgaben mit Bild: `language-task` mode `choice` mit `material: [{ type: figure, … }]` (`ort-bild`, `there-bild`); die Frage steht im `cue`, das Bild hat nur `alt` ohne Lösung.
- Rangfolge: `ordering` (Satzbau mit Behälter + of, Frage mit Is there, Zeitangabe mit on und at).
- Keine Komponente (`prefer-built-in-block`); Ziehen von Dingen in Kisten wäre ein Wunsch für ein Inkrement. Keine Datendateien: jede Tatsache steht einmal in ihrer Seite.

## Figures

- Eigene SVG-Zeichnungen in `src/images/` (Quelle „eigene Zeichnung“, Lizenz `CC-BY-4.0`): Hintergrund #f4efe2, Schrift mindestens 16 im 640er viewBox, Beschriftung innerhalb des viewBox, funktioniert bei 360 px. Keine Fotos, keine Figuren aus Büchern, Filmen oder Marken.
- Szenen: je Seite `szene-<seite>.svg` mit den Figuren, kopiert als `<g id>` aus `millbrook-klassenzimmer.svg` von hello-millbrook und gleich gelassen. `alt` sagt, was die Szene zeigt, nie die Lösung; die Bildunterschrift nennt, wer wer ist (Sophie Zöpfe, Ellie roter Pferdeschwanz, Amir Brille, Peter gelbe Jacke).
- Kisten und Gläser: Kiste = braune Kiste mit Etikett (zählbar), Glas = Glas mit Etikett (nicht zählbar); später Regalplan (`regal-*.svg`) und Zeit-Behälter (`zeit-behaelter.svg`: großer Rahmen = in, Fläche = on, Punkt = at). Gebaut (alle in `src/images/`): `szene-<seite>.svg` für jede Seite (die Szene der Wiederholungsseite fehlt), dazu `kisten-a-an`, `kisten-plural`, `namensschilder`, `hand-nah-fern`, `kisten-glaeser`, `glas-wird-zaehlbar`, `some-any-etiketten`, `etiketten-ohne-nomen`, `regal-orte`, `regal-aufgabe` (Aufgabenbild als `material`, farbige Kisten), `there-is-are`, `regal-inventur` (Aufgabenbild als `material`), `zeit-behaelter`. Das Bild einer Seite zeigt nie die Wörter, die ihre Übungen abfragen.
- Poster und Kalender sind `table`-Blöcke, sie wachsen von Seite zu Seite.

## Sources

Karte `https://lernapps.net/apps/map/englisch.json`; Grundwortschatz `https://lernapps.net/apps/map/englisch/grundwortschatz/` (A1/A2; die Wörter der Übungen stammen daraus; außerhalb der Liste stehen nur die hier genannten Wörter, die auf der Seite erklärt sind: storeroom (Lagerraum)). Fakten aus Wikipedia (nur Fakten, keine Sätze, CC BY-SA), geöffnet am 2026-11-21: `English articles` (a und an nach dem Anlaut, the vor Vokal), `English plurals`, `English possessive`, `English prepositions`, `Demonstrative`. Wörter außerhalb der Liste: storeroom (Lagerraum), im Text der Seite `artikel` und in der Tabelle von `genitiv` erklärt; sonst nur Namen und Beugungen (children, men, feet, watches, parties, got, has, shoes). Nicht geprüft: `Mass noun` und `English determiners` (HTTP 429), deutsche Wikipedia, Klexikon. Beispielsätze sind eigene aus dem Alltag der Figuren. Audio: KI-Stimme `bf_emma` (britisch, weiblich), mit Skill `lernapps-audio` erzeugt und als KI-generiert markiert. Material der Ersteller:in: keines.

## Adding a chapter or round

1. Baustein auf der Karte wählen; die Voraussetzungen müssen auf früheren Seiten stehen oder eine Wiederholungsseite bekommen (Kapitel 4 braucht `artikel` und `plural`, beide stehen auf Kapitel 1).
2. Seite `src/<kapitel>/<seite>.yaml` mit den Abschnitten `einstieg`, `neu`, `uebung`, `anwenden`, `weiter` anlegen, in `chapter.yaml` eintragen, `competencies` setzen. Stufe 7-8: Form der Geschichte wechselt zu Nachrichten und kurzen Dialogen (Konventionen 2); Kisten ohne Etikett (Nullartikel), news als Glas (is), police als Gruppe von Kisten (are).
3. Zeichnung und Poster erweitern (gleiche Bildwörter).
4. Übungen aus den Mustern oben, je mit `mistakes` und `hint`; 1 bis 3 ihrer Übungen in `selfAssessment` aufnehmen, wie Skill `lernapps-explainer-self-assessment` sagt.
5. Hörtexte: Datei `src/audio/<satz>.mp3`, Eintrag in `.agents/skills/app-content/scripts/audio-texte.json`, erzeugt mit `~/.cache/lernapps/audio/venv/bin/python .agents/skills/app-content/scripts/regen_audio.py .agents/skills/app-content/scripts/audio-texte.json "<Satz>"` (Skript aus hello-millbrook, schneidet das Ausklingen ab); anhören lassen; Sätze nicht zwischen Seiten wiederholen, Namen am Satzende zweisilbig.
6. Wörter gegen den Grundwortschatz prüfen; `npx --no -- lernapps check`; committen.

## Audio

Je Seite drei Diktatsätze (`<seite>-hoeren`) und drei Sätze zum Nachsprechen (`<seite>-nachsprechen`), 66 Sätze für 11 Seiten (die Wiederholungsseite hat keine), alle in `.agents/skills/app-content/scripts/audio-texte.json` (Datei → Satz). Der Dateiname ist der Satz in Kleinbuchstaben, jedes Zeichen außer Buchstaben und Ziffern wird zu `-` (`amir-s-bike-is-in-the-storeroom.mp3`). Erzeugen: `~/.cache/lernapps/audio/venv/bin/python .agents/skills/app-content/scripts/regen_audio.py .agents/skills/app-content/scripts/audio-texte.json "<Satz>"`.

Die Stimme hängt an Sätzen, die auf ein einsilbiges Wort enden, manchmal einen Fehllaut an. Die Sätze enden deshalb möglichst auf ein zweisilbiges Wort oder einen Namen; wo das nicht natürlich geht, steht der Satz in der **Hörliste** (42 Sätze), damit die Ersteller:in gezielt das Satzende hört. Ein angehängter Name nur zum Zweck des Klangs ist nicht erwünscht (Rückmeldung der Ersteller:in). Hörliste:

- Amir has a few books.
- Amir has three pieces of cake.
- Amir hasn't got any juice.
- Ellie has a ball and an egg.
- Ellie has no bread.
- Ellie has two eggs.
- Has Sophie got any pens?
- Have you got any rice?
- Have you got anything in the bag?
- Is anybody here?
- Mr Hill has something for you.
- Mr Hill's birthday is on 3 June.
- Mrs Parker has a cup of tea.
- Mrs Parker has some eggs.
- Mrs Parker hasn't got much rice.
- Mrs Parker's birthday is in March.
- Nobody is in the room.
- Peter has a little bread.
- Peter has two books.
- Peter hasn't got many pens.
- Peter's cap is in the box.
- Sophie has a lot of bags.
- Sophie has a pair of shoes.
- Sophie has two bottles of milk.
- That is Mr Hill's bike.
- The ball is in the bag.
- The books are on the shelf.
- The cap is behind the door.
- The children have three balls.
- The children's shoes are in the bag.
- The door of the room is red.
- The egg is in the box.
- The pen is in the bag.
- The women have two bags.
- The women have two pairs of jeans.
- There are three pens in the box.
- There is a bike next to the door.
- There is a window next to the door.
- These shoes are in the box.
- This is Sophie's coat.
- Those bikes are blue.
- Those coats are red.

## Rules learned from mistakes

Aus #470 und den Schwester-Explainern übernommen:
- Jede Übung fragt nur Wörter ab, die vorher auf der Seite stehen.
- Eine Tabelle, die eine Übung beantwortet, steht nicht direkt über ihr; das Merke-Kasten nennt andere Wörter als die Übungen.
- Englische Aufgaben enthalten kein deutsches Wort; der deutsche Hinweis steht in `source` oder in der Aufgabe.
- Mit `(a|b)` gleichwertige richtige Antworten zulassen; Kurzformen zulassen.
- Audio: Ausklingen abschneiden (`regen_audio.py`), Namen am Satzende zweisilbig.
- Bilder: Beschriftungen innerhalb des `viewBox`; `alt` verrät nie die Lösung.
- Die Antwort einer Frage steht nie im Absatz direkt darüber.
- Als Auswahl nur echte Lernerfehler, keine Unwörter.
Aus dieser App (Lerner-Check der Musterseite, zweiter Check, Auflagen der Orchestrierung):
- Das Bild einer Seite zeigt andere Wörter als die Übungen (sonst wird abgeschrieben); Tabellen und Merke-Kästen ebenfalls.
- Die Einstiegsaufgabe prüft nur, was die Kinder schon wissen (Bedeutung eines Wortes, nicht die Regel der Seite).
- Fachwörter (Vokal-Laut, zählbar, Präposition) werden dort erklärt, wo sie zum ersten Mal stehen.
- Distraktoren und Auswahlmöglichkeiten nennen nur echte Lernerfehler, keine Unwörter (kein „thees“, „muchs“).
- Je Item eine eigene Meldung (`mistakes`) für den typischen Fehler; die Meldung sagt, was nicht passt, nie die Lösung. Bei Auswahl-Lücken (mode `choice`) zeigt die Vorlage die Meldung nicht an, nur „nicht richtig“: Das Wort in `hint` trägt den Hinweis.
- Deutsche Cues dürfen die Lösung nicht verraten (kein „der, die, das“ für the): „Er/Es/Sie ist rot“.
- Bei Apostroph-Aufgaben (`genitiv`) nicht `apostrophe: ok` setzen, sonst zählt der Fehler als richtig.
- Ein Satz, der in der Aufgabe steht, steht nicht noch einmal als Hörtext derselben Seite.
- `scope`-Texte in YAML in Anführungszeichen setzen, wenn sie einen Doppelpunkt enthalten.
- Hörsätze enden möglichst auf ein zweisilbiges Wort oder einen Namen, aber kein Name nur für den Klang anhängen; einsilbige Enden stehen in der Hörliste im Abschnitt „Audio“.
- Menschen sind keine „Dinge“: nicht „Besitzer“ und „Ding“ für Personen und ihre Beziehungen (Rückmeldung der Ersteller:in zu #471).
- `punctuation: ok` in allen Schreib- und Diktataufgaben (die Vorlage meldet bei `hint` auch bei richtigen Antworten „Achte auf die Satzzeichen“).
