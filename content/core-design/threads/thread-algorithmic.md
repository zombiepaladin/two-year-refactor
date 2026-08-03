+++
title = "Algorithmic Thinking & Complexity"
weight = 50
ordinal = "1.2.5"
+++

> *Working draft for faculty review. A **spiral** deepens through escalating passes across the two-year core. This is the spiral; one of eight spirals (with three lenses and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** From Big-O as a diagnosis tool, to structural cost, to design patterns, to graph optimization, to a real bottleneck under load.

---

## Character

Closely shadowed by the Optimization Reasoning lens. Geospatial algorithms ride the graph pass (road-network routing is graph shortest-path). The final pass surfaces a key limit: systems reality (memory hierarchy, paging/thrashing) can invert asymptotic predictions — Big-O is necessary but not sufficient. Three consecutive escalation steps — structural-cost formalization, design-pattern strategy, and graph optimization — now land inside the same course (CIS 300) rather than three separate ones; see the density note under Open Questions.

## Passes across the two years

| Course | What's new at this pass |
|---|---|
| **CIS 116** (Y1 Fall) — Introduction to Programming | Informal seed, ahead of CIS 200's conceptual introduction: its own CSC1010 transfer SLOs require "designing and implementing basic algorithms" and "structured problem-solving techniques to decompose complex problems and develop effective, efficient solutions" — efficiency-consciousness without any formal cost language yet. |
| **CIS 200** (Y1 Spring) — Programming Fundamentals | Big-O introduced **conceptually** as a diagnosis tool: "how does cost grow with input size?" — recognized while reading and repairing slow code (nested loops, repeated scans). Memory architecture introduced conceptually: stack vs heap, structural choices carry memory cost. No formal notation at this pass. **Partially unconfirmed:** CIS 200's schedule is still TBD; its drafted SLOs support a general efficiency emphasis (SLO 6) but don't yet confirm this specific framing. |
| **CIS 300** (Y2 Fall) — Data and Program Structures | *Step 1:* Big-O **formalized** as the cost of structural choices — O(log n) tree operations vs O(n) unsorted scan; O(1) amortized hash table access — choosing among ADT contract-satisfying implementations. Sorting/searching as canonical examples. *Step 2:* **Design** strategies, not just measurement — divide and conquer (mergesort, binary search; recurrence relations as analysis tool, building on the recursion formalized in MATH — Recursive and Modular Computation), greedy algorithms (when local optima compose — Dijkstra previewed), an introduction to dynamic programming (memoization as the insight). *Step 3:* Design patterns applied to harder structures — shortest path/MST as explicit optimization; geospatial algorithms (road-network routing, spatial joins and nearest-neighbor/range queries using the spatial indexes from the data-structures pass). **Confirmed gap (2026-08-03):** the real 15-week schedule only weakly supports Steps 2-3 — "memoization" appears once (wk12, not framed as DP), "Shortest Path Algorithms" appears (wk13), but greedy algorithms, explicit dynamic programming, and geospatial algorithms are never named. Worse, the real order is backwards: mergesort/advanced sorting lands at wk15, *after* the wk13-14 graph unit, reversing this row's Step-2-before-Step-3 claim. Proposed fix (reorder sorting ahead of graphs, name greedy/DP explicitly) logged in `cis-300.md`'s "Proposed Changes" section, pending a course-designer/faculty decision. |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | Applied to query optimization — indexes, query plans, the cost of a full-table scan vs an indexed lookup. The query planner does the complexity reasoning; students read it. **Proposed addition, not yet in CIS 260's confirmed content** — its real 8-module schedule is query-writing only (SELECT/JOIN/subqueries/design), with no indexing or query-plan content. See the "Proposed Changes" section of `cis-260.md`. |
| **CIS 400** (Y2 Spring) — capstone of the core | Complexity reasoning meets a real deployed bottleneck. The memory hierarchy (cache misses, and — the dramatic case — virtual memory, paging, thrashing) can trump Big-O: good locality can beat better asymptotics. Asymptotic analysis is necessary but not sufficient. **Unconfirmed:** CIS 400's schedule is still TBD, so this pass can't yet be checked against real content. |

## Connections

- The Optimization Reasoning lens names the optimization character of the CIS 300 design-pattern/graph passes and the CIS 400 pass. CIS 400 converges with Computational Models (why slow under concurrent load).

## Open questions for faculty review

1. **CIS 300 density, confirmed acceptable (2026-07-15).** This thread now runs three consecutive escalation steps (structural-cost formalization, design-pattern strategy, graph optimization) inside one 3-credit course, on top of the Data Structures thread's own load there. User's explicit call: controlled through scaffolding and coverage depth, not by displacing content elsewhere — same flag as the Data Structures thread carries.
2. Recursion is needed informally before MATH — Recursive and Modular Computation formalizes it — confirm the CIS 300 / math sequencing stays well-aligned now that both moved off the old block calendar.
3. **CIS 300's Step 2/3 content confirmed thinner than described, and out of order (2026-08-03).** See the CIS 300 row above — real schedule doesn't name greedy algorithms, dynamic programming, or geospatial algorithms, and teaches sorting *after* graphs rather than before. Proposed reordering logged in `cis-300.md`; needs a course-designer/faculty decision, not just a wording fix, since it's a real content-sequencing change.
4. **CIS 260's query-optimization pass confirmed unbuilt (2026-08-03).** Logged as a proposed addition in `cis-260.md`'s "Proposed Changes" section — same open scope-vs-density question as the spatial-indexing and data-visualization proposals elsewhere in the core (this is a 1-credit intro-SQL course already thin on room).
5. **CIS 200 and CIS 400 passes unconfirmed, not contradicted (2026-08-03).** Both courses' schedules are still TBD. Revisit this thread once real schedules exist for either.

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
