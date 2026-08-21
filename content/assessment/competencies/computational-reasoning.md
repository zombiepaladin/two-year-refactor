---
title: "Computational Reasoning"
pre: "1. "
weight: 10
---

*Re-checked against real course-design pages, 2026-08-04 — see `resources/design-log.md`. Headline finding for this domain: **CIS 301 (Logical Foundations of Programming)** is a genuinely new/restructured course with no single direct predecessor, and is a strong, directly-confirmed home for formal pre/post-condition and correctness-proof evidence — see "Apply Formal Reasoning" below. This matches `content/assessment/recurring-assessments.md`'s parallel finding for the same domain.*

### Analyze Computational Systems

**I can explain the behavior of computational systems by investigating their components, interactions, and execution.**

I analyze software and computing systems to determine how they operate, identify sources of behavior, and predict outcomes under varying conditions.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 115 (Y1 Fall) | Boolean/number representation, a simplified float format, register-level state — first named encounter with how a running system works. **Note:** the memory-model and process-model content once assumed for this course was never actually incorporated — `resources/reference/degree-maps/cs.md`'s CIS 115 entry explicitly lists it as still unplaced. |
| CIS 200 (Y1 Spring) | Code Archaeology (signature) — structured investigation of unfamiliar code to explain behavior. Encapsulation/contract-boundary analysis (per course-designer's CIS 200 placement). |
| CIS 220 (Y1 Spring) | Browser as mini-OS (event loop, origin isolation, web workers, `postMessage`) — analyzing a concrete computational system. |
| CIS 300 (Y2 Fall) | Client-server dataflow; API as system structure (the "build" side of the CIS 300/CIS 320 pairing). |
| CIS 400 (Y2 Spring) | Performance analysis on a real deployed bottleneck; OS/concurrency model analysis. Confirmed against `cis-400.md`'s Confirmed Design Intent section. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Code reading — trace execution and explain behavior with guided prompts |
| Independence | Code Archaeology — unscaffolded, unfamiliar codebase, student explains without hints |
| Adaptation | Performance investigation (CIS 400) — analyze real system behavior where empirical results diverge from theory |
| Leadership | TA-led code reading sessions; mentoring peers through code archaeology in LA role |

**Recurring type:** Code Archaeology — deepens from single-module familiar code (CIS 200) through production system diagnosis (CIS 400). Also: System Analysis Task for behavior traced through operational signals rather than code.

---

### Develop Abstractions

**I can create and apply abstractions that reduce complexity while preserving essential characteristics of a problem or system.**

I organize information, processes, and system components into meaningful models that support understanding, communication, and solution development.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 116 (Y1 Fall) | Functions as values and composition — first encounter with abstraction as a mechanism. |
| CIS 200 (Y1 Spring) | Encapsulation as boundary-drawing — first time students design an interface vs. internals. Higher-order functions, iterator protocol — formalizing abstraction over behavior and traversal. |
| CIS 300 (Y2 Fall) | ADT contract-first design — the abstraction IS the contract, designed before any implementation. Confirmed against the real schedule (applications precede implementations at every pass). API as system-level abstraction across a network boundary (build side). |
| CIS 220 / CIS 320 (Y1 Spring / Y2 Fall) | Web components as encapsulated UI units — the integrate side of the same API-abstraction pairing. |
| CIS 260 (Y1 Spring) | Schema design — abstracting a messy real-world domain into a formal relational model. |
| CIS 400 (Y2 Spring) | Choosing the right abstraction for the shape of the problem (graph vs. relational vs. document) — Design Review content, re-homed here to CIS 400 (see `signature-assessments.md`). Actor-model/containers as deployment abstractions; API versioning as a compatibility abstraction (matches the confirmed "Software Versioning" topic). |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Design Brief (constrained) — design a module/ADT that hides X and exposes Y, given a contract template |
| Independence | Design Brief (open-ended) — given a problem description, design an appropriate abstraction without a template |
| Adaptation | CIS 400's team-project system-level abstraction composition — novel multi-component problem requiring the student to invent and compose abstractions. (The "System Integration Project" ceiling for this level lives at the Year 3–4 program capstone, outside the two-year core — see `signature-assessments.md` — so CIS 400 is the core's own Adaptation-level ceiling for this competency, not a stand-in for that later event.) |
| Leadership | Design Review (CIS 400) — defending abstraction choices under peer and faculty scrutiny; TA mentoring in design sessions |

**Recurring type:** Design Brief — deepens from single-component interface design (CIS 200) through system-level abstraction composition (CIS 400). Also generates evidence for Design Software Systems and Design Human-Centered Solutions.

---

### Apply Formal Reasoning

**I can use logical, mathematical, and formal methods to analyze computational problems and justify conclusions.**

I construct and evaluate arguments, proofs, and formal representations to reason about the correctness and behavior of computational systems.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| MATH Logic and Sets (Y1 Fall) | Propositional/predicate logic, formal proof, set operations. |
| CIS 115 (Y1 Fall) | Boolean logic as applied counterpart — truth tables, bitwise operations applied to computation. |
| MATH Counting Finite Configurations (Y1 Fall) | Combinatorial reasoning — formal counting as precursor to algorithmic analysis. |
| MATH Recursive and Modular Computation (Y2 Fall) | Recursive structures, modular arithmetic — formal reasoning about computation's mathematical substrate. |
| **CIS 301** (Y2 Fall) — Logical Foundations of Programming | Pre/post-conditions and loop invariants; recursive correctness argument by induction. **Re-homed here to CIS 301** — directly confirmed against its real schedule (pre/post-conditions, loop invariants, function specifications, proof by induction/contradiction), a stronger match than CIS 300 ever was for this specific claim. |
| CIS 300 (Y2 Fall) | Big-O analysis — constructing and comparing asymptotic bounds as formal argument. |
| MATH Graphs, Trees, and Maps (Y1 Spring) | Graph theory — formal proofs about graph properties. |
| CIS 400 (Y2 Spring), formalized (woven throughout CIS 116/200/300) | Testing as formal verification; property-based testing; test suite as formal specification. |
| CIS 300 (Y2 Fall) | Algorithm correctness arguments for graph algorithms. **The old "constraint/logic model (Prolog-style)" claim is confirmed absent** from CIS 301's real drafted content (pure formal-logic/proof/verification, no Prolog or constraint-solver material) — already flagged as an open question in `thread-computational-models.md`, restated here rather than re-invented. |
| CIS 400 (Y2 Spring) | Formal + empirical reconciliation — construct the argument for why Big-O prediction diverges from observed behavior. Confirmed against the Confirmed Design Intent section. |

Note: MATH and STAT courses feed Crystalis evidence directly via LTI — formal reasoning demonstrated in the mathematics sequence counts as competency evidence.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured formal analysis — construct a truth table, analyze complexity of a given algorithm, write pre/post-conditions from a template |
| Independence | Unscaffolded formal analysis — specify pre/post-conditions for a novel function (CIS 301), analyze an unseen algorithm's correctness and complexity without hints |
| Adaptation | Formal + empirical reconciliation (CIS 400) — apply formal reasoning where the textbook model breaks down; construct the argument for why it breaks down |
| Leadership | TA/LA leading algorithm analysis or proof sessions; formal critique in Design Review (CIS 400) — evaluating whether a peer's formal argument actually holds |

**Recurring type:** Formal Analysis — deepens from structured logic exercises (Y1 Fall) through formal + empirical reconciliation on a production system (CIS 400).

---

### Evaluate Algorithmic Solutions

**I can evaluate alternative algorithms and representations by analyzing their correctness, performance, and tradeoffs.**

I select and justify computational approaches using theoretical and empirical evidence appropriate to the problem context.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 300 (Y2 Fall) | Same contract, multiple implementations — seeds the idea that valid alternatives exist with different tradeoff profiles. Adjacency list vs. matrix — choosing the right graph representation for a problem. Big-O comparison of sorting/searching; selecting among implementations satisfying the same ADT contract. |
| CIS 260 (Y1 Spring) | Index choice and query optimization (still a proposed, undrafted addition — see `cis-260.md`'s "Proposed Changes"); schema design tradeoffs; relational vs. graph model selection. |
| CIS 300 (Y2 Fall) | Dijkstra vs. A\*, BFS vs. DFS, Kruskal vs. Prim — multiple algorithms for the same problem with different applicability conditions. |
| CIS 400 (Y2 Spring) | Design Review — defend algorithm and data model choices to peers and faculty. Re-homed here to CIS 400, per `signature-assessments.md`. |
| CIS 400 (Y2 Spring) | Production bottleneck — evaluate algorithm choices where formal analysis and empirical behavior diverge; concurrency model selection. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured comparison — given two algorithms/representations, analyze complexity and identify which is better for a specified scenario |
| Independence | Open-ended justification — given a problem, select and defend an algorithm/data model choice without a comparison template |
| Adaptation | Design Review (CIS 400) — defend choices to peers and faculty in a novel system context; production bottleneck evaluation (CIS 400) where formal analysis alone is insufficient |
| Leadership | Leading Design Review critique sessions as TA/LA — evaluating whether a peer's justification argument is complete and sound |

**Recurring type:** Algorithm Evaluation Task — deepens from single-structure comparison (CIS 300) through production system evaluation with formal + empirical evidence (CIS 400). Also generates evidence for Represent Information.
