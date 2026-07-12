+++
title = "Computational Models"
weight = 60
ordinal = "1.2.6"
+++

> *Working draft for faculty review. A **spiral** deepens through escalating passes across blocks. This is the flagship spiral; one of nine spirals (with three lenses and one bounded practice — 13 threads total).*

**In one line:** The landscape of ways to express computation — imperative, functional, declarative, concurrent — with 'how does each model handle failure' woven through.

---

## Character

FLAGSHIP. Reframed so the spine is the TAXONOMY of models rather than control flow (which it had drifted into). Error-handling is now a cross-cutting PROPERTY of each model, not the spine. Genuinely uncommon undergraduate content — most programs teach imperative + try/catch as the only model and never surface declarative, dataflow, logic/constraint, or actor models. The model taxonomy: imperative, functional, declarative (markup/query/logic-constraint), concurrent/reactive, and dataflow (data flowing through transformation stages). A message-queue/event-loop through-line unifies the concurrent/reactive/actor family — met concretely in the browser (B2), generalized to OS message passing and actor mailboxes (B8).

## Passes across the two years

| Block | Host context | What's new at this pass |
|---|---|---|
| B1 (Y1 Fall) | CS-101/102 / CS-103 | IMPERATIVE (steps that change state) & FUNCTIONAL (composition of transformations), now with RECURSION given two explicit angles on the same worked function (CS-101: what it does to the call stack; CS-102: what it lets you express, no mutable accumulator). Errors as ordinary (read a stack trace). Two complementary execution-model seeds land in the same block: CS-103 gives the FORMAL/OS-level view (a running program is a PROCESS the OS schedules, single-threaded for now); CS-101 gives a CONCRETE/experiential seed via an H5P widget (a melody becomes an ordered sequence of commands, then several independent voices run "at once" with nothing shared between them) — a lightweight, Go-goroutine-inspired notion of concurrency, deliberately WITHOUT shared mutable state. **Updated:** CS-101 now also poses (without resolving) a bounded, surface-level glimpse of the shared-state HAZARD itself — a hand-traced example of a shared counter losing an update — and CS-102's functional immutability is used, same week, as the paired contrast: the hazard can't happen there by construction. Locks/semaphores and other actual fixes remain deferred to B8. Both execution-model seeds, and now the hazard/fix arc, are reconciled formally at B8 (cooperative/green threads vs. OS-scheduled/preemptive threads and processes; actual synchronization; the actor/message-passing alternative). |
| B2 (Y1 Fall) | CS-106 / CS-104 | DECLARATIVE introduced (HTML/CSS: state what, not how) + CONCURRENT/REACTIVE (async/event-loop). DATAFLOW seeded: transformation pipelines (parse → filter → reshape) as proto-dataflow. The event loop processes a QUEUE of callbacks/events — first encounter with message-queue mechanics; the browser as a MINI-OS (scheduling, origin isolation, workers, postMessage) is a concrete on-ramp to the OS concepts at B8. Failure looks different across models. |
| B3 (Y1 Spring) | CS-107 Software Modeling and Design / CS-108 Computational Abstractions | OOP as a named model (CS-107); exceptions introduced as the mechanism for signaling boundary/contract violations (try/catch named, CS-107); map/filter/reduce and functional patterns formalized (CS-108). |
| B4 (Y1 Spring) | CS-111 Systems & APIs | DATAFLOW named: web-server request pipelines (parse → auth → route → handle → serialize → respond) and D3 data-join/method-chaining (client-side) — computation as data flowing through stages. Network failures/timeouts — errors you don't control. |
| B5 (Y2 Fall) | CS-201 SQL | DECLARATIVE QUERYING (SQL = the same 'state what, not how' idea as HTML, now for data). Transactional rollback (a failure model). |
| B7 (Y2 Spring) | CS-207 (light) | LOGIC & CONSTRAINT models — see and explore a small example (a few Prolog-style facts/rules + a query, or a small constraint problem a solver resolves). |
| B8 (Y2 Spring) | CS-210 Deployment & Operations | OS grounding makes the concurrent-model choice meaningful: processes vs threads (shared vs isolated memory), preemptive (OS threads) vs cooperative (green threads) scheduling, and MESSAGE QUEUES / IPC — generalizing the B2 browser event loop (the browser was a mini-OS all along). **Should explicitly resolve B1's shared-counter puzzle:** the actual synchronization fixes (locks/semaphores, at whatever depth already planned) close the loop CS-101 deliberately left open a year earlier — recommend opening this pass with a recall of the B1 lost-update example rather than introducing shared-state hazards cold. Actor mailboxes ARE message queues, tying the actor model to its substrate — the actor/message-passing model is the architectural alternative that avoids the hazard a different way than locks do (no shared memory at all, vs. shared memory made safe). The ACTOR MODEL named explicitly (Erlang/OTP). Fault-tolerance compared: try/catch vs actor/supervision vs circuit-breaker. (Without the process/thread grounding, these are vocabulary, not a reasoned choice.) |

## Connections

- Declarative passes (HTML B2, SQL B5) connect to Boundaries & Contracts (a contract is declarative about behavior). Logic/constraint (B7) connects to Trustworthy Computing's predicate logic and the Optimization lens. The concurrent models (B8) rest on programmer-facing OS grounding (processes, threads, scheduling) seeded at B1 — both the formal OS-process seed (CS-103) and the concrete goroutine-inspired independent-sequences seed (CS-101's music widget) — this also supplies the ABET operating-systems exposure. B8 converges with Algorithmic Thinking (slow under load) and Sociotechnical (blameless postmortem).

## Open questions for faculty review

1. The logic/constraint example (B7) and actor naming (B8) are small new content — confirm they fit at conceptual/see-and-explore depth in 1-credit courses.
2. The CS-101 goroutine-inspired concurrency seed (H5P music widget, see-and-explore depth) — confirm it fits within B1's already-flagged density without displacing existing content. See `resources/design-log.md`'s 2026-07-09 entries for the language-stack reconciliation and, in the follow-on 2026-07-12 session, the addition of a bounded shared-memory-hazard glimpse and CS-102's firmly-adopted companion pass.
3. **New (2026-07-12):** with CS-101 now posing the shared-counter hazard explicitly (rather than only deferring shared state entirely), confirm B8 (CS-210) is scoped to explicitly recall and resolve it — see the revised B8 row above. If B8's existing plan doesn't already include an explicit "here's the fix to the puzzle you saw a year ago" framing, that's a small but worthwhile addition to make the year-long gap pay off deliberately rather than land as a cold restart.

---

*For how this lands in a specific block, see that block's review file.*
