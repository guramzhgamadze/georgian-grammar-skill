# Georgian Sentence Structure

Beyond the verb itself, a Georgian sentence carries information in its
case marking, its word order, its particles, and in what it deliberately
leaves out. None of these map onto meaning as simply as they first appear.

## Case matrix — and why case alone isn't role

Georgian marks nouns for case (nominative, ergative, dative, genitive,
instrumental, adverbial, vocative — plus postpositional phrases, which
behave similarly for this purpose, e.g. `-თვის` "for", which always takes
the genitive: `დედისთვის`, `ოჯახისთვის`). For every significant noun
phrase, it's worth recording the token, its case, its role, and the
evidence for that role — because **the same case can carry different
roles depending on the verb and its tense series**:

- `დედას წერილი მისწერა.` — "დედას" is dative → **recipient** (wrote a
  letter *to* mother)
- `დედას გაახსენდა ბავშვობა.` — "დედას" is dative → **experiencer**
  (mother is the one remembering, not being addressed)
- `დედისთვის საჩუქარი იყიდა.` — "დედისთვის" is a `-თვის` phrase →
  **beneficiary** (bought a gift *for* mother)
- `ბავშვი წერილს წერს.` — "წერილს" is dative → **direct object**
  (present series)
- `ბავშვს წერილი დაუწერია.` — "ბავშვს" is dative → **agent** (perfect
  series)

Treating every dative noun as a recipient by default (`dative role
overgeneralization`) is one of the most frequent, well-documented AI
errors on Georgian. The verb's own meaning, and its tense series, decide
the role — not the case form by itself.

### Case patterns by tense series

Which case marks the subject and the objects depends on the screeve's
series and on the verb class (Harris 1981; Anderson 1984; Aronson 1991;
Hewitt 1995 — as tabulated by the Surrey Morphology Group; Series I/II
also in Baratashvili 2019):

| Series (screeves) | subject of a transitive verb | direct object | indirect object |
|---|---|---|---|
| I — present, imperfect, present subjunctive, future, conditional, future subjunctive | nominative | dative | dative |
| II — aorist, II subjunctive (optative) | ergative | nominative | dative |
| III — perfect, pluperfect, III subjunctive | dative | nominative | `-თვის` phrase (genitive + `-თვის`) |

The same event across the three series (Anderson 1984):
- I: `ვუხატავ დედას სურათს` — "I am painting a picture for mother"
  (`დედას`, `სურათს` both dative)
- II: `დავუხატე დედას სურათი` — "I painted a picture for mother"
  (`სურათი` now nominative)
- III: `არ დამიხატავს დედისთვის სურათი` — "I didn't paint a picture for
  mother" (`დედისთვის`; the subject is marked by the prefix `მ-`)

And with this skill's running example:
- I: `ბავშვი დედას წერილს სწერს` — "the child is writing a letter to
  mother"
- II: `ბავშვმა დედას წერილი მისწერა` — "the child wrote a letter to
  mother"
- III: `ბავშვს დედისთვის წერილი მიუწერია` — "the child has (apparently)
  written a letter to mother"

Verb class matters too:
- Intransitive verbs of the "passive" type (`მოვიდა` "came", `დაიწერა`
  "was written") keep a **nominative** subject in every series.
- "Medial" (active intransitive) verbs take an **ergative** subject in
  series II even with no object: `ძაღლმა იყეფა` "the dog barked",
  `წყალმა იდუღა` "the water boiled" (Hewitt 2008); like transitive verbs,
  they take a dative subject in series III.
- "Feeling" verbs (`მიყვარს` "I love", `მინდა` "I want", `გაახსენდა`
  "remembered") have a **dative** experiencer and a nominative theme in
  every series: `მამას თავისი შვილები უყვარს` — "Father loves his
  children" (Anderson 1984).

The Explanatory Dictionary of the Georgian Language states the `-თვის`
rule for the perfect directly: with three-person verbs, `-თვის` marks the
object of a predicate in the perfect — `წიგნი ამხანაგისათვის
გამოურთმევია` "he has (apparently) taken the book from a friend".

## Word order and focus

All permutations of the main constituents are grammatical in Georgian
(subject–object–verb is usually described as the canonical order, and
subject before object is preferred). The choice among
them is driven mainly by information structure, and intonation carries
more of that load than word order does (Skopeteas, Féry & Asatiani 2009).
Moving something changes what is topic or focus — **never the
grammatical roles**:

- `ბავშვმა დედას წერილი მისწერა.` — neutral order
- `დედას ბავშვმა წერილი მისწერა.` — "დედას" (mother/to-mother) placed
  first; the child is still the one who wrote, mother is still the
  recipient — what's changed is how the information is packaged, not who
  did what

Never assign "agent" to a sentence's first word purely on position — check
case, verb agreement and the tense series instead (`word_order_role_error`
is a named, frequent failure mode).

Focus itself is a separate dimension worth naming explicitly: neutral,
agent focus, recipient focus, object focus, predicate focus, contrastive
focus, or broad focus — plus a deliberately hedged tier (*possible* agent
/ recipient / object focus) for a reading that word order suggests but
doesn't settle. What the experimental evidence shows (Skopeteas, Féry &
Asatiani 2009):
- narrow focus is *preferably, but not obligatorily*, placed immediately
  before the verb, and question words must stand there: `ნინო სად
  წავიდა?` / `სად წავიდა ნინო?` "Where did Nino go?" — but not `*ნინო
  წავიდა სად?`
- the position in front of the focus tends to hold the **topic** — so a
  fronted element is more often what the sentence is *about* than what it
  emphasizes
- in writing there is no intonation, so a focus reading taken from word
  order alone stays tentative

Applied:
- `სწორედ ბავშვმა დაწერა წერილი.` — "It was precisely the child who wrote
  the letter" — agent focus, marked by the particle `სწორედ` and by
  `ბავშვმა` standing right before the verb (high confidence)
- `წერილი ბავშვმა დაწერა.` — the object comes first (most likely the
  topic: "the letter — the child wrote it"), and `ბავშვმა` sits in the
  preverbal focus slot: at most a *possible* agent focus, medium
  confidence and context-dependent — not object focus

Losing which element was emphasized (e.g. flattening `სწორედ ბავშვმა
დაწერა წერილი` down to a plain "the child wrote the letter") loses real
information: that the sentence is specifically ruling out anyone else
having written it.

## Particles

Small words that carry real semantic weight and are easy to drop in
translation:
- `ალბათ` — probability ("probably")
- `მაინც` — concession ("still / anyway / nevertheless")
- `სწორედ` — emphasis ("precisely / exactly")
- `თურმე` — "apparently, it turns out" (see the evidential perfect in
  `references/verb-morphology.md`)

Dropping `ალბათ` from `ალბათ მოვა` ("[they'll] probably come") and
rendering it as a flat "[they] will come" converts a hedge into an
asserted fact — a documented, high-severity error.

## Reported-speech particles

Georgian marks quoted words with enclitic particles that also tell you
*whose* words they are (Rostovtsev-Popiel 2017; Zekalashvili 2022):
- `-მეთქი` — the speaker's own words (from `მე ვთქვი` "I said"):
  `მოდი-მეთქი!` — '"Come here," I said'
- `-ო` — the words of anyone other than the speaker (you, he/she, they,
  also "we"): `მოდიო!` — '"Come here," (someone other than me) said'
- `-თქო` — words the speaker wants the listener to say or pass on:
  `მოდი-თქო!` — 'Tell him/her: "Come here!"'

Dropping the particle turns reported speech into the speaker's own
statement: `მოვალო` is "(s)he said (s)he'd come", not "I'll come" — the
person who is coming changes. In informal modern usage `-თქო` is
increasingly used in place of `-მეთქი` and `-ო` (Rostovtsev-Popiel 2017),
so read the particle together with the context.

## Zero-expression (pro-drop) and context recovery

Georgian verb agreement often makes separate pronouns unnecessary, and
established context makes restating a noun unnecessary. What's omitted
can include the agent, executor, recipient, object, cause, purpose,
temporal reference, location, direction, or the condition an event
depends on. Two related but distinct situations:

- **Zero-expression within one utterance**: `მოვიტანე` alone means "I
  brought [it]" — only the agent is verb-encoded (the `ვ-` prefix); the
  recipient and the object are both unexpressed. Don't over-read the
  verb: `მოგიტანე` *does* encode a recipient (`-გ-` = "to you"),
  `მოვიტანე` does not, so "to whom" is a genuine gap here rather than
  something the form quietly carries. The source lists agent, recipient
  and object alike as implicit information for this sentence.
- **Recovery across sentences**: given `ნინომ წერილი დაწერა.` ("Nino wrote
  a letter.") followed by `შემდეგ დედას გაუგზავნა.` ("Then [she] sent
  [it] to mother."), the second sentence's missing agent and object are
  recovered from the first — agent = Nino, object = the letter — with
  high confidence, because the preceding sentence directly supports both.

Losing this connection and treating the second sentence as referring to
an unknown person doing an unknown thing (`context_loss`) discards
information the text actually provides. But recovery has to be earned by
the actual preceding text — filling in a plausible-sounding but
unsupported specific (`fabricated_context`) is a separate, more serious
error than merely losing the connection.

In translation, a dropped argument is rendered with the pronoun the
verb's person marking points to: `შემოგვთავაზა` is "(s)he offered it to
us" — not "someone offered us something". Who "(s)he" is and what "it" is
come from context, or stay open if the context doesn't say.

## Ambiguity

Some sentences are genuinely ambiguous and should be represented that
way, not resolved by guessing:

`ნინომ წიგნი და წერილი აიღო. შემდეგ მეგობარს გაუგზავნა.` — "Nino picked
up a book and a letter. Then [she] sent [it/them] to a friend." — it's
not settled from the text whether she sent the book, the letter, or both.
Picking one silently (`ambiguity_collapse`) or presenting a guess with
unwarranted confidence (`overconfident_interpretation`) are both errors;
the accurate response names the live possibilities and flags that
clarification would be needed for certainty.

The same applies to coreference: `ნინომ მარიამს წიგნი მისცა. შემდეგ
წაიკითხა.` ("Nino gave Mariam a book. Then [someone] read [it].") — it's
not textually settled whether Nino or Mariam is the one who read it;
don't assert one reading as certain.

## Relations between clauses

**Temporal relations** — `before`, `after`, `simultaneous`, `overlapping`,
`completed_before`, `conditional_sequence`. Watch for constructions where
one event is explicitly marked as already complete relative to another:
`როცა მივედი, შეხვედრა უკვე დაწყებული იყო.` — "When I arrived, the
meeting had already started" — the meeting's start is `completed_before`
the arrival; reading this as a simple sequence ("I arrived, then the
meeting started") reverses the actual order.

**Causal relations** — `direct_cause`, `enabling_condition`,
`motivation`, `consequence`, `inferred_cause`. Only mark a cause as
explicit when the text actually states it (e.g. via `-ის გამო`, "because
of"), and don't invent a causal link the text doesn't support:
`წვიმის გამო შეხვედრა გადაიდო.` — "The meeting was postponed because of
the rain" — direct cause, explicitly marked.

## Worked example — neutral sentence

`ბავშვმა დედას წერილი მისწერა.` ("The child wrote a letter to mother.")
- tense series: II (aorist)
- case matrix: ბავშვმა (ergative → agent), დედას (dative → recipient),
  წერილი (nominative → object) — in the present series the same roles
  would be nominative / dative / dative (`ბავშვი დედას წერილს სწერს`)
- word order: agent–recipient–object–predicate, neutral, nothing fronted
- focus: neutral — nothing specifically emphasized
- nothing implicit, nothing to recover from context
- natural translation: "The child wrote a letter to the mother."

## Worked example — marked word order

`დედას ბავშვმა წერილი მისწერა.` (same event, "დედას" placed first)
- case matrix and roles: identical to the neutral version above — the
  word order changes how the information is packaged, not who did what
- word order: marked, initial element = დედას — most likely the topic
  ("as for mother, the child wrote her a letter")
- focus: not settled by word order alone; don't assume დედას is
  emphasized
- natural translation: keep the participants and roles of the neutral
  version; a neutral rendering ("The child wrote a letter to the mother")
  is safe, and a topic-style rendering ("To the mother, the child wrote a
  letter") is fine where the context is about the mother. Don't use a
  focus cleft ("It was to mother that…") unless the context or
  intonation marks mother as the focus.
