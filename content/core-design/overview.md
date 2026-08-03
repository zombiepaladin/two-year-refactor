+++
title = "Program Overview"
weight = 10
ordinal = "1.0"
+++

> *Working draft for faculty review. This is the front door to a set of 12 companion files: 8 thread files, 3 lens files, and 1 bounded-practice file. Course numbers reflect the current proposed degree map (`resources/reference/degree-maps/cs.md`), pending final department approval.*

## What this is

A competency-based, systems-thinking foundation for a B.S. in Computer Science, shared by students who will go on to specialize (Cybersecurity, Data Science, AI Systems, Software Architecture). It is built as a **spiral curriculum**: ideas recur across the two years, each return deepening or generalizing the last, rather than being taught once and left behind.

What's novel here isn't the courses — course-based structure is the familiar unit every CS faculty member already works in. What's novel is the **system underneath the courses**: a small set of threads and lenses that deliberately recur across many courses at increasing depth, and a competency model that treats those courses as evidence of program-level outcomes rather than as isolated, self-contained units. The rest of this chapter describes that system; Chapter 4 (Course Designs) describes the courses that carry it.

## The two-year core

The core spans four 16-week semesters (Years 1–2) and is **identical across every degree** — specialization happens entirely in the upper division. It combines CIS/MATH/STAT courses with K-State Core general-education requirements:

| Semester | CS/MATH/STAT courses | K-State Core / other |
|---|---|---|
| **Y1, Fall** | CIS 115 Introduction to Computing Science; CIS 116 Introduction to Programming; CIS 120 Web Foundations; MATH — Logic and Sets; MATH — Counting Finite Configurations; DEN 161 Engineering Problem Solving | ENGL 100 Expository Writing I; Communication Requirement (KSC 020) |
| **Y1, Spring** | CIS 200 Programming Fundamentals; CIS 220 Platform Programming; CIS 260 Foundations of Relational Databases; MATH — Recursive and Modular Computation; MATH — Graphs, Trees, and Maps; ECE 241 Intro to Electrical and Computer Engineering; Calculus I/II/III (KSC 030) | ENGL 200 Expository Writing II |
| **Y2, Fall** | CIS 300 Data and Program Structures; CIS 301 Logical Foundations of Programming; CIS 320 User Experience Development; CIS 225 Foundations of Computer Networks; CIS 251 Foundations of Cybersecurity; Linear Algebra (choice of MATH 350/515/551) | Natural & Physical Sciences w/ Lab (KSC 040) |
| **Y2, Spring** | CIS 141 AI/Data Science; CIS 308 C Language Laboratory; CIS 400 Object-Oriented Design, Implementation, and Testing; STAT 410 Statistics for Computing | Arts & Humanities (KSC 060); Social & Behavioral Sciences (KSC 050) |

61 credits across the two years (14/17/15/15), against a 121-credit degree total. Year 1 moves from reading and writing programs to structuring and querying data; Year 2 moves through networks, security, formal reasoning, and applied statistics, and ends at **CIS 400** — a team-based, ambiguous-requirements capstone-of-the-core built around a real historical-archive project, which validates everything the core taught before a student specializes. See `content/course-designs/` for the per-course detail (outcomes, week maps, assessments) as it's built out.

## Cross-cutting norms

Two practices don't get their own thread because confining them to one would misrepresent how they actually work: **concurrency** and **networked-computing** are paired to concept-introduction points across many courses from the very start (CIS 116 onward), rather than escalating through a single dedicated arc.

## The twelve threads

Competencies belong to the program, not to individual courses; courses are contexts in which program-level competencies are demonstrated. Twelve named threads run through the core (beyond the two cross-cutting norms above), in three kinds that mature in three different ways.

### Spirals (8) — depth increases through the topic's own escalation
1. **Data Structures & Representation** — primitive → sequence → hierarchy → relational → document; graphs spiral as a strand within (model → represent → persist → algorithms).
2. **Code Comprehension** — make it work → understand others' → organize → reason about → defend.
3. **Human-Centered Computing** — design FOR, communicate TO, validate WITH people; carries accessibility + data-visualization throughlines and owns acceptance/A-B testing (fitness-for-purpose).
4. **Algorithmic Thinking & Complexity** — theory → graph optimization → real bottleneck.
5. **Computational Models** — the landscape of ways to express computation (imperative, functional, declarative, concurrent), with failure-handling woven through as a property of each.
6. **Correctness & Verification** — informal reasoning → regression → testing and verification, contrasted. Code-correctness only ('is it correct,' vs Human-Centered Computing's 'is it what they needed').
7. **Boundaries & Contracts** — a promise at a boundary; unifies ADTs, APIs, schemas, trust boundaries, and versioning. The strongest expression of the systems-thinking ethos.
8. **Sociotechnical Structure** — systems mirror the orgs that build them (Conway's Law); the collective/team dimension (teamwork, code review as coordination, team reflection). Lands at full expression in CIS 400, the core's team-project host.

### Lenses (3) — a standing question/practice applied wherever relevant; scope grows with capability
- **Trustworthy Computing** — can people trust this system and its builders? Security, privacy, ethics; asked wherever content raises it, formalized in CIS 251 (Foundations of Cybersecurity) and revisited in-depth in CIS 415 (Ethics and Conduct for Computing Professionals).
- **Optimization Reasoning** — "best under constraints," named where it already arises; on-ramp to the AI specialization.
- **Professional Practices** — the individual craft bundle: documentation, version control, code style, code review, communication, self-reflection, estimation, continued learning.

### Bounded practice (1) — scope stays flat; only judgment deepens
- **AI-Assisted Development** — explain/discuss/quiz/critique only, never "write it for me." Deliberately does NOT grow more autonomous, to protect comprehension before the Year 3–4 Agentic AI specialization.

## The service-course model

Some courses are offered to other departments. The pattern: **we own a domain-neutral foundational unit; the partner department owns the domain-application course; together they form the visiting student's one-semester progression.**

- **CIS 260 (Foundations of Relational Databases)** — a 1-credit foundation, followed by e.g. a business data-applications course.
- **CIS 225 (Foundations of Computer Networks)** — followed by network administration (business), low-level implementation (computer engineering), etc. Physical and Data Link layers are conceptual-only; depth deferred to Computer Engineering. This bounds what we own: the shared theoretical trunk (layers 3–7 with full depth, layers 1–2 as orientation).

This bounds our development cost (no domain-specific variants) and defines a good service-course candidate: domain-neutral, foundational, recognizable, prerequisite-light.

## How to read the companion files

- **Thread files** (8) and the **bounded-practice file** (1) — the "how each idea develops" view: pass-by-pass escalation across courses.
- **Lens files** (3) — cross-cutting concerns: where each touches the curriculum and how it escalates.

A thread file names the host course at each pass; the course-design pages (Chapter 4) name the threads passing through a given course. Both views are being reconciled against the real course sequence above — see Status, below.

## Open questions — program level

These are the decisions that don't belong to any single course or thread:

1. **Thread legibility.** Twelve threads plus two cross-cutting norms is a lot for a faculty member teaching one course to hold. The threads interconnect deliberately, but the program needs a clear answer to "how does a course owner see which threads run through their course, and what each expects, without a decoder ring?" A per-course thread-tag scheme is the likely answer; not yet built.
2. **Assessment visibility for lenses.** Security, Documentation, and Optimization have no dedicated courses by design (Security now has CIS 251, but Documentation and Optimization remain lens-only); confirm faculty can see/assess that each lens was actually exercised in its host courses.
3. **Per-course density.** `cs.md` already flags specific density risks worth watching as courses are built out — CIS 115 (absorbing former computer-architecture content on top of its existing history/overview scope) and CIS 260 (holding what was previously two courses' worth of database content at 1 credit). CIS 300 carries a deliberately large share of thread content (data structures, graphs, algorithmic design patterns) by user decision — controlled through scaffolding and coverage depth rather than redistribution, but worth watching as it's built out.
4. **CS-203 (Non-Relational Databases) scope reduction.** Confirmed intentional (2026-07-15): NoSQL content no longer appears anywhere in the required core, only in the CIS 560 elective. Every CS student previously saw this; now only students who choose that elective do. Flagged here so it's visible to reviewers, not just buried in the design log.

## Status

The two-year course structure is settled (`resources/reference/degree-maps/cs.md`). This chapter is being regenerated to present that structure in course, spiral, and competency terms rather than the earlier block-based framing used during design (see `resources/design-log.md`, 2026-07-15). The thread and lens companion files are next, and — per the open question above — some of that work is genuine thread-by-thread re-derivation, not a mechanical renumbering.
