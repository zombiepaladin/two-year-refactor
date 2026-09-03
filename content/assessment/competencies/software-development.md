---
title: "Software Development"
pre: "2. "
weight: 20
---

*Re-checked against real course-design pages, 2026-08-04 — see `resources/design-log.md`. Two things propagate through this whole domain: the Design Review defense converges on CIS 400 (established in the Computational Reasoning round), and several rows depended on content that's since moved to the Year 3–4 program capstone (Round 1: System Integration Project, full acceptance testing, blameless postmortem).*

### Design Software Systems

**I can design software systems that satisfy identified requirements and constraints.**

I create and communicate system designs that consider functionality, maintainability, privacy, security, usability, and performance.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 200 (Y1 Spring) | Module boundary design — what a component hides vs. exposes; type-annotated interfaces. |
| CIS 300 (Y2 Fall) | ADT contract-first design — specifying behavior before implementation. Confirmed against the real schedule. |
| CIS 300 (Y2 Fall) / CIS 220 & CIS 320 (Y1 Spring / Y2 Fall) | Client-server decomposition; API design across a network boundary (CIS 300, build side); web component architecture (CIS 220/CIS 320, integrate side). |
| CIS 260 (Y1 Spring) | Schema design — modeling a real-world domain with formal relational structure. |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Designing for testability — testability as a first-class design quality. |
| CIS 251 (Y2 Fall) | Privacy and cybersecurity as design concerns — threat | modeling, least-privilege, data minimization embedded in design. Confirmed | directly against CIS 251's real SLOs. |
| CIS 400 (Y2 Spring) | Design Review — defend system design choices including algorithm selection, data model, and tradeoffs. Re-homed here to CIS 400, per `signature-assessments.md`. |
| CIS 400 (Y2 Spring) | Deployment architecture, fault-tolerance design, API versioning as a compatibility contract. |
| CIS 320 (Y2 Fall) | Requirements-driven design — designing from stakeholder needs outward, at CIS 320's bounded acceptance-criteria scope. **The full multi-stakeholder, System-Integration-Project-scale version of this pass has moved to the Year 3–4 capstone** (Round 1) — this row is the core's own, smaller-scoped version, not a stand-in for the relocated event. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Design Brief (constrained) — design a component or API to a given specification |
| Independence | Design Brief (open-ended) — given requirements, produce a complete system design without a template |
| Adaptation | CIS 400's team-project design work — novel multi-stakeholder system requiring synthesis of all design concerns, within the core's own scope (the old "System Integration Project" ceiling for this level is now at the Year 3–4 capstone, a later and larger event, not this one) |
| Leadership | Design Review critique (TA/LA role) — evaluating whether a peer's design satisfies stated requirements and constraints |

**Recurring type:** Design Brief (shared with Develop Abstractions and Design Human-Centered Solutions) — the rubric criteria here focus on functionality, maintainability, privacy, security, usability, and performance tradeoffs rather than abstraction structure.

---

### Implement Software Solutions

**I can construct software solutions that fulfill identified requirements using appropriate technologies and development practices.**

I develop software systems by applying suitable tools, languages, frameworks, and implementation strategies.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 116 (Y1 Fall) | First programs — imperative paradigm; heavily scaffolded. |
| CIS 200 (Y1 Spring) | Data transformation pipelines; collection classes and iterators. |
| CIS 220 (Y1 Spring) | Fetch-and-render with async/event handling. |
| CIS 200 (Y1 Spring) / CIS 300 (Y2 Fall) | OOP with type-annotated contracts (CIS 200); implementing ADTs to a pre-defined contract (CIS 300). |
| CIS 300 (Y2 Fall) / CIS 220 & CIS 320 (Y1 Spring / Y2 Fall) | Building a full API — server-side (CIS 300); client-side and web components (CIS 220/CIS 320). |
| CIS 400 (Y2 Spring) | Collaborative implementation — team workflows, PR-based development. |
| CIS 300 (Y2 Fall) | Graph algorithm implementation in a non-trivial problem context. |
| CIS 400 (Y2 Spring) / CIS 320 (Y2 Fall) | Production-grade implementation (CIS 400); human-centered system work (CIS 320). Data-analysis-notebook content is unconfirmed, pending a course-designer/faculty decision on where it lands. |

Note: automated evidence (IDE telemetry, git commits, H5P exercises) is richer here than anywhere else in the program — this sub-competency is most thoroughly covered by the telemetry tier up to Application. The gap is at Independence and above, which requires direct assessment.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured implementation task — requirements and step-by-step specification provided |
| Independence | Open-ended implementation task — requirements given, no scaffolding; student selects tools and approach |
| Adaptation | CIS 400's Team Software Project — novel, multi-stakeholder, collaborative implementation under real constraints, within the core's own scope. (The old "System Integration Project" co-anchor for this level has moved to the Year 3–4 capstone — see `signature-assessments.md`.) |
| Leadership | TA/LA supporting peers' implementation; leading code review sessions |

**Recurring type:** Implementation Task — deepens from fully-specified single function (CIS 116) through production-quality novel-domain implementation (CIS 400).

---

### Verify Software Quality

**I can evaluate software systems using testing, analysis, and verification techniques to determine whether requirements have been met.**

I apply appropriate methods to establish confidence in the correctness, reliability, and quality of software systems.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 200 (Y1 Spring) | Regression tests introduced as a safety net for code repair — first informal encounter with verification. Type checker as mechanical verifier — type annotations as static verification. |
| **CIS 301** (Y2 Fall) | Pre/post-conditions and invariants as formal specification; proof obligations for recursive functions. **Re-homed here to CIS 301**, per the Computational Reasoning round's headline finding — this is CIS 301's real, confirmed content. |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Primary home — automated unit and integration testing; property-based testing; test suite as formal specification. |
| CIS 400 (Y2 Spring) | Code review as peer verification — correctness check before merge. |
| CIS 400 (Y2 Spring) | Design Review — defending correctness of structural choices, not just "does it work." Re-homed here per `signature-assessments.md`. |
| CIS 400 (Y2 Spring) | Performance validation on a live system — empirical verification against performance requirements. |
| CIS 320 (Y2 Fall) | Acceptance testing (fitness-for-purpose) and A/B testing, at CIS 320's bounded, every-student-gets-this-once scope — **not** the full real-users acceptance-testing event, which has moved to the Year 3–4 capstone (Round 1). |

Note: three formal verification techniques are explicitly present: type checking as mechanical verification (CIS 200), property-based testing (CIS 400), and pre/post-condition invariants (CIS 301, re-homed). These complement the empirical testing emphasis.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Implement a test suite for a given specification — write unit and integration tests to a provided requirements document |
| Independence | Design and implement a complete verification strategy — given a system, determine independently what to test, at what level, and argue adequacy |
| Adaptation | Performance validation for CIS 400's team project, within the core's own scope. (Full acceptance testing with real users for a novel multi-component system — the old ceiling here — now sits at the Year 3–4 capstone.) |
| Leadership | TA/LA reviewing test suites and teaching testing practice; leading code review sessions with a correctness lens |

**Recurring type:** Verification Task — deepens from regression test as safety net (CIS 200) through performance validation on the core's own capstone (CIS 400); full acceptance-testing-with-real-users deepens further at the Year 3–4 capstone.

---

### Debug Software Systems

**I can diagnose and correct defects in software systems using systematic investigation and evidence.**

I identify the causes of unexpected behavior and implement effective solutions while validating the results of my changes.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 200 (Y1 Spring) | Primary home — debugging reframed as systematic data flow investigation; git revert and regression tests as diagnostic safety nets; AI-as-explainer verified empirically. |
| CIS 200 (Y1 Spring) | Debugging across encapsulation boundaries — exceptions as signals that a contract was violated; try/catch as a diagnostic tool. |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Test-isolated debugging — failing tests as precise diagnostic instruments. |
| CIS 400 (Y2 Spring) | Code review as pre-production defect detection. |
| CIS 400 (Y2 Spring) | Production debugging — diagnosing live system failures from monitoring data and logs. |

**Blameless postmortem — diagnosing what went wrong at the system/team level — has moved to the Year 3–4 program capstone**, confirmed independently in `thread-sociotechnical.md` (same finding as `signature-assessments.md`'s System Integration Project move, Round 1). CIS 400's own ceiling is an individually-written responsibility retrospective, a lighter, individual-facing counterpart, not a full team-level blameless postmortem.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Guided debugging challenge — bug symptom given, scaffolded hints about where to look |
| Independence | Unscaffolded debugging challenge — unfamiliar codebase, no hints, systematic investigation required |
| Adaptation | Production debugging (CIS 400) — diagnose a live system failure from operational signals (logs, monitoring), no direct test harness |
| Leadership | TA/LA mentoring debugging sessions. (Leading blameless postmortems is now a Year 3–4-capstone-level activity, not available within the core.) |

**Recurring type:** Debugging Challenge — deepens from single-function guided diagnosis (CIS 200) through production system diagnosis from logs (CIS 400). Code Archaeology and Debugging Challenge naturally pair — reading the code to understand it is the prerequisite for diagnosing it.

---

### Maintain Software Systems

**I can modify and evolve existing software systems while preserving functionality, reliability, and data integrity.**

I analyze existing codebases, implement changes, and manage software evolution without introducing unintended consequences.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| *unplaced* | Git as history/archaeology tool; semantic versioning seeds the idea of software as something that evolves over time. **Unconfirmed** — depended on a git-history capstone assessment that `cs.md`'s CIS 115 entry explicitly lists as not incorporated there. |
| CIS 200 (Y1 Spring) | Primary home — Code Archaeology; git commit/revert and regression tests introduced explicitly as safety nets for modifying code. |
| CIS 200 (Y1 Spring) | Type annotations as maintenance affordance — explicit contracts protect future maintainers. |
| CIS 260 (Y1 Spring) | Schema migration — evolving a database schema without breaking existing data. **Unconfirmed** — not in CIS 260's drafted SLOs/schedule. |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Regression tests as the foundation for safe modification. |
| CIS 400 (Y2 Spring) | Branch/PR/code review workflow — professional mechanism for modifying a shared codebase. |
| CIS 400 (Y2 Spring) | Operational maintenance — runbooks, monitoring, API versioning as a backward-compatibility contract. Confirmed (the "Software Versioning" topic). |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Guided maintenance task — modify an existing codebase to a specified change, with tests and documentation provided |
| Independence | Open-ended maintenance task — given a codebase and a change requirement, determine what needs to change without guidance |
| Adaptation | CIS 400's Team Software Project — maintaining a shared evolving codebase with real coordination overhead; schema migration on a live database (CIS 260, proposed) |
| Leadership | TA/LA managing code review for a team; leading retrospectives on a system's evolution |

**Recurring type:** Maintenance Task — deepens from guided bug repair with commit/revert (CIS 200) through API versioning on CIS 400's team project. Code Archaeology, Debugging Challenge, and Maintenance Task naturally appear in sequence: read → diagnose → repair safely.
