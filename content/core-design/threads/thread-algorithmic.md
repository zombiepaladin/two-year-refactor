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
| **CIS 200** (Y1 Spring) — Programming Fundamentals | Big-O introduced **conceptually** as a diagnosis tool: "how does cost grow with input size?" — recognized while reading and repairing slow code (nested loops, repeated scans). Memory architecture introduced conceptually: stack vs heap, structural choices carry memory cost. No formal notation at this pass. |
| **CIS 300** (Y2 Fall) — Data and Program Structures | *Step 1:* Big-O **formalized** as the cost of structural choices — O(log n) tree operations vs O(n) unsorted scan; O(1) amortized hash table access — choosing among ADT contract-satisfying implementations. Sorting/searching as canonical examples. *Step 2:* **Design** strategies, not just measurement — divide and conquer (mergesort, binary search; recurrence relations as analysis tool, building on the recursion formalized in MATH — Recursive and Modular Computation), greedy algorithms (when local optima compose — Dijkstra previewed), an introduction to dynamic programming (memoization as the insight). *Step 3:* Design patterns applied to harder structures — shortest path/MST as explicit optimization; geospatial algorithms (road-network routing, spatial joins and nearest-neighbor/range queries using the spatial indexes from the data-structures pass). |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | Applied to query optimization — indexes, query plans, the cost of a full-table scan vs an indexed lookup. The query planner does the complexity reasoning; students read it. |
| **CIS 400** (Y2 Spring) — capstone of the core | Complexity reasoning meets a real deployed bottleneck. The memory hierarchy (cache misses, and — the dramatic case — virtual memory, paging, thrashing) can trump Big-O: good locality can beat better asymptotics. Asymptotic analysis is necessary but not sufficient. |

## Connections

- The Optimization Reasoning lens names the optimization character of the CIS 300 design-pattern/graph passes and the CIS 400 pass. CIS 400 converges with Computational Models (why slow under concurrent load).

## Open questions for faculty review

1. **CIS 300 density, confirmed acceptable (2026-07-15).** This thread now runs three consecutive escalation steps (structural-cost formalization, design-pattern strategy, graph optimization) inside one 3-credit course, on top of the Data Structures thread's own load there. User's explicit call: controlled through scaffolding and coverage depth, not by displacing content elsewhere — same flag as the Data Structures thread carries.
2. Recursion is needed informally before MATH — Recursive and Modular Computation formalizes it — confirm the CIS 300 / math sequencing stays well-aligned now that both moved off the old block calendar.

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
