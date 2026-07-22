+++
title = "Correctness & Verification"
weight = 70
ordinal = "1.2.7"
+++

> *Working draft for faculty review. A **spiral** deepens through escalating passes across the two-year core. This is the spiral; one of eight spirals (with three lenses and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** Does the code do what it's specified to do? — informal reasoning → regression → testing and verification, named and contrasted.

---

## Character

Code-correctness only. Acceptance/fitness testing lives in Human-Centered Computing; this thread answers "is it correct," that one answers "is it what they needed." Testing and verification are dual-tracked (testing checks specific cases; verification reasons about all cases). Practice precedes formal naming.

## Passes across the two years

| Course | What's new at this pass |
|---|---|
| **CIS 116** (Y1 Fall) — Introduction to Programming (embedded) | Asserts/logs to explore code; informal pre/post-condition reasoning. |
| **CIS 200** (Y1 Spring) — Programming Fundamentals | Tests for regression — verify a change didn't break prior function. Testing habits continue to be woven in at each subsequent programming-track course. |
| **CIS 300** (Y2 Fall) — Data and Program Structures | Recursion correctness (termination, base cases); contracts as pre/post-conditions made into design, tied to the ADT introduction. |
| **CIS 301** (Y2 Fall) — Logical Foundations of Programming | **Verification, formalized.** This course's confirmed purpose is deepening propositional/predicate logic into program verification — giving every student at least a brush with formal verification, and depth for interested students to pursue further. Testing and verification named and contrasted: "testing shows the presence of bugs; verification can show their absence." |
| **CIS 400** (Y2 Spring) — capstone of the core | Testing, formalized (the course's full title retains "…and Testing"), applied to deployed systems — still code-correctness; fitness lives in Human-Centered Computing. |

## Connections

- Pre/post-condition reasoning (CIS 116) becomes Boundaries & Contracts at CIS 300. Converges with Trustworthy Computing at CIS 251. At CIS 400, sits beside Human-Centered Computing's acceptance/A-B testing — correctness vs. fitness.

## Open questions for faculty review

1. None outstanding — the prior open question here ("does verification need its own credit-bearing space?") is resolved: yes, CIS 301. See `cs.md`'s CIS 301 entry.

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
