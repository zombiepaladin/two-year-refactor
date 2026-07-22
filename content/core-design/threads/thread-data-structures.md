+++
title = "Data Structures & Representation"
weight = 10
ordinal = "1.2.1"
+++

> *Working draft for faculty review. A **spiral** deepens through escalating passes across the two-year core. This is the spiral; one of eight spirals (with three lenses and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** From the most primitive representation to the most general, each pass a genuine generalization — with graphs spiraling as a strand within.

---

## Character

The strongest spiral in the design. Each pass is a real generalization, not a harder repeat. After the ADT pass it is taught contract-first (interface before implementation), which lets the next pass ask "how do we choose among implementations of the same contract?" Graphs are a deliberate sub-spiral inside this thread (model → represent + theory → algorithms) rather than a single terminal pass. Geospatial data rides the thread as an applied representation sub-theme (vector/raster representation → spatial indexing via trees/hashing), which also deepens the GIS service relationship.

## Passes across the two years

| Course | What's new at this pass |
|---|---|
| **CIS 115** (Y1 Fall) — Introduction to Computing Science | Bits, booleans, numbers — the most primitive representation. Carries the former Computational Representation content (binary, Boolean logic, a simplified float format, register-level state). |
| **CIS 300** (Y2 Fall) — Data and Program Structures | Linear structures (lists, stacks, queues) as ADTs — contract first, implementation hidden. Hierarchical/associative structure (trees, hashing). Graph sub-spiral begins: graphs as a model for relationship-structured data, then representing and building them (adjacency list/matrix — the matrix also seeds basic linear algebra), basic traversal. Spatial indexing as applied trees/hashing: quadtrees, R-trees, geohashing. This is a dense pass — see the density note below. |
| **MATH — Graphs, Trees, and Maps** (Y1 Spring) | Formal graph theory (graphs, trees, networks), positioned the semester before CIS 300's hands-on graph work — a deliberate theory-then-practice sequence, not concurrent as originally planned. |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | Relational data as a formal, queryable model. |
| **CIS 300** (Y2 Fall), continued | Graph sub-spiral capstone: graph algorithms (shortest path, MST), landing on the representation and traversal work earlier in the same course. |

## Open questions for faculty review

1. **CIS 300 density, confirmed acceptable (2026-07-15).** This thread's ADT, hierarchical-structure, and full graph sub-spiral (model → represent → algorithms) all land in one 3-credit course, alongside algorithmic design patterns (see the Algorithmic Thinking & Complexity thread). User's explicit call: controlled through scaffolding and coverage depth, not by displacing content elsewhere — flagged for the later credit-optimization pass, same treatment as CIS 115/260's existing density flags.
2. **Document/NoSQL representation no longer closes the loop for every student.** The original design closed this thread with a required touch on document/NoSQL representation ("when the relational model doesn't fit"). That content (formerly CS-203, Non-Relational Databases) has no home in the required core — confirmed 2026-07-15 that this is an intentional scope reduction, not an oversight (see `resources/design-log.md`). It now lives only in the CIS 560 elective. This thread's escalation is genuinely narrower for students who don't take that elective: relational is the terminal formal model they see. Flag for the competency/ABET mapping pass if "exposure to multiple data models" was assumed as universal coverage anywhere.
3. **Graph-database touch (Neo4j) — still an open placement question, not yet a course-designer decision.** A brief graph-database touch, alongside the CIS 300 graph algorithms pass, was proposed as small additional content. Given CIS 260 is already flagged as dense and this doesn't have a confirmed course host, treat as unplaced rather than assumed-covered.
4. Confirm contract-first ADT teaching is acceptable as the thread's style.

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
