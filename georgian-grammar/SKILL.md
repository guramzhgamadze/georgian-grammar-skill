---
name: georgian-grammar
description: A semantic and grammatical analysis framework for Georgian (ქართული) — who-does-what-to-whom role assignment, how case marking shifts with the tense series (nominative, ergative or dative subjects; -თვის objects), verb decomposition (person markers, causatives, preverbs, tense/mood/aspect, არ/ვერ/ნუ negation), word order and focus, pro-drop recovery, reported-speech particles, idioms, and a catalog of the specific mistakes AI systems make on Georgian with corrected readings. Use this whenever translating to or from Georgian, explaining or analyzing a Georgian verb form or sentence, or checking Georgian text — your own or someone else's — for dropped, swapped, or invented meaning. It is not a spelling, punctuation, or style guide.
license: CC-BY-4.0
---

# Georgian Grammar for AI

A working framework for parsing and producing Georgian accurately: who is
doing what to whom, what a single verb form is quietly encoding, what case
and word order are and aren't signaling, and where AI systems on this
language characteristically go wrong.

The framework is adapted from *Georgian Grammar for Artificial
Intelligence — Stage 1* (BTU, v0.1.0, 2026), a pilot research publication
— see `references/about-this-source.md` for scope, status, and attribution
before treating anything here as final or authoritative. The specific
role/error taxonomy is the source's own pilot analytical framework, useful
as a lens rather than settled fact. Where the source's examples conflict
with standard Georgian grammar, this skill corrects them; every correction
and the literature behind it is listed in `references/about-this-source.md`.

## When to use this skill

- Translating into or out of Georgian
- Checking Georgian you write, or someone else's Georgian, for meaning
  errors (roles, causatives, negation, hedges, reported speech)
- Explaining how a Georgian sentence or verb form is built
- Checking a translation or generated sentence for dropped, merged, or
  invented meaning
- Any task that requires knowing who the agent, recipient, or object of a
  Georgian sentence actually is
- Interpreting a Georgian idiom or emotionally/socially loaded phrase

## Core mental model

Four things cause most of the damage, in both directions (Georgian → other
language, and other language → Georgian):

**1. A single Georgian verb form can compress a whole scenario.**
`მოგატანინებდი` is one word. It packs: me as the causer, *you* as the
person I would make act (the executor, marked by the `გ-` prefix), an
unnamed object ("it"), the hither direction of `მო-` (bring, not take),
and a conditional/hypothetical mood — roughly *"I would have you bring
it."* In a causative built on a transitive verb, the object prefix (`მ-`
me, `გ-` you, `გვ-` us) marks the person who is *made to act*, not a
recipient; a recipient, if one is mentioned, goes into a `-თვის` phrase.
(The source book reads `გ-` here as a recipient — "I would have someone
bring something to you"; that reading is corrected in this skill.) Never
treat a Georgian verb as just "an action word." Before translating or
analyzing one, decompose it — see `references/verb-morphology.md`.

**2. Grammatical case does not fix a semantic role — and the same role
changes case with the tense series.**
The dative alone does not tell you whether a noun is a recipient, an
experiencer, a beneficiary, a direct object, or even the agent — the verb
and its tense series decide:
- `დედას წერილი მისწერა` — wrote a letter *to* mother → dative = **recipient**
- `დედას გაახსენდა ბავშვობა` — mother *remembered* her childhood → dative = **experiencer** (mother isn't being addressed — she's the one having the mental experience; the sentence has no agent at all)
- `დედისთვის საჩუქარი იყიდა` — bought a gift *for* mother → `-თვის` phrase = **beneficiary**
- `ბავშვი წერილს წერს` — the child is writing a letter → dative = **direct object** (present/future series)
- `ბავშვს წერილი დაუწერია` — the child has written a letter (often: *apparently* has) → dative = **agent** (perfect series)

Transitive subjects are nominative in the present/future series, ergative
in the aorist series, and dative in the perfect series, where a recipient
moves into a `-თვის` phrase — see the table in
`references/sentence-structure.md`. Assigning "recipient" to every dative
noun is one of the single most common AI errors on Georgian; reading every
`-თვის` phrase as a beneficiary is its mirror image. See
`references/semantic-roles.md` for the full 11-role codebook.

**3. Word order marks information structure, not grammatical role.**
Every order of the main constituents is grammatical; changing it changes
what is topic or focus, never who did what. `ბავშვმა დედას წერილი
მისწერა` (neutral) and `დედას ბავშვმა წერილი მისწერა` assign identical
roles — the child still wrote, the mother is still the recipient.
Experimental work finds narrow focus *preferably* (not obligatorily) right
before the verb, with a topic position in front of it, and intonation
carries more of the load than order — so a fronted word is more often the
topic than the focus, and a focus reading taken from word order alone
stays tentative in writing. Never assign "agent" to whatever comes first.
See `references/sentence-structure.md`.

**4. What's missing is data, not noise — recover it, don't invent it.**
Georgian regularly omits arguments that verb agreement or prior context
already carries — but check which is which. In `მოგიტანე` ("I brought
[it] to you") the agent *and* the recipient are both verb-encoded (`-გ-`
carries "to you"), and only the object is left implicit. In `მოვიტანე`
("I brought [it]") only the agent is verb-encoded; the recipient and the
object are both simply unexpressed and have to come from context, if at
all. Mark what's genuinely unspecified as unspecified. Recover only what
prior context actually supports. Never fabricate a specific person,
object, or cause to fill a gap — this is one of the highest-severity
error patterns in the source taxonomy. When translating, render a dropped
argument with the pronoun the verb's person marking points to —
`შემოგვთავაზა` is "(s)he offered it to us", not "someone offered us
something" — and take its identity from context. Preserve real ambiguity
(e.g. "she took a book and a letter, then sent [it/them] to a friend" —
which item(s)? — don't silently pick one).

## Quick reference

**Semantic roles** (full definitions and examples in
`references/semantic-roles.md`): agent (causer), executor (direct
performer, only in causatives), recipient, object, implicit object,
experiencer, source, beneficiary, instrument, location, direction.

**Verb dimensions to check** (full detail in
`references/verb-morphology.md`): verb core / lemma; person markers (whom
each prefix and ending points to); causation (present? which of six
subtypes? who is the causer and who the executor?); preverb (direction /
completion / lexical shift); grammatical tense vs. the tense the sentence
actually means (`ხვალ მივდივარ` — grammatically present, contextually
future); the screeve's series, which decides the case pattern; mood
(indicative / conditional / imperative / subjunctive / optative) and
modality (possibility, necessity, recommendation, hypothetical, etc.) —
`უნდა` or `შეიძლება` + a II subjunctive (optative) form such as
`გააკეთოს`, `მოვიდეს` is subjunctive, not indicative; the "apparently"
(not-witnessed) sense the perfect series often carries; aspect (ongoing /
completed / habitual / repeated / inceptive / resultative); negation — and
critically, **არ** (plain negation, "did not") and **ვერ** (inability,
"couldn't") are not interchangeable, and **ნუ** is the prohibitive
("don't!").

**Sentence dimensions to check** (full detail in
`references/sentence-structure.md`): case matrix *by tense series*
(nominative, ergative, dative, genitive, instrumental, adverbial, vocative,
plus postpositional phrases — `-თვის` takes the genitive: `დედისთვის`),
word order and information structure (topic vs. focus), particles
(`ალბათ` = probability, `მაინც` = concession, `სწორედ` = emphasis —
dropping these turns hedges into flat statements), reported-speech
particles (`-მეთქი` = the speaker's own words, `-ო` = anyone else's words,
`-თქო` = words the listener should pass on — dropping them changes who said
what), zero-expression, context recovery, temporal and causal relations
between clauses.

**Idioms and loaded phrases** (full detail in
`references/idioms-and-register.md`): keep the literal reading and the
real meaning separate; don't flatten the emotional/social/moral weight a
phrase carries (`გული არ გაიტეხო` isn't just "don't stop," it's
encouragement not to lose heart); watch for phrases that are genuinely
ambiguous between literal and figurative depending on context (`გული
სტკივა` — "heart hurts" — is emotional pain in casual talk but may be
literal in a medical context).

## Before finalizing a translation, correction, or explanation

Run this checklist — it's the highest-frequency subset of
`references/common-ai-errors.md`, which has the full catalog with
input/wrong-output/correct-output triples for each:

1. Did I identify the verb's tense series before mapping case to role
   (nominative / ergative / dative subject; a `-თვის` recipient in the
   perfect series)?
2. Did I keep the causer and the person made to act as two distinct
   participants in any causative form — reading a causative's object
   prefix (`მ-`/`გ-`/`გვ-`) as the person made to act, not a recipient?
3. Did I mark unspecified participants as unspecified instead of just
   dropping them, and avoid inventing a specific value for any of them
   (a dropped argument is "he/she/it", not "someone/something")?
4. Did I assign dative-case nouns their role based on the verb and its
   series, not automatically as "recipient"?
5. Did I avoid treating the first word as the agent — or as the focus —
   just because it's first?
6. Did I preserve hedges and modal particles (probably / might / should,
   as recommendation vs. obligation) without flattening them to fact or
   adding certainty, or doubt, the source doesn't express?
7. Did I keep **არ** vs **ვერ** negation distinct (won't/didn't vs.
   couldn't)?
8. Did I preserve the preverb's directional or aspectual meaning rather
   than dropping it (`შემო-` "in, toward the speaker" is not `შე-` "in")?
9. Did I keep reported-speech particles (`-ო`, `-მეთქი`, `-თქო`) and the
   "apparently" sense of the perfect / `თურმე`?
10. If the sentence is genuinely ambiguous, did I say so instead of
    silently picking one reading?
11. For idioms: did I give the real meaning (not a literal reading), while
    checking whether *this* context is one of the cases where the literal
    reading is actually intended?

## Reference files

- `references/semantic-roles.md` — full role codebook: definitions, usage
  conditions, examples, and which roles can/cannot coexist
- `references/verb-morphology.md` — verb decomposition in full: person
  markers, causation subtypes and how the causee is marked, preverb
  semantics, tense/mood/modality/aspect/negation, the evidential perfect,
  two fully worked examples
- `references/sentence-structure.md` — case patterns by tense series,
  word order and focus, particles, reported speech, zero-expression,
  ambiguity, temporal/causal relations between clauses, two fully worked
  examples
- `references/idioms-and-register.md` — framework for idiomatic,
  metaphorical, and value-laden phrases, plus a working list of examples
- `references/common-ai-errors.md` — the full error catalog (all 33 named
  error patterns from the source, under 12 headings, plus three additional
  checks added in this skill) with concrete corrected examples; treat this
  as the lookup table when double-checking output
- `references/about-this-source.md` — what this is built from, its pilot
  status and known scope limits, the corrections this skill makes to the
  source (with the literature behind each), and the required attribution
- `references/source-book-index.md` — map of the original book: every
  part, chapter and specification module with its PDF pages and its line
  range in the text file
- `references/source-book.pdf` and `references/source-book-fulltext.txt`
  — the full original publication (338 pages, Georgian), for anything not
  covered by the distilled files above. Don't load the whole thing into
  context: find the section in `references/source-book-index.md`, then
  read just that line range of the `.txt` file or `grep` it for a term.
  The PDF keeps tables intact if a PDF tool is available (e.g.
  `pdftotext -f 103 -l 105 references/source-book.pdf -`). The book's own
  examples still contain the errors this skill corrects.
