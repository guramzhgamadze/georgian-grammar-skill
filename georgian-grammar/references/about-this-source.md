# About This Source

## What this skill is built from

This skill's framework is adapted from:

> *Georgian Grammar for Artificial Intelligence — Stage 1* (version 0.1.0),
> Business and Technology University (BTU), Tbilisi, Georgia, 2026.
> Licensed under CC BY 4.0.
> https://github.com/BTU-Business-and-Technology-University/georgian-grammar-for-ai

© 2026 Business and Technology University (BTU), Tbilisi, Georgia.
Licensed under the Creative Commons Attribution 4.0 International Licence
(CC BY 4.0): <https://creativecommons.org/licenses/by/4.0/>. The full
licence text is bundled at `LICENSE`.

**Changes were made.** This skill is an adaptation, not a copy: the
book's Georgian-language YAML specification has been selected,
condensed, reorganised and translated into English prose for use as an
agent skill, and examples that conflict with standard Georgian grammar
have been corrected (listed below, with the literature behind each
correction). The original publication is unmodified at
`references/source-book.pdf`; `references/source-book-fulltext.txt` is a
plain-text extraction of that same PDF, and
`references/source-book-index.md` maps its sections to PDF pages and text
lines. Consult either for anything this skill's distilled reference files
don't cover — keeping in mind that the book's own examples still contain
the errors corrected here.

The publication is a 338-page pilot research book, written in Georgian,
proposing a machine-readable framework for Georgian grammar: semantic-role
annotation, verb decomposition, sentence-level structure, idiom handling,
an AI error taxonomy, and a validation/benchmark architecture. It draws on
research across up to roughly 5 billion tokens of Georgian-language
material officially supplied by BTU and Palitra Media, though
annotation depth varies — broad patterns were surveyed across the full
corpus, while deep grammatical analysis was done on a targeted set of
examples.

**Third-party material note**: the license covers the publication itself
(its text, structure, schemas, and examples) — not the underlying
Georgian-language corpus BTU drew on, which isn't included here and isn't
covered by this license.

**Version and corrections.** This skill tracks version **0.1.0** (released
2026-08-09). BTU's stated policy is that published versions are never
silently replaced — corrections are issued as a new version with a new tag
and recorded in the repository's `CHANGELOG.md` and `ERRATA.md`. As of
2026-11-02 the repository still listed only version 0.1.0 and no
corrections, so the corrections below are not (yet) part of BTU's own
errata. If the framework here matters to a decision, check `ERRATA.md` in
the repository for anything published since.

## Corrections made in this skill (relative to the source)

Each correction below was checked against peer-reviewed linguistics, the
Georgian Academy's explanatory dictionary, or both (full references in the
next section). The source's pilot framework — roles, causation subtypes,
error taxonomy — is otherwise kept as is.

| # | The source book says | Corrected to | Evidence |
|---|---|---|---|
| 1 | `მოგატანინებდი`: agent = I, executor = unspecified, **recipient = you** — "I would have someone bring something to you" (record VERB-0001; reused in several error examples) | `გ-` marks the **executor** (the person made to act): "I would have you bring it". In a causative built on a transitive verb the causee is the indirect object, cross-referenced by the object prefix; a recipient would be demoted to a `-თვის` phrase. The book itself reads the same prefix slot as the executor in `გაგვაკეთებინეს` (VERB-0002) | Baratashvili 2019 (after Harris 1981:81); Hewitt 2008 (agreement sets) |
| 2 | Case-to-role guidance shows only the aorist pattern (ergative agent, nominative object, dative recipient) and treats `-თვის` as beneficiary | Case depends on the tense series: series I nominative subject + dative object; series II ergative subject + nominative object; series III dative subject + nominative object + `-თვის` indirect object; medial verbs take an ergative subject in series II; "feeling" verbs take a dative experiencer in all series. A `-თვის` phrase can be a recipient | Anderson 1984, Aronson 1991, Harris 1981, Hewitt 1995 (as tabulated by the Surrey Morphology Group); Baratashvili 2019; Hewitt 2008; Explanatory Dictionary, s.v. `თვის` |
| 3 | `დედასთვის საჩუქარი იყიდა` | `დედისთვის` — the postposition `-თვის` requires the genitive | Explanatory Dictionary, s.v. `თვის` ("მოითხოვს ნათესაობით ბრუნვას"); `დედისთვის` in Baratashvili 2019 and Anderson 1984 |
| 4 | Direction-loss example: `შემოვიდა` "correctly" paraphrased as `გარედან შიგნით შევიდა` | `შემოვიდა` = came in, toward the speaker; `შევიდა` = went in — the paraphrase itself loses the direction | Makharoblidze 2018; Explanatory Dictionary, s.v. `შემოდის`, `შედის` |
| 5 | `უნდა გააკეთოს` labelled mood: indicative (while `შეიძლება მოვიდეს`, the same II-subjunctive form type, is labelled subjunctive) | `გააკეთოს` is a II subjunctive (optative) form — a subjunctive-mood screeve; `უნდა` combines with the present subjunctive, the II subjunctive and the pluperfect | Sharashenidze 2018 (after Shanidze 1980) |
| 6 | Preverb `გა-` in `გაკეთება` / `გაგვაკეთებინეს` labelled a "lexical change" | `გა-` here only forms the perfective / future–aorist (completion), as `და-` does in `დაწერა` | Makharoblidze 2018; Explanatory Dictionary, s.v. `აკეთებს` (aorist `გააკეთა`) |
| 7 | (Adaptation's own gloss) `წყვეტა` = "to cut" | `წყვეტს` is the shared present of `გაწყვეტს` "break", `გადაწყვეტს` "decide", `შეწყვეტს` "stop", `მოწყვეტს` "pluck" | Explanatory Dictionary, s.v. `წყვეტს`, `წყვეტა` |
| 8 | Fronting a word = focusing it; `წერილი ბავშვმა დაწერა` read as possible object focus; marked-order example translated with a focus cleft | Narrow focus is preferably (not obligatorily) immediately preverbal, with a topic position before it, and prosody outweighs order — so the fronted object is most likely the topic and `ბავშვმა` sits in the focus slot | Skopeteas, Féry & Asatiani 2009 |
| 9 | Several "correct outputs" add or alter content: dropped subjects/objects rendered as "someone/something" (`ვიღაცამ ჩვენ რაღაც შემოგვთავაზა`); `ალბათ მოვა` "corrected" with an added "but this isn't confirmed"; stilted paraphrases such as `ბავშვს გააკეთებინა, რომ წერილი დაეწერა` | Dropped arguments rendered with the pronoun the person marking points to ("(s)he offered it to us"); hedges kept without adding certainty or doubt; causative readings given in English where the natural Georgian *is* the causative form | Person markers: Hewitt 2008; the source's own overexpansion rule |
| 10 | No coverage of reported-speech particles or of the evidential perfect | Added: `-მეთქი` / `-ო` / `-თქო`; the perfect's not-witnessed sense and `თურმე` | Rostovtsev-Popiel 2017; Zekalashvili 2022; Boeder 2000; Topadze 2007; Harris 1981:125 |

## References used for the corrections

- Anderson, Stephen R. 1984. On representations in morphology: case
  marking, agreement and inversion in Georgian. *Natural Language and
  Linguistic Theory* 2: 157–218.
- Aronson, Howard I. 1991. Modern Georgian. In *The Indigenous Languages
  of the Caucasus*, vol. 1: *The Kartvelian Languages*, 219–312. Delmar:
  Caravan Books.
- Baratashvili, Zurab. 2019. The types of the causative construction in
  Georgian. *Bulletin of the Georgian National Academy of Sciences* 13(1).
  (Ivane Javakhishvili Tbilisi State University.)
- Boeder, Winfried. 2000. Evidentiality in Georgian. In L. Johanson & B.
  Utas (eds.), *Evidentials: Turkic, Iranian and Neighbouring Languages*,
  275–328. Berlin: Mouton de Gruyter.
- Harris, Alice C. 1981. *Georgian Syntax: A Study in Relational Grammar*.
  Cambridge: Cambridge University Press.
- Hewitt, B. George. 1995. *Georgian: A Structural Reference Grammar*.
  Amsterdam: John Benjamins.
- Hewitt, George. 2008. Are verbs always what they seem to be? *Iran and
  the Caucasus* 12: 307–323.
- Makharoblidze, Tamar. 2018. On Georgian preverbs. *Open Linguistics*
  4(1): 163–183. doi:10.1515/opli-2018-0009.
- Rostovtsev-Popiel, Alexander. 2017. Hörensagenmarker, Deiktika und
  Zitierung des Niegesagten im Georgischen. *Georgica* 38: 27–40.
- Sharashenidze, Nino. 2018. Teaching Georgian as a second language:
  modality and tense (modal *unda*). *International Journal of
  Multilingual Education* 12: 28–36.
- Skopeteas, Stavros, Caroline Féry & Rusudan Asatiani. 2009. Word order
  and intonation in Georgian. *Lingua* 119.
- Surrey Morphology Group. Deponency database: Georgian (Kartvelian).
  University of Surrey. (Tabulates Anderson 1984, Aronson 1991, Harris
  1981, Hewitt 1995.)
- Topadze, Manana. 2007. Some remarks on lexical aspects of evidentiality
  in Georgian. Conference abstract, Max Planck Institute for Evolutionary
  Anthropology, Leipzig.
- Zekalashvili, Rusudan. 2022. სხვათა სიტყვა: კლასიფიკაცია და გადმოცემის
  საშუალებები ქართულში [Reported speech: classification and means of
  expression in Georgian]. *ქართველური ენათმეცნიერება* (Kartvelian
  Linguistics) VIII: 20–36. Tbilisi State University.
- ქართული ენის განმარტებითი ლექსიკონი [Explanatory Dictionary of the
  Georgian Language], ed. Arnold Chikobava; online edition by the Arnold
  Chikobava Institute of Linguistics and the Language Modelling
  Association (ena.ge). Entries consulted: `თვის`, `წყვეტს`, `წყვეტა`,
  `აკეთებს`, `შემოდის`, `შედის`, `გაიტეხს`, `მოითქვამს`, `აქცევს`,
  `სიტყვა`, `სტკივა`.

## Status: pilot, not peer-reviewed

The source explicitly labels itself a first-stage pilot, not a finished
or externally peer-reviewed grammar. It marks each rule and example with
an evidence status, and it's worth carrying that same distinction forward
rather than treating everything in this skill as equally certain:

- **established_grammar** — standard, well-documented Georgian
  linguistics (the case system, the existence of polypersonal verb
  agreement, the არ/ვერ negation distinction, and so on). Solid in
  general — but the source's own worked examples in this area were not
  error-free, which is why the corrections above exist.
- **pilot_result** — the project's own working analysis: the specific
  11-role codebook, the causation-subtype inventory, the named error
  taxonomy. Genuinely useful as an analytical lens, and most examples in
  this skill are drawn from the source's own worked cases — but treat the
  framework as a considered pilot proposal, not a completed academic
  consensus.
- **technical_standard** — conventions the project adopted for its own
  data format (record structure, coding schemes) rather than claims about
  Georgian itself.

## Known scope limits (stated by the source itself)

- Primarily covers standard **written** Georgian. Spoken/dialogue Georgian
  — with its heavier ellipsis, short answers, intonation-marked focus,
  and stronger context-dependence — is explicitly flagged as needing
  separate future work.
- Doesn't yet systematically cover regional dialects or historical forms
  of the language.
- Genre coverage so far is uneven; the source notes that word order,
  focus, idiom use, and typical AI errors can all shift across genres
  (official/legal/medical/academic/media/literary/social-media/spoken),
  and that findings from one genre shouldn't be assumed to hold for all
  of them.
- The role system, causation-subtype list, and error taxonomy are
  explicitly described as a starting point the source's own authors
  expect to extend (e.g. possessor, goal, result, and companion roles are
  named as likely future additions, not yet part of the current
  codebook).
- Not covered by the source or this skill: full verb paradigms (forming
  every screeve), spelling, punctuation, and style. This skill helps
  check *meaning*; it is not a grammar of forms.

None of this makes the framework unreliable for its actual scope —
standard written Georgian is exactly where it's strongest — but it's
worth not over-extending it to dialect, historical, or highly informal
spoken material without extra caution.
