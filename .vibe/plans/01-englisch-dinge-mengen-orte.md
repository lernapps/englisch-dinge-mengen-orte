---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: explore
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
- Eine Seite je Baustein, 13 Seiten in 3 Kapiteln: 12 Bausteine plus eine Sammel-Wiederholung am Anfang von Kapitel 3.
- Keine Komponente und keine Datendatei (`prefer-built-in-block`): Kisten und Gläser sind Zeichnungen (SVG); Ziehen und Füllen wäre ein Wunsch für ein Inkrement (guess).
- Hörtexte: je Seite 3 Diktatsätze und 3 Nachsprechsätze, wie in #472 (guess).

## Notes

**Quelle des Auftrags:** Issue lernapps/apps#475 (Epic #489, Konventionen dort, Kopie in `/tmp/auftraege/orchestrierung/`). Muster: hello-millbrook (#470), englisch-zeiten (#472, Branch `work`).

**Strang:** `englisch/grammatik` (Karte `https://lernapps.net/apps/map/englisch.json`, Fokus `competency`; geöffnet am 2026-11-21). Alle zwölf Bausteine sind Lücken der Karte, Band 5-6 (`practisedBy` leer).

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

**Umfang:** drin: alle 12 Bausteine, 13 Seiten, Wörter aus A1/A2 (Grundwortschatz), Aussprache nur über Hörtexte. Draußen: Kapitel 4, Phrasal verbs (#485), Possessivbegleiter (#471), Adjektive und one (#476), freie Aufgaben ohne Prüfung (nur `open-task`), Spracherkennung. Sprache: Deutsch (englische Beispiele); keine englische Fassung (Vorgabe wie #472, guess).

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
- [ ] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.

### Answers

<!-- Antworten aus dem Auftrag (Issue #475) und der Startnachricht der Orchestrator-Session; keine eigenen Antworten der Ersteller:in. -->

- Goal: „Ich kann Dinge mit dem passenden Begleiter benennen, Mengen angeben und sagen, wo und wann etwas ist.“ (Leitidee, Issue #475)
- Learners: Englisch, Stufe 5-6 (Klasse 5-6, erstes und zweites Lernjahr); Vorwissen: Hello, Millbrook! (#470), Personalpronomen (#471), Zeiten und to be (#472).
- Model and focus: Muster hello-millbrook (#470) und englisch-zeiten (#472); Schwerpunkt Übungen und Zeichnungen (Kisten, Gläser, Regale, Zeit-Behälter). (Startnachricht)
- Hurdles: Vorgabe des Auftrags: a/an, unregelmäßige Plurale, 's und of, much/many, some/any, there is/are, in/on/at. Genaue Fehler siehe Notes. Eigene Beispiele der Ersteller:in: keine.
- Content: aus Karte und Auftrag, von mir geschrieben; kein eigenes Material.
- Amount: Kapitel 1 bis 3 (13 Seiten); Kapitel 4 später als Inkrement. (Startnachricht)
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

- [ ] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [ ] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [ ] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [ ] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [ ] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [ ] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [ ] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.

### Content method

<!-- One line each: the patterns and where; the figures and how they are made; the data files; each component, what it
checks and what it cannot; how a later agent adds a chapter. It becomes the content guide in Code. -->
<!-- An explainer: per figure, model and component its learning action in two to four sentences
(`explainer-representation-explained`); per page its prerequisites the app does not practise, and which get a recap
page, which a link. -->

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [ ] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [ ] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [ ] Load skill `lernapps-explainer`.
- [ ] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [ ] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
<!-- tasks: pattern: the one page or screen that is the pattern for the others -->
- [ ] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
<!-- tasks: pages: the other pages or screens, after the pattern -->
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
