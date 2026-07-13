+++
title = "Block 3 — Model"
weight = 30
ordinal = "1.1.3"
+++

**Year 1, Spring · Weeks 1–8 · 8-week block · 4 credits**

> *Working draft for faculty review. Course codes are placeholders. This block is one of eight; it is best read alongside the two-year arc below.*

**Two-year arc:** Read (B1) → Modify (B2) → **➤ Model (B3)** → Structure (B4) → Store (B5) → Build responsibly (B6) → Judge (B7) → Operate (B8)

---

## Purpose

**Cognitive frame:** MODEL & ABSTRACT. Modeling a domain and drawing boundaries around its parts.

**Essential question:** *How do we model a domain, and draw boundaries around its parts?*

MODEL & ABSTRACT. Cognitive frame: modeling and abstraction. OOP (encapsulation as boundary-drawing, classes as domain models) plus data structures taught CONTRACT-FIRST as abstract data types (interface before implementation). Introduces the Boundaries & Contracts thread — a promise about behavior at a boundary, independent of implementation — which names B1's informal pre/post-condition reasoning and spirals through APIs, schemas, testing, security, and versioning. Algorithmic Complexity moves to B4.

## Structure

Computer science courses (3):

| Code | Course | Cr | Focus |
|---|---|---|---|
| CS-107 | **Software Modeling and Design** | 1 | Encapsulation as boundary-drawing in Python and JavaScript; type annotations as interface specification; inheritance as one reuse mechanism (with tradeoffs); Elixir modules as a contrasting expression of encapsulation (shallow Chrysalis reading exercise). |
| CS-108 | **Computational Abstractions** | 1 | Formalizes map/filter/reduce and list comprehensions introduced informally in B1; functions as values; iterator protocol as abstraction over collection structure. |
| CS-109 | **Abstract Data Types** | 1 | Lists, linked lists, stacks, queues taught CONTRACT-FIRST: the ADT interface and its guarantees before implementation. Same-contract-multiple-implementations sets up B4 cost-based choice. Function pre/post-conditions name B1 informal verification reasoning. Graph spiral begins: graphs introduced as a MODEL for relationship-structured data (people/friendships, pages/links, task dependencies) — conceptual, no algorithms yet. Geospatial representation seed: points, lines, polygons (vector) and rasters (grids) as representation choices for spatial data. |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| MATH-103 | **Discrete Math: Recursive and Modular Computation** | 1 | (External/co-designed. Recursion arrives as ADTs/trees need it; modular arithmetic seeds B6 cryptography.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 4 credits.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Boundaries & Contracts** — INTRODUCED here. A contract = a promise about behavior at a boundary, independent of implementation. ADT contracts, class interfaces, function pre/post-conditions. Names B1's informal verification reasoning; the thread then spirals through APIs (B4), schemas (B5), testing/security (B6), defense (B7), versioning (B8).
- **Data Structures & Representation** — Linear structures taught CONTRACT-FIRST as ADTs — interface and guarantees before implementation (pass 2).
- **Code Comprehension** — Encapsulation/abstraction as correctness tools; organize so correctness is structural (pass 3).
- **Professional Practices — documentation (lens)** — Documentation-as-justification: why this structure and not that one (a new register).

## Open questions for faculty review

1. Block 3 absorbed CS-107 (Software Modeling and Design, formerly OOP I) from the Block 2 reframe. To stay at a sane load (3 CS + 1 math), Algorithmic Complexity moved out to Block 4. That move is pedagogically motivated, not just load-shedding: B3 establishes "same contract, multiple implementations," and B4's complexity analysis answers "how do we choose among them?"
2. Recursion is used informally in B3/B4 (trees, ADTs) before MATH-103 formalizes it in B5. This is "informal before formal" (acceptable, consistent with the spiral approach) but the one-to-two-block gap is worth confirming as deliberate.
3. Boundaries & Contracts being promoted to a full spiraling thread adds tracking overhead — it is the 9th spiral. It is also a meta-thread (it unifies several others). See the cross-block legibility question in the program-level notes.

---

*Spine position: **Model**. Builds on Block 2. Leads into Block 4.*
