+++
title = "Data Science"
weight = 30
ordinal = "5.3"
+++

> *Working draft for faculty review. A proposal for a CS-housed Data Science specialization built on the shared two-year core, using real K-State courses. Note up front: the **Statistics department already offers a B.S. in Data Science**, so this proposal is framed as a CS-flavored, partnership-oriented specialization rather than a duplicate. CIS/STAT/MATH numbers are actual K-State courses.*
>
> **Updated 2026-08-04** — this page's core-facing claims were still in old block/CS-1xx-2xx terms; rewritten against the real course sequence. **Unlike `cybersecurity.md` and `ai-systems.md`, this page still has no real, semester-by-semester degree-map table** — bringing it up to that standard (with a confirmed Year 3–4 course sequence and a matching ABET table format) is a real gap, flagged here rather than invented in this pass.

## Premise and positioning

Under the specialization model, every degree is the identical two-year core plus a degree-specific upper division. For Data Science there is an important wrinkle: **Statistics already has a B.S. in Data Science**, built on a calculus-first, mathematical-statistics spine (Calc I–III → linear algebra → STAT 610/611). A CS-side Data Science specialization should therefore be **deliberately CS-flavored** — heavier on programming, data engineering, databases, and systems — and should **partner with Statistics** for statistical depth rather than rebuild it. The differentiator: CS contributes the computing and engineering; Statistics contributes the inferential theory.

## What the core already provides (the on-ramps)

Data-science-bound students arrive having spiraled through Data Structures & Representation (CIS 300; the geospatial sub-theme is still a proposed addition, not built — see `cis-300.md`'s "Proposed Changes"), STAT 410 (no drafted content yet — the confirmed successor to the non-calculus statistics sequence), the Human-Centered Computing visualization throughline (confirmed at CIS 320, still proposed/undrafted there), declarative SQL (CIS 260) and dataflow (CIS 300/CIS 320) in Computational Models, and Optimization Reasoning. **A "notebook data-analysis capstone with responsible-AI judgment" has no confirmed course home** — the 2026-08-04 assessment-chapter pass found this unplaced except for its AI-code-critique slice (confirmed at CIS 141).

## Prerequisite mapping (core → specialization)

K-State's DS-relevant courses carry prerequisites the core satisfies by design:

| Course prerequisite | Satisfied by |
|---|---|
| CIS 300 (data structures) | Data Structures & Representation thread — CIS 300 (Y2 Fall) |
| CIS 301 (logic) | **CIS 301** (Y2 Fall, Logical Foundations of Programming) — confirmed real content: pre/post-conditions, loop invariants, proof by induction. MATH Logic and Sets (Y1 Fall) contributes the propositional/predicate-logic substrate. |
| CC 310 (Python) | Core language-agnostic foundation + an optional Python certificate |
| STAT 225 / STAT 510 (intro stats) | **STAT 410** (Y2 Spring) — confirmed successor to the old non-calculus statistics sequence, but has no drafted content yet to verify this claim against |
| MATH 510 (discrete) | The core's MATH discrete sequence: Logic and Sets, Counting Finite Configurations (Y1 Fall), Recursive and Modular Computation, Graphs/Trees/Maps (Y1 Spring) |

## CS-side specialization stack (real undergraduate courses)

K-State has built a genuine undergraduate 500-level data-science suite — the earlier worry that depth was graduate-only was mistaken:

| Course | Role |
|---|---|
| **CIS 533 Introduction to Data Science Foundations** | Data wrangling, feature engineering, classification, regression, clustering, outlier detection, **and societal aspects** — covers much of the ABET lifecycle in one course |
| **CIS 531 Introduction to Programming Techniques for Data Science** | MapReduce, big-data tooling, data integration and transformation |
| **CIS 560 Database System Concepts** | Data management depth (CIS 260, Y1 Spring, is the core's foundation) |
| **CIS 561 Introduction to Data Science in Practice** | A **capstone-bearing practicum** — directly serves the ABET major-project requirement |
| Graduate electives (CIS 731/733/860/864) | Further depth (data engineering, advanced databases) via accelerated access |

## Statistics partnership stack (real courses)

Rather than duplicate Statistics, the specialization draws on its courses for inferential and modeling depth:

| Course | Role | Calculus needed? |
|---|---|---|
| **STAT 705 Regression & ANOVA** | Regression/modeling baseline | No (one prior stats course) |
| **STAT 766 Applied Data Mining / ML & Predictive Analytics** | Statistics-side ML (trees, SVM, random forests, boosting, clustering, topic models) | No (needs 705 + programming) |
| **STAT 745 Statistical Graphics** | **Data visualization** (serves ABET viz directly) | No (needs 705) |
| **STAT 760 Optimization for Data Science** | Optimization (convex/nonconvex, applied to ML) | Yes (needs STAT 511 + linear algebra) |
| **STAT 713 Applied Linear Statistical Models** | Matrix-based regression/modeling | Needs linear algebra |
| **STAT 511 / STAT 610–611** | Calculus-based inference; mathematical-statistics rigor | Yes (Calc II / Calc III) |
| **STAT 764 Applied Spatio-Temporal Statistics** | Geospatial statistics (ties to the core's geospatial sub-theme) | Needs 705/713 |

## Mathematics

- **Linear algebra: MATH 551 (Applied Matrix Theory)** — applied, needs only Calc I, and bundles linear programming. Preferred over MATH 515 (which needs Calc III). *A custom linear-algebra course built off the core math progression — potentially landing before calculus — would fit the foundation's philosophy better and is worth pursuing with Mathematics.*
- **Calculus** moves to year 3 (the core decision).

## The calculus-sequencing tension (flagged honestly)

This is the most important planning issue for this specialization. Statistics' own DS degree **front-loads calculus** (Calc I–III in years 1–2) precisely to make the rigorous stats sequence (STAT 510/511, 610/611) reachable on time. **Our core defers calculus to year 3**, which means the calculus-based statistics and optimization courses cannot begin until year 3 and therefore **compress into years 3–4** for our specialization students.

Partial mitigation: a meaningful slice of useful statistics is reachable **without** calculus — STAT 705 (regression) → STAT 766 (ML) and STAT 745 (visualization) form a non-calculus path covering regression, machine learning, and visualization. But statistical **inference rigor** (511, 610/611) and **optimization** (STAT 760, which needs 511) genuinely require calculus and will bunch up late. The faculty choice is explicit: (a) accept compressed year-3/4 math-statistics, (b) pull calculus earlier for DS-bound students, or (c) build the specialization preferentially on the non-calculus-reachable courses where ABET coverage allows.

---

# ABET Accreditation Mapping

ABET requires **≥45 SCH of data science coursework** covering lifecycle topics and spanning concepts, plus advanced depth, an application area, and a major project.

## Lifecycle topics

| ABET topic | Coverage | Status |
|---|---|---|
| Data acquisition & representativeness | CIS 531 (acquisition/integration); core; sampling in STAT 410 | Partial — name *representativeness/sampling bias* explicitly |
| Data management | CIS 560; CIS 260 (core foundation) | Covered |
| Data preparation & integration | CIS 531, CIS 533 (wrangling/feature engineering) | Covered |
| Data analysis | CIS 533; STAT 705/766 | A core-level notebook-analysis course has no confirmed course home (see the on-ramps note above). CIS 533/STAT 705/766 carry this on their own; no core-level notebook-analysis pass to lean on |
| Model development & deployment | STAT 766 / CIS 532 (models); deployment via CIS 400 | Covered for modeling; **deployment coverage via CIS 400 is partial** — CIS 400's confirmed deployment content (containers, hardening) doesn't include deep OS/concurrency formalization, which has no confirmed course home (see `resources/reference/spiral-threads.md`'s correction note) |
| Visualization & communication | **STAT 745** + core Human-Centered visualization throughline | Covered |

## Spanning concepts

| ABET concept | Coverage | Status |
|---|---|---|
| Data ethics, **algorithmic fairness** | CIS 533 societal aspects + core Trustworthy Computing | Partial — name *algorithmic fairness* explicitly |
| Governance (privacy, security, **stewardship**) | Core Trustworthy Computing; CIS 560 | Partial — strengthen *stewardship* |
| Applied stats/math: **inference**, modeling, linear algebra, probability, optimization | Core stats; STAT 705/713/511/610-611 (inference/modeling); MATH 551 (linear algebra); **STAT 760** (optimization) | Covered — but inference rigor is calculus-gated (year 3); sequence deliberately |
| Computing (data structures & algorithms) | Core Data Structures + Algorithmic threads | Covered strongly |

## Depth, application area, project

- **Advanced coursework:** CIS 731/733/860/864 + STAT 730/768/716/717 (graduate/upper electives).
- **Application area:** name one — **geospatial** (core geospatial theme + STAT 764), **bioinformatics** (CIS 734), or business.
- **Major project:** **CIS 561 (Data Science in Practice)** is capstone-bearing — covered.

## The 45-credit accounting

Not all of the core counts as "data science coursework." DS-counting core (~12–15) + CS-side stack (CIS 531/533/560/561 ≈ 12) + Statistics stack (STAT 705/745/760/766 ≈ 12) + math (MATH 551 + calculus-based stats ≈ 6–9) clears 45 comfortably, because the real course suite exists. Size the *required* (not merely available) courses to clear the floor.

## Bottom line

With the real course suite, Data Science is well-supported: CIS 533/531/560/561 give a CS-flavored core, Statistics supplies inference/ML/visualization/optimization depth (STAT 705/766/745/760), and CIS 561 provides the capstone. The two real issues are **the calculus-sequencing tension** (our deferral compresses the calculus-gated stats into years 3–4, unlike Statistics' calculus-first DS degree) and **coordination with the existing Statistics DS degree** (differentiate as CS-flavored, partner rather than duplicate). The remaining ABET naming gaps — representativeness, algorithmic fairness, stewardship — are targeted additions, not structural.
