# Artificial Intelligence

Proposed degree map swapping the new two-year core into a B.S. in Artificial Intelligence, assembled from existing (and a small number of proposed) K-State CIS/AI courses — there is no prior official AI degree to draw from, so this is a first construction, not a regeneration. Checked against both `resources/reference/abet/cs.md` (Computer Science criteria) and `resources/reference/abet/ai.md` (Artificial Intelligence criteria), on the same dual-degree premise as the Cybersecurity map.

**Constraint, per direct instruction**: no graduate-level courses (700+) anywhere in this map. Every AI-specific course below is undergraduate-level (≤600), which required identifying undergraduate equivalents for several courses that only currently exist as graduate offerings.

## Years 1–2 (= `cs.md`, not reproduced)

Identical to the shared core — see `cs.md` for the full annotated version.

| Semester | Courses | Credits |
|---|---|---|
| Y1S1 | CIS 115, CIS 116, DEN 161, CIS 120, MATH XXX Logic and Sets, MATH XXX Counting Finite Configurations, ENGL 100, Core Communication Requirement (KSC 020) | 14 |
| Y1S2 | CIS 260, CIS 220, CIS 200, ECE 241, Calculus Slot, MATH XXX Recursive and Modular Computation, MATH XXX Graphs/Trees/Maps, ENGL 200 | 17 |
| Y2S1 | CIS 300, CIS 320, CIS 301, Linear Algebra Slot, CIS 225, CIS 251, KSC 040 | 15 |
| Y2S2 | CIS 141, CIS 308, CIS 400, KSC 060, STAT 410, Social & Behavioral Sciences (KSC 050) | 15 |

**Math elective note**: choosing MATH 515 or 551 for the Linear Algebra Slot (Y2S1) covers the AI math floor's linear-algebra requirement directly.

## The AI course pool

No official AI course list exists to draw from, so this pool was assembled from the current CIS catalog plus courses confirmed to be in development:

| Course | Title | Status | ABET AI topic served |
|---|---|---|---|
| CIS 530 | Introduction to Artificial Intelligence | Existing | Foundations: reasoning, heuristic search, knowledge representation |
| CIS 531 | Intro to Programming Techniques for Data Science and Analytics | Existing | Data engineering |
| CIS 532 | Introduction to Deep Learning | Existing | Machine learning, including deep learning |
| CIS 534 | Information Retrieval and Text Mining | **Proposed** — undergrad equivalent of CIS 833; number 533 was unavailable (already assigned to Data Science Foundations), 534 used instead | Advanced depth / secondary application area |
| CIS 535 | Neuro-Symbolic Artificial Intelligence | **Proposed** — undergrad equivalent of CIS 835 (existing graduate course: "State of the art in combining deep learning with symbolic artificial intelligence approaches") | Advanced depth |
| CIS 536 | Knowledge Graphs for AI (Knowledge Engineering for Concordant Systems) | **Proposed** — currently piloting as CIS 590/890 (Spring 2026, Dr. Hande Küçük McGinty), permanent undergrad number not yet assigned | Data and knowledge engineering |
| CIS 537 | Computer Vision | Existing | Application area |
| CIS 635 | Introduction to Computer-Based Knowledge Systems | Existing | Foundations: knowledge representation |
| CIS 597 | AI Capstone | **New**, confirmed 2026-07-14 — parallel to CIS 599 for Cybersecurity | Major project |

**Four of these nine courses don't exist yet as numbered offerings** — this is a materially bigger dependency than the Cybersecurity map carried, which drew entirely from existing, currently-taught courses. This degree map cannot be finalized until CIS 534, 535, 536, and 597 are formally added to the catalog.

## Years 3–4 — AI-specific

### Year 3, Semester 1 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| CIS 450 | CIS 450 (Computer Architecture and Operations) | Direct match, satisfies CS ABET |
| CIS 501 | CIS 501 (Software Architecture and Design) | Direct match |
| CIS 505 | CIS 505 (Introduction to Programming Languages) | Direct match |
| Technical Writing Requirement | ENGL 415 or ENGL 516 | Direct match |
| Social & Behavioral Sciences (KSC 050, 2nd of 2) | Stays generic | No AI-specific course identified for this bucket |

### Year 3, Semester 2 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| CIS 560 | CIS 560 (Database System Concepts) | Direct match — also the prerequisite for CIS 536 |
| CIS 575 | CIS 575 (Introduction to Algorithm Analysis) | Direct match |
| CIS 415 | CIS 415 (Ethics and Conduct for Computing) | Serves both the CS general-criteria ethics requirement and, combined with the shared core's disciplined-AI-use content, the ABET AI "ethics and responsible AI" fundamental topic — **not yet confirmed as sufficient on its own; see faculty concerns** |
| Unrestricted Elective | **CIS 530** (Introduction to Artificial Intelligence) | Foundational course, positioned as early as the elective architecture allows |
| Free Elective (KSC 070) | Stays generic | — |

### Year 4, Semester 1 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| Systems Elective | Student choice (CIS 520/525/625) | CIS 625 (Concurrent Software Systems) is the natural recommendation given AI/ML's parallel-computing demands, but left as genuine student choice, matching the general map |
| Required Technical Elective #1 | **CIS 532** (Introduction to Deep Learning) | Satisfies the slot's "CIS 500+" rule |
| Required Technical Elective #2 | **CIS 537** (Computer Vision) | Application area requirement |
| Arts & Humanities (KSC 060, 2nd of 2) | Stays generic | — |
| Unrestricted Elective | **CIS 635** (Introduction to Computer-Based Knowledge Systems) | Reasoning/knowledge-representation depth |

### Year 4, Semester 2 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| Required Technical Elective | **CIS 536** (Knowledge Graphs for AI) | Data and knowledge engineering — contingent on this course receiving a permanent number |
| Capstone | **CIS 597** (AI Capstone) | New dedicated course, confirmed 2026-07-14 — parallel to CIS 599 for Cybersecurity, not a generic project course scoped after the fact |
| Upper Division Elective | **CIS 535** (Neuro-Symbolic AI) | Advanced depth — contingent |
| Upper Division Elective | **CIS 534** (Information Retrieval and Text Mining) | Advanced depth / secondary application area — contingent |
| Upper Division Elective | **CIS 531** (Programming Techniques for Data Science and Analytics) | Data engineering |

**CIS 533 (Introduction to Data Science Foundations)** is available but not placed in a required slot — it can substitute for CIS 531 in the last Upper Division Elective if preferred.

**Years 3–4 subtotal: 60 credits — identical to `cs.md`'s own Year 3–4 total.**

## Credit total

| | Y1S1 | Y1S2 | Y2S1 | Y2S2 | Y3S1 | Y3S2 | Y4S1 | Y4S2 | **Total** |
|---|---|---|---|---|---|---|---|---|---|
| Credits | 14 | 17 | 15 | 15 | 15 | 15 | 15 | 15 | **121** |

Identical to `cs.md`'s and the Cybersecurity map's own totals — the same known 1-credit gap above the typical 120-hour target, not a new or AI-specific overage.

## Open items, not resolved here

1. **CIS 534/535/536 need permanent undergraduate numbers and formal catalog approval.** Three of nine specialization courses in this map are proposed, not existing. This is the largest dependency in the map.
2. **AI system architecture & infrastructure (MLOps)** — no course exists (model serving, ML pipelines, scaling, vector stores). Confirmed as a real, standing gap, not addressed by CIS 536 (which is knowledge engineering/semantic-web content, not deployment infrastructure). Left open rather than approximated.
3. **Math/statistics floor (≥9 SCH: inference and modeling, linear algebra, probability, data visualization, optimization)** — linear algebra is covered (Y2S1 slot) and probability/inference/data-visualization are plausibly covered by STAT 410, but **optimization coverage is unconfirmed**. The prior analysis cited STAT 760, but its course level (undergraduate vs. graduate) hasn't been verified, and if it's 700+ it's excluded by the no-graduate-courses constraint. Needs a confirmed undergraduate optimization course or an alternative.
4. **CIS 415's sufficiency for "ethics and responsible AI"** — plausible given the shared core's disciplined-AI-use content, but not confirmed as meeting the ABET AI topic on its own.
5. ~~**Major-project anchor**~~ — resolved 2026-07-14: **CIS 597 (AI Capstone)**, a new dedicated course, confirmed rather than reusing CIS 598. Now part of the same "not yet in the catalog" dependency as items covered in point 1.
