+++
title = "Block 7 — Exercise Judgement"
weight = 70
ordinal = "1.1.7"
+++

**Year 2, Spring · Weeks 1–8 · 8-week block · 3 credits**

> *Working draft for faculty review. Course codes are placeholders. This block is one of eight; it is best read alongside the two-year arc below.*

**Two-year arc:** Read (B1) → Modify (B2) → Model (B3) → Structure (B4) → Store (B5) → Build responsibly (B6) → **➤ Judge (B7)** → Operate (B8)

---

## Purpose

**Cognitive frame:** INTEGRATION & JUDGMENT — design under uncertainty. The first block where problems lack a single right answer.

**Essential question:** *When problems stop having a single right answer, how do you decide — and defend it?*

Integration & Judgment — design under uncertainty. Graphs (arbitrary connection), multi-source data integration, and the application-database interface (ORMs, migrations, seeds): the first block where problems lack single right answers. The Design Review signature assessment is where students defend structures, contracts, team organization, usability, and tradeoffs under scrutiny — tradeoff reasoning (competing objectives, e.g. speed vs completeness vs privacy) named explicitly. Lighter load than B6 by design.

## Structure

Computer science courses (3):

| Code | Course | Cr | Focus |
|---|---|---|---|
| CS-207 | **Graphs & Network Algorithms** | 1 | Graph traversal, shortest path, minimum spanning trees — named explicitly as optimization (best path/structure under a metric). Graphs as the most general representation (terminal Data Structures pass). Geospatial algorithms: routing/shortest-path on road networks (weighted graphs; Dijkstra, A* as geospatially-motivated heuristic search); spatial joins and range/nearest-neighbor queries using B4 spatial indexes. Signature assessment: Design Review begins here. Computational Models pass: a brief see-and-explore example of a LOGIC/CONSTRAINT model (a few Prolog-style facts/rules + a query, or a small constraint problem a solver resolves) — connects to MATH-101 predicate logic, SQL's logical character, and the Optimization lens. |
| CS-208 | **Data Integration & Application-Database Interfaces** | 1 | Combining data across the storage models and APIs students already know (B5 relational and non-relational, B4 APIs) — the challenge is integration, not model introduction. ORM libraries: mapping between application objects and database schemas; the object-relational impedance mismatch; active record vs. data mapper patterns; the N+1 query problem as a canonical judgment case for when raw SQL beats an ORM. Database migrations: versioned schema evolution; forward and rollback; data migrations vs. schema migrations; a migration is a contract change with downstream effects (Boundaries pass). Seeds: initial data population and test fixtures; environment-specific seeding strategies. Re-identification risk from combined datasets (Trustworthy Computing lens pass). Multi-objective tradeoff reasoning — integrating for speed vs. completeness vs. privacy — defended in Design Review. |
| CS-209 | **OSI Networking Fundamentals** | 1 | The OSI 7-layer model as a shared theoretical trunk. Physical and Data Link layers introduced conceptually only (signals, framing, MAC addresses, ARP) — depth deferred to CompE. Network layer: IP addressing, CIDR subnets, routing — routing IS the shortest-path problem on a graph, making CS-207's Dijkstra/A* concrete at the network layer (deliberate same-block convergence). Transport layer: TCP (three-way handshake, reliability, flow control) vs UDP (best-effort, latency trade-off); ports; the socket abstraction as the programmer's interface to the stack — the same interface students have been using in API work (B4/CS-111) without the theory. Session/Presentation: brief — TLS sits here, connecting to CS-205 applied cryptography. Application layer: HTTP/HTTPS and DNS examined as protocols rather than magic — what students have been consuming since B2. APIs & Networked Systems thread: theoretical grounding for the whole spiral. Boundaries & Contracts: each OSI layer is a contract with its neighbors; encapsulation as a design principle at every scale. |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| STAT-103 | **Random Variables, Distributions & Sampling** | 1 | (External/co-designed, stats dept. Distributions, sampling, central limit theorem.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 4 credits.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Data Structures & Representation** — Graphs as the most general representation (arbitrary relationship); the terminal data-structures pass.
- **Algorithmic Thinking & Complexity / Optimization** — Shortest path and minimum spanning trees named explicitly as optimization — the strongest organic optimization touchpoint (pass 2).
- **APIs & Networked Systems** — OSI Networking Fundamentals provides the theoretical grounding for the whole spiral; the socket, TCP, and HTTP that students have been using since B2 are named and located in the stack (pass 3).
- **Boundaries & Contracts** — Defend the boundaries and contracts you designed; migrations as versioned contract evolution — changing a schema is changing a contract with downstream effects; ORM as an object-relational contract (pass 5).
- **Sociotechnical Structure** — Defend/retrospect how the team organized to produce the work (pass 3).
- **Human-Centered Computing** — Defend usability and accessibility choices in Design Review (pass 3).
- **Trustworthy Computing (lens)** — Re-identification risk from combined datasets — a specific, real privacy question (not a generic touch).
- **Correctness & Verification** — Both applied to harder cases (graphs).

## Open questions for faculty review

1. Block 7 was already coherent in the original architecture — unlike Blocks 2/3/4 it needed naming, not reorganization. Confirm the "design under uncertainty" framing is the intended emphasis (it is the first place professional judgment, not determinate problem-solving, dominates — central to the graduate archetype).
2. Multi-objective tradeoff reasoning (speed vs completeness vs privacy) is named explicitly here and sets up the AI degree's optimization needs. Confirm this is the right home for it.
3. Lighter than Block 6 by design — a deliberate cadence (intense B6 → judgment-focused B7).

---

*Spine position: **Judge**. Builds on Block 6. Leads into Block 8.*
