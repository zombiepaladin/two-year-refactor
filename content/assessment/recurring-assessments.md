+++
title = "Recurring Assessment Types"
weight = 30
ordinal = "2.3"
+++

Recurring assessment types are direct assessment tasks that appear multiple times across the program, deepening in scale, scaffolding, and stakes with each pass. Unlike [signature assessments](./signature-assessments), which are single formal events, recurring types generate a continuous longitudinal evidence trail — the same kind of task, executed with increasing sophistication.

Each recurring type is associated with a primary sub-competency but typically generates evidence for multiple sub-competencies simultaneously.

**Re-mapped to the real course sequence, 2026-08-04** (see `resources/design-log.md`). This round converts the Summary table's spans to real courses. The detailed per-domain tables below (Computational Reasoning through Professional Practice) get the same full-scan verification the threads and lenses already went through, one competency domain at a time, in follow-up rounds. Treat this Summary table's endpoints as a first-pass approximation until each domain's detail is re-checked.

**Crosswalk notes affecting several rows below:**
- **Design Review is homed at CIS 400** — see `signature-assessments.md`'s entry. Any row involving "Design Review" ends there, not at CIS 300.
- **System Integration Project moved to the Year 3–4 program capstone**, outside the two-year core — see `signature-assessments.md`. Rows that depended on it (deployment-at-scale, full multi-stakeholder requirements work, blameless postmortem, employer-facing reporting) now terminate there instead of inside the core.
- **A previously-envisioned Data Analysis & Responsible AI course has no confirmed new-course home**, except its AI-generated-code-critique content, which is confirmed to land in CIS 141 (see `content/core-design/threads/practice-ai-assisted.md`). Rows depending on its other content are marked unconfirmed pending a course-designer/faculty placement decision.
- **A git-history capstone assessment originally envisioned for CIS 115 is explicitly unplaced** — `resources/reference/degree-maps/cs.md`'s CIS 115 entry lists it as a piece that did *not* get incorporated there. Rows starting from it are marked unconfirmed.

## Summary

| # | Assessment Type | Primary Sub-competency | Course Span |
|---|----------------|------------------------|------------|
| 1 | Code Archaeology | Analyze Computational Systems | CIS 200 → CIS 400 |
| 2 | Design Brief | Develop Abstractions | CIS 200 → CIS 400 |
| 3 | Formal Analysis | Apply Formal Reasoning | CIS 115 → CIS 400 |
| 4 | Algorithm Evaluation Task | Evaluate Algorithmic Solutions | CIS 300 → CIS 400 |
| 5 | Implementation Task | Implement Software Solutions | CIS 116 → CIS 400 |
| 6 | Verification Task | Verify Software Quality | CIS 200 → CIS 400 |
| 7 | Debugging Challenge | Debug Software Systems | CIS 200 → CIS 400 |
| 8 | Maintenance Task | Maintain Software Systems | CIS 200 → CIS 400 |
| 9 | Data Pipeline Task | Manage Data Resources | CIS 200 → *unconfirmed* |
| 10 | Data Investigation | Investigate Questions with Data | CIS 260 → *unconfirmed* |
| 11 | Data Communication Task | Communicate Data Insights | CIS 120 → CIS 320 *(resolved in the Data and Information round — doesn't depend on the unplaced data-analysis content after all)* |
| 12 | System Analysis Task | Analyze System Behavior | CIS 115 → CIS 400 |
| 13 | Environment Configuration Task | Manage Computing Environments | CIS 200 → CIS 400 |
| 14 | Deployment Task | Deploy Operational Systems | CIS 251/CIS 400 → Year 3–4 capstone |
| 15 | Requirements Analysis Task | Gather and Analyze Requirements | CIS 120 → CIS 320 *(resolved: full depth is a Software Architecture specialization elective, not core, per `cs.md`'s CIS 320 entry)* |
| 16 | Usability Evaluation | Design Human-Centered Solutions | CIS 120 → CIS 320 *(same resolution — full depth is the same specialization elective)* |
| 17 | Ethical Evaluation | Evaluate Ethical Implications | CIS 120 → CIS 141 / *unconfirmed (data integration; broader data-analysis content)* |
| 18 | Technical Explanation Task | Communicate Technical Information | CIS 200 → CIS 320 *(full depth: same specialization elective)* |
| 19 | Collaboration Task | Collaborate on Software Teams | *unconfirmed (git-history)* → CIS 400 |
| 20 | AI-Assisted Practice Task | Utilize AI Responsibly | CIS 200 → CIS 141 |
| 21 | Reflection Assessment | Reflect on Professional Growth | CIS 200 → CIS 400 *(core ceiling; full postmortem/employer-facing reporting now at the Year 3–4 capstone)* |

### Cross-domain types

Three types generate substantial evidence for multiple sub-competencies and appear in rubrics for each:

| Type | Primary | Also serves |
|------|---------|-------------|
| Design Brief | Develop Abstractions (CR) | Design Software Systems (SD); Design Human-Centered Solutions (HCP) |
| Algorithm Evaluation Task | Evaluate Algorithmic Solutions (CR) | Represent Information (DI) |
| Code Archaeology | Analyze Computational Systems (CR) | Maintain Software Systems (SD) |

### Level ceiling by evidence tier

| Evidence tier | Ceiling |
|---------------|---------|
| Automated (telemetry, H5P, git, IDE, AI logs) | Application |
| Recurring assessment types (direct, rubric-evaluated) | Adaptation |
| TA/LA role, club leadership, peer mentoring | Leadership |

---

## Computational Reasoning

**Domain re-checked against real course-design pages, 2026-08-04** — same full-scan method as the thread pass (not just mechanical crosswalk substitution). Headline finding: **CIS 301 (Logical Foundations of Programming) was absent from this whole domain**, because it's a genuinely new/restructured course with no single direct predecessor. Its real content (pre/post-conditions, loop invariants, function specifications, proof by induction/contradiction, quantifiers, natural deduction) is a much stronger, more directly confirmed fit for Formal Analysis than the rows it's replacing below. This matches the same CIS 301 fit already confirmed independently in the Correctness & Verification thread review.

### Code Archaeology

Students investigate an existing codebase — without prior familiarity — to explain its behavior, structure, and design decisions. Scale and substrate complexity increase with each pass.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Familiar languages, single module — trace control flow and explain behavior. Confirmed as CIS 200's formal Code Archaeology pass (Code Comprehension thread), building on CIS 116's informal "read, interpret, modify" seed (SLO 4). | Function/module |
| CIS 200, continued | Encapsulation-boundary archaeology — explain a design across a component boundary. **Partially unconfirmed**: a specific "unfamiliar paradigm" vehicle has no successor anywhere in the current design; only the general encapsulation-boundary framing (per course-designer's CIS 200 placement) carries forward. | Module boundary |
| CIS 260 (Y1 Spring) | Schema archaeology — read an existing schema and explain the design decisions embedded in it. **Unconfirmed** — not in CIS 260's drafted SLOs/schedule; plausible fit with Module 6 (Database Design) but not spelled out. | Data model |
| CIS 400 (Y2 Spring) | Git history archaeology — read a PR or commit history, explain what changed and why. Reasonably supported by CIS 400's confirmed collaborative-git content, though not this specific assessment framing. | System evolution |
| *unplaced* | Integrated system archaeology — trace behavior across multiple components and data stores. Depends on the orphaned data-integration content already flagged in the lens pass. CIS 300's graph unit could carry a narrower "multi-component" version if this gets rescoped. | Multi-component |
| CIS 400 (Y2 Spring) | Production system archaeology — diagnose a live bottleneck, explain interaction under load. Confirmed — matches the "performance optimization against a real bottleneck" item just added to `cis-400.md`'s Confirmed Design Intent section. | Full system under stress |

*Also generates evidence for: Maintain Software Systems*

---

### Design Brief

Students design an abstraction, interface, or system component to a problem or specification, with scaffolding decreasing and scope increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Design a module's public interface — specify what's hidden vs. exposed. Supported by CIS 200's real SLO 4 (compose a class through design/implementation/testing). | Single component, template provided |
| CIS 300 (Y2 Fall) | Design an ADT contract before any implementation — pre/post-conditions, guarantees. Confirmed — CIS 300's real schedule teaches contract-first at every ADT pass (applications before implementations), already verified in the Data Structures thread review. | Single component, less scaffolding |
| CIS 300 (Y2 Fall) | Design an API across a network boundary — endpoints, request/response shapes, error contracts (the "build" side of the CIS 300/CIS 320 client-server pairing). The related consume/integrate sub-aspects spread across CIS 120, CIS 200, CIS 220, and CIS 320 instead — see this domain's note above. | Component-to-component |
| CIS 260 (Y1 Spring) | Design a database schema — abstract a messy real-world domain into a formal relational model. Reasonably supported (SLO 10, Module 6). | Domain model, open-ended |
| CIS 400 (Y2 Spring) | Choose and defend the right abstraction tier for the problem (graph vs. relational vs. document). **Re-homed from CIS 300 to CIS 400** — this is Design Review content (choose *and defend*), which converges on CIS 400; see `signature-assessments.md`. | Multi-option, tradeoff-driven |
| CIS 400 (Y2 Spring) | System-level design — compose abstractions across multiple layers for a novel integration problem. Matches CIS 400's team-project scope; CIS 225's protocol-layering content is a lighter contributing touch, not the primary carrier. | Full system, novel context |

*Also generates evidence for: Design Software Systems; Design Human-Centered Solutions*

---

### Formal Analysis

Students construct a formal argument — a proof, specification, complexity bound, or correctness argument — with the form and scope escalating across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| MATH Logic and Sets (Y1 Fall) | Truth tables, predicate logic exercises, set proofs. CIS 115 contributes a lighter Boolean-logic/bitwise-operations touch alongside it. | Single proposition/expression, template provided |
| **CIS 301** (Y2 Fall) — Logical Foundations of Programming | Pre/post-condition specification; recursive correctness argument (proof by induction). **Re-homed here**, per this domain's headline finding above — directly confirmed against CIS 301's real schedule (pre/post-conditions, loop invariants, function specifications, proof by induction). MATH Recursive and Modular Computation (Y2 Fall) contributes the recursive-structures/modular-arithmetic substrate. | Single function, less scaffolding |
| CIS 300 (Y2 Fall) | Big-O analysis of sorting/searching algorithms; formal graph properties. Confirmed (SLO 6); MATH Graphs, Trees, and Maps (Y1 Spring) contributes the formal graph-theory substrate ahead of it. | Algorithm-scale, student constructs the bound |
| CIS 400 (Y2 Spring), woven throughout CIS 116/200/300 | Test suite as formal specification — what does this test formally guarantee, and what does it leave unverified? Formalized in CIS 400, confirmed as woven throughout the core plus formalized there. | System behavior, open-ended adequacy argument |
| CIS 300 (Y2 Fall) / CIS 400 (Y2 Spring) | Correctness argument for a graph algorithm (CIS 300); evaluate a peer's formal argument in Design Review (CIS 400, per the Design Review re-homing above). | Multi-step, peer-facing |
| CIS 400 (Y2 Spring) | Formal + empirical reconciliation — construct the argument for why Big-O prediction diverges from observed behavior. Confirmed, same "real bottleneck" Confirmed Design Intent item as Code Archaeology's terminal pass above. | Real system, formal model boundary case |

---

### Algorithm Evaluation Task

Students compare alternative algorithms, data structures, or data models and justify a selection for a specific context using formal and/or empirical evidence.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 300 (Y2 Fall) | Compare two implementations of the same ADT contract — same interface, different performance. Confirmed (SLO 2/6). | Single structure, implementations provided |
| CIS 300 (Y2 Fall) | Compare sorting/searching algorithms by complexity for a specified scenario; adjacency list vs. matrix. Confirmed in scope, though note `cis-300.md`'s open "Proposed Changes" reordering sorting content relative to the graph unit. | Algorithm-scale, student constructs the analysis |
| CIS 260 (Y1 Spring) | Justify index strategy (still a proposed, undrafted addition — see `cis-260.md`) or schema design choice (Module 6); compare relational vs. graph model for a given domain. | Data model scale, open-ended |
| CIS 300 (Y2 Fall) / CIS 400 (Y2 Spring) | Multi-objective tradeoff — Dijkstra vs. A\* (CIS 300); defended in Design Review (CIS 400, re-homed per above). **Data-store selection with competing constraints is unplaced** — depends on the same orphaned data-integration content flagged under Code Archaeology. | Multi-algorithm, defended in Design Review |
| CIS 400 (Y2 Spring) | Production system — evaluate choices where formal and empirical evidence must both be brought to bear. Confirmed, same real-bottleneck Confirmed Design Intent item. | Real system, novel context |

*Also generates evidence for: Represent Information*

---

## Software Development

**Domain re-checked against real course-design pages, 2026-08-04.** Two recurring patterns in this domain: the Design-Review-defense content converges on CIS 400 (already established in the two domains above), and several rows depended on content that's since moved to the Year 3–4 capstone (Round 1) or is still unplaced pending the data-integration/data-analysis placement decisions.

### Implementation Task

Students implement a software solution to a specification, with scaffolding removed and scope expanded across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 116 (Y1 Fall) | Single function or module — requirements fully specified, familiar language, no design decisions. | Function/module |
| CIS 200 (Y1 Spring) | Data transformation pipelines (confirmed, SLO 5 "collection classes and iterators"). | Function/module |
| CIS 220 (Y1 Spring) | Fetch-and-render with async/event handling — confirmed against CIS 220's event-loop/asynchronous-coordination outcomes. | Component |
| CIS 200 (Y1 Spring) / CIS 300 (Y2 Fall) | OOP with type-annotated contracts (CIS 200); implementing ADTs to a pre-defined contract (CIS 300, confirmed contract-first). | Component |
| CIS 300 (Y2 Fall) / CIS 220 & CIS 320 (Y1 Spring / Y2 Fall) | Building a full API — server side (CIS 300, the "build" verb) and client side / web components (CIS 220/CIS 320, the "integrate" verb). | System boundary |
| CIS 400 (Y2 Spring) | Collaborative implementation — team workflows, PR-based development. | Shared system |
| CIS 300 (Y2 Fall) | Graph algorithm implementation in a non-trivial problem context. | Component |
| CIS 400 (Y2 Spring) / CIS 320 (Y2 Fall) | Production-grade implementation (CIS 400); human-centered system work (CIS 320). **Data-analysis-notebook content is unconfirmed** — depends on the unplaced data-analysis/responsible-AI content flagged throughout this pass. | Full production system |

Note: automated evidence (IDE telemetry, git commits, H5P exercises) is richer here than anywhere else in the program — this sub-competency is most thoroughly covered by the telemetry tier up to Application. The gap is at Independence and above, which requires direct assessment.

---

### Verification Task

Students design and implement a verification strategy for a software system, with the balance shifting toward strategy design at higher levels.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Write a regression test for a specific code repair — verification as a safety net. | Single function, guided |
| **CIS 301** (Y2 Fall) / CIS 200 (Y1 Spring) | Write pre/post-conditions and test cases that exercise them — **re-homed to CIS 301** per this pass's Round 2 finding (its real content, not CIS 300's). Type annotations as static verification stays at CIS 200. | Single function, formal spec |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Design and implement a test suite including property-based tests — argue adequacy of coverage. | System, open-ended strategy |
| CIS 400 (Y2 Spring) | Performance validation for a production system. **Acceptance testing with real users is no longer at this ceiling** — CIS 320 carries the core's own bounded acceptance-criteria/A-B-testing exposure instead; full acceptance testing at System-Integration-Project scale moved to the Year 3–4 capstone (Round 1). | Novel multi-component, real users |

---

### Debugging Challenge

Students diagnose and fix defects in given code, with scaffolding removed and system complexity increased across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Single-function bug in a familiar language, guided hints. | Function, guided |
| CIS 200 (Y1 Spring) | Bug at an encapsulation boundary — trace exception across module boundary. | Component boundary |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Write a failing test that exposes the bug, then fix it — test-first diagnosis. | System, no hints |
| CIS 400 (Y2 Spring) | Code review — find latent bugs in a peer's code before they manifest. | Peer codebase |
| CIS 400 (Y2 Spring) | Diagnose from logs and monitoring data; no direct code access. | Production system |

*The terminal pass here, "blameless postmortem — diagnosing what went wrong at the system/team level," lives at the Year 3–4 capstone, not the core (Round 1; also independently confirmed in `thread-sociotechnical.md`). CIS 400's own ceiling is the lighter individually-written responsibility retrospective, not a full blameless postmortem.*

---

### Maintenance Task

Students modify an existing codebase to meet a changed requirement, without breaking existing behavior.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| *unplaced* | Git-as-archaeology / semantic versioning as "software evolves over time." **Unconfirmed** — this depended on a git-history capstone assessment that `cs.md`'s CIS 115 entry explicitly lists as not incorporated there (same finding as Round 2's Collaboration Task start). | — |
| CIS 200 (Y1 Spring) | Repair a bug using commit/revert safely — small, guided modification. | Single function, scaffolded |
| CIS 200 (Y1 Spring) | Add a method to an existing class while preserving encapsulation. | Component boundary |
| CIS 260 (Y1 Spring) | Schema migration — evolve a data model without breaking existing records. **Unconfirmed** — not in CIS 260's drafted SLOs/schedule. | Data layer, high stakes |
| CIS 400 (Y2 Spring) | Feature branch PR — implement a change in a shared codebase, pass code review. | Shared codebase |
| CIS 400 (Y2 Spring) | API versioning — evolve a public interface while maintaining backward compatibility. Confirmed (the "Software Versioning" topic). | Production system |

---

## Data and Information

**Domain re-checked against real course-design pages, 2026-08-04.** This is the domain most affected by unplaced/unconfirmed content: a data-integration scenario (unplaced per the user's Round 1 direction) and a Data Analysis & Responsible AI course (unconfirmed except its AI-code-critique slice, which lands in CIS 141) both anchor several rows here. One genuine resolution, though: Data Communication Task's terminal "honest visualization" pass turns out **not** to depend on the unplaced data-analysis content after all — see below.

### Data Pipeline Task

Students acquire, transform, and prepare data for a stated purpose, with source complexity and ethical constraints increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Parse and reshape a single CSV/JSON source to a specified output format. | Single source, specified transformation |
| CIS 200 / CIS 300 (Y1 Spring / Y2 Fall) / CIS 260 (Y1 Spring) | API-backed pipeline (CIS 200/300, the "consume" verb) and SQL query pipeline (CIS 260) — multi-step transformation chain. | Multi-step, student designs the chain |
| *unplaced* | Integrate multiple heterogeneous sources; identify and mitigate re-identification risk. Same orphaned data-integration content already flagged in the lens pass and earlier rounds. | Multi-source, ethical constraint |
| *unplaced* | Notebook pipeline with data provenance and ethical documentation. Depends on the unconfirmed data-analysis content, beyond its AI-code-critique slice (→ CIS 141). | Full lifecycle, novel domain |

---

### Data Investigation

Students investigate a question using data and statistical methods, with the question openness and methodological rigor increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| STAT 410 (Y2 Spring) | Describe a dataset — compute and interpret summary statistics, identify distribution shape. **STAT 410 has no drafted content yet** (per `resources/reference/degree-maps/cs.md`) — it's the confirmed successor to the old four-course non-calculus statistics sequence, but this specific pass can't be checked against real course content the way the CIS-numbered rows in this pass have been. | Single dataset, guided methods |
| CIS 260 (Y1 Spring) | Data Investigation (signature) — investigate a student-driven question with a novel dataset. Confirmed, matches `signature-assessments.md`. | Open-ended, no template |
| STAT 410 (Y2 Spring) | Probability-based investigation — compute likelihoods, reason formally about uncertainty. Same STAT 410 caveat as above. | Inference under uncertainty |
| STAT 410 (Y2 Spring) | Sampling investigation — design a sampling strategy, evaluate whether evidence supports a conclusion. Same STAT 410 caveat. | Methodology design |
| *unplaced* | Full notebook investigation with visualization, ethical framing, and honest uncertainty reporting. Depends on the unconfirmed data-analysis content. | Novel domain, public-facing conclusions |
| STAT 410 (Y2 Spring) | Correlation and regression — investigating relationships between variables; causal vs. correlational reasoning. Same STAT 410 caveat. | — |

---

### Data Communication Task

Students create visualizations or explanations that communicate data-driven findings to a specified audience, with audience complexity and ethical stakes increasing across passes.

| Course | Pass | Audience & Challenge |
|--------|------|----------------------|
| CIS 120 (Y1 Fall) | Visual hierarchy and accessibility — is this information legible and accessible to all readers? Confirmed (CIS 120's real "Web Accessibility" topic). | Any reader; accessibility compliance |
| CIS 320 (Y2 Fall) | Interactive/dynamic chart that updates as data changes, consuming data from the CIS 300 service layer. **Unconfirmed** — proposed, not yet drafted; see `cis-320.md`'s "Proposed Changes." | Technical context; implementation fidelity |
| STAT 410 (Y2 Spring) | Statistical chart selection — choose and create the right chart type for the data's distributional properties. STAT 410 has no drafted content yet. | Analytical audience; appropriateness of form |
| CIS 320 (Y2 Fall) | Honest visualization with ethical documentation — what does this chart claim, is the claim justified? **Resolved, not unplaced**: this is the same "honest data visualization" pass already confirmed as CIS 320's REPRESENT content in `thread-human-centered.md` — it does **not** depend on the unplaced data-analysis content this domain's other rows depend on. Still proposed/undrafted, but with a confirmed course home. | Public/mixed audience; ethical accountability |

*The terminal pass here also implies "Design Review — communicating data-driven design decisions to critical peers and faculty under scrutiny." That's CIS 400 content, per `signature-assessments.md`'s Design Review homing — folded into this type's evidence rather than kept as a separate row, consistent with how Design Review is treated in the other domains.*

---

## Systems and Infrastructure

**Domain re-checked against real course-design pages, 2026-08-04.** One structural flag applies to several rows below — `resources/reference/spiral-threads.md` already recorded it on 2026-07-15: **deep OS/concurrency formalization** (processes vs. threads, preemptive vs. cooperative scheduling, kernel vs. user space, the actor model, comparative fault-tolerance patterns) has **no confirmed new-course home**. CIS 220 carries the required ABET OS-*exposure* anchor at a lighter level ("browser as mini-OS"), and CIS 400 absorbed general deployment/operations content, but whether the deeper theoretical material survives anywhere (core or Systems Elective) was never decided. Rows depending on it are marked accordingly rather than asserted as CIS 400 content by default.

### System Analysis Task

Students trace behavior through a computing system using observation and measurement, with system complexity and the gap between formal models and empirical reality increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| *unplaced* | Trace stack/heap state through a function call sequence. Depends on stack/heap content that `cs.md`'s CIS 115 entry explicitly lists as not incorporated there — same finding as elsewhere in this pass. | Memory model, guided |
| CIS 220 (Y1 Spring) | Trace an async fetch through the event loop — explain callback ordering. Confirmed — this is CIS 220's own "browser as mini-OS" framing. | Concurrency model, guided |
| CIS 300 (Y2 Fall) | Trace a request through the full server pipeline — explain behavior at each stage (the "build" side of the CIS 300/CIS 320 pairing). | Multi-stage system |
| CIS 400 (Y2 Spring) | Diagnose a production bottleneck using monitoring data — explain why empirical behavior diverges from Big-O prediction. Confirmed against `cis-400.md`'s Confirmed Design Intent section. | Real system under load |

*Complementary to Code Archaeology: Code Archaeology traces behavior through code; System Analysis Task traces behavior through operational signals and system interactions.*

---

### Environment Configuration Task

Students configure a computing environment to support a specified development or operational purpose, with scope and coordination complexity increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Configure git — username, email, .gitignore, initial repository setup. | Single tool, personal toolchain |
| CIS 200 (Y1 Spring) | Configure type checker and linter — static analysis integrated into the workflow. | Static analysis toolchain |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Configure a test pipeline — test runner, coverage thresholds, CI trigger on push. | Integrated automation |
| CIS 400 (Y2 Spring) | Configure a shared team environment — branch protection, PR templates, shared linting config. | Collaborative toolchain |
| CIS 400 (Y2 Spring) | Configure a production environment — containers, environment variables, secrets, monitoring, hardening. Confirmed — matches the "harden the system before it goes live" Confirmed Design Intent item added during the lens pass. | Production-grade, real constraints |

---

### Deployment Task

Students deploy, validate, and monitor a software system in an operational environment.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 400 (Y2 Spring), formalized (woven throughout) | Tag a release — ensure tests pass, cut a semantic version tag, document what changed. | Single service, staging environment |
| CIS 400 (Y2 Spring) | Deploy a containerized service — configure, deploy, monitor, and respond to an operational issue. Confirmed. | Production environment, real constraints |
| CIS 400 (Y2 Spring) / Systems Elective (Y4) or *unconfirmed* | API versioning and containers/monitoring are confirmed CIS 400 content. **Fault-tolerance comparison (actor model, circuit breakers) is the same unconfirmed deep-OS/concurrency content flagged at the top of this domain** — plausibly Systems Elective territory (CIS 520/525/625), not confirmed as core content. | — |
| Year 3–4 capstone | System Integration Project deployment — multi-component system for real user acceptance; postmortem on what broke. **Moved out of the core**, per `signature-assessments.md`'s Round 1 finding. | Novel multi-component, live users |

*Note: this sub-competency is concentrated at CIS 400 within the core. The earlier touchpoints (CIS 200's tooling, CIS 400's own testing/versioning content) are seeds; full acceptance-tested, real-user deployment with a postmortem is now a Year 3–4-capstone-level event, not a core one.*

---

## Human-Centered Practice

**Domain re-checked against real course-design pages, 2026-08-04.** This resolves the two rows Round 1 flagged (Requirements Analysis Task, Usability Evaluation) — their previously-assumed endpoint split into different content once the design moved to real courses. `cs.md`'s own CIS 320 entry is explicit: CIS 320 carries "one bounded exposure to acceptance-criteria/A-B-testing process work... not a full requirements-gathering methodology, just enough that every student has the experience once," with **a full deep dive deliberately deferred to a Software Architecture specialization elective**. So the core's ceiling for this whole family of passes is CIS 320's bounded version; the "full multi-method investigation, conflicting stakeholders" version isn't a core event at all — it's upper-division specialization depth, not the Year 3–4 general capstone this pass had guessed in Round 1.

### Requirements Analysis Task

Students identify stakeholder needs and translate them into system requirements, with method formality and stakeholder complexity increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 120 (Y1 Fall) | Identify user needs informally — who is this for, what accessibility requirements follow from their context? | Single user type, guided |
| STAT 410 (Y2 Spring) | Survey design — design a valid instrument for a specified research question; critique a given survey for bias. STAT 410 has no drafted content yet. | Research design, data collection |
| CIS 400 (Y2 Spring) | Stakeholder interview + requirements brief — conduct an interview, produce a documented requirements artifact. Plausible fit with CIS 400's confirmed estimation/scoping content, though not drafted at this specific granularity. | Real human, formal output |
| CIS 320 (Y2 Fall) | Bounded acceptance-criteria exposure — every student gets this once. **Full multi-method investigation with conflicting stakeholders is not core content** — confirmed deferred to a Software Architecture specialization elective (`cs.md`'s CIS 320 entry). | Novel context, real users, ambiguous needs *(elective, not core)* |

---

### Usability Evaluation

Students evaluate an existing design or interface against human-centered criteria, with the complexity of the system and the evaluation method increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 120 (Y1 Fall) | Accessibility audit — evaluate an existing page against accessibility criteria (contrast, keyboard navigation, screen reader). Confirmed. | Checklist-guided, single page |
| CIS 320 (Y2 Fall) | Component usability evaluation — does this component's interface make sense from the user's perspective? Unconfirmed — proposed, not yet drafted. | Interface design, less scaffolding |
| CIS 400 (Y2 Spring) | Design Review — peers evaluate each other's system designs for human-centeredness and usability fit. Re-homed to CIS 400 per `signature-assessments.md`. | Peer-facing, multi-dimension critique |
| CIS 320 (Y2 Fall) | Heuristic evaluation, A/B analysis against acceptance criteria. Confirmed — this is CIS 320's real, bounded FITNESS content. **Full user-testing-sessions-with-real-users depth is a Software Architecture specialization elective**, not core. | Real users, novel system *(elective, not core)* |

---

### Ethical Evaluation

Students identify and reason about the ethical implications of a computational decision or system, with the scope of harm and the novelty of the context increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 / CIS 120 (Y1 Spring / Y1 Fall) | Data minimization analysis — given a pipeline or form, identify what data is collected and argue for what should be removed. The confirmed carrier is CIS 120 (per the lens pass's narrowed row); the CIS 200 half of this claim is thin. | Single decision, guided framework |
| CIS 260 (Y1 Spring) | Schema ethics documentation — justify access control and data minimization decisions in a schema design. Confirmed design intent, undrafted — see `cis-260.md`'s "Proposed Changes." | Design-level, formal documentation |
| CIS 251 (Y2 Fall) / CIS 400 (Y2 Spring) | Threat analysis (CIS 251, confirmed | against its real SLOs) + responsibility retrospective (CIS 400, | confirmed). | System-level, collaborative accountability |
| *unplaced* | Re-identification risk analysis — identify risks from dataset combination and propose mitigations. Same orphaned data-integration content flagged throughout this pass. | Integration-level, emergent harm |
| CIS 141 (Y2 Spring) / *unplaced* | AI-assisted analysis critique — evaluate
an AI-generated artifact for correctness, bias, privacy, and security risk (confirmed, CIS 141 is the terminal pass for the AI-Assisted Development practice). Broader data-ethics content beyond the AI-critique slice remains unconfirmed. | Novel context, high stakes |
*This type's "blameless postmortem" component of the Adaptation level lives at the Year 3–4 capstone, not the core — see `signature-assessments.md`.*

---

### Technical Explanation Task

Students communicate technical information to a specified audience, with audience diversity and communication stakes increasing across passes.

| Course | Pass | Audience & Stakes |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Type-annotated interface documentation — document a component's contract for a peer developer. | Peer developer; asynchronous, low stakes |
| CIS 260 (Y1 Spring) | Schema-decision documentation — explain design choices to a future maintainer without your context. Confirmed design intent, undrafted. | Future maintainer; asynchronous, medium stakes |
| CIS 400 (Y2 Spring) | PR description and code review — communicate what changed, why, and what to look for. | Team; professional, collaborative |
| CIS 400 (Y2 Spring) | Design Review presentation — defend technical decisions to critical peers and faculty. Re-homed to CIS 400 per `signature-assessments.md`. CIS 501's confirmed "present and defend a design" pass (Professional Practices lens) is an even higher-stakes later instance of the same skill. | Critical audience; synchronous, high stakes |
| CIS 320 (Y2 Fall) | Stakeholder translation — communicate technical constraints and tradeoffs to non-technical decision-makers, at CIS 320's bounded scope. **Full depth is the same Software Architecture specialization elective** flagged throughout this domain, not core. | Non-technical; consequential, novel context *(elective, not core)* |

---

## Professional Practice

**Domain re-checked against real course-design pages, 2026-08-04 — the last of the six.** AI-Assisted Practice Task maps cleanly onto the four-stage progression `content/core-design/threads/practice-ai-assisted.md` already confirmed (CIS 116/200 → CIS 260 → CIS 400 → CIS 141) — the cleanest resolution of any recurring type touched by the data-analysis placement question in this whole pass, since that thread file settled it independently before this round even started. Collaboration Task and Reflection Assessment both carry the now-familiar unplaced-git-history and relocated-postmortem findings.

### Collaboration Task

Students coordinate work in a shared version-controlled codebase, with the collaborative complexity and team accountability increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| *unplaced* | Git history exploration — read a repo's log, diff, and blame to reconstruct what a collaborator changed and why. Depends on a git-history capstone that `cs.md`'s CIS 115 entry explicitly lists as not incorporated there — same finding as Round 2/3's Maintenance Task and this Summary table's row 19. | Read-only, solo |
| CIS 200 (Y1 Spring) | Commit/revert safety net — use git to checkpoint and recover during a repair task. | Write, solo |
| CIS 260 (Y1 Spring) | Solo feature branch — implement a schema change on a branch, merge cleanly. Confirmed design intent, undrafted — see `cis-260.md`'s "Proposed Changes." | Branch/merge, solo |
| CIS 400 (Y2 Spring) | Full collaborative PR cycle — branch, implement, open PR, respond to review, merge. Confirmed. Conway's Law enacted; the Team Software Project begins here. | Team, professional workflow |
| CIS 400 (Y2 Spring) | Sustained team collaboration on the historical-archive project — consolidated into this single course rather than spread across three old blocks, per `signature-assessments.md`'s Round 1 finding. **Postmortem accountability is not part of this pass** — that's moved to the Year 3–4 capstone; CIS 400's own ceiling is the individually-written responsibility retrospective. | Real product, team |

---

### AI-Assisted Practice Task

Students use AI tools for a specified purpose and are assessed on their evaluation, verification, and responsible use of AI outputs, with stakes and verification complexity increasing across passes.

| Course | Pass | Stakes & Verification Challenge |
|--------|------|----------------------------------|
| CIS 116 / CIS 200 (Y1 Fall / Y1 Spring) | AI-as-explainer — use AI to explain unfamiliar code; verify the explanation against actual runtime behavior. Confirmed, stage 1 of `practice-ai-assisted.md`'s four-stage progression. | Low stakes; verification by empirical observation |
| CIS 260 (Y1 Spring) | AI design brainstorm — generate alternatives with AI, select and justify one, document where AI reasoning was flawed. Confirmed, stage 2. | Medium stakes; verification by design argument |
| CIS 400 (Y2 Spring), formalized (woven throughout) | AI-generated tests — evaluate coverage, find gaps, verify test correctness and adequacy. Confirmed, stage 3. | Medium stakes; verification by coverage analysis |
| CIS 141 (Y2 Spring) | AI code critique — evaluate AI-generated code for correctness, security weaknesses, and bias. Confirmed, stage 4 — the terminal pass, also the prerequisite skill for the Year 3–4 Agentic AI specialization. | High stakes; verification by security and correctness analysis |

---

### Reflection Assessment

Students reflect on their own practice, identify growth areas, and plan improvements, with the accountability dimension and the evidence base for reflection increasing across passes.

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 200 (Y1 Spring) | Post-Code Archaeology debrief — what strategies worked and what would you do differently? | Individual, prompted, low stakes |
| CIS 300 / CIS 260 (Y2 Fall / Y1 Spring) | Backward reflection with new tools — revisit an earlier decision (Big-O reasoning, schema design) and argue what you'd change now. | Individual, cross-temporal, no prompts |
| CIS 400 (Y2 Spring) | Responsibility retrospective — individually-written reflection on ethical and professional practice during the team project. Confirmed. | Individual, structured, accountability dimension |
| Year 3–4 capstone | Blameless postmortem + employer-facing competency report — systemic failure analysis and curated growth narrative. **Moved out of the two-year core** — see `signature-assessments.md`'s Round 1 finding; CIS 400's own reflection ceiling is the responsibility retrospective above, not this event. | Real consequences; public-facing artifact |
