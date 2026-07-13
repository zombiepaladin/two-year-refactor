+++
title = "Redistributing the Blocks: Plugging Course-Modules into the Degree Map"
weight = 65
ordinal = "6.7"
+++

> *Working draft for faculty review. `four-year-degree-map.md` treated each 8-week block as an atomic unit dropped into a semester. This document goes a level deeper: each of the 24 individual `CS-1xx`/`CS-2xx` courses is treated as an independent, pluggable module and matched against the real course shells (`CIS ###`) in `degree-maps/cs.md`. This is a first-pass, actionable skeleton, not a finished redesign — it identifies exactly where the block/spiral structure needs to be reworked as a consequence, and says so explicitly rather than papering over it. Course codes for the new core are placeholders; CIS/MATH/STAT numbers are real K-State courses.*

## The reframe this document works from

The block model was designed as 8 self-contained units (B1–B8), each with 3 CS courses, meant to sit one-per-two-blocks-per-semester. The real degree map (`degree-maps/cs.md`) doesn't have 8 matching slots — it has a specific, uneven set of real course numbers (`CIS 115`, `116`, `120`, `260`, `200`, `300`, `301`, `225`, `251`, `141`, `400`...) of varying credit sizes, sitting in specific semesters for reasons outside the core's control (KBOR equivalency, service-course commitments, "politically tricky" survivors like ECE 241).

So instead of asking "which semester does Block 3 go in," this document asks: **for each real course shell, which individual `CS-1xx` course(s) — by actual content, not by which block they happened to be drafted into — belong there?** The block boundaries and the "two blocks per semester" pairing are treated as provisional, not load-bearing. Some blocks' three courses stay together naturally; others don't, and this document says so.

## Method and honesty check

Blocks 1–8's courses are at very different levels of design maturity. **Block 1 (CS-101/102/103) has full weekly maps, built and cross-referenced across three sessions.** Blocks 2–8 are still working-description stubs (one paragraph each, no week-by-week map yet) — real, substantive content, but not yet decomposed to the week level. This document works at the *course* level (whole 1-credit modules), which is what's actually available for blocks 2–8; it does not attempt to split a block-2–8 course into partial weeks, since that content doesn't exist yet in enough detail to split safely.

## Container inventory: what real course shells exist in Years 1–2

| Semester | Container | Credits | Current framing (from `degree-maps/cs.md`) |
|---|---|---|---|
| Y1 S1 | CIS 115 | 1–2 | "Intro to Computing Science" — survey/history, **explicitly "up for revision/adaptation"** |
| Y1 S1 | CIS 116 | 2 | "Intro to Programming" — Python, KBOR CSC1020 equivalent |
| Y1 S1 | CIS 120 | 1 | "Web Foundations" — HTML/CSS/JS |
| Y1 S2 | CIS 260 | 1 | "Foundations of Relational Databases" — explicitly meant to "serve as a service course paired with external application courses" |
| Y1 S2 | CIS 200 | 4 (may reduce to 3) | "Programming Fundamentals" — KBOR CSC1030 equivalent |
| Y2 S1 | CIS 300 | 3 | "Data and Program Structures" — KBOR CSC1040 equivalent |
| Y2 S1 | CIS 301 | 2 | "Logical Foundations of Programming" |
| Y2 S1 | CIS 225 | 1 | "Foundations of Computer Networks" |
| Y2 S1 | CIS 251 | 1 | "Foundations of Cybersecurity" |
| Y2 S2 | CIS 141 | 1 | "AI/Data Science" |
| Y2 S2 | CIS 308 | 1 | "C Language Laboratory" — **not a content container**; language-specific, kept standalone per the prior session's decision, not part of this remapping |
| Y2 S2 | CIS 400 | 3 | "OOP Design, Implementation & Testing" |

**Total container space (excluding CIS 308, which holds no core-block content): 20–23 credits**, depending on the two open variable-credit questions (CIS 115: 1 or 2; CIS 200: 3 or 4).

## Content inventory: the 24 `CS-1xx`/`CS-2xx` courses

| Block | Course | Real content (from the actual course files, not just titles) |
|---|---|---|
| B1 | CS-101 Imperative Programming | Sequence/mutation/control-flow, Python primary + Go/C reading, GOTO→structured-programming history, H5P notional-machine (stack/heap), Go-goroutine-inspired concurrency seed + shared-memory-hazard glimpse |
| B1 | CS-102 Functional Programming | Functions-as-values, composition, immutable binding (Python discipline + JS `const`), recursion (elegance angle, same worked function as CS-101), concurrency companion pass |
| B1 | CS-103 Computational Representation | Babbage's engines (history), binary representation, 8-bit float, Boolean logic/bitwise (paired w/ MATH-101), registers/ALU, formal stack/heap+register assessment, OS-process seed. **New framing (per instruction, in its `CIS 115` container): the humanistic dimension of representation and computing's social embeddedness** — see "The CIS 115 reframe" below. |
| B2 | CS-104 Data Transformation & Manipulation | Parsing/filtering/reshaping/aggregating; CSV/JSON; data-minimization |
| B2 | CS-105 Code Reading & Repair | Code Archaeology signature assessment; debugging as data-flow tracing; git commit/revert + regression tests; Big-O introduced conceptually; memory (stack/heap) recognized while reading |
| B2 | CS-106 Web Foundations & Data-Driven Rendering | Semantic HTML/CSS (declarative model), accessibility, async/event-loop via fetch, browser-as-mini-OS framing |
| B3 | CS-107 Software Modeling and Design | Encapsulation/boundaries, OOP in Python/JS, type annotations as interface spec, exceptions as contract violations, Elixir reading (unfamiliar-paradigm) |
| B3 | CS-108 Computational Abstractions | map/filter/reduce formalized, list comprehensions, functions-as-values, iterator protocol |
| B3 | CS-109 Abstract Data Types | Lists/linked-lists/stacks/queues, contract-first (pre/post-conditions), graph-as-model seed, geospatial representation seed |
| B4 | CS-110 Trees, Hashing & Hierarchies | Trees, hash tables, graph representation (adjacency list/matrix), spatial indexing, Big-O *formalized*. **Scope addition (per instruction, in its new CIS 300 container): concurrent/thread-safe hash maps as a conceptual extension of the hashing content.** |
| B4 | CS-111 Systems & APIs | Client-server, dataflow model, web components, event-driven programming formalized |
| B4 | CS-112 Algorithmic Design Patterns | Divide-and-conquer, greedy algorithms, intro dynamic programming |
| B5 | CS-201 SQL Fundamentals | SELECT/INSERT/UPDATE/DELETE/JOIN, declarative querying, query-optimization seed — explicitly "first half of the Relational Databases service unit" |
| B5 | CS-202 Database Design | Schema design, normalization, transactions/concurrency — "second half" of the same service unit |
| B5 | CS-203 Non-Relational Databases | Document/key-value/graph stores; storage-model-as-design-decision |
| B6 | CS-204 Software Testing & Validation | Automated/unit/integration testing |
| B6 | CS-205 Security Fundamentals | Threat ID, authn/authz, applied crypto (grounded in modular arithmetic), least-privilege/least-data |
| B6 | CS-206 Collaborative Development | Collaborative git, code review, Conway's Law, Team Software Project begins |
| B7 | CS-207 Graphs & Network Algorithms | Shortest path/MST as optimization, geospatial routing (Dijkstra/A*), logic/constraint see-and-explore. **Scope addition (per instruction, in its new CIS 300 container): parallel/concurrent graph traversal (e.g., parallel BFS) as a conceptual extension of the algorithms content.** |
| B7 | CS-208 Data Integration & App-DB Interfaces | ORM, migrations, multi-storage integration, re-identification risk |
| B7 | CS-209 OSI Networking Fundamentals | Full 7-layer stack, routing as shortest-path made concrete, sockets, TLS/HTTP examined as real protocols |
| B8 | CS-210 Deployment & Operations | Performance/memory hierarchy (cache, thrashing), OS-level concurrency, actor model, fault-tolerance comparison — **the resolution of the concurrency puzzle CS-101 opened** |
| B8 | CS-211 Human-Centered Design & Validation | Requirements, UX, validation-with-users, blameless postmortem |
| B8 | CS-212 Data Analysis & Responsible AI | Notebook data analysis (culmination of stats sequence), honest visualization, AI-generated-code verification |

**24 credits of content, competing for 20–23 credits of container space.** The shortfall is real and has to go somewhere — either compression, or moving content to elective/specialization status (both explicitly permitted this session).

## Proposed mapping — Year 1 (high confidence)

| Container | Assigned course(s) | Credits | Rationale |
|---|---|---|---|
| **CIS 116** (2cr) | CS-101 + CS-102 | 2 | Both paradigms in one "Intro to Programming" course is a *stronger*, not weaker, KBOR CSC1020 equivalent — and preserves CS-101/CS-102's extensive same-week cross-referencing (paired checkpoints, shared recursive function, concurrency/immutability contrast) by literally making them one course rather than two. Lowest-risk move in this whole document. |
| **CIS 115** (resolve to 1cr) | CS-103 | 1 | CS-103 already opens with Babbage's engines — genuine computing history — plus foundational representation content. This is a stronger match for "Intro to Computing Science, survey" than the original CIS 115 draft, and resolves CIS 115's own "1 or 2 credits, to be refactored" ambiguity down to 1. **Reframed per instruction — see "The CIS 115 reframe" below**: not just history, but the humanistic/social-science dimension of computing (impacts, uses, values embedded in representation choices), seeding both Sociotechnical Structure and Human-Centered Computing here, at the earliest possible point in the sequence. |
| **CIS 120** (1cr) | CS-106 | 1 | Near-exact name match ("Web Foundations"). No semester change needed — CS-106 was already positioned as the second half of the same first-semester block pairing (B1+B2), so this isn't a resequencing, just a container assignment. |
| **CIS 260** (1cr) | CS-201 | 1 | Name match ("Foundations of Relational Databases" ↔ CS-201's own self-description as "first half of the Relational Databases service unit"). **This is the boldest move in Year 1**: it pulls CS-201 a full year earlier than its current Block-5 position. Flagged in "Spiral consequences" below — CS-202 and CS-203 (currently its Block-5 siblings) do *not* move with it. |
| **CIS 200** (shrunk to 2cr) | CS-107 + CS-108 | 2 | **Shrunk per instruction.** With CS-104 and CS-105 pulled out to the new pool (below), CIS 200 becomes a tight, near-exact match for `resources/reference/kbor-transfer/CSC1030.md` — the real KBOR course that **transfers as CIS 200**, titled "Object-Oriented Programming," with six OOP-specific outcomes. CS-107 (encapsulation, OOP, exceptions-as-contract-violations) covers outcomes 1–4 directly; CS-108's iterator protocol covers most of outcome 5. **This resolves the transfer-equivalency gap flagged in the previous version of this document** — CIS 200 no longer teaches content (data transformation, code reading) that CSC1030 doesn't cover, because that content has moved out. **Also uses APIs as a data source** (per instruction — see "APIs as a data source" above) for CS-108's exercises. |
| **CIS 301** (shrunk to 1cr, **relocated from Year 2 Semester 1**) | CS-109 | 1 | **Moved per instruction.** CS-112 (formerly CIS 301's other course) is pulled out to the pool and ultimately rejoins CS-110 in `CIS 300` (see Year 2, below) — CS-112 explicitly assumes CS-110's Big-O formalization has already happened, which rules out keeping it here. With CS-112 gone, CIS 301 shrinks to 1 credit (CS-109 alone) and moves here, restoring CS-109's original Block 3 timing (it had been delayed to Year 2 Semester 1 in earlier versions of this document). See "Spiral consequences" below for what this fixes. |

**Year 1 total assigned: CIS 115+116+120+260+200+301 = 1+2+1+1+2+1 = 8 credits**, holding 8 courses (CS-101, 102, 103, 106, 201, 107, 108, 109). Up from 7 in the previous version — CS-109 joining CIS 301 here is a net addition to Year 1 Semester 2, not a swap; CS-104/105 still move to the pool (below), which reintroduces them via a new container in this same semester.

### The CIS 115 reframe

Per instruction, CIS 115 is repositioned as more than a history-of-computing survey: **"essentially a social science course posing as a technical one."** Data representation is framed as a humanistic endeavor — how a discipline chooses to represent the things it cares about, and how that choice shapes culture — not just a technical mechanism. This is a genuine content reframe, not a relabeling, and it deliberately reuses content already in CS-103 rather than adding new material to what was already flagged as the densest Block 1 course:

- **Babbage reframed, not expanded.** CS-103 already opens with Babbage's Difference and Analytical Engines as a "representation is a design choice" hook. The humanistic reframe is nearly free: Babbage's engines existed to serve a specific social and economic need (eliminating human computational error in navigation, insurance, and engineering tables) — a technology's design reflects what a society values enough to build, and whose labor it replaces or augments. This is the seed for **Sociotechnical Structure**, riding on content already scheduled to be taught.
- **One new angle, kept light: representation as a values-laden choice.** A short treatment of encoding or classification as culturally loaded — e.g., character-encoding history (ASCII's English-centric limits versus Unicode's attempt at universality), or more simply, "what fields does a form ask for" as an early, conceptual preview of the data-minimization theme that resurfaces at CS-106, CS-205, and CS-202. Framed as a discussion/hook, not a graded unit — the same bounded-aside treatment already used for CS-101's GOTO/Dijkstra material and CS-103's own Babbage material.
- **A short, explicit orienting question for Human-Centered Computing**, not a unit: "who is this built for, and whose needs are easy to forget." CS-106 (same semester, `CIS 120`) picks this up immediately and applies it concretely (accessibility) — seed and first application land in the same term.

**Effect on the spiral picture (see "Spiral consequences" below for the full audit):** this gives Sociotechnical Structure a real, on-schedule seed for the first time — previously its first pass sat inside CS-111, now in Year 2 Semester 2, *after* the thread's own Year 2 Semester 1 "defend/retrospect" pass. Anchoring the seed at CIS 115 (Year 1 Semester 1) fixes that ordering, with one honest caveat: "retrospect on how the team organized" presumes an actual team-project experience, and CS-206's "Team Software Project begins" doesn't happen until Year 2 Semester 2. CIS 115 supplies the *conceptual* vocabulary early; whether that's enough to support a meaningful retrospective before the dedicated team-project course happens is a call for whoever designs CS-206/CS-207's actual assessments, not resolved here.

**Competency note, flagged not asserted.** CS-103 currently claims only `HCP.3` (light, representation/hiding) among the Human-Centered Practice domain competencies. Real Sociotechnical/Human-Centered seed content might justify a light secondary touch on `HCP.1` (Gather/Analyze Requirements) or `HCP.2` (Design Human-Centered Solutions) as well — worth a look, not decided here.

### APIs as a data source, in CIS 200 and CIS 300

Per instruction, both `CIS 200` (CS-107 + CS-108) and `CIS 300` (CS-110 + CS-207, see below) use **API calls as the data source for their existing exercises**, rather than static CSV/JSON files: CS-108's map/filter/reduce work operates on data fetched from an endpoint; CS-110/CS-207's structures and graph algorithms run on real-world data pulled the same way (e.g., a routes/flights API supplying the graph CS-207's shortest-path work operates on). This is a low-cost addition — a data-*source* swap for exercises that were already happening, not new conceptual content requiring dedicated class time — and it reuses a skill CS-106 already taught (`fetch`, Year 1 Semester 1) one and two semesters later, rather than introducing anything from scratch.

**This measurably improves the APIs & Networked Systems thread's sequencing** (see "Spiral consequences" below) — previously CS-209's theoretical grounding (Year 2 Semester 1) landed *before* CS-111's practical, architectural treatment (Year 2 Semester 2), reversing the intended practice-before-theory order. Now there's practical *consumption* experience at multiple points before CS-111's full build-it-yourself treatment: CIS 200 (light) → CIS 300 (richer, real structured data driving real algorithms) → CS-209 (same semester as the CIS 300 touch — theory of what's happening underneath calls students are already making) → CS-111 (architecting APIs from the build side, Year 2 Semester 2). A coherent spiral, not a workaround. It does **not**, however, fix the Computational Models or Optimization Reasoning inversions described below — those are different problems (naming the *dataflow model* as a taxonomy entry, and CS-112's optimization seed, respectively), unaffected by treating APIs as a data source.

## Proposed mapping — Year 2 (lower confidence — real tradeoffs, flagged explicitly)

| Container | Assigned course(s) | Credits | Rationale / risk |
|---|---|---|---|
| **CIS 300** (back to 3cr) | CS-110 + CS-207 + CS-112 | 3 | **CS-112 rejoins per instruction**, after passing through pool consideration (see "The pool" below) — its own content explicitly opens with "students arrive with Big-O already formalized (CS-110)," which rules out any Year 1 placement and points straight back to CS-110's own container. This restores CS-110/CS-112's *original* Block 4 pairing (same block, same order: formalize, then design patterns) rather than inventing a new relationship. Trees/hashing (CS-110), graph algorithms (CS-207), and algorithmic design patterns (CS-112) is a coherent, evidence-grounded "Data and Program Structures" container — arguably the cleanest-fitting version of this container across every round of this document. Preserves the CS-207/CS-209 same-semester convergence noted below. **CIS 300 still covers concurrent algorithms and data structures** (thread-safe/concurrent hash maps extending CS-110; parallel/concurrent graph traversal extending CS-207), and **still uses APIs as a data source** for all three courses' exercises. |
| **CIS 225** (1cr) | CS-209 | 1 | Strong name match ("Foundations of Computer Networks"). **Convergence preserved, not broken**: CS-209's routing-as-shortest-path content and CS-207's Dijkstra/A* content land in the same semester (both Year 2 Semester 1), just in different containers (CIS 225 and CIS 300) rather than the same block — the pedagogical pairing survives. |
| **CIS 251** (1cr) | CS-205 | 1 | Strong name match ("Foundations of Cybersecurity"). CS-205's applied-crypto unit depends on modular arithmetic from MATH-103 (Year 1 Semester 2 in the unchanged external-course sequence) — that dependency is satisfied regardless of which CS-course container CS-205 itself moves into, so this move is lower-risk than it first looks. |

**Year 2 Semester 1 total: 5 credits, holding 5 courses (CS-110, CS-207, CS-112 in CIS 300; CS-209 in CIS 225; CS-205 in CIS 251).** Down from 7 credits in the original degree-map sizing — CS-109 relocated to Year 1 Semester 2 (via `CIS 301`, above) and doesn't come back; CS-112 briefly left for the pool but returned. **1 credit of this semester's original size remains genuinely unclaimed** — see "Where do we have hours available" logic folded into the credit-reconciliation note below.

**Note on spacing, updated again.** CS-109's graph-as-model seed has moved out of this semester entirely (now Year 1 Semester 2, via `CIS 301`) — the three-way graph-spiral convergence flagged in earlier versions of this document is now a two-way one: CS-110 (represent) and CS-207 (algorithms) still land in the same semester and the same container, which is likely fine as an internal teaching order (represent, then immediately use in algorithms), but the gap between CS-109's now-earlier seed and CS-110's represent-pass has *widened* to a full semester (Year 1 S2 → Year 2 S1) instead of being simultaneous. That's arguably healthier spaced practice than cramming all three into one term, consistent with the design log's own comfort with "informal before formal" gaps of one-to-two blocks (see `block-3-model.md`'s open question #2). The Algorithmic Thinking & Complexity thread's formalize/design-patterns/optimization-touchpoint convergence (CS-110 + CS-112 + CS-207, all in `CIS 300` now) is unchanged from previous versions of this document — still worth the same spaced-practice check flagged earlier, unaffected by today's CS-109/CS-112 moves.

### Year 2 Semester 2

| Container | Assigned course(s) | Credits | Rationale |
|---|---|---|---|
| **CIS 141** (1cr) | CS-212 | 1 | Exact name match ("AI/Data Science" ↔ "Data Analysis & Responsible AI"). |
| **CIS 400** (back to 3cr) | CS-204 + CS-206 + CS-211 | 3 | **Reverted per instruction — CS-210 pulled out to the pool** rather than stretched in here with a forced credit-growth. CIS 400 goes back to its original size and a cleaner fit: testing, collaborative development, and human-centered validation, without the "OOP...Testing" name having to stretch over deployment/operations content it never described. |

That leaves the elective bucket **CS-202, CS-203, CS-208** (unaffected by this change) plus the new pool — **CS-104, CS-105, CS-111, CS-210** — needing an organized home, addressed below.

## Where the shortfall resolves

| Course | Move to elective? | Reasoning |
|---|---|---|
| **CS-202** Database Design | **Yes** | Displaced from CIS 300 by the CS-207 swap. Reunites with CS-203 as a coherent "database depth" pair feeding `CIS 560`/`CIS 533` in the Data Science stack, while CS-201 (SQL fundamentals) stays required in `CIS 260`. |
| **CS-203** Non-Relational Databases | **Yes** | Feeds the Data Science specialization stack; travels with CS-202. |
| **CS-208** Data Integration & App-DB Interfaces | **Yes** | ORM/migrations/multi-storage integration — advanced, specialization-adjacent content; the third member of the same cluster. |

**CS-210 is not an elective candidate — it stays required, but no longer via a stretch-fit into CIS 400.** See "The pool" below for where it actually lands.

The elective bucket is CS-202 + CS-203 + CS-208 — three closely related database/data-integration courses, unchanged by this session's pool reorganization.

## The pool: CS-104, CS-105, CS-111, CS-210

Four courses displaced from forced-fit containers, by explicit instruction rather than credit-math pressure: CS-104 and CS-105 (pulled from `CIS 200` to let it become a clean OOP match), CS-111 (pulled from `CIS 300`, where it was only ever a soft landing), and CS-210 (pulled from `CIS 400`, where it required an unconfirmed credit-growth to fit at all). **Exactly 4 credits, matching exactly the 4 credits freed by shrinking CIS 200 (−2), CIS 300 (−1), and reverting CIS 400 (−1).** The required-core credit total is unchanged overall — this is a repackaging, not a net addition or cut.

**A fifth course, CS-112, passed through this pool and left again.** It was pulled from `CIS 301` per instruction, considered for a home here, and — via the fit-and-sequencing analysis below — determined to belong back with CS-110 in `CIS 300` rather than in either new course: CS-112 explicitly requires CS-110's Big-O formalization to already be done, which both new courses' timing would have violated or made an awkward stretch. So the pool's actual membership for organizing new courses stays at four (CS-104, CS-105, CS-111, CS-210) — CS-112's brief pool status was a real step in reasoning through where it belongs, not a course this document is proposing to relocate into a new container.

### What actually clusters together

| Course | Real content | Original block timing |
|---|---|---|
| CS-104 Data Transformation & Manipulation | Parsing/filtering/reshaping/aggregating data; CSV/JSON; data-minimization | B2 — early, right after Block 1 |
| CS-105 Code Reading & Repair | Code Archaeology; debugging as data-flow tracing; git commit/revert + regression tests; Big-O conceptual seed; memory recognition | B2 — early, right after Block 1 |
| CS-111 Systems & APIs | Client-server decomposition, dataflow model, web components, event-driven programming formalized | B4 — mid-sequence, after OOP/abstractions/ADTs |
| CS-210 Deployment & Operations | Performance/memory hierarchy, OS-level concurrency, actor model, fault-tolerance comparison | B8 — the final block; deliberately the terminus of several spiral threads (concurrency, Trustworthy Computing's harden-before-live, Documentation's operational runbooks, Boundaries' semver-loop-closing) |

These four don't share one difficulty level or one moment in the sequence. **CS-104/CS-105 are early, foundational "apply what you just learned in Block 1" skills. CS-111/CS-210 are mid-to-late, systems-facing content — and CS-210 specifically needs to be *last*, because it's where multiple other spiral threads converge, not just concurrency.** That split is the basis for the recommendation below.

### Recommended: two new courses, not one

**New Course A (working title: "Data Transformation & Code Reading") — 2 credits, Year 1 Semester 2.** CS-104 + CS-105. Both are "apply Block-1 paradigm knowledge to real inputs" skills — CS-104 to data, CS-105 to code — and both were always meant to immediately follow Block 1 (their original Block 2 timing). Placed in Year 1 Semester 2 alongside the now-shrunk `CIS 200`, using exactly the 2 credits that shrink freed: Y1 S2 stays at 5 credits total (`CIS 260` 1 + `CIS 200` 2 + New Course A 2), identical to its total before any of this session's changes — fully credit-neutral within the semester.

**New Course B (working title: "Systems, APIs & Deployment") — 2 credits, Year 2 Semester 2.** CS-111 + CS-210. Rationale for pairing these two specifically, not leaving CS-111 elsewhere: there's real narrative continuity — CS-111 establishes client-server/API system structure; CS-210 deploys and operates such a system, resolving the concurrency question a networked system raises. And CS-210 has a hard constraint the other three don't: it needs to be the *last* required course in the two-year sequence, because it's the convergence point for threads well beyond concurrency. Year 2 Semester 2 is the only semester where "last" is true. This is a **net addition of 2 credits to Year 2 Semester 2** (it was not offset by a same-semester shrink the way New Course A was) — Y2 S2 goes from `CIS 141` (1) + `CIS 400` (3) = 4 credits to 6. The credit is real, not free; it comes from the 1-credit shrink `CIS 300` took in Year 2 Semester 1, so the *year* is credit-neutral even though the *semester* isn't.

### Alternatives considered, and why the two-course split is recommended over them

1. **One combined 4-credit course instead of two.** Doesn't work cleanly: CS-104/105 want Year 1 Semester 2 and CS-111/210 want Year 2 Semester 2 — a full year apart. A single course occupies one registration slot in one term (or a fixed adjacent pair, like the Statistics course's two movements in the *same* semester); it can't span a year-long gap the way two separate courses can. The Statistics-course precedent (one course, two internal movements) only works because both movements happen in the same term — this pool's natural split is much wider than that.
2. **Bundle CS-111 with CS-104/105 instead (all three early, Year 1 Semester 2), and let CS-210 find its own late slot alone.** Considered and not recommended: CS-111's content (client-server, APIs) assumes OOP and boundaries/contracts thinking that, in this remapping, CS-107 (now in `CIS 200`, same semester) is only just introducing — teaching CS-111 in the *same* term as its own conceptual prerequisite is tighter than teaching it a term later. Also would leave CS-210 as a lone 1-credit item needing its own container anyway, which doesn't save any complexity.
3. **Split CS-111 itself** (event-driven/web-component content joins CS-106 in `CIS 120`; client-server/dataflow content joins CS-210's course instead of all of CS-111 moving together). Possibly the *best* long-term fit, but it requires week-level detail that doesn't exist yet for CS-111 (still a stub) — premature per this document's own honesty check. Worth revisiting once CS-111 gets a real week-by-week design.

### What this still doesn't resolve

- **Institutional cost.** Two new course numbers is a bigger ask than the five the original `degree-maps/cs.md` draft already proposed (CIS 120/260/225/251/141) — now seven new courses total. Worth knowing that cost before committing, even though the content case for splitting is strong.
- **Sequencing detail within each new course** — which of CS-104/105 comes first, how CS-111 and CS-210 divide an 8-week-equivalent term — needs the same week-level design work the rest of Blocks 2–8 still need.
- **The four-year-degree-map.md credit reconciliation needs re-running.** Year 2 Semester 2 gains a net 2 credits under this plan; that changes the 120-credit-total math worked out there, on top of the changes already pending from the CS-207 swap and the CIS 200/CIS 300 shrinks.

## Spiral consequences — a full audit across all 13 threads

This remapping is not spiral-neutral, and the effects are bigger than any single flag can capture in isolation. This section audits all 13 threads (9 spirals, 3 lenses, 1 bounded practice) against the cumulative set of moves made this session, organized by severity — from genuine logical breaks down to things that turned out fine or improved.

### Order inversions — a later-designed pass now lands before the content it builds on

These are not spacing problems; they're cases where the sequence no longer makes narrative sense.

1. **Computational Models (flagship) — still open, not fixed by anything this session.** The taxonomy's build-up order was imperative/functional → declarative → OOP → **dataflow** → declarative-querying → logic/constraint → concurrent/OS-terminal. Under this remapping, dataflow (CS-111, now Year 2 Semester 2) lands *after* declarative-querying (CS-201, pulled to Year 1 Semester 2) and logic/constraint (CS-207, Year 2 Semester 1) — dataflow was meant to be its own distinct waypoint, and now it's crammed in beside the terminal pass instead. Treating APIs as a data source (above) doesn't fix this — that's practical consumption, not naming the dataflow model itself as a taxonomy entry. **Still needs its own fix**, most likely a CS-111/CS-201 timing swap.
2. **APIs & Networked Systems — resolved this session.** Previously CS-209's theory (Year 2 Semester 1) preceded CS-111's practical, architectural treatment (Year 2 Semester 2), reversing "practice before theory." Treating APIs as a data source in `CIS 200` and `CIS 300` (above) supplies practical consumption experience at two earlier points, so the order is now: light consumption (Y1S2) → richer consumption (Y2S1) → theory, same semester as the richer consumption (Y2S1) → full architectural build (Y2S2). Coherent, not reversed.
3. **Sociotechnical Structure — resolved, with one caveat.** Previously the thread's first pass sat inside CS-111 (now Year 2 Semester 2), *after* the thread's own Year 2 Semester 1 "defend/retrospect" pass (via CS-207's Design Review). The CIS 115 reframe (above) gives this thread a real seed at Year 1 Semester 1, fixing the ordering. Caveat: "retrospect on how the team organized" presumes an actual team-project experience, and CS-206's Team Software Project doesn't begin until Year 2 Semester 2 — CIS 115 supplies conceptual vocabulary early, which may or may not be sufficient grounding for a Year 2 Semester 1 retrospective. Flagged for whoever designs CS-206/CS-207's actual assessments.
4. **Human-Centered Computing — partially helped, not fully resolved.** The CIS 115 reframe strengthens this thread's *opening* (a real seed at Year 1 Semester 1, immediately applied by CS-106 the same semester) — a genuine improvement. But the thread's later inversion is untouched: CS-207's "defend usability choices in Design Review" (Year 2 Semester 1) still precedes CS-111's data-visualization throughline pass (Year 2 Semester 2). Same underlying cause as the Computational Models inversion (CS-111 landing late) — the same CS-111/CS-201-family fix would likely resolve this one too.
5. **Optimization Reasoning (lens) — still open, confirmed unresolved.** A hypothetical this session (moving all of `CIS 301`, including CS-112, to Year 1 Semester 2) would have softened this inversion — but CS-112 had to stay behind with CS-110 in `CIS 300` (Year 2 Semester 1) because of its own Big-O prerequisite. So CS-201's query-optimization touch (Year 1 Semester 2) still precedes CS-112's seed (Year 2 Semester 1) — reversed from the original seed-then-apply order, exactly as before. Lower stakes than the others (it's a lens, lighter-touch by design), but confirmed still open, not quietly fixed as a side effect.

**Net: two of five inversions resolved this session (APIs & Networked Systems, Sociotechnical Structure), one partially helped (Human-Centered Computing), two untouched (Computational Models, Optimization Reasoning).** The remaining ones share a common root — CS-111 landing in Year 2 Semester 2 while CS-201/CS-207/CS-209 landed in Year 1 Semester 2/Year 2 Semester 1 — and would likely respond to one shared fix rather than three separate ones.

### Elective-status losses — content that may not happen at all for general-track students

- **CS-202 (Database Design) going elective is the single most expensive individual move in this remapping** — it doesn't cost one thread, it costs **four**: Boundaries & Contracts (schema-as-contract pass), Human-Centered Computing (visualize query results), Trustworthy Computing (data minimization in schema design), and Professional Practices — version control (solo feature branching). All four passes lived in that one course. Worth weighing that multiplicative cost specifically, separate from the general "is this content specialization-flavored" judgment that made it look like a clean cut in isolation.
- **CS-203 (Non-Relational Databases) going elective** costs Data Structures & Representation its persist-pass (graph databases) — one thread, one pass.
- **CS-208 (Data Integration) going elective** costs Boundaries & Contracts (the "defend" pass, migrations-as-contract-change) and Trustworthy Computing (re-identification risk) — two threads.

**Boundaries & Contracts and Trustworthy Computing are hit twice each** by these three electives combined, on top of Boundaries & Contracts already being the "9th spiral... a meta-thread" the original design log worried would carry high tracking overhead. Of the six originally-planned Boundaries & Contracts passes (intro at B3, APIs at B4, schemas at B5, testing/security at B6, defend at B7, versioning at B8), a general-track student now gets: intro (fragmented across two semesters, below) → *no schemas pass* → testing/security (also fragmented, below) → defend (partial — the CS-207 half only, CS-208's half gone) → APIs (very delayed) → versioning (on schedule). This is the thread that's taken the most cumulative damage across every decision this session, not any single one.

### Compression — passes that were meant to be spread out, now landing in the same semester

- **Data Structures & Representation, eased by CS-109's move.** Previously three of four passes (CS-109's model-seed, CS-110's represent, CS-207's algorithms) converged in Year 2 Semester 1. With CS-109 now in Year 1 Semester 2, only two converge (CS-110's represent + CS-207's algorithms) — a real improvement, and the model-seed-to-represent gap widened to a full semester instead of zero, which is arguably healthier spaced practice (see the spacing note above).
- **Algorithmic Thinking & Complexity**: formalize (CS-110), design patterns (CS-112), and the optimization touchpoint (CS-207) all converge in Year 2 Semester 1, versus their original B4/B7 spread — unchanged by this session's CS-109/CS-112 moves, since all three still land in `CIS 300` together.
- **Boundaries & Contracts' testing/security pass still splits.** CS-205 stays Year 2 Semester 1 (`CIS 251`); CS-204 moves to Year 2 Semester 2 (`CIS 400`) — see the Block 6 note below. (Its intro-pass split is now resolved — see "What's unaffected or actually improved.")
- **Professional Practices — documentation and AI-Assisted Development** each have their second-to-last and terminal passes collapse into the same semester (Year 2 Semester 2, via CS-206 and CS-210/CS-212 respectively).
- **Block 6 quietly splits.** CS-204 and CS-206 (originally Year 2 Semester 1 alongside CS-205) both moved to `CIS 400` — which is Year 2 Semester 2. CS-205 alone stayed on Block 6's original schedule (`CIS 251`, Year 2 Semester 1). This wasn't a deliberate decision anywhere in this document — it fell out of other moves — and it's worth naming explicitly since Block 6's internal cohesion (testing and the team project reinforcing each other in the same term) is now broken by a full semester.

### What's unaffected or actually improved

- **Trustworthy Computing's surviving passes stay exactly on schedule.** CS-103 (Year 1 Sem 1), CS-106 (Year 1 Sem 1), CS-205 (Year 2 Sem 1), and CS-210 (Year 2 Sem 2, terminal) are all unchanged — only the two elective-status losses (CS-202, CS-208) touch this thread. Best-preserved thread in the whole remapping.
- **Boundaries & Contracts' intro-pass split is now resolved.** CS-107 and CS-109 were meant to introduce this thread together (ADT contracts, class interfaces, function pre/post-conditions, one coherent moment); they'd split a full year apart earlier in this document. Both now land in Year 1 Semester 2 (`CIS 200` and `CIS 301` respectively) — different containers, same semester, thread introduced as one moment again.
- **Correctness & Verification improves twice over.** CS-109's pre/post-condition reasoning sits in `CIS 301`, a container whose real catalog content is already about program correctness and proof (see the CIS 301 rationale above) — a stronger, evidence-grounded home than it had before this remapping began. And with CS-109/CIS 301 now in Year 1 Semester 2, its gap from CS-101's informal verification seed (Year 1 Semester 1) shrinks from three semesters to one, and CIS 301's real content (proof by induction) runs *concurrent* with MATH-103 (recursion/induction, also Year 1 Semester 2) instead of three semesters removed from it — tighter alignment with the actual math sequence than any previous version of this document achieved.
- **The concurrency spiral now has three touchpoints instead of two.** CS-101 (seed, Year 1) → `CIS 300`'s new concurrent-algorithms touchpoint (Year 2 Semester 1, conceptual only) → CS-210 (the actual OS-grounded fix, now in its own pool course, Year 2 Semester 2). Previously the gap between seed and resolution was the longest, highest-stakes spacing interval in the whole document; this closes it with a genuine middle beat, not just a shorter wait. CS-210 should open by recalling both the CS-101 lost-update example and the `CIS 300` touchpoint.
- **CS-207/CS-209's "routing = shortest path" convergence survives**, both landing in Year 2 Semester 1 in different containers rather than the same block.
- **CS-110/CS-112's original Block 4 pairing is restored**, not just preserved — see the `CIS 300` rationale above.

## Cleanup items surfaced along the way

- **`stat-101.md` through `stat-104.md` already exist** as block-5–8 external-course stub files (`content/course-designs/block-5/stat-101.md`, etc.), each describing one-quarter of a statistics sequence (descriptive, probability, distributions/sampling, regression). This predates the decision (this session) to consolidate statistics into a single 4-credit course with two internal movements. **These four files should be merged into the two-movement structure already described in `four-year-degree-map.md`** (Movement 1 ≈ STAT-101 + STAT-102; Movement 2 ≈ STAT-103 + STAT-104) rather than left as four separate, now-superseded stub files. Not done in this pass — flagged for whoever next touches the statistics course description.

## Credit accounting: where hours are, and where they're still unclaimed

Tallying every container against the original `degree-maps/cs.md` sizing, semester by semester:

| Semester | Original size | Current proposed size | Delta |
|---|---|---|---|
| Y1 S1 | 5 | 4 | −1 |
| Y1 S2 | 5 | 6 | +1 |
| Y2 S1 | 7 | 5 | −2 |
| Y2 S2 | 4 | 6 | +2 |
| **Total** | **21** | **21** | **0** |

The required-core total is unchanged overall — everything this document has done is a repackaging, not a net addition or cut. But **2 credits remain genuinely unclaimed**: 1 in Year 1 Semester 1 (from resolving CIS 115's "1 or 2 credits" ambiguity down to 1, with nothing filling the gap) and 1 in Year 2 Semester 1 (CS-109's original share of `CIS 301`'s size, now permanently relocated to Year 1 Semester 2 rather than replaced). Both are real slack, not yet earmarked for anything — candidates for absorbing part of a future CS-111 split (see "Alternatives considered" above) or simply left as breathing room.

## What this document does not do

- It does not re-author any block-2–8 course's week-by-week content for its new container — that content doesn't exist yet at the week level, so there's nothing to move at that resolution.
- It does not touch Years 3–4 — `four-year-degree-map.md` already addresses the upper-division "objectives shifted, electives specialization-shaped" plan, and that reasoning is unaffected by this document's Year 1–2 remapping.
- It does not re-derive exact credit-hour totals against the 120-credit target — that reconciliation lives in `four-year-degree-map.md` and should be re-run against the table above, which supersedes every earlier credit tally in this document.
- It does not resolve the Computational Models / Human-Centered Computing / Optimization Reasoning order-inversions that still trace to CS-111 landing in Year 2 Semester 2 — flagged repeatedly across this document's revisions, not yet fixed.
