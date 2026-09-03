+++
title = "The Spiral Method"
weight = 10
ordinal = "3.1"
+++

> *Working draft for faculty review. This page describes the pedagogical principles behind the curriculum's spiral structure. For the course-by-course expression of those principles, see the thread files in Chapter 1 (Core Design) and the course pages in Chapter 4 (Course Designs).*

## What a spiral curriculum is — and isn't

A spiral curriculum is one in which ideas **recur** — not as review, but as return. Each time a concept appears, the context is richer, the student's tools are sharper, and the encounter goes deeper. The alternative is coverage: teach a topic once, test it, and move on. Coverage is efficient but brittle; the spiral is slower but builds genuine understanding.

This two-year core is organized as a spiral. Twelve named threads (plus two cross-cutting norms) run across the four-semester course sequence. No thread appears only once. The earliest pass at any thread is deliberately incomplete — sufficient for the current course's work, insufficient for what comes later. The later pass is not a re-explanation of what the student already heard; it is a genuine new encounter with the same idea, from a vantage point that didn't exist before.

Four design principles shape how the spiral works here.

---

## Principle 1: Practice precedes formal naming

Students encounter ideas through use before those ideas are formally named and analyzed. This is deliberate and consequential.

In CIS 116, students use `git log`, `git diff`, and `git blame` to understand a codebase they didn't write. They are not told "this is version control" or "version control serves the following purposes." They use a tool, observe its behavior, and build intuition. By CIS 200, when they use `git commit` and `git revert` as safety nets while repairing code, they have operational experience to ground the concept.

The same pattern holds throughout:

| Idea | First practical encounter | Formal naming |
|---|---|---|
| Version control | CIS 116 — git as a history-reading tool | CIS 200 — commit/revert as a safety net for change |
| Correctness reasoning | CIS 116 — asserts and logs to explore behavior | CIS 200 — regression tests; CIS 300 — pre/post-condition reasoning as ADT contracts |
| Event-driven execution | CIS 220 — the browser's event loop, encountered concretely | CIS 300 / CIS 320 — dataflow/pipeline structure named as a general pattern |
| Privacy and data minimization | CIS 200 — "why are we asking for this?" in form fields | CIS 251 — data minimization as a design principle with a name and an ABET anchor |

The pattern is not accidental. When formal naming follows practice, students already have an experience to attach the concept to. When naming precedes practice, students memorize a definition that has no grip.

---

## Principle 2: Ideas return through genuine generalization, not harder repetition

The spiral would fail if each return were simply a harder version of the same thing. "Here is sorting again, but now with larger arrays" is not a spiral — it is repetition with harder parameters. A genuine spiral return is a **generalization**: the new encounter shows that the old concept was a special case of something larger.

The Data Structures & Representation thread is the clearest example, and also the clearest place where the new course sequence introduces a real tension worth naming honestly:

| Course | What's new | Why it's a generalization |
|---|---|---|
| CIS 115 (Y1 Fall) | Bits, booleans, integers | The most primitive representation |
| CIS 260 (Y1 Spring) | Relational data | A generalization of hierarchical data — but taught *before* the hierarchical/ADT material below, not after |
| CIS 300 (Y2 Fall) | Lists, stacks, queues, trees, hashing, graphs, as ADTs | Each a further generalization (a sequence generalizes a single value; a tree generalizes a sequence; a graph generalizes a tree) |

**Open tension, not resolved here:** the logical generalization order (primitive → linear → hierarchical → relational → graph) no longer matches the taught order. CIS 260 (relational) now falls a full year before CIS 300 (linear/hierarchical/graph), because the real course sequence places databases in Y1 Spring and data structures in Y2 Fall. The generalization *logic* still holds — relational data is still a generalization of hierarchical data — but a student won't experience it as a clean escalation in the order this table's logic implies. This should be named explicitly to faculty rather than narrated as if the old clean ordering survived the move from blocks to real courses; whether to reorder the courses or simply re-teach the generalization framing at whichever point it's actually needed is a decision for `course-designer`.

This principle applies to every thread with varying cleanliness. Code Comprehension moves from "make it work" (CIS 116) to "understand others' code" (CIS 200) to "reason formally about correctness" (CIS 301) to "defend it" (CIS 400) without the same ordering problem, because its course sequence already runs chronologically forward. Computational Models moves from "two paradigms exist" (CIS 116) to "more models, and failure looks different in each" (CIS 120/200/260/300) to a still-unconfirmed formal capstone — see the Computational Models thread's own open questions.

---

## Principle 3: Threads are designed to converge

Twelve threads and two norms running independently would produce fragmentation, not coherence. The spiral's threads are designed to **meet** at certain points — places where independently developed ideas formalize together and reinforce each other. These convergence points are the strongest evidence that the design is integrated rather than assembled.

**CIS 116** is the first convergence: several "reading tools" arrive together — git history, asserts/logs, documentation, and the AI-explainer bounded practice — all feeding into CIS 200's Code Archaeology assessment the following semester.

**The old "Build Responsibly" convergence is now two courses, not one.** In the block design, testing, collaboration, team-facing documentation, and errors-as-attack-surface (cybersecurity) all formalized together in a single block. In the real course sequence, that convergence has split: **CIS 251** (Y2 Fall) formalizes cybersecurity and trust; **CIS 400** (Y2 Spring, the following semester) formalizes testing, collaboration, and team accountability. This is a real structural change, not just a renaming — the "responsible development" idea is now a two-course arc spanning a semester, rather than a single simultaneous convergence. Worth confirming this is acceptable pacing rather than a diluted version of the original intent.
**CIS 400** is the terminal convergence for the core: real-bottleneck performance, hardening, versioning, and (per the confirmed course design) deployment/operations all land together as the core's final pass. The full team-level **blameless postmortem**, however, is now placed at the **Year 3–4 program capstone**, not inside the core — see the Sociotechnical Structure thread. Deep concurrency/OS formalization's landing point is unconfirmed (see the Computational Models thread's open questions) — it may or may not still converge here.

---

## Principle 4: The spiral is a transfer design

The cognitive science rationale for a spiral curriculum is **transfer**: the ability to apply a learned idea in a novel context. Transfer is how learning becomes capability, and it is notoriously hard to teach directly. The spiral is an indirect route to transfer — by encountering the same idea in multiple, structurally different contexts, students develop representations that are not tied to any single context, and can therefore be applied in new ones.

In this curriculum:

- Git appears first as a history-reading tool (CIS 116), then as a safety net (CIS 200), then seeded conceptually around system structure (CIS 300/320), then as a full collaboration/contribution workflow (CIS 400). A student who has used git in all four contexts does not have a "git skill" — they have a model of version control that they can apply in any context, including ones not encountered in the curriculum.

/ Boundary and contract thinking appears in schema design (CIS 260), ADT interfaces and API design (CIS 300/220/320), formal verification (CIS 301), trust boundaries (CIS 251), and secure-by-design (CIS 400). As with Principle 2's tension, this list is in a defensible thematic order but not a clean chronological one — CIS 260's schema-as-contract pass comes before CIS 300's ADT-contract pass, the reverse of the old block ordering. The point still lands (by CIS 400, "what is the contract at this boundary?" is a question a student has asked and answered in several different forms) but faculty should know the path there isn't a straight line through the calendar.
**The transfer/exit checkpoint** at the end of Year 1 is a structural expression of this principle. A student who exits after two semesters (CIS 115/116/120/200/220/260 plus the math sequence) has a coherent, if narrower, foundation — not complete, but transferable. Year 2 continues and deepens the same foundation; it does not unlock it.

---

## What the spiral is not

The spiral is not the same as "everything is connected." Not all threads converge, not all ideas return with equal depth, and not all courses are equally dense. The design makes deliberate choices about what recurs and what does not. The Optimization lens, for example, is named where it arises organically (CIS 300's algorithmic work, CIS 400's deployment work) rather than being forced into every course. The spiral disciplines those choices — an idea recurs when the recurrence is a genuine generalization; it does not recur to produce the appearance of connection.

The spiral is also not an excuse for incompleteness. The first pass at a thread must be sufficient for the work of that course, not merely a teaser for the later pass. Each pass must stand on its own within its course, while preparing the ground for the next.

## Open questions for faculty review

1. **The generalization-order tension (Principle 2, Principle 4)** is the most consequential finding of this rewrite: the real course sequence doesn't preserve the old block design's clean escalation order for at least two threads (Data Structures & Representation, Boundaries & Contracts), because CIS 260 (databases, Y1 Spring) now precedes CIS 300/301 (data structures, formal logic — Y2 Fall). This needs a real decision, not just documentation: reorder the courses, or accept the chronology and re-derive the pedagogical narrative to fit it.
2. Whether the "Build Responsibly" convergence being split across CIS 251 and CIS 400 (a semester apart) is acceptable pacing, or whether it needs tighter coupling.
