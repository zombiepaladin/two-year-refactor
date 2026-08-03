+++
title = "Recurring Developmental Experiences"
weight = 20
ordinal = "3.2"
+++

> *Working draft for faculty review. This page describes the experiential cycle that grows across the two years. For the real systems that serve as its substrate, see [Signature Applications](./signature-applications) in this chapter.*

## The premise: systems-level thinking before programming skill

Traditional CS instruction begins with programming skill: write a loop, write a function, write a class. The ability to read and reason about existing code — to navigate a large unfamiliar codebase, diagnose where something is wrong, and extend it without breaking what works — is treated as an advanced skill developed later, after programming foundations are established.

This curriculum inverts that priority.

Reading and reasoning about existing systems is not an advanced skill that emerges after programming. It is a foundational skill that programming skill can only partially substitute. A student who can write code from scratch but cannot read others' code is not prepared for professional practice — in an era of large open-source codebases, AI-generated code, and million-line legacy systems, the ability to understand what already exists is more economically valuable than the ability to produce new code from a blank page.

More importantly, engaging with large existing systems from the beginning develops **systems-level thinking** — the capacity to reason about how components relate, where responsibilities lie, and how data flows across boundaries — far earlier than a write-first pedagogy permits.

The [Signature Applications](./signature-applications) — the classroom plant-sensor API, the Kansas Mesonet, the "Where Did They Go?" data-visualization tool, and the historical archive — are real, institutionally-grounded systems students engage with as this substrate, in place of invented toy examples wherever a real one is actually usable.

## The growing cycle

Each course adds engagement modes on top of what came before, always ending in reflection. **Confirmed straightforwardly:** Read comes first (CIS 116) and Reflect is constant throughout. **Not yet a clean one-mode-per-course escalation, and this page says so rather than forcing it:** the real course sequence compresses what were eight separate 8-week blocks into roughly seven substantive touchpoints across four semesters, and — per the same finding already logged for `spiral-method.md` — CIS 260 (databases, Y1 Spring) now lands a full semester *before* CIS 300/320 (Y2 Fall), which is where several earlier modes (Model, Build) would otherwise debut. The table below is ordered by actual chronology, not by the old block-verb narrative, and flags where multiple modes now converge on the same course rather than debuting one at a time.

| Course | New mode(s) added | Note |
|---|---|---|
| **CIS 116** (Y1 Fall) | **Read** | Foundational — every later mode depends on being able to read accurately before acting. |
| **CIS 200** (Y1 Spring) | **Repair** | Code Archaeology lands here (see below). |
| **CIS 260** (Y1 Spring) | **Query** | Chronologically earlier than Model/Build below — a real inversion of the old block order, not a simplification. |
| **CIS 300 / CIS 320** (Y2 Fall) | **Model, Build** | ADT/contract modeling (CIS 300) and building a new component against a provided API (CIS 320) — the client/server pairing introduces both at once. |
| **CIS 251** (Y2 Fall) | *(Secure, folded into Test below rather than tracked separately)* | Formalizes trust/security; the full "Test" mode doesn't converge until CIS 400 the following semester. |
| **CIS 400** (Y2 Spring) | **Test, Integrate, Operate** | The core's capstone converges three modes at once — a real structural change from the old design, where these were three separate blocks (B6, B7, B8). This is where the growing cycle reaches its fullest expression in the core. |
| **Reflect** (constant) | — | Present from CIS 116 onward, not a terminal phase. |

By CIS 400, engagement with a signature application involves every mode developed before it, converging in one course rather than unfolding one mode per touchpoint the way the old block design implied.

## What each mode means

**Read.** Read code you did not write. Trace data flow across files and modules. Understand the entry point. Read the commit history to understand how the system evolved. Ask: what does this do, and how can I tell? This is the foundational mode — every subsequent mode depends on being able to read accurately before acting.

**Repair.** Identify something that is wrong and fix it without breaking anything that was right. This is the Code Archaeology signature assessment: trace a bug, form a hypothesis about its cause, verify the hypothesis, write a regression test, apply the fix, and confirm the test passes. The regression-test discipline is load-bearing: repair without a test is not repair, it is a guess.

**Model.** Take a part of a system and express it more abstractly — as an ADT, a class hierarchy, a formal contract, or a data model. This is not reverse-engineering for its own sake; it is the process by which students develop the ability to articulate what a piece of code *is responsible for*, independent of how it implements that responsibility.

**Build.** Add something new to a system. Not from scratch — the existing architecture must be respected, existing tests must continue to pass, and the new addition must integrate with the existing component model. Building within a system is harder than building from scratch, because the constraints are real and visible.

**Query.** Ask a system's data layer a question it was not asked before. Query requires understanding both what data exists and how it is organized — gaps and normalization decisions become visible only through the act of trying to answer a real question with the existing schema.

**Test.** Write automated tests for a system, including for code added in Build. Unit and integration tests. Tests for failure modes. Test mode formalizes the contract discipline from Model: a test is an executable specification of what a module is supposed to do.

**Integrate.** Connect a system to something external — a new data source, a new partner API, a new output format. Defend the integration design: what is the data provenance? What happens when the external source changes format or goes offline? This is where multi-objective tradeoff reasoning becomes unavoidable.

**Operate.** Deploy, monitor, and maintain a system under real conditions. Set up alerting. Respond to a failure. Optimize a bottleneck. Operate mode reveals that a system that passes all its tests can still misbehave in production.

**Reflect** (constant). After every mode, students articulate what they observed, what surprised them, what they would do differently, and what questions they now have. Early on, reflection is informal. Later, it takes the form of structured postmortems, design-defense presentations, and competency self-assessments — though the full team-level blameless postmortem, specifically, is placed at the Year 3–4 capstone rather than inside the core (see the Sociotechnical Structure thread in Chapter 1).

## How this differs from the traditional model

| Traditional CS pedagogy | This program |
|---|---|
| Write from scratch first | Read at scale first |
| Programming skill is the foundation | Systems-level thinking is the foundation |
| Large codebases are an advanced topic | Large codebases are the starting point |
| Each assignment is self-contained | Assignments build on real, institutionally-grounded systems |
| Reading others' code is a supplementary skill | Reading others' code is a primary skill, assessed from CIS 116 |
| Complexity is introduced gradually via toy problems | Complexity is immediately visible; the student's role in it grows |

The traditional model is not wrong — it produces capable programmers. But it produces programmers who are well-prepared for the first job that involves building greenfield systems, and less well-prepared for the far more common first job that involves extending, maintaining, and reasoning about systems that already exist, that were written by other people, and that must continue to work while being changed.

## Connection to the signature assessments

**A structural change from the old design, worth naming plainly:** two of the four signature assessments — Team Software Project and Design Review — now converge on the same course (CIS 400), where the old block design kept them a full block apart (B6, B7). Whether that convergence needs its own pacing decision is an open question, not resolved here.

- **Code Archaeology:** the Repair mode, formalized as an assessed exercise — lands in **CIS 200**.
- **Data Investigation:** the Query mode, extended to a full research question with visualization and presentation — the most likely host is **CIS 260**, based on the Human-Centered Computing thread's "comprehend" pass, but this is an inference, not a confirmed placement.
- **Team Software Project:** the Build + Test modes, performed collaboratively on a real codebase with real code review — lands in **CIS 400**, the confirmed team-project host.
- **Design Review:** the Integrate mode, formalized as a presentation-and-defense exercise — also lands in **CIS 400**, as part of its live-walkthrough/architecture-defense assessment.

Reflection mode underlies all four assessments: each requires students to articulate not just what they did but why, and what they would do differently given what they now know.

## Open questions for faculty review

1. **Mode naming and mapping need ratification**, same as before — but now against real courses, not blocks. The compression of Model/Build/Test/Integrate/Operate into fewer touchpoints (see the cycle table above) is a bigger change than a renaming and should be reviewed as such.
2. **CIS 400's convergence load.** Test, Integrate, Operate, Team Software Project, and Design Review all land in one course now. Confirm this is pedagogically sound density, not overload — the same question already raised for CIS 300's thread load in Chapter 1.
3. **Signature-application assignment design is not yet written.** This page describes the cycle in general terms; which real assignment (against the plant-sensor API, Mesonet, the data-visualization tool, or the historical archive) happens at which course is `course-designer`'s work once `content/course-designs/` is built out. Don't read silence on a specific asset-to-course pairing as an oversight — it's genuinely undesigned yet.
4. **Reflection instrumentation.** How is reflection collected and assessed? The format and rubric still need to be designed, independent of the course-mapping changes here.
5. **External course connections.** How do the external co-designed math/stat courses participate in the developmental cycle? Not yet decided.
