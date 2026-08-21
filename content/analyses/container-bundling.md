+++
title = "Administrative Container Bundling Analysis"
weight = 50
ordinal = "6.5"
+++

> *Working draft for faculty review. Examines the costs and benefits of grouping the 24 proposed 1-credit, 8-week CS courses into semester-length "administrative containers" for enrollment and transcript purposes, while preserving the internal 8-week block structure. Identifies recommended bundlings, prerequisite chain implications, required restructuring, and alignment with Kansas Board of Regents (KBOR) statewide transfer course outcomes. Course codes are placeholders.*

## The problem containers solve

The proposed core contains 24 CS courses, each carrying 1 credit and spanning 8 weeks. From a pedagogical standpoint this is a deliberate choice: 1-credit modules allow tighter competency targeting, sharper assessment, and a spiral revisit structure that 3-credit courses would make administratively cumbersome. From an administrative standpoint, 24 separate course records per student create friction at every interface: the university workload policy (calibrated for 3-credit courses), degree-audit systems, transcript legibility, and transfer articulation with other institutions.

An **administrative container** addresses this without changing the pedagogy: the 8-week courses remain exactly what they are, but for enrollment and transcript purposes they are grouped into a single semester-length course entry. The registrar sees a 3-credit (or 2-credit) course; internally, students and faculty work through the same two or three 8-week modules they would have otherwise.

---

## Cost-benefit analysis

### Benefits

**1. Workload accounting.** The K-State faculty workload policy (FHXY) benchmarks teaching load in section credit hours, calibrated for 3-credit courses. A faculty member teaching two 3-credit containers per semester earns 6 SCH/semester = 12 SCH/year, the standard 40%-teaching benchmark. Under the unbundled 1-credit structure, the same faculty member teaching six 1-credit courses earns the same 6 SCH but with six distinct course records, six syllabi, and six sets of preparation — none of which the SCH metric captures. Containers allow workload negotiations to be grounded in recognizable units.

**2. Preparation burden recognition.** A 3-credit container spanning three 8-week modules is legitimately one course preparation in the administrative sense: one syllabus, one grade record, one ABET mapping. This matters for annual reviews and merit cases, where "taught two courses" reads very differently from "taught six courses."

**3. Transfer articulation.** KBOR statewide transfer course outcomes are defined at the 3-credit level (CSC1020, CSC1030, CSC1040, CSC1050). Containers sized and scoped to align with these allow straightforward equivalency rulings. Twenty-four 1-credit courses require 24 individual articulation decisions at every community college in Kansas; eight 3-credit containers require eight.

**4. Transcript legibility.** Eight course entries over two years is the norm for a structured CS curriculum. Twenty-four entries covering the same content raises questions from graduate admissions offices and employers unfamiliar with the design.

**5. Degree audit simplicity.** Fewer catalog entries reduce the surface area for audit errors and advising exceptions.

### Costs

**1. Loss of CBE granularity.** In a competency-based model, each 1-credit course is a distinct checkpoint: a student demonstrates mastery, earns the credit, and moves on. Bundling three courses into a single 3-credit container means the container grade is an aggregate — a student who masters two of three modules still passes or fails the container as a whole. Internal competency tracking must compensate for what the administrative record no longer shows.

**2. Within-semester sequencing complexity.** Each semester contains two sequential blocks (weeks 1–8 and weeks 9–16). Bundling each block into a separate container creates a within-semester prerequisite: Container 1 must be completed before Container 2 can begin, even though both are registered in the same semester. Most university registration systems do not natively support mid-semester prerequisite enforcement. This requires registrar accommodation (see below).

**3. Partial-credit transfer complexity.** A transfer student with credit for CSC1030 (OOP) but not CSC1020 (Programming Fundamentals) still needs Container 2 ("Data, Code & the Web"), which has no KBOR equivalent. The container structure does not eliminate the need for advising judgment on non-standard transfer paths — it just makes the standard paths cleaner.

**4. Grade aggregation.** One container grade represents three distinct learning experiences. If a student excels in two modules but struggles sharply in one, the container grade must reflect this coherently. Assessment design within each container needs to weight modules appropriately and make failure conditions explicit.

---

## Prerequisite chain and within-semester sequencing

The block structure imposes a strict linear prerequisite chain:

```
Block 1 → Block 2 → Block 3 → Block 4 → Block 5 → Block 6 → Block 7 → Block 8
```

Across semesters, this is a normal prerequisite chain — each semester's containers require the prior semester's containers as prerequisites. The challenge is *within* each semester, where two blocks run sequentially:

| Semester | Weeks 1–8 | Weeks 9–16 |
|---|---|---|
| Year 1 Fall | Block 1 (Container 1) | Block 2 (Container 2) |
| Year 1 Spring | Block 3 (Container 3) | Block 4 (Container 4) |
| Year 2 Fall | Block 5 (Container 5) | Block 6 (Container 6) |
| Year 2 Spring | Block 7 (Container 7) | Block 8 (Container 8) |

A student registers for both semester containers at enrollment time, but Container 2 cannot begin until Container 1 is complete. Three administrative mechanisms can handle this, in order of preference:

**Option A — 8-week part-of-term enrollment (recommended).** K-State supports part-of-term registration for courses that do not span the full 16-week semester. Registering Container 1 as a "Part A" (weeks 1–8) course and Container 2 as a "Part B" (weeks 9–16) course resolves the prerequisite problem entirely: Container 1 is formally complete and graded before Container 2 begins enrollment. This is the cleanest path and the one most community colleges and online programs already use for accelerated formats.

**Option B — Co-enrollment with conditional release.** Students register for both containers at the semester start. Container 2 carries a "permission of instructor required" flag for the first eight weeks; the department releases students into active Container 2 participation after Container 1 concludes. This is administratively possible but requires manual coordination each semester.

**Option C — Single 6-credit semester course.** Bundle both blocks into one 6-credit course per semester. This eliminates the within-semester sequencing problem and gives each semester a single grade record. The cost is unusual credit-hour packaging (6-credit courses are rare outside of labs or studios) and loss of per-block transfer articulation granularity.

**Recommendation:** Pursue Option A. K-State's Center for the Future of Learning has existing infrastructure for this format. It is the only option that preserves a clean per-block prerequisite record while avoiding manual coordination overhead.

---

## Proposed container structure

The 24 CS courses group into 9 containers across 4 semesters. Most blocks bundle as straightforward 3-credit containers. Block 4 is the exception: the recommended KBOR alignment for CSC1040 is best served by a **2-credit + 1-credit split** within that block (see restructuring recommendation below).

| Container | Block | Courses | Credits | Proposed title | KBOR alignment |
|---|---|---|---|---|---|
| **C1** | 1 | CS-101, CS-102, CS-103 | 3 | Programming Fundamentals | CSC1020 — strong |
| **C2** | 2 | CS-104, CS-105, CS-106 | 3 | Data, Code & the Web | None |
| **C3** | 3 | CS-107, CS-108, CS-109 | 3 | Object-Oriented Programming | CSC1030 — strong |
| **C4a** | 4 | CS-110, CS-112† | 2 | Data Structures & Algorithms | CSC1040 — strong (with restructuring) |
| **C4b** | 4 | CS-111 | 1 | Systems & APIs | None |
| **C5** | 5 | CS-201, CS-202, CS-203 | 3 | Database Foundations | None |
| **C6** | 6 | CS-204, CS-205, CS-206 | 3 | Responsible Software Development | None |
| **C7** | 7 | CS-207, CS-208, CS-209 | 3 | Advanced Structures & Networks | None |
| **C8** | 8 | CS-210, CS-211, CS-212 | 3 | Software Engineering Practice | None |

† CS-112 requires restructuring; see below. Total CS credits: **24**.

The within-semester prerequisite chain expressed as container dependencies:

```
C1 (Part A, Sem 1) → C2 (Part B, Sem 1) → C3 (Part A, Sem 2) → C4a/C4b (Part B, Sem 2)
  → C5 (Part A, Sem 3) → C6 (Part B, Sem 3) → C7 (Part A, Sem 4) → C8 (Part B, Sem 4)
```

C4a and C4b are co-requisites within the same 8-week block; neither has a prerequisite on the other.

---

## Restructuring recommendation: Block 4 and CSC1040 alignment

### The problem

CSC1040 (Data Structures) requires coverage of graphs and graph algorithms (Dijkstra's, greedy, sorting/searching on graphs). In the current design, graphs appear in Block 7 as CS-207 "Graphs & Network Algorithms." This is too late for a clean CSC1040 equivalency: a student transferring in with CSC1040 credit would need to skip Container 4 but still take Container 7 for graph content that CSC1040 already covered — an awkward gap.

### The restructuring

Move **basic graph representation and traversal** from CS-207 (Block 7) into Block 4. Specifically:

**CS-112 — rename from "Algorithmic Design Patterns" to "Algorithmic Thinking & Graphs."** Add: graph representation (adjacency matrix, adjacency list), BFS and DFS traversal, basic pathfinding, and graph as a data structure. This completes the data-structures thread (linear → hierarchical → hash-mapped → arbitrarily connected) within Block 4, and aligns Block 4 with the full scope of CSC1040.

**CS-207 — retain as "Advanced Graph Algorithms."** The course keeps its network algorithm depth — Dijkstra's algorithm, minimum spanning trees, network flow — but now frames this as a *return to graphs* at a higher level of sophistication, an explicitly designed spiral pass. This is stronger pedagogy than the current design, which introduces graphs at full complexity in a single exposure. The redesign log entry for the data-structures spiral explicitly notes that each pass should "apply it in a harder/messier context than before" — an early BFS/DFS pass in Block 4 followed by an advanced algorithms pass in Block 7 is exactly this pattern.

### Why the split C4a / C4b

CS-111 (Systems & APIs) has no CSC1040 analog — it covers file systems, OS abstraction, and API consumption, content that is genuinely distinct from data structures. Bundling CS-111 into C4 with CS-110 and CS-112 would dilute the CSC1040 equivalency claim. Separating it as a 1-credit standalone (C4b) keeps the C4a equivalency clean and honestly represents what CSC1040 does and does not cover.

Students in the normal track take C4a and C4b concurrently within the Block 4 8-week period, so the split creates no scheduling burden for them. The split only matters for the transfer case.

---

## KBOR transfer alignment

### CSC1020 — Programming Fundamentals → Container 1 (3 credits)

**Match quality: strong.** C1 covers all seven CSC1020 outcomes:

| CSC1020 outcome | Coverage in C1 |
|---|---|
| Variables, data types, control structures, functions, arrays | CS-101 (imperative programming, state/mutation, lists) |
| Design and implement basic algorithms; write/test/debug | CS-101, CS-103 |
| Conditional statements and loops | CS-101 |
| Functions for modularity, reusability, abstraction | CS-101; extended in CS-102 (functional decomposition) |
| User input/output, file I/O | CS-101, CS-104 (note: file I/O lands primarily in Block 2) |
| Fundamental data structures: arrays, lists | CS-101, CS-103 |
| Structured problem decomposition | CS-101, CS-102, CS-103 |

C1 adds content beyond CSC1020: the functional programming paradigm (CS-102) and low-level computational representation — binary, Boolean algebra, encoding (CS-103). These additions strengthen the course and do not conflict with CSC1020's outcomes. File I/O is lightly covered in Block 1 and deepened in Block 2; this minor gap is defensible given that C1 otherwise fully satisfies CSC1020.

**Transfer ruling:** Accept CSC1020 as satisfying C1.

### CSC1030 — Object-Oriented Programming → Container 3 (3 credits)

**Match quality: strong.** C3 covers all six CSC1030 outcomes:

| CSC1030 outcome | Coverage in C3 |
|---|---|
| OOP principles: subclasses, encapsulation, inheritance, abstraction | CS-107, CS-108 |
| Error handling and exception handling | CS-107, CS-108 |
| Differences between imperative and OOP paradigms | CS-101 (imperative, in C1) + CS-107/CS-108 (OOP) |
| Class design, implementation, and testing to meet behavioral requirements | CS-107 |
| Collection classes and iterators | CS-109 (Abstract Data Types) |
| Structured problem decomposition via OOP | CS-107, CS-108, CS-109 |

C3 requires C1 and C2 as prerequisites, which ensures students arrive with the imperative programming background CSC1030 assumes. The comparison between paradigms (CSC1030 outcome 3) is made explicit by the spiral structure: students revisit programming paradigms they first encountered in CS-101 and CS-102, now in an OOP context.

**Transfer ruling:** Accept CSC1030 as satisfying C3. Students transferring with CSC1030 but not CSC1020 must complete C1 and C2 before enrolling in C4 onward.

### CSC1040 — Data Structures → Container 4a (2 credits, with restructuring)

**Match quality: strong after restructuring; partial without it.**

| CSC1040 outcome | Coverage in C4a |
|---|---|
| Implement data structures: strings, lists, arrays, linked lists, stacks, queues, trees, sets, hash tables, heaps, graphs | CS-109 (ADTs — linear structures) in C3; CS-110 (trees, hashing) in C4a; CS-112† (graphs, basic) in C4a |
| Select appropriate structures for real-world problems; explain performance implications | CS-110, CS-112† |
| Implement searching, sorting, manipulation algorithms | CS-112† (design patterns + graph traversal) |
| Analyze algorithmic complexity and performance differences | CS-108 (complexity introduced), CS-110, CS-112† |
| Advanced OOP concepts: generics, interfaces, indexers, enumerators | CS-108 (Computational Abstractions), CS-109 |

† Requires restructuring of CS-112 as described above.

The linked list, stack, and queue content from CSC1040 sits in CS-109 (C3). This creates a mapping where CSC1040 credit maps across C3 *and* C4a — a student with CSC1040 transfer credit has covered content that spans two containers. The recommended handling is:

**Transfer ruling:** Accept CSC1040 as satisfying C4a (2 credits). Accept it as *co-satisfying* the Abstract Data Types portion of C3 (CS-109 content), but require the student to complete the OOP and modeling content of C3 (CS-107 and CS-108) unless they also hold CSC1030 credit. In practice, students who hold both CSC1030 and CSC1040 satisfy all of C3 and C4a and can enter C4b (Systems & APIs, 1 credit) and C5 directly.

C4b (CS-111, Systems & APIs) has no CSC1040 coverage. Students with CSC1040 credit must still complete C4b.

### CSC1050 — Intro to Digital Logic Design

**Match quality: partial.** CSC1050's outcomes 1–4 (Boolean expressions, truth tables, binary/decimal conversion, simple arithmetic circuits) are covered by CS-103 (Computational Representation) within C1. The remaining five outcomes (K-maps, flip-flops, FSMs, HDL, FPGAs) have no analog in the proposed software-focused core.

Forcing a full-course equivalency between CSC1050 and C1 would misrepresent what C1 teaches (programming paradigms and software-level representation) and what CSC1050 teaches (hardware design and digital logic). The intellectual foundations overlap at the binary/Boolean layer, but the curricula diverge immediately above it.

**Transfer ruling:** Accept CSC1050 as satisfying the CS-103 component of C1. Students with CSC1050 credit must complete CS-101 (Imperative Programming) and CS-102 (Functional Programming) — either through the full C1 container or through challenge/placement mechanisms — before proceeding to C2. Alternatively, treat CSC1050 as a CS technical elective that satisfies an upper-division elective requirement outside the core. The latter path avoids the awkward partial-container split and more honestly reflects CSC1050's hardware orientation.

---

## Summary of transfer acceptance rulings

| KBOR course | Satisfies | Condition |
|---|---|---|
| CSC1020 Programming Fundamentals | C1 (3 credits) | None |
| CSC1030 Object-Oriented Programming | C3 (3 credits) | Must have C1 + C2 or equivalent before proceeding to C4 |
| CSC1040 Data Structures | C4a (2 credits) + CS-109 content in C3 | Must complete C3 OOP content (CS-107, CS-108) if not holding CSC1030; must complete C4b (1 credit) regardless |
| CSC1050 Digital Logic Design | CS elective (recommended) | Core entry still requires completion of C1 content; consider placement exam for CS-101/CS-102 |

A student arriving with CSC1020 + CSC1030 + CSC1040 credit enters at **C4b → C5**, having satisfied C1, C3, and C4a. They must still complete C2 (Data, Code & the Web) and C4b (Systems & APIs), as neither has a KBOR equivalent, and then proceed normally through C5–C8.

---

## Recommendations

1. **Adopt per-block 3-credit containers (with the Block 4 exception) as the default administrative structure.** This minimizes catalog complexity while enabling clean KBOR articulation at all four alignment points.

2. **Pursue 8-week part-of-term enrollment (Option A) to resolve the within-semester sequencing problem.** This is the only mechanism that creates a clean prerequisite record without manual coordination overhead. Coordinate with the Registrar before the first offering.

3. **Restructure CS-112 and CS-207 as described.** Moving basic graph content to Block 4 both strengthens the CSC1040 transfer alignment and improves the spiral pedagogy by creating a deliberate two-pass treatment of graphs. This is the only structural content change required by this analysis; all other bundling decisions are administrative.

4. **Publish explicit transfer equivalency rulings before the program's first enrollment.** Students transferring from Kansas community colleges will ask about CSC1020/1030/1040 equivalencies before applying. Uncertainty here delays enrollment decisions. File the equivalency determinations with the Registrar's articulation database as part of program approval.

5. **Build CBE competency tracking outside the container grade record.** The container grade is a summary. Individual module completion, competency checkpoints, and spiral-pass records should live in the LMS or a parallel tracking system so advisors can see which 8-week experiences a student has and has not mastered, regardless of what the transcript shows.
