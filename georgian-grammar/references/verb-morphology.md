# Georgian Verb Morphology

Georgian is a polypersonal, highly synthetic language: a single finite
verb form can agree with and encode multiple participants at once (who
causes, who performs, who it's directed at), plus direction, tense, mood,
and aspect — all without a single extra word. Treat every non-trivial verb
form as a small structure to decompose, not a single lexical unit to
look up.

## Person markers — read these first

Decomposition starts with the person markers, because they say which
participants the form encodes (Hewitt 2008; Anderson 1984, as tabulated by
the Surrey Morphology Group):

| | singular | plural |
|---|---|---|
| subject markers | 1 `ვ-` · 2 none (`ხ-` in a few verbs, e.g. `ხარ` "you are") · 3 `-ს` / `-ა` / `-ო` (depending on the tense) | 1 `ვ-…-თ` · 2 `…-თ` · 3 `-ენ` / `-ან` / `-ნ` / `-ეს` / `-ნენ` (depending on the tense) |
| object markers | 1 `მ-` · 2 `გ-` · 3 none, or `ს-` / `ჰ-` (`უ-` with some verbs) for an indirect object | 1 `გვ-` · 2 `გ-…-თ` · 3 as singular |

Only one object person is ever marked on the verb. Three rules decide what
the object prefixes mean:

- In ordinary forms of the present/future and aorist series, `მ-` / `გ-`
  / `გვ-` mark an object: `მომიტანა` "(s)he brought it to me".
- In a causative built on a transitive verb, the object prefix marks the
  **person made to act** (the causee), not a recipient: `გაგვაკეთებინეს`
  "they had *us* do it", `მოგატანინებდი` "I would have *you* bring it"
  (Baratashvili 2019, following Harris 1981:81).
- In the perfect series of transitive verbs, and in every form of
  "feeling" verbs (`მიყვარს` "I love", `მინდა` "I want", `გაახსენდა`
  "(s)he remembered"), the same prefixes mark the **subject or
  experiencer** — the so-called inversion: `დამიხატავს` "I have painted
  it".

## What to extract from a verb form

For any verb form, work out:

1. **Verb form vs. verb core vs. lemma** — keep the exact surface form
   (never silently replace it), then identify the underlying action/state
   (verb core) and its dictionary/citation form (lemma). These are often
   different from what the surface form looks like at a glance:
   - `მოგატანინებდი` → core: "bringing" (მოტანა), lemma: მოტანა
   - `გაგვაკეთებინეს` → core: "doing" (გაკეთება), lemma: გაკეთება
   - `გადაგვაწყვეტინა` ("(s)he made us decide") → core: "making a
     decision," lemma: გადაწყვეტა — the preverb is what selects the
     meaning: `წყვეტს` is the shared present tense of several distinct
     verbs — `გაწყვეტს` "break, tear", `გადაწყვეტს` "decide", `შეწყვეტს`
     "stop, interrupt", `მოწყვეტს` "pluck, tear off" (Explanatory
     Dictionary of the Georgian Language) — so don't gloss the bare stem
     as one fixed verb

2. **Participants** — agent, recipient, and object are the default roles
   to check for every verb; executor is required whenever causation is
   present; implicit object is required whenever the verb semantically
   needs an object that isn't stated. Experiencer, source, beneficiary,
   instrument, location, and direction apply when relevant. Full
   definitions in `references/semantic-roles.md`.

3. **Causation** — is one participant making, asking, ordering, allowing,
   or arranging for another to act? If so, mark it present and keep both
   the causer and the direct performer distinct (never collapse them, and
   never simplify the form down to a plain action).
   - **Who is who:** the causer is the subject. In a causative built on a
     transitive verb, the person made to act is the indirect object — a
     dative noun, cross-referenced by the verb's object prefix:
     `მასწავლებელმა ბავშვს წერილი დააწერინა` "the teacher had the child
     write the letter". If the base verb already has a recipient, the
     recipient is pushed out into a `-თვის` phrase: `მამამ მიაცემინა
     (მას) დედისთვის ტორტი` "Father made him give the cake to mother"
     (Baratashvili 2019; Harris 1981:81). So in a causative, a `გ-` or
     `მ-` prefix is the performer, never the recipient.
   - **Subtype** — often can't be pinned down without context; don't
     force one:
     - `none` — no causation
     - `cause_to_act` — made someone do it
     - `request_to_act` — asked someone to do it
     - `order_to_act` — ordered someone to do it
     - `enable_to_act` — allowed/enabled someone to do it
     - `arrange_to_act` — arranged for someone to do it
     - `unspecified_causative` — causation is clearly present but the
       exact flavor above isn't determinable from the form alone (this is
       the default for a bare form like `გაგვაკეთებინეს` without context —
       don't upgrade it to "forced" or "ordered" without evidence, and
       don't downgrade it by dropping causation entirely)

4. **Preverb** — Georgian verbs commonly take a prefix that can mark
   direction, mark the action as completed, shift the verb's core meaning
   (sometimes idiomatically), or some combination:
   - `შემოვიდა` → `შემო-` marks direction (from outside in, toward the
     speaker)
   - `დაწერა` → `და-` marks completion, not a directional or lexical
     shift; `გააკეთა` → `გა-` likewise only marks completion (the
     dictionary gives `გააკეთა` simply as the aorist of `აკეთებს`). In the
     present/future series a preverb turns a present into a future
     (`აკეთებს` → `გააკეთებს`); in the other series it carries aspect
     (Makharoblidze 2018)
   - `გადაწყვიტა` → `გადა-` here selects a lexical meaning — "decide" —
     rather than "across"; treat the combination as its own lexical item
   - Directional preverbs (Makharoblidze 2018): `მი-` away from the
     speaker, `მო-` toward the speaker (or the hearer); `ა-`/`ამო-` up,
     `ჩა-`/`ჩამო-` down, `შე-`/`შემო-` from outside in, `გა-`/`გამო-` from
     inside out, `წა-`/`წამო-` away from something, `გადა-`/`გადმო-`
     across. The compound forms with `-მო-` add orientation toward the
     speaker: `შევიდა` "went in" vs. `შემოვიდა` "came in".
   - A preverb's function should be confirmed per verb rather than
     assumed, since the same preverb can do different jobs on different
     verbs (`გა-` is directional in `გავიდა` "went out" but only marks
     completion in `გააკეთა`)
   - Losing the preverb's contribution is a frequent, specific error —
     e.g. reading `გადაწყვიტა` as generic "moved" instead of "decided"

5. **Direction** — when direction is carried by the preverb or verb form
   rather than a separate word, state both the value and that it's
   preverb-encoded:
   - `შემოვიდა` — direction: outside → inside, toward the speaker
   - `მომიტანა` — direction: toward the speaker

6. **Tense — grammatical vs. contextual.** The verb's grammatical tense
   and the time the sentence actually refers to are not always the same,
   and conflating them is a documented error:
   - `ხვალ მივდივარ` — "tomorrow I'm going" — grammatically **present**
     tense, but contextually **future** (the adverb "tomorrow" overrides
     the surface tense — this is ordinary and shouldn't be read as "going
     right now")
   - `ანგარიში მოამზადა` — "prepared the report" — grammatical and
     contextual tense agree: past

7. **Mood and modality.** Mood is the basic stance the action is
   presented in: `indicative`, `conditional`, `imperative`, `subjunctive`,
   `optative` — or `ambiguous`/`unknown` when the form genuinely doesn't
   settle it. In Georgian grammar the subjunctive-mood screeves are the
   present subjunctive, the future subjunctive, the II subjunctive (also
   called the optative) and the III subjunctive (Shanidze's
   classification, as summarized by Sharashenidze 2018). Modality layers
   finer shades on top and can co-occur with any mood: `possibility`,
   `probability`, `necessity`, `obligation`, `recommendation`, `desire`,
   `request`, `command`, `hypothetical`, `uncertainty`.
   - `მოგატანინებდი` — mood: conditional, modality: hypothetical
   - `შეიძლება მოვიდეს` — "might come" — `მოვიდეს` is a II subjunctive
     (optative) form; mood: subjunctive, modality: possibility
   - `უნდა გააკეთოს` — "must/should do it" — `გააკეთოს` is likewise a II
     subjunctive (optative) form; mood: subjunctive, modality: necessity /
     obligation. `უნდა` combines with three screeves: the present
     subjunctive (`უნდა ვაკეთებდე`), the II subjunctive (`უნდა გავაკეთო`)
     and the pluperfect (`უნდა გამეკეთებინა`, roughly "I should / must
     have done it") (Sharashenidze 2018). The source book labels `უნდა
     გააკეთოს` as indicative; that label is corrected here.
   - Losing conditional/hypothetical marking and presenting the action as
     settled fact is a high-severity, frequent error, as is turning a
     recommendation (`ჯობს...` — "it would be better to...") into a stated
     obligation

8. **Aspect.** `ongoing`, `completed`, `habitual`, `repeated`,
   `inceptive`, `resultative`:
   - `ანგარიშს ამზადებდა` — "was preparing the report" — ongoing
   - `ანგარიში მოამზადა` — "prepared the report" — completed

9. **Negation (polarity).** Georgian distinguishes at least two negators
   that are not interchangeable:
   - `არ` — plain negation ("did not / will not / is not")
   - `ვერ` — negation of ability ("could not / can't manage to")
   - `მოვიდა` — "came" (positive) → `არ მოვიდა` — "did not come" (plain
     negation) vs. `ვერ გააკეთა` — "was unable to do [it]" (inability, not
     plain non-occurrence) — treating these as the same negator drops real
     meaning (whether the failure was about ability/circumstance, not just
     that something didn't happen)
   - There is also a prohibitive form used with commands (`ნუ` + verb,
     "don't...!") — a separate function from both of the above

10. **Evidential perfect.** The perfect series (traditionally the I and
    II `თურმეობითი`, named after `თურმე` "apparently") often presents an
    event as not witnessed — inferred or reported — rather than simply
    past. Georgian has no separate evidential affix; this meaning is
    carried mainly by the perfect (Boeder 2000; Topadze 2007), and the
    particle `თურმე` ("apparently" — inference or hearsay) reinforces it:
    - `გელას თურმე დაურწმუნებია თავისი თავი` — "Apparently Gela has
      convinced himself" (Harris 1981:125)
    - Translating such a perfect as a plain witnessed past drops the
      speaker's distance from the claim — but don't add "apparently"
      mechanically where context shows the perfect is simply resultative
    - In the perfect series of a transitive verb the agent is in the
      dative and a recipient takes `-თვის` — see the case table in
      `references/sentence-structure.md`

11. **Contextual recovery.** State explicitly which participant or detail
    (agent, executor, recipient, object identity, cause, purpose,
    direction, or the condition an event depends on) isn't present in the
    form itself and must come from context — and don't add a specific
    value unless context actually supports one.

12. **Translation decompression.** When rendering a compressed Georgian
    verb into another language (or into a fuller Georgian paraphrase),
    keep every dimension above that the form or context actually
    supports: participants, causation, tense, mood, direction, and any
    residual uncertainty. Two matched failure modes to avoid:
    - **Underexpansion** — collapsing a rich form into something thinner
      than it is: `მოგატანინებდი` → "I would bring" loses the causation
      and the executor entirely.
    - **Overexpansion** — adding specifics the form doesn't support:
      `გაგვაკეთებინეს` → "The manager forced us to prepare the report"
      invents a manager, a forcing reading, and a report that aren't in
      the source. The accurate rendering keeps the vagueness: "They had us
      do it."
    - A dropped argument is rendered with the pronoun the person markers
      point to ("he/she/it/they"), not "someone/something".

## Worked example — `მოგატანინებდი`

One word, roughly *"I would have you bring it."*
- verb core / lemma: მოტანა ("to bring")
- preverb: `მო-`, direction toward the speaker ("bring", not "take")
- agent (causer): "I" (verb-encoded, certain)
- executor (the person made to act): "you" — the `გ-` prefix
  (verb-encoded, certain); in a causative built on a transitive verb the
  object prefix marks the performer, not a recipient
- object: unnamed ("it"; identity from context)
- recipient: not encoded in this form; if one mattered it would be added
  separately, e.g. as a `-თვის` phrase
- causation: present, subtype unspecified without more context — "have
  you bring" is the neutral rendering; "make you bring" claims more
  pressure than the bare form shows
- mood: conditional; modality: hypothetical
- tense: context-dependent, but the modal sense is hypothetical
- what's genuinely uncertain without more context: what the object is,
  the precise causation subtype, and the condition the event depends on
- documented failure modes for this exact form: losing the executor and
  the causation ("I would bring it"), misreading `გ-` as a recipient ("I
  would have someone bring it to you" — the reading given in the source
  book), inventing a specific object, losing the conditional mood, and
  losing the directional sense

## Worked example — `გაგვაკეთებინეს`

One word: *"They had us do it."*
- verb core / lemma: გაკეთება ("to do/make")
- preverb: `გა-`, marking completion (aorist), as in `გააკეთა`; not a
  directional or lexical shift
- agent: "they" (verb-encoded, high confidence)
- executor: "we" — the `გვ-` prefix (verb-encoded, certain)
- object: unnamed ("it"; medium confidence about its identity — nothing in
  the form names one)
- causation: present, subtype unspecified
- tense: past (grammatical and contextual agree); mood: indicative
- documented failure modes for this exact form: reading it as plain "we
  did it" (losing both causation and the executor), or overexpanding the
  causation into something forceful ("they forced us to...") that the
  bare form doesn't support
