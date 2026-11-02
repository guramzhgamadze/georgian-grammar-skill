# Source Book Index

A map of `source-book.pdf` (338 pages, Georgian) and its plain-text twin
`source-book-fulltext.txt`. Use it to load only the part you need: read
the line range of the `.txt` file (or `grep` inside it), or extract the
PDF pages with a PDF tool (`pdftotext -f <first> -l <last>
references/source-book.pdf -`). PDF page numbers are physical pages of
the file; text line numbers are 1-based lines of the `.txt` file. The PDF
keeps tables intact; in the `.txt` file tables are flattened.

The book's own examples still contain the errors this skill corrects —
see `about-this-source.md`.

| Section | PDF pages | TXT lines |
|---|---|---|
| **Part I — სამეცნიერო საფუძველი** (scientific foundation) | 5 | 132–133 |
| Introduction (შესავალი) | 5–7 | 134–218 |
| Ch. 1 — ქართული ენა ხელოვნური ინტელექტის ეპოქაში (Georgian in the age of AI) | 7–9 | 219–323 |
| Ch. 2 — საერთაშორისო გამოცდილებიდან ქართული ენის კვლევის მეთოდამდე (from UD, FrameNet, PropBank, AMR to the Georgian method) | 10–22 | 324–857 |
| Ch. 3 — BTU-ს მიერ შექმნილი ციფრული საფუძველი (BTU's digital resources and data scale) | 22–24 | 858–945 |
| Ch. 4 — ქართული ენის ციფრული სუვერენიტეტი (the digital sovereignty of Georgian; the long-term platform) | 25–27 | 946–1060 |
| Ch. 5 — პირველი ეტაპის კვლევითი არქიტექტურა (first-stage research architecture and results) | 27–35 | 1061–1369 |
| **Part II — ქართული ენის გრამატიკა** (machine-readable grammar specification, YAML modules) | 35 | 1370–1372 |
| Introduction to Part II | 36–48 | 1373–1900 |
| Module `01_README` — package overview, scope, status, evidence levels, expression types, confidence levels, mandatory roles | 48–59 | 1901–2480 |
| Module `02_CORE_SCHEMA` — common record structure, IDs, statuses, traceability | 59–75 | 2481–3379 |
| Module `03_ROLE_CODEBOOK` — the 11 semantic roles: definitions, usage conditions, examples | 75–89 | 3380–4177 |
| Module `04_VERB_RULES` — verb records: causation, preverbs, tense/mood/aspect, polarity | 89–108 | 4178–5224 |
| Module `05_SENTENCE_RULES` — sentence records: case matrix, word order, focus, zero expression, context recovery, clause relations | 108–127 | 5225–6290 |
| Module `06_IDIOM_RULES` — idiom and value-laden phrase records | 127–143 | 6291–7185 |
| Module `07_ERROR_TAXONOMY` — the 33 AI error types with severity, examples, prevention rules | 143–164 | 7186–8358 |
| Module `08_JSONL_EXAMPLES` — JSONL encodings of every record type | 164–181 | 8359–9219 |
| Appendix (დანართი) — validation system, AI benchmark, versioning | 181–185 | 9220–9380 |
| Part II summary (შეჯამება) — from description to a machine-readable system | 185–199 | 9381–9972 |
| **Part III — კვლევითი საფუძველი და შედეგები** (research basis and results: 25 studies) | 200–203 | 9973–10117 |
| Ch. 1 — ქართული ზმნა როგორც ინფორმაციული სისტემა (the verb as an information system) | 204–213 | 10118–10527 |
| Ch. 2 — ბრუნვა და მონაწილეთა სემანტიკური როლები (case and semantic roles) | 213–222 | 10528–10902 |
| Ch. 3 — სიტყვათა რიგი, ფოკუსი და ნულოვანი გამოხატვა (word order, focus, zero expression) | 223–232 | 10903–11278 |
| Ch. 4 — ბუნდოვანება და კონტექსტური აღდგენა (ambiguity and context recovery) | 232–241 | 11279–11675 |
| Ch. 5 — ქართული ინფორმაციის თარგმნითი გაშლა (translational decompression) | 241–252 | 11676–12149 |
| Ch. 6 — იდიომები, ემოციური და ღირებულებითი მნიშვნელობა (idioms, emotional and value-laden meaning) | 253–264 | 12150–12606 |
| Ch. 7 — AI შეცდომების კვლევა და მათი პრევენციის წესები (AI error research and prevention rules) | 264–276 | 12607–13109 |
| Ch. 8 — ანოტაციის სტანდარტების კვლევითი საფუძველი (annotation standards) | 276–284 | 13110–13453 |
| Ch. 9 — კვლევების რაოდენობრივი საფუძველი და მონაცემთა დაფარვა (quantitative basis, data coverage) | 284–307 | 13454–14502 |
| Ch. 10 — გაერთიანებული შედეგები (combined results) | 307–316 | 14503–14872 |
| Ch. 11 — შეზღუდვები და შემდეგი კვლევითი პროგრამა (limitations and next research programme) | 316–327 | 14873–15291 |
| **Bibliography (ბიბლიოგრაფია)** | 327–338 | 15292–15777 |

## Frequently needed spots

- `04.21` full worked record for `მოგატანინებდი` (VERB-0001): PDF p. 103,
  text line 4943 — note that its recipient/executor analysis is corrected
  in this skill
- `04.22` full worked record for `გაგვაკეთებინეს` (VERB-0002): PDF p. 105,
  text line 5088
- The error taxonomy entries with their example inputs are in module
  `07_ERROR_TAXONOMY` (text lines 7186–8358); search for `error_group:`
  or for an error code such as `executor_loss`
