# Udemy course specification — CCA Foundations Practice Tests

Everything needed to publish the contents of this repository as a Udemy
**Practice Test** course. Source of truth is `index.html`; the counts below are
generated from it, so re-check them after any content change.

| | |
|---|---|
| Course type | Practice Test (not video) |
| Total questions | **412** |
| Practice tests | **12** — 5 full mock exams + 7 domain sets |
| Source | `index.html` in this repository |
| Last verified against source | 26 Jul 2026 |

---

## 1. Landing page copy

### Title
> Claude Certified Associate — Foundations: 5 Practice Exams

*Alternatives if the primary is rejected on trademark grounds — see §5:*
- `CCA Foundations Practice Exams: 412 Questions with Explanations`
- `AI Assistant Certification Practice Tests — Foundations Level`

### Subtitle
> 412 exam-style questions across all 7 domains, blueprint-weighted, with a full
> written explanation for every single answer.

### Description

Most practice exams for this credential are thin. This one is not.

You get **five complete 60-question mock exams**, each weighted to the official
domain blueprint, plus **seven domain-specific question sets** so you can drill
the areas you are actually weak in rather than re-taking a full exam to find out.

Every question carries a full written explanation — not just which answer is
correct, but why each of the other three is wrong. That is where the learning
happens, and it is the part most practice tests skip.

**What makes these questions different**

The item bank was audited for the defects that let candidates score well without
knowing the material. Distractor lengths are balanced so "pick the longest
option" gets you nowhere. Correct answers are evenly distributed across A, B, C
and D. No question repeats across the five exams, and no domain set gives away
an exam question. If you pass these, you passed on knowledge.

**How to use this course**

1. Take Exam 1 cold to establish a baseline.
2. Work the domain sets for anything below 70%.
3. Take Exams 2–4 at one-week intervals.
4. Save Exam 5 for the week before your test — it is the hardest of the five.

*This is an independent study aid. It is not affiliated with, endorsed by, or
sponsored by Anthropic. All questions are original.*

### What you'll learn
- Write and refine prompts that produce reliable, task-appropriate output
- Evaluate and validate AI output, and recognise when it cannot be trusted
- Choose the right product and model tier for a given task and constraint
- Design workflows that integrate an AI assistant into real business processes
- Configure projects, knowledge and instructions so behaviour is consistent
- Apply governance, risk and responsible-use judgment to realistic scenarios
- Diagnose failures systematically instead of guessing at prompt changes
- Sit the real exam knowing exactly which domains you are weakest in

### Requirements
- No prior certification required
- Hands-on familiarity with an AI assistant in day-to-day work is enough
- No coding required — this is the foundations tier

### Who this course is for
- Anyone booked in for the Foundations exam who wants realistic practice
- Professionals using AI assistants at work who want to formalise that knowledge
- Teams standardising on a shared level of AI literacy
- Anyone who has failed once and needs to find the specific gap

---

## 2. Curriculum

Udemy renders each of these as a separate practice test.

### Full mock exams

| # | Test name | Q | Time | Pass |
|---|---|---|---|---|
| 1 | Practice Exam 1 — Baseline | 60 | 120 min | 70% |
| 2 | Practice Exam 2 | 60 | 120 min | 70% |
| 3 | Practice Exam 3 | 60 | 120 min | 70% |
| 4 | Practice Exam 4 | 60 | 120 min | 70% |
| 5 | Practice Exam 5 — Hardest | 60 | 120 min | 70% |

> **On the 70% pass mark.** The real exam reports a scaled score of 100–1000 with
> 720 to pass. Under the scoring model used here — `100 + (correct ÷ 60) × 900` —
> 41 correct scores 715 and fails, 42 correct scores 730 and passes. So the
> honest raw threshold is **42 of 60 = 70%**, not 72%. Set Udemy's pass mark to
> 70 or candidates will be told they failed runs that would have passed.

### Domain question sets

Each set is 16 questions: 6 introductory, then 10 at exam difficulty.

| # | Test name | Blueprint weight | Q | Time | Pass |
|---|---|---|---|---|---|
| 6 | D1 — Prompting & Task Execution | 14% | 16 | 30 min | 70% |
| 7 | D2 — Output Evaluation & Validation | 21% | 16 | 30 min | 70% |
| 8 | D3 — Product & Model Selection | 12% | 16 | 30 min | 70% |
| 9 | D4 — Workflow Integration & Solution Design | 16% | 16 | 30 min | 70% |
| 10 | D5 — Configuration & Knowledge Management | 12% | 16 | 30 min | 70% |
| 11 | D6 — Governance, Risk & Responsible Use | 15% | 16 | 30 min | 70% |
| 12 | D7 — Troubleshooting & Optimization | 10% | 16 | 30 min | 70% |

**Recommended ordering note for the description:** D2 is the heaviest domain on
the exam at 21% — nearly a fifth of your score — and is where most candidates
lose marks. Suggest taking test 7 first among the domain sets.

### Per-exam blueprint

Every full exam carries this distribution, matching the published weighting:

| Domain | Weight | Items per exam |
|---|---|---|
| D1 Prompting & Task Execution | 14% | 8 |
| D2 Output Evaluation & Validation | 21% | 13 |
| D3 Product & Model Selection | 12% | 7 |
| D4 Workflow Integration & Solution Design | 16% | 10 |
| D5 Configuration & Knowledge Management | 12% | 7 |
| D6 Governance, Risk & Responsible Use | 15% | 9 |
| D7 Troubleshooting & Optimization | 10% | 6 |
| **Total** | **100%** | **60** |

---

## 3. Per-question settings

For every question in every test:

- **Type:** multiple choice, single correct answer, four options
- **Explanation:** required — the bank already has one for all 412 items
- **Knowledge area / tag:** set to the domain (`D1`…`D7`) so Udemy's results
  screen produces a per-domain breakdown. This is the single most valuable
  setting in the whole course and is easy to skip during import.

---

## 4. Extracting the questions

The question bank lives in two JSON blocks inside `index.html`:

- `<script id="exam-data">` — the five full exams
- `<script id="domain-data">` — the seven domain sets

Each item has the shape:

```json
{
  "qid": "e1q1",
  "domain": 2,
  "domainName": "Output Evaluation & Validation",
  "type": "single",
  "options": ["…", "…", "…", "…"],
  "correct": [1],
  "rationale": "…"
}
```

`correct` is a zero-based index into `options`. Udemy's bulk question importer
expects a different shape, so a conversion pass is needed — say the word and I
will write it.

---

## 5. Before you publish

**Trademark.** "Claude" and any official certification name are Anthropic marks.
Udemy routinely rejects or forces retitling of courses that use a certification
name in a way implying endorsement. Two mitigations, both worth doing:

- Keep the disclaimer in the first paragraph of the description, not buried at
  the bottom.
- Have the fallback titles in §1 ready rather than scrambling after a rejection.

**Original content.** Every question here is original, written from documented
product behaviour. Nothing is transcribed from a real exam. State this plainly —
Udemy removes practice-test courses that are suspected exam dumps, and the
distinction is worth making explicitly rather than leaving to inference.

**Accuracy of the blueprint.** The domain weights come from the published outline
and are reproduced in `index.html`. If the certification blueprint changes, the
weights table in §2, the per-exam distribution, and the item counts all move
together. Do not update one without the others.

**Assets still needed**
- Course image, 750×422
- Promo video, 2–5 minutes. For a practice-test course the strongest script is
  simply: walk through one hard question, show the explanation, and say what the
  distractors were designed to catch.

---

## 6. Regenerating the numbers in this file

```bash
python3 - <<'EOF'
import json, re
s = open('index.html').read()
E = json.loads(re.search(r'<script id="exam-data" type="application/json">(.*?)</script>', s, re.S).group(1))
D = json.loads(re.search(r'<script id="domain-data" type="application/json">(.*?)</script>', s, re.S).group(1))
ex = sum(len(e['questions']) for e in E)
dm = sum(len(x['practice']) + len(x['exam']) for x in D)
print('exams: %d x %d = %d' % (len(E), len(E[0]['questions']), ex))
print('domains: %d sets = %d' % (len(D), dm))
print('total: %d' % (ex + dm))
EOF
```
