# Computer Science

This is a proposed degree map based on the revised 2-year curriculum created from our existing degree map. Note this is reported in 16-week semesters, not 8-week blocks.

**Note on repeated K-State Core codes (2026-07-14):** KSC 050 (Social & Behavioral Sciences) and KSC 060 (Arts & Humanities) each appear twice in this map — that's correct, not a duplicate-entry error. Both are 6-hour categorical requirements under KBOR's seven-bucket general-education framework (kansasregents.gov/academic_affairs/general-education/seven-bucket-framework), normally satisfied by two separate 3-credit courses each.

## First Year

### Semester 1

#### CIS 115  - Introduction to Computing Science

*1 or 2 credits, to be refactored as needed as part of the revision.*

This course contains computing history and a broad overview of the field of computing with the goal of introcuding much at the surface level that will be picked up more deeply in later courses. It is completely up for revision/adapatation.

Confirmed (2026-07-13): v1's CS-103 "Computational Representation" content moves here — an exploration of how digital computers work, run side-by-side with the history thread. Pulled from `content-archive/v1/course-designs/block-1/cs-103.md`: number representation as a design choice (Babbage's decimal mechanical engines vs. why electronic computers standardized on binary — this is the natural bridge between the history thread and the "how computers work" thread, not two unrelated topics), binary representation of integers/characters, Boolean logic and bitwise operations (originally scoped as the applied counterpart to MATH XXX Logic and Sets, same semester — the pairing still fits), and a simplified 8-bit float format worked by hand, plus the register/register-transfer model (load-operate-store). This is the required-content fix for the ABET "computer architecture & organization" gap (see design-log.md 2026-07-13 coverage check).

**Not included in this move, still unplaced:** CS-103 also carried a stack/heap notional-machine formal assessment pass and a process-execution/OS seed (a running program as an OS-scheduled process), cross-referenced in v1 against CS-101/102's own memory-model and concurrency content. Those two pieces are closer to the still-open "operating systems" ABET gap than to "how digital computers work," and CIS 115 (a history/overview course) may not be the natural home for them — not decided here, flagged for a separate decision. CS-103's git-history capstone assessment also isn't addressed by this move.

**Credit-density flag:** v1's own assessment called CS-103 "the densest of the three B1 courses" as a *full 1-credit course*, and the content moving here is most of that course (minus stack/heap and the process seed). Landing it inside CIS 115 on top of the existing history/overview content is a real density question, similar to the CIS 260 flag — worth watching once this gets built out, not resolved here. CIS 115's credit hedge ("1 or 2 credits") should probably resolve toward 2 given this addition, but that's not decided either.

**Processor-architecture touchpoint, seeded here (2026-07-14):** the register/register-transfer model above is a CPU-shaped notional machine. Add a light, named-awareness touch (same treatment as the logic-programming "see and explore" pattern, not deep instruction): CPUs are one architecture among several, built for general-purpose control flow with a handful of powerful cores; other architectures exist because different workloads want different tradeoffs. Deepens in CIS 200/300 (CPU vs. GPU execution models, paired with the parallel-processing norm) and CIS 141 (GPU/TPU specifically for AI/ML workloads) — see those entries.

**CS-theory touchpoint, seeded here (2026-07-14):** a single unit on computability theory (confirmed already a fit for this course's breadth-survey character) — awareness-level, e.g. the halting problem as a concrete instance of "some problems have no algorithm that solves them," not formal proof. This is the entry point for the ABET "computer science theory" gap's computability sub-area, deepened in CIS 301 (decidability as the ceiling on formal verification) and CIS 575 (P vs. NP, elective depth). See design-log.md 2026-07-14.

#### CIS 116  - Introduction to Programming

*2 credits, likely will need to continue to be taught in smilar form; an important service course for other departments. Needs to contiue to serve as eqivalent to KBOR CSC1020.*

A traditional first programming course for students with no prior experience in programming.  Taught in Python.

#### DEN 161 - Engineering Problem Solving

*1 credit, controlled by the College of Engineering*

This is a creative thinking and problem-solving course.  While not CS-specific, the ways of thinking it teaches are very much useful to a CS student.

#### CIS 120 - Web Foundations

*1 credit, a new course that is part of the proposed core packaging*

This would be an introductory course in HTML, CSS, and JavaScript.  Intended to introduce students to web interfaces, as we will use those as the primary visualizaiton/GUI tool in later courses.

#### MATH XXX - Logic and Sets

*1 credit, first 8 weeks of the semester. New discrete math content being developed for the core*

Sets and logic. Topics include:

1. Propositional Logic
2. Truth tables
3. Equivalence
4. Normal forms
5. Clauses
6. SAT
7. Sets
8. Functions
9. Relations

#### MATH XXX - Counting Finite Configurations

*1 credit, second 8 weeks of the semester. New discrete math content being developed for the core*

Topics include:
1. Sets
2. Finite cardinality
3. Counting principles
4. Inclusion-exclusion
5. Pigeonhole principle
6. Permutations
7. Combinations
8. Binomial Coefficients  

#### ENGL 100  - Expository Writing I

*3 credits, part of the K-State core required of all students, KSC 010.*

A first college course in English composition.

#### Core Communication Requirement

*3 credits. Part of the K-State core required of all students, KSC 020.*

*(Social & Behavioral Sciences Requirement, KSC 050, relocated to Y2S2 — 2026-07-14, credit-balancing pass. See design-log.md. The other KSC 050 course stays in Y3S1 per KBOR's seven-bucket framework, which requires two.)*

			
### Semester 2			

#### CIS 260 - Foundations of Relational Databases

*1 credit, proposed course for the new two-year core. Will also serve as a service course paired with external "application" courses.*

Density concern flagged (2026-07-13), held at 1 credit for now: the anticipated content/schedule in `kstate-catalog/cis-260.md` (8 modules — DB overview, single-table queries, joins, subqueries, table expressions/views, database design, data modification, final practical) covers what v1 split across two separate 1-credit courses (CS-201 SQL Fundamentals + CS-202 Database Design). User has decided to hold this at 1 credit rather than grow it to 2, but the density concern stands and should be watched — trimming (database-design theory is the clearest candidate to defer elsewhere) may be needed once this gets built out to block-file completeness. No KBOR course maps to CIS 260 — full freedom on scope/credit if this needs revisiting later.

#### CIS 220 - Platform Programming

*1 credit. New course, added 2026-07-13. Prerequisite: CIS 120.*

**Reframed 2026-07-15 — generic catalog identity, specific curriculum design.** Catalog-facing name, description, and learning outcomes are deliberately platform-agnostic, so this course number can host different platform *sections* (Web, Mobile, Desktop) in the future without needing a new catalog entry each time — only the section syllabus changes, not the approved course. The curriculum design below is specific, as it should be: the two-year core runs the **Web section**, and everything that follows describes that section's actual content.

*Proposed catalog description*: "Programming against an interactive computing platform's execution and event model — how the platform schedules code, isolates security boundaries, and supports concurrent and asynchronous behavior. Sections focus on a specific platform (e.g. web, mobile, desktop); consult the section syllabus for the platform and tools used."

*Proposed catalog learning outcomes (generic)*: explain how an interactive platform schedules and executes code (event-loop/message-queue model); reason about the platform's security/isolation boundaries; write programs that respond to asynchronous events and coordinate concurrent work using platform-appropriate mechanisms; manipulate a platform's structured content/state model programmatically.

**Web section curriculum (what the core actually teaches):** a deeper dive into JavaScript, event-driven programming, and DOM manipulation, building on CIS 120's HTML/CSS/JS seed. Carries v1's "browser as a mini-OS" framing (from `content-archive/v1/course-designs/block-2/cs-106.md`): the event loop schedules your code, origins are isolated as a security/process boundary, web workers run concurrent work, `postMessage` is IPC — a concrete, familiar on-ramp to operating-system concepts. This is the required-content fix for the ABET "operating systems" gap (see design-log.md 2026-07-13 coverage check), at the "exposure" level the criterion actually asks for (a lower bar than the "substantial coverage" language used elsewhere in the same criteria).

Also serves as real prerequisite depth for CIS 320 (User Experience Development, Web section) (Y2S1) — understanding vanilla JS/DOM/events before a component-based UI library sits on top of them is a stronger sequence than learning a framework cold. Positioned here specifically to close the Y1S2 spacing gap identified earlier (see design-log.md 2026-07-13) with real content rather than a light touchpoint — supersedes the touchpoint previously added to CIS 200's entry, now removed.

**CS-theory touchpoint (2026-07-14):** a light formal-languages callout — the browser parses HTML against a formal grammar; worth one line naming that explicitly (not a unit) when DOM parsing comes up. Free content, not new instructional time — the connection is already latent in what this course teaches. Part of the same ABET "computer science theory" coverage as CIS 115/301/505/575/225/200/300, below.

#### CIS 200  - Programming Fundamentals

*3 credits (confirmed 2026-07-13, reduced from 4 — see design-log.md shakedown). Another course that will be heavily refactored for the two-year core.  Needs to continue to serve as equivalent to KBOR CSC1030.*

Redesign direction (2026-07-13, confirmed): Windows Forms and Visual Studio are dropped completely — no native-GUI unit. GUIs across the two-year core are largely HTML-based instead (see CIS 120 / the planned client-side course). Language not yet decided, but must be object-oriented, likely from the C++/Java/C# family — expect a language switch relative to CIS 116 (proposed in Python), so some early-week time remains legitimate syntax onboarding even though the underlying concepts (variables, conditionals, loops, arrays) are review from CIS 116. Inheritance must be required content (currently optional in the existing Fall 2024 offering, per `kstate-catalog/cis-200.md`) — CSC1030 outcome 1 requires it explicitly.

Confirmed (2026-07-13): parallel processing is woven throughout CIS 200 (paired with CIS 300, below) — this is the required-content fix for the ABET "parallel & distributed computing" gap flagged in the 2026-07-13 coverage check (see design-log.md). Specific weaving points not yet scoped at block-file level.

Processor-architecture touchpoint (2026-07-14): CPU multi-threading — a handful of powerful cores, control-flow-heavy, the model CIS 200's own parallel-processing content is built around — is the concrete contrast point for the GPU/TPU touch deepened in CIS 141. Seeded conceptually in CIS 115 (register/register-transfer model, above).

CS-theory touchpoint (2026-07-14): wherever regex/pattern-matching is taught as a practical string-processing tool, name explicitly that a regex is a finite automaton under the hood — the automata-theory sub-area of the ABET CS-theory gap, applied rather than invented. Same treatment in CIS 300 if the fit lands better there instead.

#### ECE 241  - Introduction to Electrical and Computer Engineering

*3 credits, controled by Computer Engineering. Potentially removable in updated curriuclum, but politically tricky. Might be convertable to an elective.*

Focus on  programming Arduino and similar devices.

#### Calculus Slot

*4 credits. Placeholder for calculus course, most likely MATH 220  - Analytic Geometry and Calculus I, but some students may come with high school credit and be ready for Calculus II or III. Also fulfils K-State Core requirement KSC 030.*

Choose one of:

- Calculus I,
- Calculus II,
- Calculus III

#### MATH XXX - Recursive and Modular Computation

*1 credit, first 8 weeks of the semester. New discrete math content being developed for the core.*

Topics include:

1. Recursion relations
2. Recursive definitions
3. Arithmetic, Geometric, and Logistic Sequences
4. Modular arithmetic
5. Common divisors
6. Fundamental Theorem of Arithmetic
7. Euclid’s Algorithm

#### MATH XXX - Graphs, Trees, and Maps

*1 credit, second 8 weeks of the semester. New discrete math content being developed for the core.*

Topics include:

1. Basic Vocabulary of Graphs 
2. Weighted graphs 
3. Shortest paths 
4. Traversals 
5. Euler paths 
6. Hamiltonian paths 
7. Matrix representations of graphs 

#### ENGL 200  - Expository Writing II

*3 credits, part of the K-State core required of all students, KSC 010. Many students will have credit from high school.*

A second college course in English composition.

## Second Year

### Semester 1

#### CIS 300  - Data and Program Structures

*3 credits. Will be subject to refactoring under the new core. Needs to provide equivalence with KBOR 1040.*

A traditional data structures course.

Redesign direction (2026-07-13, confirmed): Windows Forms and Visual Studio are dropped completely here too, per the same program-wide decision as CIS 200 — the current course's desktop Windows-Forms practice vehicle goes away entirely. This is a vehicle swap, not a content cut: KBOR CSC1040's required outcomes (lists, linked lists, stacks, queues, trees, hash tables, sets, dictionaries, heaps, graphs; sorting/searching/tree/graph algorithms; complexity analysis; generics/interfaces/indexers/enumerators) are unchanged. The new practice vehicle is a server layer in a client/server web architecture — leveraging files, databases, and APIs as data sources, with HTML forms for input — deliberately paired with the new client-side course (see design-log.md 2026-07-13) as the same system boundary taught from both sides.

Confirmed (2026-07-13): CIS 300's purview now explicitly includes **concurrent algorithms and thread-safe data structures**, alongside the sequential CSC1040 baseline. This pairs naturally with the server-layer vehicle above — a server fielding concurrent requests is a real, motivating instance of the concurrency problem, not a bolted-on unit. This is the required-content fix for the ABET "parallel & distributed computing" gap (see design-log.md 2026-07-13 coverage check) — CIS 625 (Concurrent Software Systems, the Y4 Systems Elective option) now sits on top of this as legitimate elective depth, the same pattern already established for CIS 560/575, rather than being the only source of parallel-computing exposure.

Processor-architecture touchpoint (2026-07-14): thread-safe data structures assume a CPU's shared-memory model (a handful of cores, coherent shared memory) — worth naming explicitly that this assumption doesn't hold on a GPU, where thousands of simple cores execute the same instruction across different data (SIMD/SIMT) rather than running independent threads. Not deep GPU programming — a contrast point that sharpens what "concurrent" actually meant in the CPU-shaped content just above. Deepened further in CIS 141 for AI/ML-specific hardware (GPU/TPU).

CS-theory touchpoint (2026-07-14): the regex-as-finite-automaton callout from CIS 200 lands here too if string-processing/pattern-matching content fits better in this course's data-structures context — one or the other, not necessarily both; see CIS 200's entry.

Open, not yet decided: "design patterns" (in the current topic blurb, not a CSC1040 outcome) is a soft cut/move candidate — CIS 400 or CIS 501 look like more natural homes. CSC1040 outcome 5's "indexers and enumerators" is C#-specific idiom, which may bias the still-undecided CIS 200/300 language choice toward C# to keep the transfer-equivalence claim clean. Also unverified: the current course's topic blurb omits graphs/heaps/sets/dictionaries/priority queues that its own SLOs list — worth checking against the actual syllabus rather than trusting the blurb, same pattern as CIS 200's optional-inheritance gap.

#### CIS 320 - User Experience Development

*1 credit. New course, added 2026-07-13. Prerequisites: CIS 120, CIS 200 (matches CIS 300's own prerequisite chain, since co-scheduled with it), and CIS 220 (Platform Programming, Web section) (added 2026-07-13 — vanilla JS/DOM/event fluency before a component library sits on top of it).*

**Reframed 2026-07-15 — generic catalog identity, specific curriculum design.** Same treatment as CIS 220: the catalog name, description, and learning outcomes are platform-agnostic, so this course number can host Web, Mobile, or Desktop UX sections in the future without a new catalog entry. The curriculum design below is specific to the **Web section**, which is what the two-year core runs.

*Proposed catalog description*: "Building user-facing interfaces using a component-based architecture, consuming data from a provided service layer, with an introduction to validating a design against user needs. Sections focus on a specific platform (e.g. web, mobile, desktop); consult the section syllabus for the platform and tools used."

*Proposed catalog learning outcomes (generic)*: build a user interface from reusable, composable components; consume data from a provided service/API layer to populate and update an interface; apply accessibility and usability standards to an interface design; evaluate a design against a stated set of acceptance criteria.

**Web section curriculum (what the core actually teaches):** CIS 300's deliberate pair: same client/server system boundary, opposite side. This course is the *client* — consuming APIs from a provided/external server — while CIS 300 is the *server*, providing APIs consumed by a provided UI. Deepens CIS 120's HTML/CSS/JS seed with a component-based UI library (not yet chosen). Includes one bounded exposure to acceptance-criteria/A-B-testing process work — not a full requirements-gathering methodology, just enough that every student has the experience once. A full deep dive on acceptance testing is planned as a Software Architecture specialization elective instead (see design-log.md 2026-07-13) — less relevant to other specializations, but this course's bounded slice guarantees everyone gets at least one exposure.

Open, not yet decided: the specific component-library choice. The Y1S2 spacing gap this course's prerequisite chain used to rely on a light CIS 200 touchpoint for is now closed by CIS 220 (Platform Programming, Web section) instead (see design-log.md 2026-07-13).

#### CIS 301  - Logical Foundations of Programming 

*2 credits. May be broken up and placed in other courses as part of the refactor...* (2026-07-13: no clear case for cutting has emerged yet — see design-log.md shakedown; new goals below may absorb time freed elsewhere rather than reduce the total.)

Redesign direction (2026-07-13): the MATH XXX Logic and Sets / Counting Finite Configurations courses (Y1S1/S2) didn't exist when CIS 301 was first scoped — CIS 301 was carrying that introductory weight itself. Now that they exist, CIS 301 should **deepen** propositional/predicate logic and proof technique rather than re-introduce it — a genuine spiral revisit (apply logic to program verification), not redundant re-teaching. Purpose reframed: give every student at least a brush with formal verification, and enough depth for interested students to pursue it further. This resolves an open question from v1's `thread-correctness-verification.md` ("does verification need its own credit-bearing space?") — yes, here.

Two items **soft-flagged, not decided, pending faculty input:**
- Whether to introduce the logic programming paradigm (Prolog-style) as real practiced instruction, or keep the lighter "see and explore an example" touch already logged elsewhere in `design-log.md` (Rounds 28-29) as the standing decision — full logic programming was previously treated as specialization-only. Also unresolved: whether Prolog is even an intended core language at all (`.claude/agents/course-designer.md` still lists it as part of an established "multi-paradigm core," which later design-log entries call "NOT adopted").
- Possible use of a theorem prover as a course tool, to support the formal-verification goal. Not yet decided.

No KBOR course maps to CIS 301 (checked `resources/reference/kbor-transfer/`) — it carries no transfer-equivalence obligation, unlike CIS 116/200/300, and is fully free to restructure.

**CS-theory touchpoint (2026-07-14):** decidability/undecidability as the natural ceiling on the formal-verification goal above — "here's why you can't always automatically verify every property of every program" follows directly from what this course is already building toward, not a bolted-on unit. Deepens the CIS 115 computability seed; deepens further (P vs. NP, elective) in CIS 575. See design-log.md 2026-07-14.

#### Linear Algebra Slot

*3 credits. Placeholder for linear algebra course, which will vary based on student preparation and interest.*

Choose One of:

- MATH 350 - Scholars Math,
- MATH 515 - Linear Algebra,
- MATH 551 - Matrix Theory

#### CIS 225 - Foundations of Computer Networks

*1 credit. New course created for the two-year refactor. Will also serve as a shared introduction to other courses needing a grounding in networks housed in business and computer engineering.*

Coverage of the OSI 7-layer model, with exploration of HTTP/HTTPS and web sockets, some packet structuring.

**CS-theory touchpoint (2026-07-14):** protocol state machines (the TCP handshake/connection lifecycle) as a concrete, already-present instance of a finite automaton — a real system already in this course's scope, not an invented example. Second automata-theory touchpoint alongside the regex callout in CIS 200/300.

#### CIS 251 - Foundations of Cybersecurity

*1 credit.  New course for the core.*

**Home for authentication and authorization, confirmed 2026-07-13.** This isn't a new question — `content/core-design/lenses/lens-trustworthy-computing.md` (v1's security/privacy/ethics lens, kept as idea bank) already names its own FORMALIZED pass explicitly: "Authentication, authorization, threat modeling, applied cryptography... likely the primary ABET ethics anchor." CIS 251 is the new-map home for that formalized pass. Concrete anchors already in place, not invented for this note:
- **Applied cryptography ties to MATH XXX Recursive and Modular Computation** (Y1S2 — modular arithmetic, Euclid's algorithm — already scheduled *before* this course, correct prerequisite order, not a new dependency).
- **A ready-made concrete example**: `resources/reference/plant-sensor-api-roadmap.md` already flags its no-auth GET endpoint as "deliberately minimal... flagged as a future pairing point for whenever the core introduces a security/auth unit ('why would you not leave a write endpoint open the way this read endpoint is')." That pairing point is this course.
- **Same-semester reinforcement**: CIS 251 sits in Y2S1 alongside CIS 300 and the new CIS 320 (User Experience Development, Web section) — the client/server pairing is a natural place to *apply* authn/authz concepts practically (protecting server endpoints, consuming protected APIs, session/token handling), not just learn them in the abstract.
- **Later reinforcement**: CIS 400's capstone-of-the-core project (the historical archive) needs real contributor accounts — distinguishing historian/community-contributor edit rights from public anonymous viewing is a genuine, substantial application of what's learned here, at integration scale.
- Earlier, lighter touches already exist in the security/privacy thread too (CIS 115's representation-and-hiding question from the CS-103 content, CIS 260's schema-level access control) — CIS 251 is this thread's formalized capstone, not its first appearance.

#### Natural & Physical Sciences Requirement - with Lab	

*4 credits.  Required as part of the K-State core, KSC 040.*
			
### Semester 2			

#### CIS 141 - AI/Data Science

*1 credit.  New course to be developed as part of the 2-year core.*

**Processor-architecture touchpoint, deepened here (2026-07-14):** the natural home for GPU and TPU content specifically, completing the CPU (CIS 115, seeded) → CPU-vs-GPU parallel execution contrast (CIS 200/300) → GPU/TPU-for-AI escalation. Why AI/ML training leans on GPUs and TPUs: neural network training is dominated by matrix multiplication, an embarrassingly data-parallel operation GPUs' SIMD/SIMT design and TPUs' matrix-multiply-specialized ASIC design both accelerate directly, in a way general-purpose CPU cores don't. Conceptual/awareness-level, matching this course's other content — not a hardware-programming unit (no CUDA/kernel-writing expected at this credit size).

#### CIS 308  - C Language Laboratory

*1 credit. Might be replaced with any 1-credit programming language course?*

Introduction to the C programming langauge.

#### CIS 400  - Object-Oriented Design, Implementation, and Testing

*3 credits. Will be heavily refactored - likely will become mid-tier capstone course.*

**Redirection confirmed, 2026-07-13 — becomes a capstone of the core.** The prior version (a point-of-sale app built solo across a semester of 2-week sprints, each with a well-defined spec, several involving refactoring the growing codebase) is retired: AI can complete a well-defined-spec milestone without the student demonstrating understanding, and the course's own assessment (did the sprint meet its spec?) couldn't tell the difference. Per `content/pedagogy/ai-discipline.md`'s core principle — verification must be built into the assignment, not bolted on — the fix isn't banning AI, it's changing what's assessed.

New shape: a substantial, deliberately **ambiguous-requirements** team project (small teams, 2-4; formation method not yet decided — self-select vs. instructor-assigned still open) building toward the **historical archive** (the green-field replacement for the Chapman Center's commercial tool — see `resources/reference/real-world-assets-index.md` — not "Where Did They Go?", which is a live external project used only as motivating context, not a build target, to avoid the administrative risk of student teams touching a real shipping codebase). **Scope rotates by cohort** — each semester's teams tackle a different scoped slice/feature of the eventual system, confirmed deliberately to keep requirements genuinely ambiguous and authentic rather than letting solutions go stale or get shared across cohorts.

This makes CIS 400 a **capstone of the core** — validating everything through the two-year core (CIS 200/300/260/225/251/301/141, the client-side pairing) before specialization — distinct in purpose from the Y4 program capstone, which validates the whole degree plus specialization work. Also **confirms CIS 400 as the team-project host** for the `professional-practice`/`sociotechnical-collaboration` re-homing table in `spiral-threads.md` (previously an unconfirmed proposal) — collaborative git/PRs, team-facing docs, shared conventions, code review as interpersonal skill, individually-written responsibility retrospective, estimation, all land here. AI is framed per the existing bounded-practice pattern (v1's old CS-206 frame, carried forward): a code-review participant, one input among several — never an implementer. Assessment leans on defended/oral components (live walkthrough, architecture defense) as the actual verification mechanism, not spec-compliance alone.

**This also resolved the Communication Elective cut's one open precondition** — that cut has since been executed (2026-07-14), see Y2S2 below.

#### Arts & Humanities Requirement

*3 credits, part of K-State core, KSC 060.*

#### STAT 410 - Statistics for Computing

*4 credits. New stats course developed to support the two-year core. Numbered 2026-07-15 — no conflict with any existing K-State STAT course.*

#### Social & Behavioral Sciences Requirement

*3 credits. Part of the K-State Core required of all students, KSC 050. Relocated here from Y1S1, 2026-07-14, credit-balancing pass — backfills the Communication Elective cut below. See design-log.md.*

**Cut executed, 2026-07-14: Communication Elective removed.** Communication and team-collaboration touchpoints have been re-homed across CIS 116/200/260/300/400/501/Capstone via the `professional-practice` and `sociotechnical-collaboration` norms — see `resources/reference/spiral-threads.md`'s 2026-07-13 re-homing table. CIS 400's role as the team-project host (capstone of the core, historical-archive team project) confirmed the precondition for this cut. Formerly: 3 credits, choice of COMM 323, COMM 326, MANGT 220, THTRE 171, or THTRE 265.

## Third Year

### Semester 1

##### CIS 450  - Computer Architecture and Operations

*3 credits. May become an elective in new program as some content migrates down to earlier courses.*

#### CIS 501  - Software Architecture and Design

*3 credits. Probably will be shifting focus to incorporate more AI usage as a development tool.*

#### CIS 505  - Introduction to Programming Languages

*3 credits. Leaning required (2026-07-14) — not fully settled, but no longer just "may become an elective." Confirmed as the home for most of the core's formal-language content (grammars, parsing) — the required-content anchor for the ABET "computer science theory" formal-languages sub-area. See design-log.md 2026-07-14.*

#### Technical Writing Requirement

*3 credits.*

#### Social and Behavioral Sciences Requirement

*3 credits. Fulfills K-State Core KSC 050.*

### Semester 2

#### CIS 560  - Database System Concepts

*3 credits. May become an elective.*

**CS-theory touchpoint (2026-07-14):** P vs. NP and NP-completeness as the elective-depth capstone on the computability arc seeded in CIS 115 and deepened in CIS 301 — same "required foundation, elective depth" pattern already used for CIS 560's relationship to CIS 260.

Deeper coverage of relational databases, relational agebra, no-sql databases.

#### CIS 575  - Introduction to Algorithm Analysis

*3 credits. May become an elective.*

#### CIS 415  - Ethics and Conduct for Computing

*3 credits. May reduce to 1 as ethics is integrated into the core.*

#### Unrestricted Elective

*3 credits. Any course.*

#### Free Elective

*3 credits. Fulfils K-State Core requirement KSC 070.*

## Fourth Year

### Semester 1

#### Systems Elective

*3 credits. Fufils ABET networking and OS requirements; may become a regular tech elective instead.*

Choose one of the following:

- CIS 520 - Operating Systems I Credits: 3
- CIS 525 - Introduction to Network Programming Credits: 3
- CIS 625 - Concurrent Software Systems Credits: 3

#### Required Technical Elective

*3 credits.*

Any CIS course at the 500-level or above OR any of the following:
- DEN 590 Interdisciplinary Engineering Capstone Design Experience I
- ECE 542 Computer Networking
- GEOG 602 Computer Mapping and Geographic Visualization
- MATH 615 Digital Image Processing
- MATH 620 Convex Optimization for Data Science
- MATH 655 Elementary Numerical Analysis I
- MATH 656 Elementary Numerical Analysis II
- MATH 725 The Mathematics of Data and Networks I
- MATH 726 The Mathematics of Data and Networks II
- MIS 670 Social Media Analytics and Web Mining

#### Required Technical Elective

*3 credits.*

Any CIS course at the 500-level or above OR any of the following:
- DEN 590 Interdisciplinary Engineering Capstone Design Experience I
- ECE 542 Computer Networking
- GEOG 602 Computer Mapping and Geographic Visualization
- MATH 615 Digital Image Processing
- MATH 620 Convex Optimization for Data Science
- MATH 655 Elementary Numerical Analysis I
- MATH 656 Elementary Numerical Analysis II
- MATH 725 The Mathematics of Data and Networks I
- MATH 726 The Mathematics of Data and Networks II
- MIS 670 Social Media Analytics and Web Mining

#### Arts & Humanities Requirement

*3 credits.*

#### Unrestricted Elective

*3 credits. Any course.*
			
### Semester 2			

#### Required Technical Elective

*3 credits.*

Any CIS course at the 500-level or above OR any of the following:
- DEN 590 Interdisciplinary Engineering Capstone Design Experience I
- ECE 542 Computer Networking
- GEOG 602 Computer Mapping and Geographic Visualization
- MATH 615 Digital Image Processing
- MATH 620 Convex Optimization for Data Science
- MATH 655 Elementary Numerical Analysis I
- MATH 656 Elementary Numerical Analysis II
- MATH 725 The Mathematics of Data and Networks I
- MATH 726 The Mathematics of Data and Networks II
- MIS 670 Social Media Analytics and Web Mining

#### Capstone

*3 credits.*

Choose one of the following:

- CIS 598 - Computer Science Project Credits: 3
- CIS 643 - Software Engineering Project II Credits: 3
- DEN 591 - Interdisciplinary Engineering Capstone Design Experience II Credits: 3

#### Upper Division Elective

*3 credits.*

Any courses at the 300 level or above.

#### Upper Division Elective

*3 credits.*

Any courses at the 300 level or above.

#### Upper Division Elective

*3 credits.*

Any courses at the 300 level or above.