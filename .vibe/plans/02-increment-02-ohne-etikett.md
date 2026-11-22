---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, as in the app's first plan. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs of this increment, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: {}
---

# Increment: increment-02-ohne-etikett

<!--
For you, the assistant. One increment of a published app: new competencies, chapters, pages, rounds, questions, or a
correction. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Content method and Retrospective, in the creator's
  language. Delete the comment of a section once the section is filled.
- The first version's decisions stand: archetype, content method, content guide. Never change an earlier plan.
- Work on the branch `increment/<NN>-<short name>`. Until Commit everything is local: push nothing.
-->

*Started 2026-11-22. Explore, Plan, Code, Commit.*

## Goal

Jugendliche (Stufe 7-8) entscheiden, wann im Englischen kein „the“ steht (allgemeine Aussagen, school, bed, Sonntage, Plural), und verbinden Nomen wie news, information, advice und police mit dem passenden Verb. Zwei Lesestücke tragen die Seiten: ein Chat und ein Artikel der Schülerzeitung.

## Key decisions

- Der Archetyp, die Muster und der Inhaltsführer der ersten Version gelten (Auftrag Orchestrator-Session, Konventionen Abschnitt 8).
- Kapitel 4 `ohne-etikett` mit drei Seiten: Wiederholung `das-brauchst-du` (recap simple-present), `artikel-gebrauch`, `nomen-kongruenz`; je Seite ein Lesestück (Chat, Schülerzeitung) (guess: Reihenfolge und Formen).
- Figuren: Sophie 13 bis 14, Ellie, Amir 13, Peter 11 bis 12, Mr Hill; Chats statt Szenenbilder; Bilder nur, wo sie etwas zeigen (guess).
- Das Etikettenbild (Kisten, Gläser) trägt weiter: Kiste ohne Etikett (Plural, Allgemeines), news als Glas, police als Gruppe von Kisten.
- `scope`: die App hat es schon (open-task nutzt es); Kapitel 4 bekommt `scope` je Seite wie bisher, `app.yaml` bekommt den Hinweis auf Kapitel 4 (in) statt „später“ (out).

## Notes

**Karte** (`https://lernapps.net/apps/map/englisch.json`, geöffnet am 2026-11-22), Strang `englisch/grammatik`, beide Lücken, Band 7-8, Schritt 1:
- `artikel-gebrauch`: „Ich kann entscheiden, wann ich „the“ weglasse, zum Beispiel bei allgemeinen Aussagen (Life is short.) und bei school, church oder bed.“ (requires `artikel`, steht in Kapitel 1)
- `nomen-kongruenz`: „Ich kann bei Nomen wie news, information, advice und police das Verb richtig anpassen.“ (requires `simple-present` aus #472 und `much-many`, Kapitel 2; darum eine Wiederholungsseite für simple-present)

**Kapitel `ohne-etikett` („Ohne Etikett und Sonderfälle“), drei Seiten:** `das-brauchst-du` (recap `englisch/simple-present`, ohne Übung), `artikel-gebrauch`, `nomen-kongruenz`.

**Didaktik:** Kiste ohne Etikett: allgemeine Aussagen (Plural und Glas ohne Etikett: Music is fun. Dogs are friendly.) und feste Ausdrücke (go to school, in bed, at home, on Sunday) aus Chat-Beispielen ableiten, dann sortieren (the/ohne). news, information, advice sind Gläser (is, kein -s, kein a: a piece of advice); police ist eine Gruppe von Kisten (are). Lesestück 1: Chat der Klasse zur Schülerzeitung (Sophie 13, Ellie, Amir, Peter, Mr Hill), 150 bis 300 Wörter; Lesestück 2: Artikel der Schülerzeitung „Millbrook News“ über den Besuch der Polizei (Verkehrssicherheit), 150 bis 300 Wörter. Aufgaben in drei Stufen (Verstehen, Belegen mit Zeile, Meinung), Schreibauftrag, Diktat und Nachsprechen (3+3 Sätze, eigene Sätze).

**Scope:** drin: the-Weglassung bei Allgemeinem, Mehrzahl und Glas, festen Ausdrücken (school, bed, home, work, Sunday/Monday, by bus) und Namen; news, information, advice, furniture, homework, police. Draußen: Artikel bei Ländernamen und Straßen (keine Karte), Phrasal verbs, Passiv; keine Religions- oder Herkunftsdetails (church nur als Beispiel der Karte, wenn überhaupt neutral; Entscheidung: nicht benutzen).

**Quellen und Prüfung:** alle Texte und Sätze sind eigene Texte nach Fakten. Geöffnet am 2026-11-22: Wikipedia `English articles` (Zusammenfassung: no determiner is the default for other common nouns; the, wenn alle den Gegenstand kennen), `Mass noun` (Zusammenfassung: uncountable nouns, undifferentiated unit), `Collective noun` (HTML: in British English können Sammelnomen den Singular oder den Plural des Verbs nehmen, je nach Zusammenhang). Nicht geprüft (HTTP 429 oder nur Zusammenfassung): Abschnitt „zero article“ von English articles, Wörterbuch-Einträge zu police (Plural im britischen Englisch), news, advice, information; keine VOA/Wikinews-Texte benutzt.

**Geprüft und behoben (Musterseite `artikel-gebrauch`, Lerner-Check Klasse 7 und Sprachprüfung durch Sub-Agenten):** Das Etikett-Bild wird im Einstieg erklärt; Einstiegsfrage mit anderem Satz („Close the door“); der Gegensatz Gebäude/Tätigkeit stand nur im Merke und steht jetzt mit hospital im Merke und mit school im Chat (Zeile 5 und 12); Zeitplan des Chats stimmig (nächsten Freitag, Konzert Samstag); Randglossar um until und Life is short ergänzt; Poster- und Übungsbeispiele getrennt; Tipps ohne Lösung; Ordnen als Frage mit eindeutiger Reihenfolge; Schreibaufgaben mit deutschem Satz, Varianten (loves|likes) und eigenen Meldungen; Meinungsaufgabe mit anderem Beispiel; kleine Deutschfehler. Offen (Vorlage): Meldung „Deine Fassung kann trotzdem richtig sein“, Titel erscheint zweimal, Hinweis zum KI-Tutor.

**Gesamtcheck Kapitel 4 (Sub-Agent, Kind Klasse 7-8, alle drei Seiten, 360 und 1280 px, beide Selbsteinschätzungen) und Sprachprüfung von `nomen-kongruenz`, behoben:** Wiederholungsseite erinnert an be (is/are) und an Kisten/Gläser; Sätze „Du brauchst das bei news …“ geklärt; App-Einleitung nennt Klasse 7-8; Glossar um Year 8, exciting, free; Kistengruppe vor dem Artikel erklärt; Beispiele in Merke/Poster von den Übungen getrennt (by train statt by bus, The water is cold, neues Zuordnungsbeispiel, anderes Beispiel der Meinungsaufgabe); doppelte Sätze zwischen Wahl und Schreiben ersetzt; Schreibaufgaben mit deutschem Satz (keine Raten-Cues in der Selbsteinschätzung); police immer Mehrzahl (britisch); Hausaufgabe-Cue; Rückblick nennt alle Kapitel. Offen (Vorlage): Auswahl-Lücken zeigen nur „nicht richtig“; Bildfehler in der Einschätzung (leeres src, unsichtbar).

## Explore

<!--
- All content questions belong here; Plan maps the answers onto the app. Ask; write no code.
- Skip what earlier answers or the app already tell. At most 2 questions per message, one topic each.
-->

### Tasks

- [x] Read the README of the archetype's template (its path is in skill `lernapps-app`): what the app can do now.
      Tell the creator what is new, if it matters for this increment.
- [x] Load the content guide `.agents/skills/app-content/SKILL.md` and read the earlier plans in `.vibe/plans/`: what
      the app teaches, how its content is made, what is open.
- [x] Interview, one topic per question, the creator's words under "Answers": which competencies, chapters or rounds,
      for which school years; hurdles and examples; the amount; any change of look and feel or of terms. No answer:
      ask once more, then write your assumption with "(guess)".
- [x] Load skill `lernapps-content-research`. Research what the content guide does not cover. Write under "Notes":
      the new competencies by chapter with their ids, the sources you opened.
- [x] Write under "Notes" the didactic approach per competency and the scope (in, out, data range).
- [x] The increment needs a kind of content the guide does not cover (a new page structure, screen, component or kind
      of exercise): load skills `lernapps-explainer-design` and `lernapps-exercise-patterns`. Else skip this task.
- [x] **Checkpoint:** research. Show in plain words: the new competencies by chapter, the didactic approach, the
      scope, every "(guess)", the sources and what is unchecked. Stop and wait. Changes: change them, then ask again.
      Creator: Ja, passt (drei Seiten, Wiederholung simple-present nur Text und Tabelle, zwei Lesestück-Sorten Chat und Schülerzeitung). Weiter zu Plan und Inhaltsmethode. Nichts weiter pushen, bis die Ersteller:in es erlaubt; Pull-Request noch nicht öffnen.

### Answers

- Aus der Auftragsnachricht der Orchestrator-Session (in der Rolle der Ersteller:in): Kapitel 4 „Ohne Etikett und Sonderfälle“, Stufe 7-8, als Inkrement im selben Repository, Muster der ersten Version, Regeln aus Abschnitt 7 und 8 der Konventionen; Vorschau-Pull-Request offen lassen, nichts nach `main`, kein Katalogeintrag.
- Issue #475, Kapitel 4: „Ich weiß, wann ich the weglasse (school, Sunday, people), und kann Nomen wie news und police mit dem passenden Verb verbinden.“

## Plan

<!--
- Map the new content onto the app with the guide's patterns. The creator confirms the plan in one read.
- After the yes you work on your own.
-->

### Tasks

- [x] Load skill `lernapps-content-growth`. Add the tasks of Code as slices, one per competency, in the guide's
      order, one call each: `npx --no -- lernapps plan add --at slices "<task>"`. Say in each which sub-agent may
      write it in parallel, if any.
- [x] Write "Content method": the guide's patterns, figures and components per slice. Anything new: map it as skill
      `lernapps-explainer-design` says, and say why the guide's patterns do not fit.
- [x] Draw a sketch of each new component or interactive exercise, in `.vibe/sketches/`.
- [x] Show the creator, short: goal, new competencies by chapter, slices; in plain words what learners see and do and
      what is new. At most 2 questions.
- [x] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.
      Creator: Ja, Plan und Inhaltsmethode bestätigt. Weiter mit Slice 1 und der Musterseite artikel-gebrauch.

### Content method

**Das Neue gegenüber der ersten Version: das Lesestück** (Konventionen Abschnitt 8). Die Muster der Seiten bleiben (Abschnitte einstieg/neu/uebung/anwenden/weiter, Neue-Wörter-Tabelle, Poster, Merke, `language-task`, `ordering`, Diktat, `speaking-task`, `open-task`, selfAssessment). Neu ist nur die Form des Einstiegs: ein Lesestück statt einer Szene. Mit den vorhandenen Blöcken, keine Komponente (`prefer-built-in-block`):
- **Chat:** `table` mit den Spalten Zeile, Wer, Nachricht, 8 bis 14 nummerierte Zeilen (so kann „Belege mit Zeile“ fragen). Bei der Schülerzeitung: `text`-Blöcke je Abschnitt (zwei bis drei).
- **Randglossar:** `definition`-Blöcke direkt unter dem Abschnitt (schwere Wörter am Rand, höchstens 6; sie erscheinen im Glossar der App).
- **Aufgaben in drei Stufen** (id-Präfix wie bisher): Verstehen (`single-choice`/`multiple-choice`, ohne die Antwort im Text direkt darüber), Belegen (`language-task` mode `choice` „In welcher Zeile steht …“ oder `single-choice` mit Zeilenzahl), Meinung (`open-task`). Dazu die Übungen zur Regel (Wahl, Zuordnung, Schreiben, Ordnen), Diktat und Nachsprechen.
- **Figuren:** ein Bild nur, wo es etwas zeigt (Kistenbild: Kiste ohne Etikett; news = Glas; police = Gruppe von Kisten); keine Szenenbilder der Figuren (Sophie ist 13 bis 14, Chat).
- Warum die Muster nicht ausreichen: ein Lesestück hat bisher gefehlt; es steht nach dem Bau der Seite `artikel-gebrauch` im Inhaltsführer (Abschnitt „Content structure“ und „Exercise patterns“).

**Seiten:**
1. `das-brauchst-du` (recap `englisch/simple-present`): Text und Tabelle (Person, Verb mit -s bei he/she/it), kein Lesestück, keine Übung; sie nennt den „Ich kann“-Satz der Karte.
2. `artikel-gebrauch` (`competencies: [artikel-gebrauch]`): Lesestück 1 „Millbrook News: Wer macht mit?“ (Chat, Schülerzeitung, 8 bis 10 Zeilen, Sophie 13, Ellie, Amir, Peter, Mr Hill; Beispiele für go to school, at home, in bed, by bus, Music is fun, People like …); Regel: Kiste ohne Etikett bei Allgemeinem (Plural, Glas), bei school/bed/home/work und Wochentagen, the bei Bestimmtem. Poster „Klassenzimmer-Poster · Kiste ohne Etikett“. Übungen: Zuordnung the/ohne, Lücke (the oder nichts als `[ ]`-Auswahl mit echten Fehlern: „the school“ für go to school, „the music“), Schreiben, Ordnen, Belegen mit Zeile, Meinung; Diktat/Nachsprechen 3+3.
3. `nomen-kongruenz` (`competencies: [nomen-kongruenz]`): Lesestück 2 „Die Polizei besucht die Schule“ (Artikel Millbrook News, Verkehrssicherheit, 3 Abschnitte); Regel: news, information, advice, furniture, homework sind Gläser (Verb in der Einzahl, kein a, kein -s: a piece of advice), police ist eine Kistengruppe (Verb in der Mehrzahl: the police are). Poster „Klassenzimmer-Poster · Glas oder Kistengruppe“. Übungen wie oben.

**Figuren (eigene SVG, `CC-BY-4.0`, wie Kapitel 1 bis 3):** `kiste-ohne-etikett.svg` (leeres Schild bei Allgemeinem), `glas-news.svg` (Glas news, Verb is), `kistengruppe-police.svg` (viele Kisten, Verb are). Jede erklärt ihre Lernaktion: Kinder sehen, dass die Kiste kein Etikett braucht, wenn nicht ein bestimmtes Ding gemeint ist; ein Glas bleibt in der Einzahl; die Kistengruppe nimmt das Verb in der Mehrzahl.

**Quellen und Prüfung:** eigene Texte, keine Sätze aus fremden Texten; Fakten (the bei Bekanntem, Mass nouns, britische Verbform bei police) mit den geöffneten Wikipedia-Seiten der Notes; was ungeprüft ist, steht im Inhaltsführer. Hörliste im Inhaltsführer (66 plus 12 Sätze, Schnitte).



## Code

<!--
- Build locally on the branch, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first.
-->

### Tasks

- [x] `git switch -c increment/<NN>-<short name>` from `main`. Commit this plan on it.
- [x] Load skill `lernapps-cli`. Update the app as its section "Update" says. Commit the update alone and fix its
      findings before any content. The update replaces the `lernapps-*` skills: read again those you use.
- [x] Load skill `lernapps-explainer` and the content guide.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [x] Kapitel `ohne-etikett` anlegen (app.yaml, chapter.yaml) und Wiederholungsseite `das-brauchst-du` (recap englisch/simple-present, nur Text und Tabelle, kein Sub-Agent).
- [x] Seite `artikel-gebrauch` (Musterseite für das Lesestück: Chat, Randglossar, Aufgaben Verstehen/Belegen/Meinung, Schreibauftrag, Diktat und Nachsprechen); Figuren, Audio, Inhaltsführer (kein Sub-Agent).
- [x] Seite `nomen-kongruenz` (Lesestück: Artikel der Schülerzeitung, Aufgaben, Audio, Selbsteinschätzung Kapitel 4; kein Sub-Agent, weil sie das Muster der vorigen Seite braucht).
<!-- tasks: slices (3 added): one per competency, as written in Plan -->
- [x] **Checkpoint:** the pattern page, after the first slice. A slice in a pattern the app already has: show it to
      the creator and go on. A new pattern: load skill `lernapps-learner-check`, do its learner check, fix what it
      finds, then ask the creator whether the others may follow it, and wait.
      Creator: Ja, nomen-kongruenz darf nach dem Muster folgen (Orchestrator-Session in der Rolle der Ersteller:in).
- [x] Update the content guide so that it describes the app as it is now (`app-content-matches`).
- [x] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every changed screen, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.

## Commit

<!--
- Publish with the creator's yes. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
-->

### Tasks

- [ ] If pages or exercises changed, load skill `lernapps-explainer-self-assessment` and update the self-assessment
      as it says. Commit.
- [ ] Load skill `lernapps-github`. Push the branch, open the preview pull request and see its checks to green, as it
      says.
- [ ] **Checkpoint:** publish. Show what the increment adds and the preview link. Ask whether it may go online. Stop
      and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: the pull request squash-merged into
      `main`, the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm the new content. Never use a derived address.
- [ ] The app is listed and its entry changes (school years, summary): load skill `lernapps-listing` and write the
      changed entry. Else skip this task.
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it. A push of only `.vibe/` publishes nothing.
- [ ] **Checkpoint:** list. The entry changed: open the pull request to the catalog as skill `lernapps-listing`
      says, without asking first, see it to "bestanden", then show the creator the pull request and its result. The
      entry did not change: tell the creator that the catalog updates the app by itself.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

## Retrospective

<!-- At the end of Commit. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, content guide, messages or answers, and your choice. "None" if none. -->
