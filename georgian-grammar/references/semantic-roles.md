# Semantic Roles in Georgian

Eleven participant roles cover who/what is involved in a Georgian clause
and how. A role is never assigned from case or word order alone — always
check what the verb's meaning actually requires, and which tense series
the verb is in (the same role can be nominative, ergative or dative
depending on the series — see `references/sentence-structure.md`). Roles
are recorded with an expression type — `explicit`, `verb_encoded`,
`case_encoded`, `preverb_encoded`, `word_order_encoded`,
`context_recovered`, `implicit_unspecified`, `inferred`, `ambiguous`,
`unknown` (individual roles allow only a subset: `preverb_encoded` is
mainly a *direction* value, `case_encoded` doesn't apply to a role the
verb alone carries) — and a confidence level (`certain`, `high`, `medium`,
`low`, `unknown`), because Georgian frequently leaves a role implicit
rather than stating it — and an implicit role is information ("there is
an unspecified performer here"), not an absence of information.

## The roles

**Agent** — the person, force, or entity that initiates, causes, or
controls the action. Don't assign this purely from word position, and
don't merge it with the executor in a causative form.
- `ბავშვმა წერილი დაწერა` — "the child wrote a letter" — explicit
  (ergative, aorist series)
- `მოგწერე` — "I wrote to you" — agent (I) is verb-encoded, not a separate word
- `გაგვაკეთებინეს` — "they had us do [it]" — agent (they) is
  verb-encoded (keep the executor, "us", in the gloss — dropping it here
  is `executor_loss`)
- `ბავშვს წერილი დაუწერია` — "the child has (apparently) written a
  letter" — the agent is **dative** here, because the verb is in the
  perfect series

**Executor** — in a causative construction, the one who actually carries
out the action, distinct from whoever caused them to. Only applies when
causation is present; if causation is present, an executor must be marked
even if their identity is unspecified — it must not simply disappear. In
a causative built on a transitive verb the executor is the indirect
object — a dative noun, cross-referenced by the verb's object prefix
(Baratashvili 2019).
- `მასწავლებელმა ბავშვს წერილი დააწერინა` — "the teacher had the child
  write a letter" — agent = teacher, executor = child
- `გაგვაკეთებინეს` — "they had us do it" — agent = they, executor = we
  (verb-encoded by `გვ-`)
- `მოგატანინებდი` — "I would have you bring it" — agent = I, executor =
  you (verb-encoded by `გ-`; not a recipient)
- `სახლი ავაშენებინე` — "I had [someone] build a house" — executor exists
  but is unspecified, not absent

**Recipient** — who or what the action, information, or object is
directed toward (writing, speaking, sending, giving, bringing, offering).
Don't assign every dative noun this role automatically, and don't merge it
with beneficiary without contextual support.
- `დედას წერილი მისწერა` — "wrote a letter to mother" — explicit
- `მოგწერე` — recipient (you) is verb-encoded
- `შემოგვთავაზა` — "(s)he offered [it] to us" — recipient (us) is
  verb-encoded; who offered what remains unspecified — don't invent either
- A recipient is **not** always dative: in the perfect series it is a
  `-თვის` phrase (`ბავშვს დედისთვის წერილი მიუწერია` — "the child has
  written a letter to mother"), and in a causative of a three-place verb
  it is pushed into a `-თვის` phrase too (`მამამ მიაცემინა (მას)
  დედისთვის ტორტი` — "Father made him give the cake to mother"). So a
  `-თვის` phrase is not automatically a beneficiary.

**Object** — the thing the action directly concerns. If the verb
semantically requires an object but none is stated, mark an *implicit
object* instead of leaving the role out — but never invent what it is.
- `ბავშვმა წერილი დაწერა` — object = "წერილი" (letter), explicit
  (nominative, aorist series)
- `ბავშვი წერილს წერს` — object = "წერილს", explicit (dative, present
  series)
- `წავიკითხე` — "I read [it]" — object is implicit/unspecified, not "a book"

**Implicit object** — a required object that the text doesn't name. Its
value may be recovered from context if the context actually supports a
specific value; otherwise it stays unspecified. Never duplicate this
alongside an explicit object for the same event.
- `მოგიტანე` alone — "I brought it to you" — the object is unnamed; its
  identity is unspecified
- With prior context "წიგნი ხომ მთხოვე?" ("didn't you ask me for the
  book?") — same sentence now recovers object = "წიგნი" (the book), from
  context, not invented

**Experiencer** — a person or being undergoing an emotional, mental,
physical, or perceptual state (memory, fear, pain, liking, need,
perception). Frequently dative-marked, and frequently mistaken for a
recipient or an agent.
- `მას გაახსენდა ბავშვობა` — "he/she remembered [their] childhood" —
  "მას" is the experiencer, not an addressee — nothing here is being sent
  to them, they're the one having the memory
- `ბავშვს შეეშინდა` — "the child got scared"
- `მას ეს წიგნი მოსწონს` — "he/she likes this book"

**Source** — the place, person, or origin something moves or comes from.
- `ინფორმაცია უნივერსიტეტიდან მიიღო` — "received the information from
  the university"
- `წერილი მეგობრისგან მიიღო` — "received the letter from a friend"

**Beneficiary** — who the action is performed for the sake, interest, or
benefit of. Don't merge this with recipient automatically — a recipient
receives something directly; a beneficiary benefits, which is a different
relation even when it looks similar on the surface.
- `ოჯახისთვის სახლი ააშენა` — "built a house for the family"
- `სტუდენტებისთვის პროგრამა შექმნა` — "created a program for the students"
- A beneficiary can also be a plain dative, cross-referenced on the verb
  with the version vowel `უ-`: `ვუხატავ დედას სურათს` — "I am painting a
  picture for mother" (Anderson 1984)

**Instrument** — the object, technology, or method used to carry out the
action.
- `კალმით დაწერა` — "wrote with a pen"
- `მანქანით წავიდა` — "went by car"
- `პროგრამის საშუალებით დაამუშავა` — "processed [it] using the program"

**Location** — where the action, state, or event takes place.
- `უნივერსიტეტში შეხვედრა გაიმართა` — "the meeting was held at the
  university"
- `სახლში მუშაობს` — "works at home"

**Direction** — the spatial, goal-oriented, or metaphorical direction of
an action or movement. In Georgian this is very often carried by the verb
prefix (preverb) rather than a separate word — see
`references/verb-morphology.md` for the preverb system itself.
- `შემოვიდა` — "came in" — direction (outside → inside, toward the
  speaker) is preverb-encoded in `შემო-`
- `გავიდა` — "went out" — direction (inside → outside), preverb `გა-`
- `მომიტანა` — "brought [it] to me" — direction is "toward the speaker",
  preverb `მო-`

## How roles combine

- Agent and executor can coexist in a causative and must have different
  values — if causation is present, don't collapse them into one.
- Recipient and beneficiary can share the same surface value, but don't
  merge them automatically — treat the choice as needing evidence, not a
  default.
- Recipient and experiencer do not normally coexist for the same
  participant in the same event.
- An explicit object and an implicit object are mutually exclusive for
  the same event — if the object is stated, don't also add a "the object
  is implicit" marker.
- Source and location can coexist but shouldn't take the same value;
  location and direction can coexist and may share a value.

## Worked examples

**Simple sentence** — `ბავშვმა დედას წერილი მისწერა.` ("The child wrote a
letter to mother.") — aorist series
- agent: ბავშვმა (certain, explicit — ergative case + verb form)
- recipient: დედას (certain, case-encoded — dative case + the verb
  "მისწერა")
- object: წერილი (certain, explicit — nominative)
- executor / implicit object: not applicable — no causation, object is
  already explicit
- the same event in the perfect series: `ბავშვს დედისთვის წერილი
  მიუწერია` — agent dative, recipient `-თვის`, object nominative; the
  roles are unchanged

**Causative form** — `გაგვაკეთებინეს.` ("They had us do [it].")
- agent: ისინი / "they" (high confidence, verb-encoded)
- executor: ჩვენ / "we" (certain, verb-encoded)
- object: unspecified (medium confidence — the verb doesn't name one)
- causation: present, subtype unspecified (see
  `references/verb-morphology.md` for the six causation subtypes)
- watch for: losing the executor and reading this as simply "we did it,"
  or losing the causation and reading it as "they did it for us" — both
  are documented, frequent errors

**Experiencer construction** — `მას გაახსენდა ბავშვობა.` ("He/she
remembered [their] childhood.")
- experiencer: მას (certain — the verb's meaning plus the dative form)
- object: ბავშვობა / "childhood" (high confidence, explicit)
- watch for: reading "მას" as a recipient just because it's dative
