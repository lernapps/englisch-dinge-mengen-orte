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

Jede Seite nennt `competencies: [<id>]` mit der Karten-Id; die „Ich kann“-Sätze stehen wie in der Karte (nicht umformulieren). Übungs-IDs: Präfix = Seite (`artikel-…`), Einstieg `<seite>-start`, Diktat `<seite>-hoeren`, Nachsprechen `<seite>-nachsprechen`, freie Aufgabe `<seite>-<thema>`.

## Content structure

- Pfad: `src/<kapitel>/chapter.yaml`, Seiten `src/<kapitel>/<seite>.yaml`.
- Jede Seite hat dieselben Abschnitts-IDs in dieser Reihenfolge: `einstieg` (Szene, kurzer Text, „Das kannst du danach“, Tabelle „Klassenzimmer-Poster · Neue Wörter“, erste leichte Aufgabe), `neu` (Zeichnung der Kiste, des Glases, des Regals oder des Zeit-Behälters, wachsende Poster-Tabelle, Kasten „Merke“), `uebung` (mindestens vier Übungen, leicht → schwer, Diktat), `anwenden` (`speaking-task`, `open-task`), `weiter` (nächster Schritt der Geschichte; am Kapitelende ein Rückblick). Titel sagen, was der Abschnitt tut. Die Wiederholungsseite hat nur Text und Tabellen.
- Länge: höchstens 350 Wörter Text, höchstens 4 Textblöcke hintereinander, Bild oder Übung in den ersten vier Blöcken. Jede Seite bringt einen neuen Schritt (`explainer-one-step`).
- Geschichte: Mr Hill lässt die Klasse den **Lagerraum** der Millbrook School (ein Raum im Erdgeschoss neben dem Klassenzimmer) für das **Schulfest** ordnen: Zählbares kommt in **Kisten**, Nicht-Zählbares in **Gläser**, alles bekommt **Etiketten** (a, an, the, some, much …) und einen Platz im Regal. Das Schulfest ist am ersten Samstag im Dezember um 10 Uhr; der Schulkalender hängt neben der Lagerraumtür. Mrs Parker backt Kuchen fürs Fest (keine weiteren neuen Figuren). Figuren und Orte sonst wie in #470 (nicht ändern): Sophie (blond, Zöpfe, grüne Jacke, aus Deutschland, wohnt bei den Parkers, 11 bis 12), Ellie Parker (11, roter Pferdeschwanz, rote Jacke), Peter Parker (9, kurze braune Haare, gelbe Jacke), Amir (11, schwarze Locken, Brille, blaue Jacke), Mr Hill (graue Haare, braune Jacke). Millbrook School, Schultag ab 8:45. Geburtstage: Peter 5. Mai, Ellie 10. Juli, Amir 12. Oktober, Sophie 14. Oktober. Lagerraum und Schulfest sind gesetzte Fakten der Reihe (`konventionen.md`).
- Tabellen: „Klassenzimmer-Poster · Neue Wörter“ (Wort, Bedeutung; alle Wörter, die die Seite abfragt, vor der ersten Übung, außer dem, was die Einstiegsaufgabe selbst prüft), „Klassenzimmer-Poster · Kisten und Etiketten“ (wächst in Kapitel 1 und 2), „Klassenzimmer-Poster · Orte“ und „Schulkalender · Zeitangaben“ (Kapitel 3).
- Anrede „du“.

## Terminology

- „Ausdruck“ (fester Ausdruck), nie „Wendung“. Fachbegriffe noun, verb, adjective, sentence, tense (aus #470).
- Bildwörter, immer gleich: **Kiste** (zählbares Nomen), **Glas** (nicht zählbares Nomen), **Etikett** (Begleiter: a, an, the, this, some, much …), **Überraschungskiste** (unregelmäßiger Plural), **Zeit-Behälter** (in, on, at bei Zeitangaben), **Regal** (Ort). Kein „Artikelwort“, kein „Zählwort“ ohne Erklärung; „zählbar / nicht zählbar“ steht daneben.
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
- Keine Komponente (`prefer-built-in-block`); Ziehen von Dingen in Kisten wäre ein Wunsch für ein Inkrement. Keine Datendateien: jede Tatsache steht einmal in ihrer Seite.

## Figures

- Eigene SVG-Zeichnungen in `src/images/` (Quelle „eigene Zeichnung“, Lizenz `CC-BY-4.0`): Hintergrund #f4efe2, Schrift mindestens 16 im 640er viewBox, Beschriftung innerhalb des viewBox, funktioniert bei 360 px. Keine Fotos, keine Figuren aus Büchern, Filmen oder Marken.
- Szenen: je Seite `szene-<seite>.svg` mit den Figuren, kopiert als `<g id>` aus `millbrook-klassenzimmer.svg` von hello-millbrook und gleich gelassen. `alt` sagt, was die Szene zeigt, nie die Lösung; die Bildunterschrift nennt, wer wer ist (Sophie Zöpfe, Ellie roter Pferdeschwanz, Amir Brille, Peter gelbe Jacke).
- Kisten und Gläser: Kiste = braune Kiste mit Etikett (zählbar), Glas = Glas mit Etikett (nicht zählbar); später Regalplan (`regal-*.svg`) und Zeit-Behälter (`zeit-behaelter.svg`: große Kiste = in, Fläche = on, Punkt = at). Gebaut: `szene-artikel`, `kisten-a-an` (Seite `artikel`).
- Poster und Kalender sind `table`-Blöcke, sie wachsen von Seite zu Seite.

## Sources

Karte `https://lernapps.net/apps/map/englisch.json`; Grundwortschatz `https://lernapps.net/apps/map/englisch/grundwortschatz/` (A1/A2; die Wörter der Übungen stammen daraus; außerhalb der Liste stehen nur die hier genannten Wörter, die auf der Seite erklärt sind: storeroom (Lagerraum) und jar (Glas)). Fakten aus Wikipedia (nur Fakten, keine Sätze, CC BY-SA), geöffnet am 2026-11-21: `English articles` (a und an nach dem Anlaut, the vor Vokal), `English plurals`, `English possessive`, `English prepositions`, `Demonstrative`. Nicht geprüft: `Mass noun` und `English determiners` (HTTP 429), deutsche Wikipedia, Klexikon. Beispielsätze sind eigene aus dem Alltag der Figuren. Audio: KI-Stimme `bf_emma` (britisch, weiblich), mit Skill `lernapps-audio` erzeugt und als KI-generiert markiert. Material der Ersteller:in: keines.

## Adding a chapter or round

1. Baustein auf der Karte wählen; die Voraussetzungen müssen auf früheren Seiten stehen oder eine Wiederholungsseite bekommen (Kapitel 4 braucht `artikel` und `plural`, beide stehen auf Kapitel 1).
2. Seite `src/<kapitel>/<seite>.yaml` mit den Abschnitten `einstieg`, `neu`, `uebung`, `anwenden`, `weiter` anlegen, in `chapter.yaml` eintragen, `competencies` setzen. Stufe 7-8: Form der Geschichte wechselt zu Nachrichten und kurzen Dialogen (Konventionen 2); Kisten ohne Etikett (Nullartikel), news als Glas (is), police als Gruppe von Kisten (are).
3. Zeichnung und Poster erweitern (gleiche Bildwörter).
4. Übungen aus den Mustern oben, je mit `mistakes` und `hint`; 1 bis 3 in `selfAssessment`.
5. Hörtexte: Datei `src/audio/<satz>.mp3`, Eintrag in `.agents/skills/app-content/scripts/audio-texte.json`, erzeugt mit `~/.cache/lernapps/audio/venv/bin/python .agents/skills/app-content/scripts/regen_audio.py .agents/skills/app-content/scripts/audio-texte.json "<Satz>"` (Skript aus hello-millbrook, schneidet das Ausklingen ab); anhören lassen; Sätze nicht zwischen Seiten wiederholen, Namen am Satzende zweisilbig.
6. Wörter gegen den Grundwortschatz prüfen; `npx --no -- lernapps check`; committen.

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
