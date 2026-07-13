+++
title = "Block 4 — Structure"
weight = 40
ordinal = "1.1.4"
+++

**Year 1, Spring · Weeks 9–16 · 8-week block · 3 credits**

> *Working draft for faculty review. Course codes are placeholders. This block is one of eight; it is best read alongside the two-year arc below.*

**Two-year arc:** Read (B1) → Modify (B2) → Model (B3) → **➤ Structure (B4)** → Store (B5) → Build responsibly (B6) → Judge (B7) → Operate (B8)

---

## Purpose

**Cognitive frame:** STRUCTURE across scales. The same idea — parts and relationships — in data, systems, networks, and the humans who build them.

**Essential question:** *How does structure work — in data, systems, networks, and the humans who build them?*

STRUCTURE across scales. Cognitive frame: structure/representation as one idea (parts + relationships) at every scale — data (trees/hashing), systems (client-server/APIs), networks, and humans (Conway's Law seeds the Sociotechnical thread). Algorithmic Complexity arrives as the COST of structural choices — how to choose among contract-satisfying implementations (clean handoff from B3). Data visualization is embedded (HCI throughline), not a course. Persistence-proper moves to B5; file formats appear only as representation. End-of-Year-1 checkpoint / transfer point.

## Structure

Computer science courses (3):

| Code | Course | Cr | Focus |
|---|---|---|---|
| CS-110 | **Trees, Hashing & Hierarchies** | 1 | Hierarchical and associative structure (Data Structures spiral). Taught as structure; ADT contracts from B3 continue (a tree/map has a contract too). Graph spiral: representing and building graphs (adjacency list/matrix — the adjacency matrix is also a natural seed for basic linear algebra), basic traversal. Spatial indexing as applied trees/hashing: quadtrees and R-trees (trees), geohashing (spatial hashing) — a real-world application that makes the structures concrete. |
| CS-111 | **Systems & APIs** | 1 | Client-server decomposition; the API as system structure across a network boundary (APIs spiral + Boundaries network-boundary pass). Conway Law seed links system structure to human/org structure (Sociotechnical thread). Dataflow model named (Computational Models): a web-server request flows through a pipeline of stages (parse to auth to route to handle to serialize to respond). Data visualization embedded here (Human-Centered Computing throughline), not a separate course; D3 data-join and method-chaining as the client-side dataflow counterpart. **Component-based GUI architecture (web components):** custom elements, shadow DOM, and slots as the "structure" applied to user interfaces — a reusable boundary unit whose name is its contract, shadow DOM is its encapsulated internals, and slots are its interface. Event-driven programming formalized as a structural pattern (register → dispatch → handle in queue), deepening the event-loop first named in B2. |
| CS-112 | **Algorithmic Design Patterns** | 1 | Students arrive with Big-O already formalized (CS-110); this course teaches how to design fast algorithms. Three canonical strategies: divide and conquer (mergesort, binary search; recurrence relations as the analysis tool — builds on MATH-103 B3 recursion); greedy algorithms (when local optima compose to global optimum; Dijkstra previewed as motivation for B7); introduction to dynamic programming (overlapping subproblems, memoization as the insight). Optimization lens: algorithmic design as optimization — making a hard problem tractable by exploiting its structure. |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| MATH-104 | **Discrete Math: Graphs, Trees, and Networks** | 1 | (External/co-designed. Concurrent with CS-110's first graph pass — provides formal graph theory as students begin representing and traversing graphs in this block.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 3 credits.

> **End-of-Year-1 checkpoint.** A student exiting after this block has completed a coherent foundation (read → modify → model → structure) plus the Kansas transfer-aligned core. This is a real, defensible exit/transfer point worth formalizing.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Data Structures & Representation** — Trees, hashing, hierarchies — hierarchical/associative structure (pass 3).
- **APIs & Networked Systems** — Build + consume an API; system structure across a network boundary (pass 2).
- **Boundaries & Contracts** — The boundary becomes a process/network boundary; an API is a contract (pass 2).
- **Algorithmic Thinking & Complexity** — Two passes here: CS-110 formalizes Big-O as the cost of structural choices (students arrive with the concept from CS-105 B2); CS-112 extends to algorithmic design (divide and conquer, greedy, intro DP) — the vocabulary CS-207 assumes (passes 2 and 3).
- **Sociotechnical Structure** — SEEDED here via Conway's Law — systems mirror the organizations that build them; links system structure to human structure (pass 1). Spirals to B6 (team forms), B7 (defend), B8 (postmortem).
- **Human-Centered Computing** — SVG data visualization — honest visual representation of data; the data-viz throughline (pass 2). Embedded, not a separate course.
- **Computational Models** — Server-side concurrency, conceptual (pass 3).

## Open questions for faculty review

1. Data visualization is now an embedded HCI throughline, not a standalone course — it appears woven into Trees or Systems & APIs. Confirm faculty can see/assess it without a dedicated course slot.
2. Persistence-proper moved to Block 5; only file formats (as representation) remain in Year 1. An exiting student at the Year-1 checkpoint has files/CSV/JSON from B2 transformation work but no databases — acceptable, since databases were always Year 2.
3. Containers (deployment structure) are foreshadowed here via the Boundaries thread but belong properly to Block 8.

---

*Spine position: **Structure**. Builds on Block 3. Leads into Block 5.*
