# Georgian Grammar — a Claude skill

[ქართული ვერსია](README_ka.md)

An agent skill that helps Claude analyze, translate and check Georgian
(ქართული) text for meaning errors: who does what to whom, how case marking
shifts with the tense series, verb decomposition (person markers,
causatives, preverbs, tense/mood/aspect, negation), word order and focus,
pro-drop, reported speech and idioms — plus a catalog of the mistakes AI
systems typically make on Georgian, with corrected readings.

> **Based on BTU's work.** The analytical framework, the semantic-role
> codebook, the AI error taxonomy and most examples come from *Georgian
> Grammar for Artificial Intelligence — Stage 1* (version 0.1.0) by
> Business and Technology University (BTU), Tbilisi, 2026, licensed under
> CC BY 4.0. This repository is an independent adaptation with
> corrections; it is not affiliated with or endorsed by BTU. See
> [Attribution and license](#attribution-and-license).

## What's inside

| Path | Contents |
|---|---|
| `georgian-grammar/SKILL.md` | Entry point: core mental model, quick reference, pre-finalization checklist |
| `georgian-grammar/references/semantic-roles.md` | The 11-role codebook |
| `georgian-grammar/references/verb-morphology.md` | Person markers, causatives, preverbs, tense/mood/aspect, negation, evidential perfect |
| `georgian-grammar/references/sentence-structure.md` | Case patterns by tense series, word order and focus, particles, reported speech, pro-drop |
| `georgian-grammar/references/idioms-and-register.md` | Idioms and value-laden phrases |
| `georgian-grammar/references/common-ai-errors.md` | The 33 error types of the source taxonomy plus three added checks |
| `georgian-grammar/references/about-this-source.md` | Provenance, pilot status, every correction with its evidence, references |
| `georgian-grammar/references/source-book-index.md` | Section → PDF page → text-line map of the original book |
| `georgian-grammar/references/source-book.pdf`, `source-book-fulltext.txt` | BTU's original publication (unmodified) and its text extraction |

The packaged skill (`georgian-grammar.skill`) is attached to each
[release](../../releases).

## Install

- **Claude apps (claude.ai, desktop):** download `georgian-grammar.skill`
  from the latest release and upload it in Claude's skills settings. If an
  older skill with the same name is installed, replace it.
- **Claude Code:** copy the `georgian-grammar/` folder into
  `~/.claude/skills/` (personal) or into `.claude/skills/` inside a project.

## What this adaptation changed

The book's Georgian-language YAML specification was condensed and
translated into English skill files, and examples that conflict with
standard Georgian grammar were corrected. Each correction cites
peer-reviewed literature, the Georgian Academy's explanatory dictionary,
or both (details in
[`about-this-source.md`](georgian-grammar/references/about-this-source.md)):

1. `მოგატანინებდი`: the prefix `გ-` marks the executor — "I would have you
   bring it" — not a recipient.
2. Case marking by tense series (nominative / ergative / dative subjects;
   `-თვის` indirect objects in the perfect series) was added.
3. `დედასთვის` → `დედისთვის` (`-თვის` takes the genitive).
4. The direction-loss example: `შემოვიდა` "came in" is not `შევიდა` "went
   in".
5. `უნდა გააკეთოს` is subjunctive (II subjunctive), not indicative.
6. `გა-` in `გაკეთება` marks completion, not a lexical change.
7. The gloss of `წყვეტა` was corrected.
8. Word order and focus follow the experimental findings (narrow focus is
   preferably immediately preverbal).
9. Dropped arguments are rendered as "he/she/it", not "someone/something",
   and model answers no longer add content.
10. Reported-speech particles, the evidential perfect and a section index
    for the book were added.

## Attribution and license

**Original work** (attribution in the form BTU requests):

> *Georgian Grammar for Artificial Intelligence — Stage 1* (version 0.1.0),
> Business and Technology University (BTU), Tbilisi, Georgia, 2026.
> Licensed under CC BY 4.0.
> <https://github.com/BTU-Business-and-Technology-University/georgian-grammar-for-ai>

- **Changes were made** — see the list above, [NOTICE.md](NOTICE.md) and
  [`about-this-source.md`](georgian-grammar/references/about-this-source.md).
  The original publication is included unmodified.
- **License:** this adaptation is distributed under the same license,
  [CC BY 4.0](LICENSE). If you reuse it, credit both BTU's original work (in
  the form above) and this adaptation (suggested wording in
  [NOTICE.md](NOTICE.md)).
- **No endorsement:** this project is not affiliated with, reviewed by or
  endorsed by BTU; the corrections are this adaptation's own. As of
  2026-11-02 BTU's `ERRATA.md` listed no corrections to version 0.1.0.
- **Third-party material:** the corpus BTU's research used is not included,
  and neither is BTU's separately licensed *Georgian Language AI Modeling
  Dataset* (CC BY-NC 4.0).
- **Other sources:** the corrections draw on Anderson (1984), Aronson
  (1991), Baratashvili (2019), Boeder (2000), Harris (1981), Hewitt (1995,
  2008), Makharoblidze (2018), Rostovtsev-Popiel (2017), Sharashenidze
  (2018), Skopeteas, Féry & Asatiani (2009), Topadze (2007), Zekalashvili
  (2022) and the Explanatory Dictionary of the Georgian Language; full
  references are in
  [`about-this-source.md`](georgian-grammar/references/about-this-source.md).

## Status

The underlying framework is BTU's first-stage pilot and has not been
externally peer reviewed. The corrections here were checked against the
literature listed above, but this skill is a working tool for checking
meaning, not an authoritative grammar of Georgian.

Adaptation: Guram Zhgamadze, 2026.
