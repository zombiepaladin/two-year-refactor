---
title: "Human-Centered Practice"
pre: "5. "
weight: 50
---

*Re-checked against real course-design pages, 2026-08-04 — see `resources/design-log.md`. This resolves two rows Round 1 flagged (Requirements Analysis Task, Usability Evaluation): their previously-assumed endpoint didn't map cleanly onto a real course, and `cs.md`'s own CIS 320 entry is explicit that CIS 320 carries only a bounded, every-student-gets-this-once exposure to acceptance-criteria/requirements work — "not a full requirements-gathering methodology" — with full depth deliberately deferred to a **Software Architecture specialization elective**, not the Year 3–4 general capstone this pass had guessed in Round 1.*

### Gather and Analyze Requirements

**I can identify stakeholder needs and translate them into actionable system requirements.**

I use appropriate methods to understand problems, clarify expectations, and define criteria for successful solutions.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 120 (Y1 Fall) | Accessibility and data-minimization as non-functional requirements — first encounter with requirements imposed by human needs rather than technical constraints. Confirmed (per the lens pass's narrowed CIS 120 row). |
| STAT 410 (Y2 Spring) | Survey design as a data collection methodology — constructing valid survey instruments, question bias, Likert scales, sampling considerations. STAT 410 has no drafted content yet. |
| CIS 400 (Y2 Spring) | Team project scoping — assessed requirements artifact: conduct a stakeholder interview and produce a functional/non-functional requirements brief before implementation begins. Plausible fit with CIS 400's confirmed estimation/scoping content, not drafted at this specific granularity. |
| CIS 400 (Y2 Spring) | Design Review — defending choices against stated requirements; requirements surface through critique. Re-homed to CIS 400 per `signature-assessments.md`. |
| CIS 320 (Y2 Fall) | Bounded exposure — every student translates ambiguous needs into acceptance criteria once. **Formal requirements-gathering methods, stakeholder interviews, and qualitative/quantitative investigation at full depth are not core content** — confirmed deferred to a Software Architecture specialization elective. |

Note: the STAT 410 survey-design content requires coordination with the statistics department — survey design is within scope for a statistics course (sampling, instrument validity, response bias) but the extension needs their buy-in. Unrelated to this pass's STAT 410 drafting caveat, but still open.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured requirements analysis — given a stakeholder description, identify and categorize functional and non-functional requirements |
| Independence | Requirements brief — conduct a requirements analysis for a specified system; define acceptance criteria without a template |
| Adaptation | CIS 320's bounded acceptance-criteria work, within the core's own scope. (The old "System Integration Project" ceiling — gathering requirements from real stakeholders with ambiguous or conflicting needs — is not a core event; it's Software Architecture specialization-elective depth.) |
| Leadership | TA/LA facilitating requirements workshops; leading stakeholder interviews for a team project |

**Recurring type:** Requirements Analysis Task — deepens from informal user-needs identification (CIS 120) through CIS 320's bounded acceptance-criteria exposure; full multi-method investigation with real stakeholders is specialization-elective depth, not a core ceiling.

---

### Design Human-Centered Solutions

**I can design computational solutions that account for human needs, accessibility, usability, and context.**

I evaluate design decisions based on their impact on the people and communities who interact with the system.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 120 (Y1 Fall) | First pass — semantic HTML, accessibility substrate, data-minimization in forms; designing for all users as a baseline constraint. |
| CIS 320 (Y2 Fall) | Interactive/data-driven visualization and web component architecture — designing data-driven and component-based interfaces. Unconfirmed — proposed, not yet drafted. |
| CIS 400 (Y2 Spring) | Design Review — defending human-centered design choices under peer scrutiny; usability as a named dimension of the critique. Re-homed to CIS 400 per `signature-assessments.md`. |
| CIS 320 (Y2 Fall) | Bounded exposure — requirements-driven design and UX validation at CIS 320's every-student-gets-this-once scope. **UX research methods and real-user validation at full depth are Software Architecture specialization-elective content**, not core. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Design Brief (human-centered lens) — design an accessible interface or experience for a specified user and scenario |
| Independence | Open-ended Design Brief — given a problem and a user population, design a human-centered solution without a template |
| Adaptation | CIS 320's bounded design-for-real-users work, within the core's own scope. (The old "System Integration Project" ceiling — designing for real users with ambiguous needs and iterating on validation results — is specialization-elective depth, not a core event.) |
| Leadership | Design Review critique (TA/LA role) — evaluating whether a peer's design genuinely serves human needs; leading UX evaluation sessions |

**Recurring types:** Design Brief (creating a human-centered solution) and Usability Evaluation (assessing an existing design against human-centered criteria) — see below.

**Second recurring type — Usability Evaluation:**

| Course | Pass | Scale & Challenge |
|--------|------|-------------------|
| CIS 120 (Y1 Fall) | Accessibility audit — evaluate an existing page against accessibility criteria (contrast, keyboard navigation, screen reader). Confirmed. | Checklist-guided, single page |
| CIS 320 (Y2 Fall) | Component usability evaluation — does this component's interface make sense from the user's perspective? Unconfirmed, proposed. | Interface design, less scaffolding |
| CIS 400 (Y2 Spring) | Design Review — peers evaluate each other's system designs for human-centeredness and usability fit. | Peer-facing, multi-dimension |
| CIS 320 (Y2 Fall) | Heuristic evaluation, A/B analysis against acceptance criteria. Confirmed — CIS 320's real, bounded FITNESS content. **Full user-testing-sessions-with-real-users depth is Software Architecture specialization-elective content**, not core. | Real users, novel system *(elective, not core)* |

---

### Evaluate Ethical Implications

**I can evaluate the ethical, social, and professional implications of computational decisions and actions.**

I apply ethical reasoning to identify risks, responsibilities, and consequences when designing and using computational systems.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 120 (Y1 Fall) | First pass — data minimization as an embedded constraint: what data should this pipeline collect, and why? Accessibility as ethical obligation. The CIS 200 half of this old claim is thin — the confirmed carrier is CIS 120. |
| CIS 300 / CIS 320 (Y2 Fall) | Conway's Law seed — organizational structure shapes what gets built and who it serves. **Unconfirmed** — same client/server-vehicle documentation gap already logged in `thread-sociotechnical.md`. |
| CIS 260 (Y1 Spring) | Schema ethics — access control and data minimization decisions documented and justified; least-privilege at the data layer. Confirmed design intent, undrafted — see `cis-260.md`'s "Proposed Changes." |
| CIS 251 (Y2 Fall) | Threat identification, authentication, authorization; least data collection as a security and ethical principle. Confirmed against CIS 251's real SLOs. |
| CIS 400 (Y2 Spring) | Responsibility retrospective — the team project includes an assessed, individually-written ethical accountability reflection. Confirmed. |
| *unplaced* | Re-identification risk — combining individually innocuous datasets creates privacy harms neither dataset posed alone. Same orphaned data-integration content flagged throughout this pass. |
| CIS 400 (Y2 Spring) | Harden-before-live as ethical practice. Confirmed. **Blameless postmortem as systemic accountability has moved to the Year 3–4 capstone** — see `signature-assessments.md`. |
| CIS 141 (Y2 Spring) / *unplaced* | AI-generated code critique for correctness, security, and responsible use — confirmed, CIS 141 is the terminal pass for the AI-Assisted Development bounded practice. Broader data-ethics/honest-visualization framing beyond the AI-critique slice is unconfirmed (honest visualization itself is resolved elsewhere — see `competencies/data-and-information.md` — but the combined "data ethics + AI critique" framing this row implies isn't a single confirmed course pass). |

Note: ethical reasoning in this program is grounded in concrete technical decisions — data minimization, access control, re-identification risk, honest visualization — rather than abstract philosophical frameworks. The escalation is from single-decision ethics (CIS 120) through AI-assisted development ethics (CIS 141), with the team-level accountability ceiling now split between CIS 400 (responsibility retrospective, core) and the Year 3–4 capstone (blameless postmortem).

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured ethical analysis — given a system and context, identify ethical risks and responsibilities using a provided framework |
| Independence | Open-ended ethical evaluation — given a design decision, independently construct an ethical argument without a framework |
| Adaptation | Responsibility retrospective (CIS 400) — evaluate ethical responsibilities in a real collaborative project, within the core's own scope. (Blameless postmortem, the old co-anchor, is now Year 3–4-capstone-level.) |
| Leadership | Leading responsibility retrospectives; TA/LA facilitating ethical discussion in Design Review (CIS 400). (Leading blameless postmortems is now Year 3–4-capstone-level.) |

**Recurring type:** Ethical Evaluation — deepens from data minimization analysis (CIS 120) through AI-assisted analysis critique (CIS 141). Escalates from single-decision ethics → design ethics → system ethics → AI ethics; full integration-scale ethics (re-identification, blameless postmortem) is unplaced or relocated, not a confirmed core ceiling.

---

### Communicate Technical Information

**I can communicate technical concepts, decisions, and results to technical and non-technical audiences.**

I create documentation, presentations, visualizations, and explanations that support understanding and informed decision-making.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 200 (Y1 Spring) | Type annotations and interface specifications — the type signature communicates a contract to peer developers; first explicit technical documentation. |
| CIS 260 (Y1 Spring) | Schema-decision documentation — documenting design choices and their rationale for future maintainers. Confirmed design intent, undrafted. |
| CIS 400 (Y2 Spring), formalized (woven throughout) | Test naming and documentation — what does this test guarantee, and for whom? |
| CIS 400 (Y2 Spring) | PR descriptions, commit messages, code review comments — professional asynchronous technical communication. |
| CIS 400 (Y2 Spring) | Design Review — present and defend technical decisions to a critical peer and faculty audience; highest-stakes synchronous technical communication within the core. Re-homed to CIS 400 per `signature-assessments.md`. CIS 501's confirmed "present and defend a design" pass is an even higher-stakes later instance of the same skill. |
| CIS 400 (Y2 Spring) | Operational runbooks and API documentation — technical communication that outlives the author and must be read under pressure. |
| CIS 320 (Y2 Fall) | Stakeholder communication — translate technical constraints and design decisions for non-technical decision-makers, at CIS 320's bounded scope. **Full depth is the same Software Architecture specialization elective** flagged throughout this domain. |

Note: automated evidence (git telemetry) captures the presence of commit messages and PR descriptions but not their quality — this sub-competency requires rubric-based direct assessment at every touchpoint.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Technical documentation task — write API documentation, a PR description, or a test name for a specified audience and purpose |
| Independence | Audience-appropriate explanation — given a technical concept or decision, produce documentation appropriate for a specified audience without a template |
| Adaptation | Design Review (CIS 400) — defend technical decisions under live critique; CIS 320's bounded stakeholder translation. (Full stakeholder-translation depth with real, consequential decision-making is specialization-elective content.) |
| Leadership | TA/LA creating learning materials for students; writing runbooks adopted by a team; leading documentation sprints |

**Recurring type:** Technical Explanation Task — deepens from type-annotated interface docs for a peer developer (CIS 200) through CIS 400's Design Review and CIS 320's bounded stakeholder translation. Audience escalates: peer developer → future maintainer → team → critical panel → non-technical stakeholders (specialization-elective depth for the last step).
