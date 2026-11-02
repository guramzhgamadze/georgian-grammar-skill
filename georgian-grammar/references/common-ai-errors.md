# Common AI Errors on Georgian

A catalog of the specific, recurring ways AI systems mishandle Georgian —
each with the Georgian input, the wrong reading, and the correct one. Use
this as a lookup table: when producing or checking Georgian text (or a
translation of it), scan the relevant group below.

The ✓ lines give the correct *reading*. Where a natural Georgian
paraphrase exists it is shown; where the most natural Georgian is the
original form itself (typical for causatives), the reading is given in
English instead — don't imitate stilted analytic paraphrases in real
translations.

Severity follows the source framework's scale:
- **low** — doesn't significantly change the core meaning, just precision
- **medium** — an important grammatical, stylistic, or contextual layer is lost
- **high** — the meaning changes noticeably, or roles are misassigned
- **very_high** — the output describes a factually different event, adds
  fabricated information, or draws a confident but false conclusion

## Participant-role errors

**Agent loss** (high) — the causer of an action disappears; a causative
gets read as a plain action.
`გაგვაკეთებინეს` → ✗ "ჩვენ გავაკეთეთ" (we did it) → ✓ "მათ ჩვენ
გაგვაკეთებინეს" (they had us do it)

**Executor loss** (very high) — in a causative, the person who actually
performed the action disappears.
`მასწავლებელმა ბავშვს წერილი დააწერინა` → ✗ "მასწავლებელმა წერილი
დაწერა" (the teacher wrote the letter) → ✓ "the teacher had the child
write the letter" — the child wrote it; the teacher caused it

**Agent–executor confusion** (very high) — the causer and the direct
performer get merged into one person.
`სახლი ავაშენებინე` → ✗ "სახლი მე ავაშენე" (I built the house myself) →
✓ "სახლი სხვას ავაშენებინე" (I had someone else build the house)

**Recipient loss** (high) — who the action was directed toward
disappears.
`მოგწერე` → ✗ "დავწერე" (I wrote) → ✓ "მე შენ მოგწერე" (I wrote to you)

**Recipient–executor confusion** (very high) — in a causative, the
addressee and the direct performer get swapped or merged.
`ბავშვს წერილი დააწერინა` → ✗ "ბავშვისთვის წერილი დაწერა" (wrote a
letter for the child) → ✓ "had the child write the letter" — the child is
the writer, not the one it was written for.
`მოგატანინებდი` → ✗ "I would have someone bring it to you" (`გ-` misread
as the recipient — the reading given in the source book) → ✓ "I would
have you bring it" — in a causative, the object prefix marks the person
made to act

**Experiencer–recipient confusion** (high) — a dative-marked person
undergoing a mental/emotional state gets read as someone things are being
sent to.
`მას გაახსენდა ბავშვობა` → ✗ "ვიღაცამ მას ბავშვობა შეახსენა" (someone
reminded him/her of their childhood) → ✓ "მას ბავშვობა გაახსენდა" (he/she
remembered their childhood — no outside agent involved)

## Object errors

**Object loss** (high) — a stated direct object gets dropped.
`ბავშვმა წერილი დაწერა` → ✗ "ბავშვმა დაწერა" (the child wrote) →
✓ "ბავშვმა წერილი დაწერა" (the child wrote a letter)

**Implicit object loss** (medium) — a verb that requires an object, left
unstated in the text, doesn't get marked as having one at all.
`მოგიტანე` → ✗ "მოვედი შენთან" (I came to you) → ✓ "I brought it to
you" — the object is there but unnamed; its identity comes from context

**Fabricated object** (very high) — a specific object gets invented where
none is supported.
`მოგიტანე` → ✗ "წიგნი მოგიტანე" (I brought you a book) → ✓ "I brought it
to you" — don't name the object unless the context does

## Case and word-order errors

**Dative role overgeneralization** (high) — every dative-case noun gets
read as a recipient, regardless of what the verb and its tense series
actually require.
`დედას წერილი მისწერა` → recipient. `დედას გაახსენდა ბავშვობა` →
experiencer. `ბავშვი წერილს წერს` → direct object (present series).
`ბავშვს წერილი დაუწერია` → agent (perfect series). And `დედისთვის
საჩუქარი იყიდა` → a `-თვის` phrase, beneficiary. Same surface pattern,
different roles — check the verb and the series each time.

**Word-order role error** (high) — the first word in the sentence gets
treated as the agent regardless of its actual case and role.
`დედას ბავშვმა წერილი მისწერა` → ✗ "დედამ ბავშვს წერილი მისწერა"
(mother wrote to the child — roles reversed) → ✓ "ბავშვმა დედას წერილი
მისწერა" (the child wrote to mother; mother is just placed first, most
likely as the topic)

## Causation errors

**Causation loss** (very high) — a causative form gets simplified into an
ordinary action, losing the fact that one participant made another act.
`მოგატანინებდი` → ✗ "მოგიტანდი" (I would bring it to you) → ✓ "I would
have you bring it" (causation and executor kept)

**Causation overinterpretation** (high) — general causation gets
sharpened into force/coercion without evidence for that specific flavor.
`გაგვაკეთებინეს` → ✗ "ძალით გვაიძულეს, გაგვეკეთებინა" (they forcibly
compelled us to do it) → ✓ "they had us do it" — whether by force,
request, or arrangement is unknown without context

## Preverb and direction errors

**Preverb loss** (high) — the preverb's directional, aspectual, or
lexical contribution disappears.
`შემოვიდა` → ✗ "მოძრაობდა" (was moving) → ✓ "გარედან შიგნით შემოვიდა"
(came in, from outside to inside). `გადაწყვიტა` → ✗ "გადაადგილდა"
(relocated) → ✓ "გადაწყვეტილება მიიღო" (made a decision)

**Direction loss** (high) — direction gets dropped, or reversed.
`შემოვიდა` (came in) → ✗ "გავიდა" (went out — opposite direction) →
✓ "came in" — from outside to inside, toward the speaker. Rendering it
as `შევიდა` ("went in") would also lose part of the direction: `შემო-`
adds "toward the speaker", `შე-` does not

## Tense and modality errors

**Future–present confusion** (medium) — grammatical present tense used
for near/scheduled future gets read as happening right now.
`ხვალ მივდივარ` → ✗ "ახლა მივდივარ" (I'm going now) → ✓ "ხვალ წავალ ან
ხვალ მივემგზავრები" (I will go/leave tomorrow)

**Event-order error** (high) — which of two events happened first gets
reversed.
`როცა მივედი, შეხვედრა უკვე დაწყებული იყო` → ✗ "ჯერ მივედი და შემდეგ
შეხვედრა დაიწყო" (first I arrived, then the meeting started) →
✓ "შეხვედრა ჩემს მისვლამდე უკვე დაწყებული იყო" (the meeting had already
started before I arrived)

**Conditional loss** (very high) — a conditional/hypothetical action gets
presented as settled fact.
`მოგატანინებდი` → ✗ "მოგატანინე" (I had you bring it — stated as
something that actually happened) → ✓ "I would have you bring it (under
some condition)" — hypothetical, not a past event

**Probability-to-fact error** (very high) — a hedge word gets dropped and
a possibility becomes an assertion.
`ალბათ მოვა` → ✗ "მოვა" ((s)he will come) → ✓ "სავარაუდოდ მოვა"
((s)he will probably come) — keep the hedge, and don't add or remove
certainty

**Recommendation-to-obligation error** (high) — advice gets turned into a
requirement.
`ჯობს, ექიმს მიმართოთ` → ✗ "ვალდებული ხართ, ექიმს მიმართოთ" (you're
obligated to see a doctor) → ✓ "რეკომენდებულია ექიმთან მიმართვა" (seeing
a doctor is recommended)

## Context and coreference errors

**Context loss** (high) — a follow-on sentence's omitted participants
don't get connected back to the preceding sentence that actually supplies
them.
Context: `ნინომ წერილი დაწერა.` Then: `შემდეგ დედას გაუგზავნა.` → ✗ "an
unclear person sends an unclear thing" → ✓ "ნინომ წერილი დედას გაუგზავნა"
(Nino sent the letter to mother)

**Wrong coreference** (high) — an omitted participant gets linked to the
wrong antecedent with unwarranted certainty.
Context: `ნინომ მარიამს წიგნი მისცა.` Then: `შემდეგ წაიკითხა.` → ✗ "წიგნი
მარიამმა აუცილებლად წაიკითხა" (Mariam definitely read the book) →
✓ "მკითხველი კონტექსტის გარეშე ზუსტად ვერ დგინდება" (who read it can't
be pinned down exactly without more context)

**Fabricated context** (very high) — specifics get invented that neither
the sentence nor prior context supports.
`შემოგვთავაზა` → ✗ "დირექტორმა ახალი პროექტი შემოგვთავაზა" (the director
offered us a new project) → ✓ "(s)he offered it to us" — who and what
must come from context; don't invent a director or a project

## Focus error

**Focus loss** (medium) — the core fact survives translation but which
participant was emphasized doesn't.
`სწორედ ბავშვმა დაწერა წერილი` → ✗ "ბავშვმა წერილი დაწერა" (flat: the
child wrote the letter) → ✓ "წერილი კონკრეტულად ბავშვმა დაწერა და არა
სხვამ" (specifically the child wrote the letter, and not someone else)

## Idiom errors

**Idiom read as literal** (very high) — a figurative phrase gets
processed word-for-word.
`სიტყვა გატეხა` → ✗ "სიტყვა ფიზიკურად გატეხა" (physically broke a word)
→ ✓ "პირობა დაარღვია" (broke a promise)

**Literal read as idiom** (high) — a phrase that's meant literally in
context gets over-read as figurative.
Context: a doctor has scheduled a medical exam. `გული სტკივა` →
✗ "ემოციურად განიცდის" (experiencing emotional distress) → ✓ "შესაძლოა
ფიზიკური ტკივილი ჰქონდეს; კონტექსტი სამედიცინოა" (may have physical
pain; the context is medical)

**Emotional-effect loss** (high) — the correct gist survives but the
phrase's supportive/sympathetic/encouraging tone doesn't.
`გული არ გაიტეხო` → ✗ "არ გაჩერდე" (don't stop) → ✓ "არ დანებდე, იმედი
შეინარჩუნე" (don't give up, keep hope)

**Social/moral-effect loss** (high) — the literal event survives but the
interpersonal weight (broken trust, damaged reputation, a boundary) gets
flattened out.
`სიტყვა გატეხა` → ✗ "გადაწყვეტილება შეცვალა" (changed a decision) →
✓ "პირობა დაარღვია და ნდობა დააზიანა" (broke a promise and damaged
trust)

## Translation errors

**Translation underexpansion** (very high) — a compressed Georgian form
gets rendered as something thinner than it actually is.
`მოგატანინებდი` → ✗ "I would bring" → ✓ "I would have you bring it"

**Translation overexpansion** (very high) — specifics get added in
translation that the Georgian source doesn't support.
`გაგვაკეთებინეს` → ✗ "The manager forced us to prepare the report" →
✓ "They had us do it"

## Ambiguity errors

**Ambiguity collapse** (very high) — a genuinely ambiguous sentence gets
resolved to one reading without acknowledging the alternatives.
Context: `ნინომ წიგნი და წერილი აიღო.` Then: `შემდეგ მეგობარს გაუგზავნა.`
→ ✗ "ნინომ წიგნი გაუგზავნა" (Nino sent the book) → ✓ "შესაძლოა წიგნი,
წერილი ან ორივე გაეგზავნა; დაზუსტება საჭიროა" (could be the book, the
letter, or both; clarification is needed)

**Overconfident interpretation** (high) — a context-dependent reading
gets presented with more certainty than the evidence supports.
`შემოგვთავაზა` → ✗ "დირექტორმა პროექტი შემოგვთავაზა" (the director
offered the project) → ✓ "(s)he offered it to us" — the specifics are
unknown without context

## Evidence-status error

**Evidence-status loss** (very high) — this framework's own pilot-stage
assessments get restated as settled scientific fact rather than working
hypotheses. Applies to this skill's own material too: treat the role
codebook and error taxonomy as a useful, evidence-grounded lens — not as
an infallible or complete description of Georgian. Note that some of the
source book's own examples were wrong and have been corrected here; see
`references/about-this-source.md`.

## Additional checks (added in this skill, not part of the source taxonomy)

**Tense-series case misreading** (high) — a case is mapped to a role
without checking the verb's tense series.
`ბავშვს წერილი დაუწერია` → ✗ "a letter was written to/for the child" →
✓ "the child has (apparently) written a letter" — in the perfect series
the agent is dative. `ბავშვს დედისთვის წერილი მიუწერია` → ✗ "wrote for
mother's sake" → ✓ "has written a letter to mother" — in the perfect
series the recipient takes `-თვის`

**Reported-speech loss** (high) — a quotative particle is dropped, so
someone else's words become the speaker's own.
`მოვალო` → ✗ "I'll come" → ✓ "(s)he said (s)he'd come" (`-ო` = words of
someone other than the speaker; `-მეთქი` = the speaker's own words;
`-თქო` = words to pass on)

**Evidential loss** (medium) — the not-witnessed sense of the perfect or
of `თურმე` is flattened into a plain, witnessed past.
`თურმე წასულა` → ✗ "(s)he left" (stated as witnessed fact) →
✓ "apparently (s)he has left" / "it turns out (s)he left"

## Quick index by symptom

- *Sentence has a causative verb* → check agent/executor loss or
  confusion, recipient–executor confusion (read the object prefix as the
  person made to act), causation loss/overinterpretation
- *Sentence has a dative-case noun* → check the tense series first, then
  dative overgeneralization, experiencer–recipient confusion
- *Sentence has a `-თვის` phrase* → beneficiary, or a recipient (perfect
  series, causatives)? — tense-series case misreading
- *Word order looks unusual* → check word-order role error, focus loss
- *Verb has a prefix (preverb)* → check preverb loss, direction loss
- *Sentence has "ალბათ", "შეიძლება", "ჯობს", or similar hedges* → check
  probability-to-fact, recommendation-to-obligation, conditional loss
- *Something is missing from the sentence* → check implicit object loss
  vs. fabricated object, context loss vs. fabricated context
- *Sentence follows on from prior text* → check context loss, wrong
  coreference
- *A word ends in `-ო`, `-მეთქი` or `-თქო`* → reported-speech loss
- *Verb is in the perfect series, or `თურმე` appears* → evidential loss
- *Phrase might be figurative* → check idiom-as-literal,
  literal-as-idiom, emotional/social/moral effect loss
- *Sentence allows more than one reading* → check ambiguity collapse,
  overconfident interpretation
- *Translating a compressed verb form* → check underexpansion vs.
  overexpansion
