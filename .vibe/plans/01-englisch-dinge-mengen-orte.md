---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: {}
---

# Plan: englisch-dinge-mengen-orte, first version

<!--
For you, the assistant. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Entry draft, Content method and Retrospective, in the
  creator's language. Delete the comment of a section once the section is filled.
- Work on the branch `work`, locally: push nothing before Commit.
-->

*Started 2026-11-21. Explore, Plan, Code, Commit.*

## Goal

Kinder der Klassen 5-6 füllen Kisten (zählbar) und Gläser (nicht zählbar) fürs Schulfest und lernen dabei Artikel, Plural, Genitiv, this/that, many/much, some/any, there is/are und die Präpositionen des Ortes und der Zeit. Gebaut werden nur die Kapitel 1 bis 3 (Stufe 5-6); Kapitel 4 (Stufe 7-8) kommt später als Inkrement.

## Key decisions

- Archetyp `explainer`: Kinder lesen kurze Seiten mit Bild und üben auf jeder Seite; Sprachaufgaben (`language-task`), Diktat und Nachsprechen sind eingebaut. Kein Spiel nötig (gelesen: README des Explainers).
- Strang-App `englisch/grammatik`, Format 2, Sprache Deutsch mit englischen Beispielen (Vorgabe aus Issue #475).
- Eine Seite je Baustein, 12 Seiten in 3 Kapiteln: 11 Bausteine plus eine Sammel-Wiederholung am Anfang von Kapitel 3.
- Keine Komponente und keine Datendatei (`prefer-built-in-block`): Kisten und Gläser sind Zeichnungen (SVG); Ziehen und Füllen wäre ein Wunsch für ein Inkrement (guess).
- Hörtexte: je Seite 3 Diktatsätze und 3 Nachsprechsätze, wie in #472 (guess).

## Notes

**Quelle des Auftrags:** Issue lernapps/apps#475 (Epic #489, Konventionen dort, Kopie in `/tmp/auftraege/orchestrierung/`). Muster: hello-millbrook (#470), englisch-zeiten (#472, Branch `work`).

**Strang:** `englisch/grammatik` (Karte `https://lernapps.net/apps/map/englisch.json`, Fokus `competency`; geöffnet am 2026-11-21). Alle elf Bausteine sind Lücken der Karte, Band 5-6 (`practisedBy` leer).

**Bausteine nach Kapitel** (Reihenfolge nach `requires`, „Ich kann“-Sätze aus der Karte, nicht umformuliert):
1. `ein-ding-viele-dinge` („Ein Ding, viele Dinge“): `artikel` (Schritt 1), `plural` (1), `genitiv` (2, braucht plural), `demonstrativ` (2, braucht plural).
2. `wie-viel-wie-viele` („Wie viel und wie viele?“): `much-many` (2), `mengen-mit-of` (2), `some-any` (2), `somebody-anything` (3, braucht some-any). Alle brauchen `plural` aus Kapitel 1.
3. `wo-und-wann` („Wo und wann?“): Sammel-Wiederholung `recap: [englisch/to-be, englisch/datum, englisch/uhrzeit]` (`das-brauchst-du`, ohne Übung: `to-be` aus #472, `datum` und `uhrzeit` aus #470), dann `praepositionen-ort` (1), `there-is-are` (3, braucht to-be und plural), `praepositionen-zeit` (3, braucht uhrzeit und datum).
Von außen braucht die Karte: `to-be`, `datum`, `uhrzeit` (alle nur in Kapitel 3). Kapitel 4 (`artikel-gebrauch`, `nomen-kongruenz`) ist nicht Teil dieser Session.

**Didaktik:** Kisten (zählbar: a box, two boxes) und Gläser (nicht zählbar: water, rice) tragen den Explainer. Etiketten auf Kiste/Glas = Begleiter (a/an, the, this/that, some/any, much/many). Wo eine Kiste steht, sagen die Präpositionen; für die Zeit werden daraus Zeit-Behälter (in = große Kiste für Monat/Jahr, on = Fläche für den Tag, at = Punkt für die Uhrzeit). Geschichte: Mr Hill lässt die Klasse den Lagerraum der Millbrook School fürs Schulfest sortieren (Kisten, Gläser, Regale, Schulkalender) (guess; neue Orte: Lagerraum und Schulfest, im Inhaltsführer eingetragen).

**Wie die Kinder üben (Muster, `lernapps-exercise-patterns` und `references/foreign-languages.md`):** zuordnen/wählen (Kiste oder Glas? a oder an?) → Lücke → Form bilden mit Cue (Plural, Genitiv) → Entscheiden mit Begründung (much oder many, some oder any, in/on/at) → Diktat und Nachsprechen → `open-task` (eigene Kiste oder eigenes Regal beschriften). Je Übung `mistakes` mit eigener Rückmeldung. Typische Fehler: a vor Vokal, `childs`/`mans`, Apostroph im Plural (apple’s), `the Sophie’s bike`, `Peters’s`, much bei zählbaren Dingen, some in der Frage, `there is` bei Mehrzahl, `in Monday`, `at July`, `on 8 o’clock`.

**Wie sie dorthin kommen und welchen Fehler die Rückmeldung fängt (eine Zeile je Baustein):**
- `artikel`: Kinder sortieren Dinge in Kisten und leiten aus dem Anlaut (nicht dem Buchstaben) a oder an ab; the beim ersten und zweiten Mal. Fehler: „an university“, „a hour“, a vor Vokalbuchstaben.
- `plural`: Kiste mit -s, dann -es, -ies, Überraschungskisten (children, men, feet); sie bilden den Plural mit Cue. Fehler: „childs“, „mans“, „apple’s“, -s an Wörtern auf -y.
- `genitiv`: Besitzer an die Kiste schreiben (Sophie’s bag, the girls’ room), of für Dinge (the door of the room). Fehler: „the bag of Sophie“ als Regelfall, Apostroph vor oder nach dem s vertauscht, „Peters“.
- `demonstrativ`: Hand nah/fern am Bild, dann Singular/Plural (this/these, that/those). Fehler: „this books“, nah/fern vertauscht.
- `much-many`: Kiste (many) oder Glas (much) entscheiden, a lot of als Joker, a few/a little. Fehler: „much books“, „many water“.
- `mengen-mit-of`: das Glas wird mit a cup of zählbar (two cups of tea). Fehler: of vergessen, Plural am falschen Wort („two cup of teas“).
- `some-any`: Etikett wechselt in Frage und Verneinung; no als Verneinung in der Aussage. Fehler: „I have any apples“, some in der Verneinung.
- `somebody-anything`: Etiketten ohne Nomen (somebody, anything, nobody, everywhere) aus some/any ableiten. Fehler: „nobody doesn’t“, anybody in Aussagen.
- `praepositionen-ort`: Kiste im Zimmer platzieren (in, on, under, next to, behind) nach Zeichnung. Fehler: on und in vertauscht, „under of“.
- `there-is-are`: Kisten im Regal zählen: eine → there is, mehrere → there are, Verneinung und Frage. Fehler: „there is two boxes“, „is there any boxes“.
- `praepositionen-zeit`: Zeit-Behälter in (Monat, Jahr) / on (Tag, Datum) / at (Uhrzeit). Fehler: „in Monday“, „at July“, „on 8 o’clock“, „in the 5th of May“.

**Umfang:** drin: alle 11 Bausteine, 12 Seiten, Wörter aus A1/A2 (Grundwortschatz), Aussprache nur über Hörtexte. Draußen: Kapitel 4, Phrasal verbs (#485), Possessivbegleiter (#471), Adjektive und one (#476), freie Aufgaben ohne Prüfung (nur `open-task`), Spracherkennung. Sprache: Deutsch (englische Beispiele); keine englische Fassung (Vorgabe wie #472, guess).

**Quellen:** Karte (s. o.); Grundwortschatz `https://lernapps.net/apps/map/englisch/grundwortschatz/`; Wikipedia, nur Fakten, keine Sätze (CC BY-SA), geöffnet am 2026-11-21: `English articles`, `English plurals`, `English possessive`, `English prepositions`, `Demonstrative`. Nicht geprüft: `Mass noun` und `English determiners` (HTTP 429), deutsche Wikipedia und Klexikon nicht gelesen. Beispielsätze eigene aus dem Alltag der Figuren. Material der Ersteller:in: keines.

## Explore

<!--
- Find out what the app teaches, for whom, how much and how it looks. Ask; write no code, run no `create`.
- An answer counts only in the creator's words under "Answers". At most 2 questions per message, one topic each.
-->

### Tasks

- [x] Check the start: the folder `.agents/skills/lernapps-app` exists (else stop and tell the creator that the folder
      was not started with `init`), and `git branch --show-current` prints `work` (else `git switch -c work`).
- [x] Load skill `lernapps-app`. Tell the creator in two sentences what a lernapps app is and where it will live: at
      their own address, free and public, and once listed as a copy on lernapps.net. Say that the technical part
      (GitHub) comes at the end and that you do it.
- [x] Interview: ask the topics "Goal" and "Learners" of "Answers".
- [x] Load skill `lernapps-map-assignment` and read the learning map of the subject as it says. The creator brings
      the content themselves (material, a word list, the pages): note under "Notes" which competencies of the map it
      covers. Else write the skill's assignment, with its story; the creator's yes answers the topics Content and
      Amount. A subject without a map: skip this task and say so.
- [x] Load skill `lernapps-exercise-patterns` and read its reference for the subject. Note under "Notes" how learners
      will practise what the goal names.
- [x] Choose the archetype as skill `lernapps-app` says: read the README of each archetype in question, then tell the
      creator in plain words what the chosen one can and cannot do. Write the archetype and its reason under "Key
      decisions".
- [x] Run `npx --no -- lernapps skills --archetype <name>` with the chosen archetype. It installs the archetype's
      skills and adds the archetype's tasks to this plan.
- [x] Load skill `lernapps-explainer-design`. An explainer has the look of the runtime: write "fixed by the
      archetype" under the topic "Look and feel" of "Answers".
- [x] Interview: ask every other topic of "Answers", in order. Leave out only a topic that an answer of the creator
      already covers, and note which answer. A topic nobody answered is asked once before you write an assumption
      with "(guess)".
- [x] Load skill `lernapps-content-research` and research as it says. Write under "Notes": the strand or subject, the
      competencies by chapter with their ids, the sources you opened.
- [x] Write under "Notes" which competency goes on which page and which pages form a chapter, as "Map the content" of
      skill `lernapps-explainer-design` says. Per page, name the prerequisites the app does not practise.
- [x] Write under "Notes", one line per competency: how learners get there (they derive it, they do not only read it
      off), and which misconception the feedback catches.
- [x] Write under "Notes" the scope: what is in, what is out and why, the data range (for example "all main-group
      elements", never a silent "1–20"), the languages.
- [x] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.
      Creator: Ja, zum Plan übergehen; Zählung korrigieren (11 Bausteine, 12 Seiten); Geschichte Lagerraum/Schulfest einverstanden, Beschreibung in zwei Sätzen schicken, nichts erfinden, was #471/#472/#476/#478 benutzen; Seiten von #471 und #480 im Detail lesen.

### Answers

<!-- Antworten aus dem Auftrag (Issue #475) und der Startnachricht der Orchestrator-Session; keine eigenen Antworten der Ersteller:in. -->

- Goal: „Ich kann Dinge mit dem passenden Begleiter benennen, Mengen angeben und sagen, wo und wann etwas ist.“ (Leitidee, Issue #475)
- Learners: Englisch, Stufe 5-6 (Klasse 5-6, erstes und zweites Lernjahr); Vorwissen: Hello, Millbrook! (#470), Personalpronomen (#471), Zeiten und to be (#472).
- Model and focus: Muster hello-millbrook (#470) und englisch-zeiten (#472); Schwerpunkt Übungen und Zeichnungen (Kisten, Gläser, Regale, Zeit-Behälter). (Startnachricht)
- Hurdles: Vorgabe des Auftrags: a/an, unregelmäßige Plurale, 's und of, much/many, some/any, there is/are, in/on/at. Genaue Fehler siehe Notes. Eigene Beispiele der Ersteller:in: keine.
- Content: aus Karte und Auftrag, von mir geschrieben; kein eigenes Material.
- Amount: Kapitel 1 bis 3 (12 Seiten); Kapitel 4 später als Inkrement. (Startnachricht)
- Languages: Deutsch mit englischen Beispielen, wie #472 (guess).
- Look and feel: fixed by the archetype.
- Terms: Kiste (zählbar), Glas (nicht zählbar), Etikett (Begleiter), Zeit-Behälter; „Ausdruck“, „Klassenzimmer-Poster“, „Schulkalender“ (Konventionen).
- Finding the app: „Englisch Grammatik Artikel Plural much many some any there is there are Präpositionen“ (guess).

## Plan

<!--
- Map the confirmed content onto the archetype. No new content questions: a gap in the content goes back to Explore.
- The creator confirms the plan in one read. After the yes you work on your own.
-->

### Tasks

- [x] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [x] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [x] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [x] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [x] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [x] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [x] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.
      Creator: Ja, Plan und Inhaltsmethode ok, artikel als Musterseite. Bedingungen: competencies je Seite auf Karten-Ids, Wiederholungsseite ohne; keine neuen Figuren; Neue-Wörter-Tabelle A1/A2, Ausnahmen im Inhaltsführer; vor Musterseiten-Meldung Lerner-Check (Kind 5/6) und Sprachprüfung per Sub-Agent.

### Content method

**Gelesen vor dem Plan:** #472 (englisch-zeiten, Inhaltsführer und `das-brauchst-du`), #471 (englisch-pronomen: `wer-tut-es`, Inhaltsführer), #480 (englisch-verbketten: Inhaltsführer), hello-millbrook. Übernommen: Abschnitts-IDs `einstieg`/`neu`/`uebung`/`anwenden`/`weiter`; je Seite eine Szene `szene-<seite>.svg` aus den Figuren von #470; Tabelle „Klassenzimmer-Poster · Neue Wörter“ im `einstieg` jeder Seite (Wörter vor der ersten Übung, wie #480); wachsende Poster-Tabellen (`rowHeaders: true`, nicht direkt über der Übung, die sie beantwortet); Übungs-IDs mit Seitenpräfix; `mistakes` mit Regel, nie nur Lösung; Merke-Kasten mit anderen Wörtern als die Übungen; Antwort nie im Absatz darüber.

**Quelle der Wörter:** Grundwortschatz Englisch (A1/A2), `https://lernapps.net/apps/map/englisch/grundwortschatz/`. Wörter außerhalb der Liste (storeroom, jar, shelf, fair o. ä.) nur mit deutscher Bedeutung auf der Seite eingeführt und hier nach dem Bau gelistet.

**Geschichte (Bild: Kisten und Gläser):** Mr Hill lässt die Klasse den Lagerraum der Millbrook School (ein Raum im Erdgeschoss neben dem Klassenzimmer) für das Schulfest ordnen: Zählbares kommt in Kisten, Nicht-Zählbares in Gläser, alles bekommt Etiketten und einen Platz im Regal. Das Schulfest ist am ersten Samstag im Dezember um 10 Uhr; der Schulkalender hängt neben der Lagerraumtür. Sophie, Ellie, Peter, Amir und Mr Hill wie in den Konventionen; Mrs Parker backt Kuchen fürs Fest. Nichts davon benutzen #471 (Sports day), #472 (Zeitstrahl), #480 (Flur, Wochenende, Café).

**Seiten** (Kapitel-ID/Seiten-ID → Baustein; Zeile je Seite nach `explainer-design`: Eröffnung · Wechsel · Belohnung · Geschichte):
1. `ein-ding-viele-dinge/artikel` (Musterseite): Eröffnung: Kiste mit Dingen aus dem Lagerraum, a oder an auf das Etikett (leichte Wahl, mit Begründung nach dem Anlaut). Wechsel: sehen (Szene) → Etikett setzen (matching) → Lücke → schreiben. Belohnung: „Ich kann Kisten richtig beschriften.“ Geschichte: erster Tag im Lagerraum, Mr Hill verteilt Etiketten. Führt Kisten ein.
2. `…/plural`: Eine Kiste wird viele Kisten: -s, -es, -ies, Überraschungskisten (children, men, feet). Geschichte: die Kisten stapeln sich.
3. `…/genitiv`: Wem gehört die Kiste? Sophie’s box, the girls’ box, the lid of the box. Geschichte: Namensschilder auf Kisten.
4. `…/demonstrativ`: this/these nah, that/those fern: Hand zeigt. Geschichte: Mr Hill fragt von der Tür, welche Kiste gemeint ist. Rückblick Kapitel 1.
5. `wie-viel-wie-viele/much-many`: many für Kisten, much für Gläser, a lot of, a few/a little. Geschichte: Gläser kommen dazu (rice, water, sugar). Führt Gläser ein.
6. `…/mengen-mit-of`: a cup of, a bottle of, a pair of machen das Glas zählbar. Geschichte: Mrs Parker braucht Zutaten fürs Fest.
7. `…/some-any`: Etikett wechselt in Frage/Verneinung, no. Geschichte: Was ist noch da? Inventarliste.
8. `…/somebody-anything`: Etiketten ohne Nomen. Geschichte: Jemand hat etwas versteckt. Rückblick Kapitel 2.
9. `wo-und-wann/das-brauchst-du` (Wiederholung, nur Text und Tabellen, `recap: [englisch/to-be, englisch/datum, englisch/uhrzeit]`): am, is, are; Monate und Wochentage; Uhrzeiten, kompakt.
10. `…/praepositionen-ort`: in, on, under, next to, behind: Kiste im Regal/Zimmer. Geschichte: Regalplan des Lagerraums.
11. `…/there-is-are`: There is a box on the shelf. There are two jars under the table. Geschichte: Inventur.
12. `…/praepositionen-zeit`: Zeit-Behälter in/on/at fürs Schulfest und den Schulkalender. Rückblick auf die ganze App (Kisten, Gläser, Regal, Kalender).

**Muster (Übungsarten, in den Inhaltsführer):** (a) zuordnen: `matching` Ding ↔ Etikett/Kiste/Glas; (b) Etikett wählen: `language-task` mode `choice` mit `distractors`; (c) Lücke: mode `gap`; (d) Form bilden: mode `write` mit `cue` (`cue: "child · 2"`); (e) Tabelle ableiten: mode `table` (Singular/Plural, this/these, some/any); (f) Reihenfolge: `ordering` (Satzbau mit there is/are, Zeitangabe); (g) entscheiden: `true-false` und `single-choice`, Begründung nennt die Kiste, das Glas oder den Zeit-Behälter; (h) Diktat `<seite>-hoeren` und Nachsprechen `<seite>-nachsprechen` (je Seite 3 + 3 ganze Sätze, eigene Sätze, nie wiederholt); (i) `open-task`: eigenes Etikett, eigenes Regal, eigener Kalendereintrag. Je Seite mindestens vier Übungen, nicht überwiegend Raten; `selfAssessment` je Kapitel, zwei Übungen je Seite (Skill `lernapps-explainer-self-assessment`).

**Figuren:** eigene SVG-Familie in `src/images/` (CC-BY-4.0, Quelle „eigene Zeichnung“, Hintergrund wie #472, Schrift mindestens 16 im 480er viewBox, 360 px): `kiste-*.svg` (Kiste mit Etikett, Einzahl/Mehrzahl, Überraschungskiste), `glas-*.svg` (Glas mit Etikett), `regal-*.svg` (Regalplan für Orte und there is/are), `zeit-behaelter.svg` (große Kiste = in, Fläche = on, Punkt = at). Je Seite eine Szene `szene-<seite>.svg` mit Figuren, kopiert aus `millbrook-klassenzimmer.svg` von hello-millbrook (`<g id>`, nicht verändert). `alt` verrät nie die Lösung; Bildunterschrift nennt, wer wer ist. Poster und Kalender sind `table`-Blöcke: „Klassenzimmer-Poster · Kisten und Gläser“ (wächst durch Kapitel 1 und 2), „Klassenzimmer-Poster · Orte“, „Schulkalender · Zeitangaben“ (Kapitel 3).

**Engagement je Seite** (Eröffnung · Wechsel · Belohnung · Geschichte):
- `artikel`: a oder an auf ein Etikett kleben · Szene sehen → Etikett wählen → Lücke → schreiben · „Du beschriftest Kisten richtig“ · Mr Hill gibt Etiketten aus; nächster Schritt: viele Kisten.
- `plural`: eine Kiste, zwei Kisten: Etikett der Mehrzahl wählen · matching → Tabelle ableiten → schreiben mit Cue · Überraschungskisten gefunden · die Kisten stapeln sich; nächster Schritt: Namen darauf.
- `genitiv`: Wem gehört die Kiste? Namensschild wählen · wählen → schreiben → ordnen · alle Kisten haben Besitzer · Namensschilder; nächster Schritt: Mr Hill fragt von der Tür.
- `demonstrativ`: Hand nah oder fern zeigt auf die Kiste · wählen → Tabelle → schreiben · „Du zeigst richtig“ + Rückblick Kapitel 1 · Mr Hill ruft von der Tür.
- `much-many`: Kiste oder Glas? sortieren · sortieren → wählen → schreiben · Zutatenliste stimmt · die Gläser kommen.
- `mengen-mit-of`: Wie viel Tee ist ein Glas? a cup of · zuordnen → schreiben → ordnen · Einkaufsliste fertig · Mrs Parker braucht Zutaten.
- `some-any`: Was liegt noch im Regal? Etikett some oder any · wählen → Lücke → entscheiden · Inventarliste · Fragen an Peter.
- `somebody-anything`: Jemand hat etwas versteckt: Etikett ohne Nomen · zuordnen → Lücke → schreiben + Rückblick Kapitel 2 · Suche im Lagerraum.
- `das-brauchst-du`: nur Text und Tabellen (is/are, Monate, Uhrzeiten) · Wechsel Tabelle/Bild · „Du bist bereit“ · Regal und Kalender erscheinen.
- `praepositionen-ort`: Wo steht die Kiste? Regalbild · zuordnen → wählen → schreiben · Regalplan ist fertig · Peter stellt die Kisten.
- `there-is-are`: Wie viele Kisten stehen im Regal? zählen · wählen → ordnen → schreiben · Inventur gelingt · Inventurliste an Mr Hill.
- `praepositionen-zeit`: Wann ist das Schulfest? Zeit-Behälter wählen · zuordnen → wählen → entscheiden → eigener Kalendereintrag · Rückblick der App · Schulfest beginnt.

**Muster je Baustein:** artikel → (a), (b), (d); plural → (e), (d), (c); genitiv → (b), (d), (f); demonstrativ → (a), (b), (e); much-many → (a), (b), (g); mengen-mit-of → (a), (d), (f); some-any → (b), (c), (g); somebody-anything → (a), (c), (d); praepositionen-ort → (a) nach Regalbild, (b), (d); there-is-are → (b), (f), (d); praepositionen-zeit → (a) Termin ↔ Behälter, (b), (g), (i).

**Keine Komponente, keine Datendatei:** jede Tatsache steht einmal in ihrer Seite (`prefer-built-in-block`). Ziehen von Dingen in Kisten wäre ein Wunsch für ein Inkrement.

**Ein späterer Agent fügt Kapitel 4 so hinzu** (`artikel-gebrauch`, `nomen-kongruenz`, Stufe 7-8): Karte lesen, Voraussetzungen prüfen (`artikel`, `plural` stehen auf den Seiten 1 und 2), Seite `src/<kapitel>/<seite>.yaml` mit denselben Abschnitten anlegen, in `chapter.yaml` eintragen, Form wechselt auf Nachrichten und kurze Dialoge (Stufe 7-8, Konventionen 2), Kisten ohne Etikett (Nullartikel), news als Glas (is), police als Kistengruppe (are).

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [x] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [x] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [x] Load skill `lernapps-explainer`.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [ ] Musterseite `ein-ding-viele-dinge/artikel`: Szene und Kisten-Zeichnung, Wörter-Tabelle, Merke-Kasten, mindestens vier Übungen mit mistakes, Diktat und Nachsprechen (Audio), open-task; dazu app.yaml und chapter.yaml des Kapitels. Zeigt die Kisten-Idee und den Seitenaufbau.
<!-- tasks: pattern (1 added): the one page or screen that is the pattern for the others -->
- [ ] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
- [ ] Seite `plural` (Kisten mit -s, -es, -ies, Überraschungskisten) mit Übungen, Audio und Szene.
- [ ] Seite `genitiv` (Sophie’s box, the girls’ box, of) mit Übungen, Audio und Szene.
- [ ] Seite `demonstrativ` (this/these, that/those) mit Übungen, Audio, Szene, Kapitelrückblick und selfAssessment von Kapitel 1.
- [ ] Seite `much-many` (Kisten und Gläser, a lot of, a few/a little) mit Übungen, Audio und Szene.
- [ ] Seite `mengen-mit-of` (a cup of, a bottle of, a pair of) mit Übungen, Audio und Szene.
- [ ] Seite `some-any` (some, any, no) mit Übungen, Audio und Szene.
- [ ] Seite `somebody-anything` mit Übungen, Audio, Szene, Kapitelrückblick und selfAssessment von Kapitel 2.
- [ ] Kapitel 3: Sammel-Wiederholung `das-brauchst-du` (recap to-be, datum, uhrzeit) und Seite `praepositionen-ort` mit Regalbild, Übungen, Audio und Szene.
- [ ] Seite `there-is-are` mit Übungen, Audio und Szene.
- [ ] Seite `praepositionen-zeit` (Zeit-Behälter in/on/at, Schulkalender) mit Übungen, Audio, Szene, Rückblick der App und selfAssessment von Kapitel 3.
- [ ] Alle Wörter gegen den Grundwortschatz prüfen, Medienübersicht und Quellen im Inhaltsführer ergänzen, Inhaltsführer nachführen.
<!-- tasks: pages (11 added): the other pages or screens, after the pattern -->
- [ ] Update the content guide so that it describes the app as built (`app-content-matches`).
- [ ] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every screen and state, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.
      Compare each with its sketch.
- [ ] Do the whole-app check of skill `lernapps-learner-check`. Fix what it finds and write under "Notes" what you
      fixed.

## Commit

<!--
- Put the app on GitHub, publish it with the creator's yes, then list it. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
- The creator asked to stop before publishing (a trial): stop here and say so.
-->

### Tasks

- [ ] Load skill `lernapps-explainer-self-assessment`. Add the self-assessment as it says, or write under "Key
      decisions" why the app has none. Commit.
- [ ] Load skill `lernapps-github`. Set up the repository and Pages as it says. Ask for the repository's name and
      every click only the creator can make, in one message.
- [ ] Push `work`, open the preview pull request and see its checks to green, as skill `lernapps-github` says.
- [ ] **Checkpoint:** publish. Show what the app does and the preview link from the comment "Vorschau der App". Ask
      whether it may go online. Stop and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: `work` into `main` as one squash commit,
      the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm that the app shows. Never use a derived address.
- [ ] Load skill `lernapps-listing`. Write the entry under "Entry draft" as it says, with the creator's answer to
      "Finding the app".
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it: the listing check and the review read it there.
- [ ] **Checkpoint:** list. Open the listing pull request as skill `lernapps-listing` says, without asking first: the
      pull request is the review. See it to "bestanden", then show the creator the pull request and its result.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

### Entry draft

<!-- YAML valid against the entry schema the listing skill names. Only known values, never invented. -->

```yaml
```

## Retrospective

<!-- At the end of Commit, before the listing pull request. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, messages or answers, and your choice. "None" if none. -->
