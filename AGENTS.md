# AGENTS.md

# Alimida project instructions

This repository contains the specification documents for Alimida, a learning-oriented constructed language.

## Primary goal

Maintain consistency across the Alimida specification documents.

Do not expand the language unnecessarily. Prefer closing, classifying, or deferring TODO items over adding new ones.

## Document roles

* `00_index.md`: document index
* `01_overview.md`: project overview and design philosophy
* `02_phonology.md`: pronunciation and writing rules
* `03_grammar.md`: grammar rules
* `04_vocabulary_core100.md`: core vocabulary
* `05_examples.md`: examples
* `06_vocabulary_basic_systems.md`: numbers, directions, colors, quantity/degree, time/date basics
* `90_decisions.md`: accepted decisions
* `91_todo.md`: TODO / roadmap
* `92_changelog.md`: change history
* `alimida_review_issues_v1.md`: review notes and archived discussion points

## Editing rules

* Keep v1.1 focused on stabilization.
* Do not introduce new grammar, vocabulary, or notation unless explicitly requested.
* If a topic is not needed for v1.1, classify it as `v1.x`, `v1.2以降`, or `Frozen` instead of solving it immediately.
* When changing a specification, check whether related examples, decisions, TODOs, and changelog entries also need updates.
* Prefer standard forms in examples.
* Do not treat acceptable forms as standard forms unless the decision file says so.
* Do not remove historical review notes unless explicitly requested.

## Version scope

### v1.1

Focus on:

* grammar consistency
* adopted core vocabulary
* adopted basic systems vocabulary
* standard / acceptable / non-standard form classification
* minimal learner-facing explanations
* TODO cleanup and roadmap organization

### v1.x

Use for:

* example set expansion
* lesson organization
* learner-facing explanations
* pronunciation practice materials
* AI correction / teaching guidelines

### v1.2 or later

Use for:

* ordinals
* full date notation
* time notation
* weekdays and month names
* numbers over 9999
* existential negation
* possession negation
* derivation rules
* compound word rules
* loanword rules

### Frozen

Use for topics intentionally postponed and not currently blocking v1.1.

## Style

* Write documents in Japanese, except for direct quotations or examples from other languages.
* Alimida examples, English glosses, command names, file names, code blocks, and technical identifiers may remain in their original language when appropriate.
* Keep explanations clear and learner-friendly.
* Use concise examples.
* Prefer consistency over cleverness.
* When unsure, preserve the existing specification and add a TODO rather than changing the rule.

## Validation checklist

Before finishing a task, check:

* Are `03_grammar.md` and `05_examples.md` consistent?
* Are vocabulary forms consistent between `04_vocabulary_core100.md` and `06_vocabulary_basic_systems.md`?
* If a decision was made, is `90_decisions.md` updated?
* If user-visible spec changed, is `92_changelog.md` updated?
* If a TODO was resolved or deferred, is `91_todo.md` updated?
