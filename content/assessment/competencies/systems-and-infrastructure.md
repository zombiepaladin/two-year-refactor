---
title: "Systems and Infrastructure"
pre: "4. "
weight: 40
---

*Re-checked against real course-design pages, 2026-08-04 — see `resources/design-log.md`. One structural flag applies throughout, already on record in `resources/reference/spiral-threads.md` since 2026-07-15: **deep OS/concurrency formalization** (processes vs. threads, scheduling, kernel/user space, the actor model, comparative fault-tolerance patterns) has **no confirmed new-course home**. CIS 220 carries the required ABET OS-*exposure* anchor at a lighter level; whether the deeper theoretical material survives in the core or only at the Systems Elective (CIS 520/525/625) was never decided. Rows depending on it are marked accordingly.*

### Analyze System Behavior

**I can investigate the behavior of computing systems by examining interactions among software, hardware, networks, and data.**

I explain system performance, reliability, and resource utilization using evidence gathered from observation and measurement.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| *unplaced* | Stack/heap memory model; "a running program is a process the OS schedules." Depends on content `cs.md`'s CIS 115 entry explicitly lists as not incorporated there. | 
| CIS 220 (Y1 Spring) | Browser as mini-OS — tracing async requests through the event loop; origin isolation; web workers as concurrent processes; `postMessage` as IPC. Confirmed. |
| CIS 300 (Y2 Fall) | Client-server dataflow — tracing a request through parse → auth → route → handle → serialize → respond (the "build" side of the CIS 300/CIS 320 pairing). |
| CIS 300 (Y2 Fall) | Big-O as a tool for analyzing performance characteristics theoretically. Confirmed (SLO 6). |
| CIS 400 (Y2 Spring) | Performance analysis on a real deployed bottleneck. Confirmed against the Confirmed Design Intent section. **The deep-OS-internals half of this old pass (memory hierarchy/cache/virtual-memory/thrashing, processes-vs-threads, preemptive-vs-cooperative scheduling, kernel-vs-user-space) is the same unconfirmed content flagged at the top of this file** — not asserted as CIS 400 content here. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Trace execution through a model — given a system description, trace interactions and explain observed behavior |
| Independence | Unscaffolded system investigation — given a system and a symptom, investigate and explain without guided prompts |
| Adaptation | Production system analysis (CIS 400) — explain a live performance bottleneck using monitoring data; reconcile theoretical and empirical behavior |
| Leadership | TA/LA leading system analysis sessions. (Leading blameless postmortems is now a Year 3–4-capstone-level activity — see `signature-assessments.md`.) |

**Recurring type:** System Analysis Task — deepens from CIS 220's event-loop trace through CIS 400's production bottleneck diagnosis; a stack/heap starting point remains unplaced. Complementary to Code Archaeology: Code Archaeology traces behavior through code; System Analysis Task traces behavior through system interactions and operational signals.

---

### Manage Computing Environments

**I can configure and operate computing environments that support software development, deployment, and maintenance.**

I establish and manage the tools, services, dependencies, and resources needed for effective system operation.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 200 (Y1 Spring) | Git setup and configuration — first explicit tool configuration in the program. |
| CIS 200 (Y1 Spring) | Type checker and linter configuration — static analysis tools as part of the development environment. |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Test runner configuration — setting up automated test environments, not just writing tests. |
| CIS 400 (Y2 Spring) | Collaborative toolchain — shared Git workflow configuration, branch protection, code review tooling. |
| CIS 400 (Y2 Spring) | Primary home — containers as environment abstraction; dependency management; production configuration; monitoring and logging tooling; hardening before live. Confirmed — matches the "harden the system before it goes live" Confirmed Design Intent item added during the lens pass. |

Note: automated evidence (IDE telemetry, git logs) captures environment *use* but not environment *configuration and management* — this sub-competency requires direct assessment to demonstrate beyond Application level.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Guided environment configuration — set up a development or test environment to a provided specification |
| Independence | Open-ended environment configuration — given a system and its requirements, determine and configure an appropriate environment |
| Adaptation | Container-based deployment (CIS 400) — configure a production environment with real security, dependency, and operational constraints |
| Leadership | TA/LA supporting peers with environment setup and toolchain issues; writing and maintaining team tooling documentation |

**Recurring type:** Environment Configuration Task — deepens from single personal tool configuration (CIS 200) through CIS 400's production-grade container and secrets management.

---

### Deploy Operational Systems

**I can deploy, monitor, and maintain software systems in operational environments.**

I prepare systems for use, manage releases, and support ongoing operation while addressing reliability, security, and performance concerns.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 300 / CIS 320 (Y2 Fall) | Conceptual seed — client-server decomposition makes "where does each component run?" a named question. |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Test suite as pre-deployment validation gate. |
| CIS 400 (Y2 Spring) | Git PR workflow as release mechanism — merge to main as a deployment trigger; semantic versioning as release communication. |
| CIS 400 (Y2 Spring) | Primary home within the core — containerized deployment; monitoring and logging; operational runbooks; harden-before-live; API versioning as backward-compatibility contract; performance analysis under real load. **Fault-tolerance comparison (actor model, circuit breakers) is the same unconfirmed deep-OS/concurrency content flagged at the top of this file** — plausibly Systems Elective territory, not confirmed core content. |
| Year 3–4 capstone | System Integration Project — deploy for real user acceptance testing; blameless postmortem as operational retrospective. **Moved out of the two-year core**, per `signature-assessments.md`'s Round 1 finding. |

Note: this sub-competency is concentrated at CIS 400 within the core. The earlier touchpoints are seeds — this is appropriate, deployment requires security, testing, and environment-management foundations that aren't complete until CIS 251/CIS 400. Full acceptance-tested, real-user deployment with a postmortem is a Year 3–4-capstone-level event, not a core one.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Guided deployment — deploy a pre-built application to a specified environment following provided steps |
| Independence | Open-ended deployment — given a system, determine and execute an appropriate deployment strategy without step-by-step guidance |
| Adaptation | CIS 400's deployment work — deploy with real reliability, security, and performance constraints, within the core's own scope. (The old "System Integration Project" ceiling — a novel multi-component system with live-issue response — is now at the Year 3–4 capstone.) |
| Leadership | TA/LA leading deployment workshops; writing operational runbooks for team use. (Leading incident response and blameless postmortems is now a Year 3–4-capstone-level activity.) |

**Recurring type:** Deployment Task — starts with CIS 400's release-tagging content and deepens through its production deployment work; full multi-component deployment with a real-user postmortem now sits at the Year 3–4 capstone.
