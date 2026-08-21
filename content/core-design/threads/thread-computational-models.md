+++
title = "Computational Models"
weight = 60
ordinal = "1.2.6"
+++

> *Working draft for faculty review. A **spiral** deepens through escalating passes across the two-year core. This is the flagship spiral; one of eight spirals (with three lenses and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** The landscape of ways to express computation — imperative, functional, declarative, dataflow, logic/constraint — with 'how does each model handle failure' woven through.

---

## Character

FLAGSHIP. The spine is the TAXONOMY of models, not control flow. Error-handling is a cross-cutting property of each model, not the spine. Genuinely uncommon undergraduate content — most programs teach imperative + try/catch as the only model and never surface declarative, dataflow, or logic/constraint models.

**Refactored 2026-07-15: concurrency content moved out.** This thread previously carried a full concurrency arc of its own (goroutine-inspired seeds, event-loop mechanics, OS process/thread formalization, the actor model). That's now owned by the **`concurrency` cross-cutting norm** (see the Program Overview) instead of duplicated here — concurrency is paired to concept-introduction points across many courses from day one, not confined to a handful of passes inside this one thread. This is a de-duplication, not a content cut: nothing about the ABET operating-systems/parallel-computing exposure was lost in the move, because `cs.md`'s own coverage-check work already anchors that exposure independently (CIS 220's browser-as-mini-OS framing for OS, CIS 200/300's woven-in parallel-processing content for parallel/distributed) — see the Correctness & Verification and norm documentation for the current anchor, not this thread.

## Passes across the two years

| Course | What's new at this pass |
|---|---|
| **CIS 116** (Y1 Fall) — Introduction to Programming | IMPERATIVE (steps that change state) & FUNCTIONAL (composition of transformations), using the same widgets carried forward from the original design, with RECURSION given two explicit angles on the same worked function (call-stack effects vs. what it lets you express without a mutable accumulator). Errors as ordinary (read a stack trace). Some of this introduction may shift to CIS 115 — not yet decided which pieces (see `resources/design-log.md`, 2026-07-15). |
| **CIS 120** (Y1 Fall) — Web Foundations | DECLARATIVE introduced: HTML/CSS states *what*, not *how*. |
| **CIS 200** (Y1 Spring) — Programming Fundamentals | DATAFLOW seeded: transformation pipelines (parse → filter → reshape) as proto-dataflow. OOP named as a model, with exceptions (try/catch) introduced as the mechanism for signaling boundary/contract violations. Map/filter/reduce and functional patterns formalized — explicitly as a comparison point against the course's OOP focus, reflecting that the languages actually taught blend all three paradigms. |
| **CIS 300 / CIS 320** (Y2 Fall) | DATAFLOW named at system scale: CIS 300's server-side request pipeline (parse → auth → route → handle → serialize → respond) and CIS 320's client-side data-join/method-chaining pattern — computation as data flowing through stages, now across a network boundary rather than within one program. **Not visible in either course's drafted page (2026-08-03), confirmed intentional:** the client/server vehicle is program-specific project scaffolding, not a catalog-facing outcome, so `cis-300.md`'s description/schedule don't spell it out the way a generic syllabus wouldn't — noted in its "Proposed Changes" section so the omission reads as deliberate. CIS 320 has no drafted schedule yet to check against. |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | DECLARATIVE QUERYING: SQL is the same "state what, not how" idea as HTML, now for data. Transactional rollback as a failure model. **Rollback content is a proposed addition, not yet in CIS 260's confirmed content** — see the "Proposed Changes" section of `cis-260.md`. |
| **CIS 301** (Y2 Fall) — Logical Foundations of Programming *(placement not yet confirmed — see below)* | LOGIC & CONSTRAINT models — see-and-explore depth (a few Prolog-style facts/rules and a query, or a small constraint problem a solver resolves). **Confirmed absent from the real course (2026-08-03):** CIS 301's drafted content is purely formal logic/proof/verification (propositional/predicate logic, induction, program-correctness proofs) — no Prolog or constraint-solver material anywhere. Strengthens, doesn't change, open question #1 below. |
| **CIS 400** (Y2 Spring) — capstone of the core | EVENT-DRIVEN / DATAFLOW revisited at project scale: "Event-based programming" is a confirmed topic in CIS 400's course-design page, alongside its OOP/testing focus — a capstone-level return to the dataflow/event model in the context of a real, non-trivial project rather than a single-course exercise. |

## Connections

- Declarative passes (CIS 120, CIS 260) connect to Boundaries & Contracts (a contract is declarative about behavior). Logic/constraint connects to Trustworthy Computing's predicate logic and the Optimization lens.

## Open questions for faculty review

1. **Logic/constraint placement in CIS 301 is soft, not confirmed — and confirmed absent from the real course (2026-08-03).** `cs.md`'s own CIS 301 entry flags this as unresolved: whether to introduce logic programming (Prolog-style) as real practiced instruction, keep it at the lighter "see and explore" touch, or whether Prolog belongs in the core's language stack at all. CIS 301's actual drafted content contains no logic-programming or constraint-solver material at all, which is consistent with "not yet decided" but means the row above is aspirational, not built. Don't read the table row above as settled.
2. **Deep OS/concurrency formalization's new home is unconfirmed.** A final pass covering process/thread formalization, preemptive vs. cooperative scheduling, the actor model, and fault-tolerance comparison doesn't have a clear successor course. CIS 220 now carries the required ABET OS-*exposure* anchor at a lighter level ("browser as mini-OS"), and CIS 400 absorbed general deployment/operations content — but whether the deeper theoretical generalization (processes vs. threads, actor model) still gets taught anywhere, or was intentionally narrowed to CIS 220's exposure-level treatment, hasn't been decided. Flag for `course-designer` when CIS 400 and the Systems Elective are actually built out.
3. Confirm the original interactive widgets this thread relies on carry over into CIS 116 without displacing existing content there, given CIS 116 is also the confirmed landing point for the thread's own competency-assessment artifacts (see the design log, 2026-07-15).

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
