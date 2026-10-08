# From storm-damaged paper to records found in seconds

**Case study: a zero-cost web app that keeps a team's paper routine but stores every signature in the cloud, plus the migration of ~1,550 handwritten records (and counting).**

### [▶ Read the case study and try the demo](https://josecabfe.github.io/storm-proof-records/)

A training and consulting firm (5,100+ alumni, 190+ courses in 11 years) kept proof of every certificate handover on paper, until the strongest hailstorm in years broke parts of the office roof and rainwater soaked the sheets kept closest at hand. Finding a record used to take ~3 minutes, or 6+ if the sheet was archived. Now it takes seconds.

---

## The problem

- Paper sheets were the only proof of delivery. During an El Niño season, the strongest hailstorm in years (tennis-ball-sized hail) broke parts of the office roof, and leaking water soaked and stained the sheets kept closest at hand.
- Checking whether someone had picked up a certificate meant flipping through sheets by hand: ~3 minutes for the current year, twice as long or more if archived.
- Records were messy: signatures over two rows, wrong years, margin notes, signed slips taped to the back.

**Constraints from the owners:** keep signing on paper; make it a standalone system, independent from all the company’s existing software (not just payments), moving from stored paper sheets to fully digital records; no new software costs.

## The solution

1. The person signs a redesigned paper slip (course code and number in boxes).
2. Staff take a photo with a phone from the web app.
3. The photo is compressed in the browser (3–5 MB → ~250 KB).
4. It is saved to Drive by year and course, with an automatic file name.
5. The spreadsheet (same layout as the paper sheet) gets a "View signature" link.
6. Anyone can search by name or ID across all courses and years.

## The data migration

| | 2024 | 2025 | 2026 | Total |
|---|---|---|---|---|
| Courses | 15 | 14 | 8 | 37 |
| Records (people) | ~590 | ~630 | ~350 | **~1,550** |
| Certificate handovers | ~450 | ~500 | ~160 | **~1,100** |
| Scanned pages | 39 | 42 | 21 | **~100** |
| Ambiguous cases resolved | 17 | 44 | 19 | **~80** |

- Handovers include signatures on the sheet, signed slips and courier deliveries with a tracking number.
- Transcription, automatic validation (numbering, ID and date formats) and ~80 ambiguous cases resolved with the business owner, paper in hand.
- Business rules applied consistently: date without signature = not picked up; signature without date = picked up on the course's most common date; two dates = the most recent; margin marks = ignored.
- **0 records lost.** Every year back to 2018 is now being loaded with the same process.

## Results

| | Before | After |
|---|---|---|
| Did this person get their certificate? | ~3 min flipping sheets (6+ if archived) | Answer in seconds |
| Proof of delivery | One damaged paper copy | Photo backed up in the cloud |
| Team routine | Sign on paper | Sign on paper + one photo |
| Software cost | — | $0 (Google Workspace) |

## Tools

Google Apps Script (JavaScript) · Google Sheets · Google Drive · HTML/CSS/JS · clasp · git

---

*Real project at my current job. Our clients trust us with their personal information, so no names, ID numbers or screenshots of the real system are shown. The demo data and the recreated sheet are fictional and were generated with AI. Numbers are rounded.*

*Another project for the same team: [Recording a course payment went from 5 minutes to under 1](https://josecabfe.github.io/payments-invoicing-case-study/)*

*Built by José Cabral Ferraro · [LinkedIn](https://www.linkedin.com/in/jose-cabral-ferraro/)*
