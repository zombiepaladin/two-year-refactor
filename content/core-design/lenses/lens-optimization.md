+++
title = "Optimization Reasoning"
weight = 20
ordinal = "1.3.2"
+++

> *Working draft for faculty review. A **lens** is a standing question or practice applied across the two-year core, scope growing with capability — not a topic taught in one place. One of three lenses (with eight spirals and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** "Best under constraints," named wherever it already arises, so students reach the AI specialization already thinking in optimization terms.

---

## Why this is a lens, not a spiral

A lightweight lens, not a new spiral, because "find the best X under constraints" already occurs organically at several points — it needs naming, not new content. Mathematical optimization proper (gradient descent, convex methods) is deferred to the specialization; the foundation seeds the reasoning pattern.

## Where it touches the curriculum

Each touch is woven into the host course — not separately credit-bearing. Touches escalate across the two years.

| Course | The standing question / practice |
|---|---|
| **CIS 300** (Y2 Fall) — Data and Program Structures | Seed: choosing among implementations of the same contract is optimization — optimize for which operation (lookup vs. insertion vs. memory)? **Confirmed** against the real course (SLOs 2/3/6). |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | Query optimization — indexes, query plans. Light. **Proposed, not yet built** — the course's real 8-module schedule is query-writing only; logged in `cis-260.md`'s "Proposed Changes." |
| **CIS 300**, continued | Strongest organic point: shortest path *is* optimization. (MST is not currently named anywhere in the course's real schedule/SLOs — softened from an earlier MST-specific claim.) Also note: the course's real Week 15 sorting content currently comes *after* the Week 13-14 graph unit, reversing this escalation's intended divide-and-conquer-before-graph-optimization order — see `cis-300.md`'s "Proposed Changes" (reordering proposal, shared with the Algorithmic Thinking & Complexity thread). |
| **CIS 220 / CIS 320** (Y1 Spring / Y2 Fall) | Multi-objective tradeoff reasoning — integrating multiple sources for speed vs. completeness vs. privacy, at the structural-boundary depth those courses now own. **Proposed, not yet built, and with no confirmed course to carry it** — the confirmed real content for this pairing is a single-API client/server boundary (event loop/security isolation on CIS 220's side; component UI consuming one provided service layer on CIS 320's side), not multi-source integration. Logged in both `cis-220.md`'s and `cis-320.md`'s "Proposed Changes"; needs a course-designer/faculty decision on whether the multi-source scenario returns here or the lens is rescoped to the confirmed single-API-boundary content. |
| **CIS 400** (Y2 Spring) — capstone of the core | Applied: performance optimization of a real deployed system against a real bottleneck. Long-confirmed design intent, now written into `cis-400.md`'s "Confirmed Design Intent" section — not yet drafted into a real schedule. |

## Convergences with other threads

- Rides the Algorithmic Thinking & Complexity spiral closely (CIS 300 → CIS 400).
- The multi-objective tradeoff pass converges with CIS 400's integration/judgment work.
- Connects to the logic/constraint example in Computational Models — constraint satisfaction is optimization-adjacent.
- Forward link: on-ramp to the AI specialization's optimization requirement.

## Open questions for faculty review

1. The lightest lens — confirm these touchpoints suffice as specialization preparation.
2. Mathematical optimization deliberately deferred — confirm the foundation needs only the reasoning pattern.
3. **Re-checked against fleshed-out course-design pages, 2026-08-04.** Two of five touchpoints (CIS 260 query optimization; CIS 220/CIS 320 multi-objective tradeoff) are proposed, not yet built. The CIS 220/CIS 320 item specifically traces to a retired pre-refactor course design and needs a real decision, not just drafting — see its row above and `cis-220.md`/`cis-320.md`'s "Proposed Changes."

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
