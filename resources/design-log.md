# Spiral Curriculum Planning

## What makes a spiral pass legitimate (not just repetition)
A return to a topic should do at least one of:
- Apply it in a harder/messier context than before
- Combine it with a topic introduced since the last pass
- Reveal a limitation/edge case of the earlier simplified treatment
- Shift the lens (e.g. from "how do I do this" to "how do I judge whether this was done well")

If a "spiral" pass doesn't do one of these, it's just review, not a spiral.

## Major topic strands to trace through current 8 blocks

### 1. PROGRAM CORRECTNESS / WHAT IS THIS CODE DOING
- B1: write small correct programs (control structures, functions) - lens: "make it work"
- B2: read OTHERS' code, explain unfamiliar behavior (Code Archaeology) - lens: "understand it before judging it"
- B3: OOP correctness (encapsulation/abstraction as correctness tools, not just organization)
- B6: testing as FORMAL verification of correctness, not eyeballing - lens: "prove it works systematically"
- B7: Design Review - defend correctness of structural choices to peers - lens: "justify it under scrutiny"
- Gap: no explicit "correctness under failure/edge cases" pass until testing in B6 - could seed earlier (e.g. B1/B2 already touch debugging which IS edge-case correctness, just not named as such)
This is actually a strong spiral already: make it work -> understand others' -> organize for correctness -> verify systematically -> defend publicly. Good throughline, just needs to be NAMED as a thread in the doc.

### 2. DATA STRUCTURES & REPRESENTATION
- B1: bits/booleans/numbers - the most primitive representation
- B3: linear structures (lists/stacks/queues) - lens: "representation as sequence"
- B3/4: trees/hashing - lens: "representation as hierarchy/lookup"
- B4: persistence (files) - lens: "representation that survives the program ending"
- B5: relational data (SQL/schema) - lens: "representation as a formal queryable model"
- B7: graphs - lens: "representation as arbitrary relationship, the most general case"
- B7: document/NoSQL - lens: "representation when the formal relational model doesn't fit"
This is a genuinely strong, ALREADY GOOD spiral: primitive -> sequence -> hierarchy -> persistent -> formally modeled -> arbitrarily connected -> irregularly shaped. Each step is a real generalization of the last. Worth highlighting as the flagship spiral in the doc.

### 3. SECURITY
- B1: implicit only (bits/booleans -> binary representation underlies everything, but no explicit security framing) - WEAK, not a real pass yet, just foundation
- B5: modular arithmetic -> sets up crypto but isn't security content itself
- B6: dedicated security course - first REAL pass: authn/authz, threat ID, crypto applied
- B6 (same block): least-privilege extended to data collection
- B7: data integration has "light" security touch per original doc - this is vague, not a real spiral pass
- B8: deployment has "light" security touch - also vague
PROBLEM: Security spirals ONCE (B6) then trails off into vague "light touches" that aren't really designed passes. This is the weakest spiral in the current design and should be fixed. A real spiral would have:
  - an EARLY naive pass (e.g. B2 or B4: "here's a system with an obvious vulnerability, find it" - no formal vocabulary yet, just intuition)
  - B6: formal vocabulary and systematic treatment (current)
  - a LATE pass that's harder: B7 or B8 should have a real assessed security task, not just a "touch" - e.g. B8 deployment could include "harden this before it goes live" as an actual graded task, not a mention

### 4. APIs / NETWORKED SYSTEMS
- B2: consume a basic API (read-only, simple)
- B4: BUILD an API + consume own API + visualize results (more complex, two-directional)
- B5/7: data integration - combining MULTIPLE data sources, which implies multiple APIs/sources at once
- B8: deploy a service that presumably exposes/depends on APIs
Decent spiral: consume -> build+consume -> integrate multiple -> operate in production. Could be named more explicitly.

### 5. HCI / ACCESSIBILITY / HUMAN-FACING DESIGN
- B2: HTML/CSS + accessibility basics, single static page, single user in mind
- B4: SVG visualization - still single page, but now dynamic/data-driven
- B7: Design Review should include usability defense (per last doc's recommendation) - lens shifts to JUSTIFYING design to others
- B8: formal UX/requirements gathering - lens: design FOR others' needs, not just compliance with accessibility checklist
Decent spiral: build accessibly -> extend to dynamic data -> defend choices -> design from others' requirements outward. The shift from "checklist compliance" (B2) to "requirements-driven design" (B8) is a real depth change, not just repetition - worth naming explicitly.

### 6. COLLABORATION / TEAMWORK / GIT
- B2 (implicit, "intro Git" was mentioned in earlier planning but not in final doc actually - CHECK)
- B6: Collaborative Development course - Git workflows, code review, Team Software Project begins
- B7/8: Team Software Project continues
WEAK: this spirals only once with continuation, not really repeated independent passes. Git/version control as a SKILL should probably have an earlier solo pass (using git for your OWN work, B1 or B2) before the B6 collaborative/team pass. Currently Git isn't explicitly placed until B6 which is late and conflates "learning version control" with "learning to collaborate using version control" - these are different skills.

### 7. TESTING / VALIDATION
- B4: "Validate" listed as recurring experience but not a dedicated course until B6
- B6: dedicated Software Testing & Validation course
- B8: implied validation in deployment/operations context
WEAK similar to Git: testing doesn't have an early informal pass. Students debug in B2 but debugging != testing. An early "does this code do what I think it does, how would I check" informal pass (even just embedded in B1/B2) would set up B6's formal treatment much better.

### 8. ALGORITHMIC THINKING / COMPLEXITY
- B3: Big-O, complexity, paired with discrete counting
- B7: applied to graphs (harder structures = harder complexity reasoning)
- Could use a pass where complexity reasoning is applied to a REAL system bottleneck (B8 performance analysis exists in the original architecture as a phrase but isn't a real pass)
Decent but could be strengthened by making B8's "performance analysis" mention into a real spiral pass: revisit Big-O reasoning but now applied to an actual deployed system's bottleneck, not toy examples.

### 9. AI-ASSISTED DEVELOPMENT
- Per last doc: should be modeled as habit from B1, explicit skill in B8
- Currently this is a STANCE not a designed spiral - "model it as a norm" isn't the same as "here are 3 deliberately different passes with increasing sophistication of judgment required"
Could become a real spiral:
  - B1/B2: use AI to explain/read code you didn't write (low stakes, supports the Code Archaeology spiral too)
  - B4/B5: use AI to brainstorm design alternatives, but human picks/justifies (medium stakes)
  - B8: verify/critique AI-generated solutions for correctness AND security (high stakes, converges with security spiral)
This could be one of the more interesting EXPLICIT spirals to design well, since it's genuinely new pedagogical territory and not just an old CS curriculum that already does this.

## Summary of strength assessment
STRONG existing spirals (just need explicit naming/visualization): Data Structures & Representation, Program Correctness, APIs/Networked Systems
MODERATE existing spirals (need 1 more deliberate pass each): HCI/Accessibility, Algorithmic Thinking
WEAK spirals (need real redesign): Security (trails off into vagueness), Collaboration/Git (only one real pass), Testing (only one real pass), AI-assisted development (stance not design)

## Implication for block placement
The weak spirals (testing, git, security) all currently lack an EARLY informal pass. Pattern: each was bolted on as a single dedicated course in B6 rather than seeded early and revisited. This suggests B1-B2 are slightly under-loaded for "informal seeding" purposes relative to their role in the spiral - worth checking whether something can be embedded (not new credit) into existing B1/B2 courses to seed these three threads.

## USER-DIRECTED REDESIGNS (this round)

### GIT — full redesign per user direction
- B1: Git as a HISTORY/ARCHAEOLOGY tool, not yet a workflow tool. Explore an existing repo's history (log, diff, blame), connect to semantic versioning (what does a version number COMMUNICATE about change). This pairs naturally with B1's existing "Computational Representation" framing AND foreshadows B2's Code Archaeology - you're literally reading history as a form of reading code. Good convergence.
- B2 (the "modification block" - this must mean wherever students start MODIFYING code, which is debugging/repair in B2, or could mean B1's second half) - NEED TO CLARIFY which block user means by "modification block." Likely candidates: B2 (Code Reading & Debugging - students fix things, so committing/reverting fits) - this is my best guess, will confirm.
  - commit/revert added here: now git is a SAFETY NET for the repair work happening in this same block. Strong thematic fit.
- "sometime after" - feature branches/merges: this should land BEFORE team collaboration needs them, so probably mid-program, maybe B4 or B5, as a SOLO skill (branching to try an alternative approach safely) before it's a TEAM skill
- B6: collaborative git - code review, PRs, merge conflicts with OTHER people's changes. This matches existing B6 placement (Collaborative Development) - no change needed there, just now it's pass 4, not pass 1.

So Git spiral: B1 (read history, semantic versioning) -> B2 (commit/revert as safety net for repair) -> B4/B5 (branching, solo experimentation) -> B6 (collaborative, PRs, conflict resolution). FOUR deliberate passes instead of one. This is much stronger and doesn't cost new credits - it's embedded practice within existing courses.

### TESTING — full redesign per user direction
- B1: asserts, tests, and logs introduced as ways to EXPLORE existing code (not write from scratch) - this is an archaeology/comprehension tool first: "how do I figure out what this does" -> add print/log statements, write an assert to confirm a hypothesis about behavior. This is a great fit with B1 and reinforces the Git-history-as-reading-tool idea from the same block. Two reading tools introduced together: history (git log) and runtime behavior (asserts/logs).
- B2 (modification block, same clarification needed): tests used to VERIFY functionality and ensure changes don't break prior function - i.e., regression-testing mindset, introduced informally, before any formal "testing" vocabulary. This is the CLASSIC spiral move - using the practice before naming/formalizing it.
- B6: formal Software Testing & Validation course - now this is pass 3, formalizing what's already been informally practiced twice. Much stronger pedagogically - students aren't meeting "testing" cold in B6, they're getting a name and systematic treatment for something they've already done twice.

So Testing spiral: B1 (asserts/logs to understand code) -> B2 (tests to verify changes/prevent regression) -> B6 (formal testing methodology). THREE deliberate passes.

### CLARIFY "modification block"
Re-reading the original architecture: B1 = Programming Fundamentals (writing NEW small programs, not modifying). B2 = "Code Reading & Debugging I" - debugging IS modification (you read, find a bug, you CHANGE the code to fix it). This is almost certainly what the user means by "modification block." I'll proceed on this assumption and flag it as an assumption to confirm.

### SECURITY, PRIVACY, ETHICS — reframed as fully interleaved, not a separate spiral
User wants this NOT treated as its own spiral with its own passes, but rather as a LENS applied to every other topic as it comes up. This is actually a different design pattern than the others - not "revisit this topic with more depth" but "apply this lens every time ANY topic touches it." 
This means: instead of Security having dedicated B1/B6/B8 passes, security/privacy/ethics questions should be EMBEDDED as a recurring QUESTION asked within other topics' coverage:
- B1 (Computational Representation/bits): how does representation choice affect what can be hidden/obscured? (light, conceptual)
- B2 (Web Foundations / data collection): privacy-by-design in form fields (ALREADY EXISTS in current doc - good, keep)
- B3 (Data Structures): does choice of structure leak information (e.g. timing attacks via hash collisions) - light touch, optional enrichment
- B5 (Database Design): data minimization in schema (ALREADY EXISTS - keep), plus: who can see what (access control as a design dimension of the schema itself, not bolted on later)
- B6 (dedicated Security course): the formal/systematic treatment - this remains the deep dive, but now it's not the ONLY place security shows up, it's where the scattered threads get formalized
- B7 (Graphs/data integration): combining data sources raises NEW privacy questions (re-identification from combined datasets) - this is a real, meaningful, NOT generic security touch (much better than the old vague "light touch")
- B8 (Deployment): operating a live system raises NEW stakes (this is now real - "harden before going live" as discussed in original weak-spiral diagnosis)
This is a genuinely different and better pattern: security/privacy/ethics isn't "introduced then revisited at increasing depth," it's "asked as a standing question every time relevant content appears." I should represent this differently in the document - not as a spiral row but as a cross-cutting lens, with a explicit mapping table of "when this topic comes up, what's the security/privacy/ethics question."

### COMPUTATIONAL MODELS (NEW STRAND - not in original 9)
User wants: event loops, lightweight processes/threads, asynchronous code, parallelization seeded THROUGHOUT.
This is a significant addition - the original "notional machine" concept (People -> Requirements -> ... -> Processes -> Memory -> Files -> Networks -> Users) already names "Processes" as a layer, but the current course content never actually unpacks what a process/concurrency model IS. This is a real gap, not just an under-narrated existing thread.

Where does this fit in current blocks without new credit?
- B1: programs execute sequentially by default - this IS a computational model (the simplest one), should be NAMED as such even if implicitly taught. "Your program is a single sequence of steps" is the baseline model students should know they're using.
- B2: JS-based web work (HTML/CSS + consuming an API) is a NATURAL place to introduce the event loop / async concept, since fetch() is inherently async. Currently the course description doesn't mention this explicitly - "basic error handling" for API calls likely already touches callback/promise patterns informally. This could be elevated to an explicit "here's a different computational model" moment rather than just "here's how you call fetch."
- B4 (APIs & Visualization, building APIs): server handling concurrent requests is a natural moment to introduce "many things happening at once" conceptually (doesn't need implementation depth, just conceptual: a server doesn't process one request at a time necessarily)
- B5/7 (databases): transactions, concurrent access to shared data (two users editing the same record) - this is a REAL parallelism/concurrency concept (race conditions on shared state) that naturally arises from databases, good fit
- B6 (testing): concurrent/flaky tests, or could introduce lightweight processes/threads here if pairing with testing infrastructure
- B7 (graphs): could introduce parallel graph algorithms conceptually (e.g., "could multiple machines compute parts of this graph simultaneously?") - optional enrichment, probably too much for foundation year
- B8 (deployment/operations): THIS is where concurrency/scaling stakes become real - a deployed system handles multiple simultaneous users, monitoring shows concurrent load, performance analysis NOW has a "why is this slow under load" angle that ties directly to computational models. Strong natural fit.

So Computational Models spiral: B1 (naming the sequential model) -> B2 (event loop / async, concrete via fetch) -> B4 (server-side concurrency, conceptual) -> B5/7 (concurrent data access, race conditions) -> B8 (real production concurrency/scaling stakes). FIVE touchpoints, increasing from "name what you're already doing" to "reason about production-scale concurrent systems."

This is exciting because it's the SAME pattern as Data Structures (the strongest existing spiral): start with the simplest case (sequential), generalize repeatedly (async, server concurrency, shared-state races, production scale).

## OTHER GAPS USER ASKED ME TO IDENTIFY

Let me think about what's missing beyond what's been named.

1. ERROR HANDLING / FAILURE AS A FIRST-CLASS CONCERN
Currently "exception handling" appears once (B3, OOP II) and "error handling" appears once (B4, APIs). But failure handling is exactly the kind of thing that SHOULD spiral: B1 (what happens when a program crashes - read a stack trace, your first encounter with failure), B3 (formal exception handling vocabulary), B4 (error handling across a network boundary - failures you don't control), B8 (failure in production - monitoring, alerting, what does "the system is down" actually mean operationally). This is closely related to but distinct from Testing (testing tries to PREVENT failure, this is about HANDLING failure when it happens anyway) and distinct from Security (security failures are adversarial, this is about ordinary/expected failure). Worth naming as its own thread.

2. ESTIMATION / SCOPING / "HOW LONG WILL THIS TAKE"
Nothing in the current doc addresses professional estimation skills - how long will this feature take, how do you scope work. This is a real professional-practice gap. Could be lightly seeded in Team Software Project (B6-8) without needing new credit - probably not worth a dedicated spiral but worth flagging as an embedded-practice opportunity within existing team project work.

3. READING/INTERPRETING REQUIREMENTS (AMBIGUOUS OR CONFLICTING)
"Requirements gathering" appears once (B8, HCI course). But real requirements are often ambiguous, incomplete, or contradictory, and learning to handle THAT is different from learning to gather requirements the first time. Given the spiral philosophy, a second pass where requirements are deliberately ambiguous/conflicting (capstone-adjacent, maybe push to Year 3-4 rather than try to cram into this 2-year foundation) - I'll flag this as appropriately OUT of scope for the 2-year foundation rather than force it in.

4. DOCUMENTATION AS A SKILL (mentioned in original program competency example "I can produce technical documentation...") 
This doesn't appear ANYWHERE explicitly in the current 8-block design despite being the FIRST example competency statement given in the original project summary. This seems like a real gap - documentation should probably spiral too: B2 (document your own small program - comments, README), B6 (document for teammates - the stakes change when someone else depends on your docs), B8 (document a deployed system - operational documentation, different audience/purpose again). Worth flagging as a clear gap since it's literally the example competency in your original framework.

5. PERFORMANCE / EFFICIENCY AS LIVED EXPERIENCE VS THEORETICAL
B3 teaches Big-O as theory. The "implication for block placement" note from before already flagged that B8's "performance analysis" should become a REAL pass where complexity reasoning meets a real bottleneck. This connects directly to the NEW Computational Models thread (B8: why is this slow under concurrent load) - these two threads should probably converge at B8, not stay separate. Worth noting as a convergence point, not a new gap.

## CONVERGENCE POINTS WORTH HIGHLIGHTING (multiple spirals meeting at the same block)
- B1: Git-as-history-reading + Asserts/logs-as-behavior-reading + sequential computational model naming = "B1 establishes MULTIPLE reading/comprehension tools simultaneously, all in service of Code Archaeology's eventual formal treatment in B2"
- B2: Git commit/revert (safety net) + tests-for-regression (safety net) = "B2 introduces TWO different safety-net practices at the same time modification/debugging work begins" - strong thematic coherence
- B8: Computational models (production concurrency) + Performance/complexity (real bottlenecks) + Security (harden before live) + AI verification (high-stakes) = B8 is becoming a genuine "everything gets harder and real" capstone-adjacent block. This is GOOD for a capstone bridge but I should check it's not OVERLOADED - need to verify B8 still only has 3 courses and isn't trying to cram too much new content vs. just reframing existing content with higher stakes.

## ROUND 3 REFINEMENTS

### DOCUMENTATION — reframed as embedded practice (NOT a 3-pass spiral), same pattern as Security
User's framing: "whenever a student modifies or writes code, we expect them to document, with each new skill introduction bringing with it the practices for documenting that." This is a STANDING REQUIREMENT attached to every other thread, not its own spiral.
Concretely:
- B1: reading code -> explain it via BOTH inline comments AND a standalone explanatory document (two different documentation registers introduced together: code-adjacent vs. document-adjacent). This is more specific than what I had - I previously said B1 was about asserts/logs/git-history as reading tools; NOW documentation is a third reading/explaining tool introduced in the same block. B1 is getting dense - need to check course count isn't exploding (still embedded practice within CS-101/102/103, no new course, just explicit expectations).
- EVERY subsequent course, whenever NEW skill is introduced, documentation practice for THAT skill is introduced alongside it:
  - B2 (OOP, debugging, web): document classes/APIs as you build them (docstrings, API documentation conventions), document a bug fix (what was broken, why, what changed)
  - B3 (data structures): document algorithmic choices/tradeoffs (why this structure not that one) - this is documentation-as-justification, a different register than B1/B2's documentation-as-explanation
  - B5 (databases): document schema decisions (ties to existing data-minimization justification work - actually ALREADY documentation practice, just needs to be NAMED as such)
  - B6 (testing, security, collaboration): document for TEAMMATES specifically (different audience than self-documentation) - PR descriptions, code review comments as a documentation form
  - B8 (deployment): operational documentation (runbooks, "how do I bring this back up if it goes down") - different purpose again (documentation for FUTURE-YOU-AT-3AM or a different on-call person, not for a code reviewer or a grader)
This is a genuinely good design: documentation REGISTER changes each time (inline comment -> explanatory doc -> API doc -> design-decision doc -> team-facing review doc -> operational runbook) even though it's not a "spiral of its own" - it's better described as "documentation practice attached to and shaped by whatever's being learned at that point."

### VERIFICATION — testing AND formal verification, also embedded not just a 3-pass spiral
User wants formal verification techniques ALONGSIDE testing, not instead of. This is new technical content I hadn't included.
Formal verification (proving correctness via reasoning, not just running examples) is a genuinely different skill from testing (checking specific cases). Where does it fit?
- B1: asserts/logs (testing-adjacent, already planned) - could ALSO introduce the simplest form of reasoning-based verification here: informal pre/post-condition reasoning ("before this loop runs, what's true? after?") - this is the seed of formal verification (loop invariants, Hoare-logic-adjacent thinking) without naming it formally yet. Very early, very informal.
- B2: tests-for-regression (already planned)
- B3 (Data Structures/Algorithms): natural home for slightly more formal correctness reasoning - e.g., proving a sorting algorithm's loop invariant, or reasoning about why a recursive function terminates (this connects beautifully to B5's discrete math Recursive/Modular course IF we move it earlier... but that's placed at B5 not B3. Could note this as a possible sequencing tension worth flagging, not necessarily changing.) Actually recursion correctness (termination, base cases) is ALSO needed conceptually whenever recursion is taught in CS (likely B3's trees/B4's hierarchies use recursion implicitly) even before MATH-103 formalizes it at B5. Worth flagging as a place where CS needs recursion before discrete math formally covers it - minor sequencing note.
- B6 (formal testing course): THIS is where formal verification gets named and treated systematically alongside testing - "testing shows the presence of bugs, verification can show their absence" type framing. Both techniques taught side by side, contrasted explicitly.
- B7/8: applying both testing AND verification thinking to harder cases (graphs, deployed systems)
So: verification spirals similarly to testing (informal pre/post-condition reasoning at B1 -> recursion correctness reasoning around B3-4 -> formal named treatment at B6 alongside testing) but is a genuinely separate skill from testing that should be explicitly dual-tracked starting at B6, not collapsed into "testing" as one thing.

### ERROR HANDLING — normative, with comparative computational models (NEW substantial content)
User wants errors treated as NORMAL (not exceptional/rare) and wants COMPARISON of how different computational models handle errors (try/catch vs Erlang/OTP supervision trees, etc.) This connects directly to the Computational Models thread already planned - in fact this should probably MERGE with that thread rather than be fully separate, since "how does this computational model handle failure" is one of the most important properties of any computational model.

Revised Computational Models + Error Handling combined thread:
- B1: sequential model named; what happens when YOUR program crashes (read your first stack trace) - error as an ordinary, expected thing to encounter and read, not a shameful mistake to hide. Normalize errors from day one.
- B2: async/event-loop model (via fetch) - what happens when an async call fails? (a rejected promise, a failed fetch) - errors look DIFFERENT in this model than in B1's sequential crash - first real comparison point ("the same KIND of problem - a failure - looks different depending on the computational model")
- B3/B4 (OOP, building APIs): formal try/catch exception handling - the "classical" model of error handling, named and practiced
- B4 (APIs across network boundary): errors you don't control (network failures, timeouts) - different STAKES than B1-B3's errors (those were your own bugs; these are environmental/unavoidable failures)
- B5/B7 (databases, concurrent access): what happens when a transaction fails partway through? (atomicity, rollback) - a THIRD model of error handling (transactional rollback vs try/catch vs unhandled crash)
- B6 (security/testing): errors as ATTACK SURFACE (poor error handling leaking information, e.g. verbose stack traces shown to users) - converges error-handling thread with security thread, which is a nice intentional convergence
- B8 (deployment, operations): production error handling at scale - this is where comparative computational models for fault tolerance become genuinely interesting and worth real treatment: try/catch (handle locally, classical), Erlang/OTP-style "let it crash" + supervision trees (isolate failure, restart, don't try to handle every case locally), maybe a brief mention of circuit breakers / retry-with-backoff as a third practical pattern. This is a CONCEPTUAL comparison (not asking students to write Erlang) - the point is students should know that "wrap it in try/catch" is ONE design philosophy for handling failure, not the only one, and production systems often choose differently.

This combined thread (Computational Models + Error Handling) is now one of the richer, more original strands in the whole document - it's genuinely distinctive content (most undergrad CS programs never explicitly compare error-handling philosophies across computational models) and ties together B1's crash, B2's async, B4's network failures, B5/7's transactions, B6's security convergence, and B8's production fault-tolerance comparison. This deserves to be a flagship thread in the map alongside Data Structures.

## REVISED THREAD TAXONOMY (for the map document)
Three different KINDS of threads now, need to be visually/structurally distinguished:

TYPE A - CLASSIC SPIRAL (deliberate increasing-depth passes, topic-centered):
1. Data Structures & Representation (strongest existing)
2. Program Correctness / Code Comprehension
3. APIs & Networked Systems
4. HCI / Accessible & Human-Centered Design
5. Algorithmic Thinking & Complexity
6. Git & Version Control (redesigned this round)
7. Computational Models & Error Handling (MERGED, new flagship thread)
8. Testing & Formal Verification (redesigned/expanded this round)
9. AI-Assisted Development (still need to design - was deferred pending this round's other changes)

TYPE B - CROSS-CUTTING LENS (not a depth-spiral, a standing question applied wherever relevant):
1. Security, Privacy & Ethical Reasoning
2. Documentation Practice

TYPE C - hmm, is Verification Type A or Type B? User said "similar process for verification" referring back to documentation's embedded framing, but ALSO described actual new content (pre/post-conditions, loop invariants) that increases in sophistication - that's depth-spiral shaped. I think Verification is actually BOTH: it has real depth-increasing passes (Type A shape) but ALSO should be triggered embedded-style whenever new code constructs are introduced (Type B shape), similar to how Documentation works but with more formal technical content. I'll present it as Type A (it has clear escalating sophistication: informal reasoning -> recursion correctness -> formal methods alongside testing) but NOTE the embedded-trigger quality explicitly, since that's the more unusual/valuable part of the design.

Need to finalize AI-Assisted Development thread design before drafting full document.

## AI-ASSISTED DEVELOPMENT — final design (comprehension-protective, not embedded-everywhere)

Key constraint from user: avoid AI becoming a crutch in years 1-2; comprehension is the priority; agentic AI development is explicitly deferred to a YEAR 3-4 specialization. This means the Type B "embedded everywhere, expanding scope" pattern used for Documentation/Security is WRONG here - that pattern assumes the practice should grow more autonomous/trusted over time, which directly contradicts "avoid crutch" for AI specifically. Documentation and security get MORE delegated/automated as students mature professionally (e.g. relying on linters, scanners) - AI assistance should NOT follow that same growth curve in years 1-2, since growing AI delegation IS the crutch risk.

Instead: AI-Assisted Development should be tightly bounded to specific, COMPREHENSION-BUILDING use cases, explicitly NOT expanding toward "AI writes more of the code as you go." A few candidate design principles:
1. AI as an EXPLAINER of existing material (supports Code Archaeology, reading) - LOW risk to comprehension because the student still has to verify the explanation against the actual code, and explaining doesn't replace the student's own construction of understanding
2. AI as a SOCRATIC/QUIZZING partner (ask AI to quiz you, or to poke holes in your understanding) - this actively REQUIRES comprehension rather than substituting for it
3. AI as a DEBUGGING RUBBER DUCK (describe the bug to AI, articulate the problem) - the value is in the ARTICULATION, not the AI's answer
4. AI as a DESIGN-ALTERNATIVES generator for discussion (already in original AI Philosophy doc: "brainstorming, design alternatives, tradeoff analysis") - student must evaluate/choose, AI doesn't decide
5. EXPLICITLY NOT included in years 1-2: AI generating substantial original code the student then merely reviews/submits. This is the "crutch" pattern and should be named as something the program is deliberately avoiding, not just something that isn't mentioned.

This suggests AI-Assisted Development should NOT spiral toward "more AI involvement" but should spiral toward "more SOPHISTICATED and CRITICAL use of AI for a CONSTANT, bounded set of purposes" - i.e., the depth increase is in the STUDENT'S judgment/verification skill, not in how much work AI is allowed to do.

Revised passes:
- B1/B2: AI as explainer/study aid for reading unfamiliar code (Code Archaeology) - student uses AI explanation as a STARTING hypothesis, then must verify against actual code behavior (using asserts/logs from the same block!) - nice convergence, AI claim vs empirical verification
- B3/B4: AI as design-alternatives/tradeoff discussion partner when making structural choices (which data structure, how to design an API) - but the JUSTIFICATION and final choice must be the student's own, articulated independently
- B6: AI-assisted code review as ONE input among several (peer review, automated tests) - explicitly not a replacement for human code review, introduced alongside the Collaborative Development course's other practices
- B8: the "verify AI-generated solutions" skill becomes explicit and HIGH-STAKES - given AI-GENERATED code (not the student's own), critique it for correctness, security flaws, and whether it actually does what was asked. This is the moment where students evaluate AI output AS A SUBJECT, not just use AI as a tool - directly converges with the Security and Verification threads. This is also explicitly preparatory for (but distinct from) the Year 3-4 Agentic AI Development specialization - B8 establishes "can you tell if AI-generated code is correct and safe" as a prerequisite skill before that specialization teaches "how do you direct AI agents to build systems."

This keeps the THING that grows being student critical judgment, while the SCOPE of permitted AI use stays narrow and constant (explain, discuss, quiz, critique - never "write this for me and I'll submit it"). I should state this design principle explicitly and prominently in the document, since it's a deliberate and slightly unusual stance worth defending in writing for faculty who may have other assumptions about how much "AI-assisted development" coverage should mean rising AI autonomy.

## FINAL THREAD TAXONOMY (locked)

TYPE A - CLASSIC SPIRAL (depth increases through topic-native escalation):
1. Data Structures & Representation
2. Program Correctness / Code Comprehension  
3. APIs & Networked Systems
4. HCI / Accessible & Human-Centered Design
5. Algorithmic Thinking & Complexity
6. Git & Version Control
7. Computational Models & Error Handling (flagship - merged thread)
8. Testing & Formal Verification

TYPE B - CROSS-CUTTING LENS (standing question/practice attached wherever relevant, scope naturally grows with student capability):
1. Security, Privacy & Ethical Reasoning
2. Documentation Practice

TYPE C - BOUNDED PRACTICE (deliberately NOT growing in scope/autonomy; depth increase is in student critical judgment only, applied to a constant, narrow set of permitted uses):
1. AI-Assisted Development (uniquely this type - the "don't let this grow into a crutch" constraint makes it structurally different from both A and B)

This 3-type taxonomy is itself a notable design feature worth explaining in the document - it shows the team made a deliberate choice about HOW each kind of competency should mature, not just THAT it should mature.

## ROUND 4: Block 1 reframe — Imperative vs. Functional, not Sequential I/II

User insight: CS-101/102 as written are NOT actually parallel (II depends on I despite being designed for the "short parallel chains" philosophy). Real fix: split by PARADIGM, not by topic-sequence.

CS-101 (revised): Imperative Programming — variables, state, control structures (loops/conditionals), mutation. The "tell the computer a sequence of steps that change things" paradigm.
CS-102 (revised): Functional Programming — functions as values, composition, immutability, recursion (basic), no/minimal mutation. The "describe what you want as a composition of transformations" paradigm.

Does this actually work as TRUE parallel content (no dependency either direction)? Mostly yes:
- Both need: basic syntax, data types (numbers, strings, booleans), how to run a program
- Imperative needs: assignment, loops, conditionals, mutation
- Functional needs: function definition/application, composition, basic recursion, immutable data
- Arrays/lists and file I/O (currently dumped into old CS-102) need to be reconsidered - these are CONTENT areas, not paradigm-specific. Lists exist in both paradigms (mutable list in imperative, immutable/persistent list in functional) - this is actually a GREAT teaching opportunity: same data, two different treatments, taught in parallel courses simultaneously. File I/O is more naturally imperative (reading a file is inherently sequential/stateful) but can be touched in functional too (read file -> pure transformation pipeline). 

Where does this leave "problem decomposition" (was in old CS-102)? This is paradigm-NEUTRAL - both imperative and functional decompose problems, just differently (imperative: into steps/procedures; functional: into composable transformations). Could live in BOTH courses as a shared/comparative exercise, or could be the thing that explicitly CONNECTS the two courses (e.g., "solve the same small problem both ways, compare").

This actually creates a built-in spiral/comparison opportunity I hadn't planned: students solve the SAME problem twice, once each paradigm, in the SAME block. That's an extremely strong "compare and contrast" moment for a first block - arguably better pedagogy than the original sequential I/II ever offered, and it reinforces the "notional machine" philosophy (multiple ways of modeling the same computation) right from week one.

## Does this change CS-103 (Computational Representation) or MATH-101?
Not directly - Boolean logic/number systems/bitwise ops are paradigm-neutral, this course is unaffected by the imperative/functional split. Could note that boolean logic feeds conditionals (imperative) AND predicate functions (functional) - small connective tissue worth mentioning in course description but not a structural change.

## Does this change the OTHER threads loaded onto Block 1?
- Git-as-history-tool: unaffected, paradigm-neutral
- Asserts/logs: unaffected, but NOW has an interesting angle - asserts in imperative code check STATE at a point in time; in functional code, you're more likely checking that a pure function's OUTPUT matches expectation for given input (property-based thinking, even if not formalized yet). This is actually a nice subtle reinforcement of the paradigm split, not a complication.
- Documentation (inline + explanatory doc): unaffected, paradigm-neutral, though "explain this code" exercises now naturally have TWO different unfamiliar codebases to read (one imperative, one functional) instead of one - arguably strengthens Code Archaeology prep, since real unfamiliar code could be either paradigm.
- Computational model naming (sequential execution): needs a tweak - "sequential execution" was framed as THE baseline model, but if functional programming is introduced in the SAME block, "sequential" isn't quite the universal baseline anymore. Better framing: Block 1 should name TWO baseline models (imperative/sequential-with-state vs. functional/declarative-composition) rather than one model with functional positioned as a later generalization. This is a GOOD strengthening of the Computational Models thread, not a complication - it means that thread's "B1: name the simplest model" pass becomes "B1: name that there's more than one model, starting here" which is actually a more honest and more interesting opening move for that whole spiral.
- Error normalization (read your first stack trace): unaffected in spirit, though now there's a nice angle - what does failure look like differently in imperative (state corrupted, crash mid-sequence) vs functional code (a function simply has no valid output for that input) - light optional comparison, probably too much for week 1-2 but worth flagging as a possible enrichment.
- AI-as-explainer: unaffected, paradigm-neutral, though again benefits from two codebases to practice on.
- Light security question (representation hiding): unaffected, paradigm-neutral.

## Net assessment: does this split make Block 1 MORE or LESS overloaded?
Interesting result: it doesn't reduce the NUMBER of threads converging on Block 1, but it makes the convergence more COHERENT, because now there's a real structural reason (two paradigms, taught in parallel, on purpose) for why students are encountrons multiple "ways of thinking about computation" at once - the density stops being incidental overload and starts being the actual POINT of the block. The "How does information become computation?" essential question fits BETTER now than before, because the answer is genuinely "it depends which model you're using" rather than just "here's the one way."

This doesn't resolve the mechanical question (does this actually fit in 8 weeks x 2 courses) but it does mean the content that's there has stronger internal justification.

## Revised Block 1 course list
- CS-101: Imperative Programming — state, mutation, control structures, paired exercises with CS-102
- CS-102: Functional Programming — functions as values, composition, immutability, basic recursion, paired exercises with CS-101
- CS-103: Computational Representation — Boolean logic, number systems, bitwise ops (unchanged)
- MATH-101: Discrete Math Logic & Sets (unchanged, external)

Shared cross-course element: "solve it both ways" comparison exercise, likely the natural home for the FIRST explicit naming of "there's more than one computational model" (ties to Computational Models & Error Handling flagship thread) and a natural place for the first documentation-as-justification exercise (why did this problem feel different to solve each way) even though that register was originally slated for Block 3 - could PULL FORWARD a light version here, formal version stays at Block 3 for data-structure choice justification specifically.

## ROUND 5: Block 1 identity clarified — READING is the center, not production

User: "the focus for the block is reading code, so file I/O can be used in both without spending much instructional time on it."

This reframes Block 1 more than it first appears. If file I/O doesn't need dedicated instruction because it just needs to APPEAR in code students read, the same logic likely applies to other content pieces - the question for everything in this block isn't "do we teach this as a skill" but "does this need to be PRODUCED by students, or does it just need to APPEAR in things they read and explain."

Re-examining CS-101/102 content against this lens:
- Variables, control structures, mutation (imperative) - PRODUCED (students need to write basic imperative code, this is genuine skill-building, can't be reading-only)
- Functions, composition, immutability, basic recursion (functional) - PRODUCED (same - genuine skill-building)
- File I/O - READ ONLY (per user direction - appears in examples, not separately taught/produced)
- Arrays/lists - likely PRODUCED at a basic level (hard to write ANY real program without them, in either paradigm) but the depth is shallow - just enough to have something to iterate over / map over
- Problem decomposition - this is actually BOTH - students need to decompose problems to write anything, but it's also explicitly something they should be able to articulate when READING someone else's decomposition choices

So Block 1 has a two-tier structure: a SMALL set of genuinely produced/practiced skills (imperative basics, functional basics, minimal lists) and a LARGER set of things that only need to be encountered, recognized, and explained (file I/O, git history, more complex control flow, multi-paradigm idioms, errors/stack traces, AI explanations to verify). This actually resolves a good chunk of the overload worry from before - the "7 additional threads" I flagged earlier aren't all asking for produced skill at the same depth as the core paradigm content; most of them are asking students to READ, RECOGNIZE, and ARTICULATE, which is a lighter and more uniform cognitive task than "learn to write 6 different things."

This means the right week-by-week structure is probably NOT "week 1-4 imperative content, week 5-8 functional content" (treating them as 2 independent skill-building tracks running in parallel) but something more like: a smaller number of weeks producing basic competence in each paradigm, with READING/comprehension threads (git, asserts, docs, AI-verification, errors) woven across BOTH courses throughout, using progressively more complex code samples (including file I/O, since it just needs to appear) as the vehicle for practicing reading.

This is a genuinely cleaner design than what I had - I was on track to map "8 weeks of imperative + 8 weeks of functional, with 6 extra things stapled on" which risked exactly the overload problem. The actual design is closer to: "16 combined course-weeks (8+8 across 2 parallel courses) where roughly half the time is spent producing basic fluency in each paradigm, and the OTHER half (interleaved, not blocked) is spent reading increasingly complex/unfamiliar code in both paradigms using a growing toolkit (git history, asserts, docs, AI-as-verified-explainer) - with file I/O, more advanced control flow, and paradigm contrasts appearing AS READING MATERIAL rather than as taught content."

I should build the week-by-week map with this two-tier structure (produce vs. read/recognize) explicit, rather than just listing topics by week.

## ROUND 6: Week-by-week draft map for Block 1

Building the actual schedule now. Two courses, 8 weeks each, run in parallel. Structure: roughly weeks 1-5/6 build paradigm fluency (lighter each week as reading threads ramp up), weeks 6-8 shift weight toward integrative reading/comprehension work feeding directly into Block 2's Code Archaeology.

Both courses share a weekly "paired comparison" element - same small problem/concept, both paradigms, compared - rather than living as a separate bolt-on.

Reading threads to interleave (not blocked): git history/semantic versioning, asserts+logs, documentation (inline + explanatory doc), AI-as-explainer (verified empirically), error/stack-trace normalization, light representation/security question. These should ramp from "introduced" to "applied to messier code" across the 8 weeks, riding on whatever paradigm content that week provides as material.

Decomposition: treating as BOTH per my note - light produced practice each week (small), and an explicit READING/articulation angle in the weeks where students examine others' decomposition choices (week 5-6ish, once they have enough vocabulary in both paradigms to compare decomposition strategies across them).

DRAFT WEEK MAP:

CS-101 Imperative Programming:
Wk1: Variables, state, basic control structures (if/loops). Reading thread: git log/diff on a trivial repo - "what changed and why" as a warm-up parallel activity, not graded yet.
Wk2: Mutation, simple lists (imperative style - indexed access, mutation in place). Reading thread: asserts/print-debugging introduced - add a print statement to confirm a hypothesis about what a loop is doing.
Wk3: Slightly larger programs (combining control structures). Decomposition (produced, light): break a small problem into steps. Reading thread: read a short unfamiliar imperative program with a file I/O call in it (not taught, just present) - explain what it does using asserts/print.
Wk4: Error encounters - intentionally trigger and read a stack trace from common imperative mistakes (off-by-one, null/undefined access, type error). Normalize: this is expected, here's how you read it. Documentation: inline comments on own code from wk1-3.
Wk5: Paired comparison checkpoint (shared with CS-102): same small problem solved imperatively here, functionally in CS-102 same week. Reading thread: AI-as-explainer introduced - ask AI to explain a short unfamiliar imperative snippet, then verify the explanation against actual behavior using asserts from wk2.
Wk6: Reading decomposition choices in someone else's imperative code (medium-sized, multiple functions/procedures) - articulate why they likely broke it up that way. Documentation: write a standalone explanatory doc (not just inline comments) for a piece of unfamiliar code.
Wk7: git history applied - given a repo's commit history (not your own), reconstruct the story of how the program evolved; connect commit messages to semantic versioning concepts (what kind of change justifies a version bump).
Wk8: Integrative: read a moderately unfamiliar imperative program combining several wk1-7 elements (control structures, mutation, file I/O present, an error case). Produce: inline comments + explanatory doc + verified AI explanation + git history reconstruction, all on the SAME piece of code. This is the direct on-ramp to Block 2's Code Archaeology.

CS-102 Functional Programming:
Wk1: Functions as values, function application, basic expressions (no mutation). Reading thread: git log/diff on the SAME trivial repo as CS-101 (shared artifact, different lens - "what changed" framed without assuming imperative state changes).
Wk2: Composition (combining small functions into bigger ones), simple immutable lists (map/filter conceptually, even if not named that way yet). Reading thread: asserts as input/output checks - "does this function return what I expect for this input" (property-style framing begins here, lightly).
Wk3: Basic recursion (simple cases: countdown, sum-a-list). Decomposition (produced, light): break a problem into composable pieces rather than sequential steps - explicit contrast framing with CS-101's wk3 decomposition. Reading thread: read a short unfamiliar functional snippet with file I/O present (read-file-then-transform pattern) - explain it.
Wk4: Error encounters in functional style - what does "no valid output for this input" look like (vs. CS-101's crash-mid-sequence framing) - light, comparative call-out to CS-101 wk4 without requiring deep parallel instruction. Documentation: inline comments on own wk1-3 code.
Wk5: Paired comparison checkpoint (shared with CS-101): same small problem solved functionally here. Reading thread: AI-as-explainer on a short unfamiliar functional snippet, verified against behavior using wk2's input/output asserts.
Wk6: Reading decomposition in someone else's functional code (medium-sized, composed of multiple small functions) - articulate the composition strategy. Documentation: standalone explanatory doc for unfamiliar functional code.
Wk7: git history applied to a functional-style repo's evolution; same semantic versioning concepts as CS-101 wk7, different codebase.
Wk8: Integrative: read a moderately unfamiliar functional program (composition, basic recursion, file I/O present, an input with no valid output to find/explain). Same four-part production as CS-101 wk8: comments + doc + verified AI explanation + git history. Direct on-ramp to Code Archaeology.

Shared/connective elements across both courses:
- Wk1: same trivial repo for git warm-up (give both courses a common reference point from day one)
- Wk3: decomposition contrast (sequential steps vs. composable pieces) - could be an explicit joint discussion/reflection prompt
- Wk4: error-handling contrast (crash-mid-sequence vs. no-valid-output) - light, not deep instruction
- Wk5: the paired comparison checkpoint - solve the same small problem twice, write a short reflection comparing the two solutions (this is where "computational model" gets explicitly named as a concept - there's more than one way to model this computation)
- Wk8: parallel integrative reading assessments, same structure, different paradigm - both feed directly into Block 2

Light/optional touches not given dedicated weeks (per "doesn't need much instructional time"):
- File I/O: present in wk3 (both) and wk8 (both) reading material, never separately taught
- Security/representation question (does a representation choice affect what can be hidden): could be a single short discussion prompt attached to wk2 (CS-101, mutation/state) or wk1-2 CS-103 (Boolean/representation) rather than needing its own week - probably best homed in CS-103, not 101/102, since CS-103 already owns representation content directly

## Sanity check: does this fit, and is it actually lighter than before?
8 weeks x 2 courses = 16 course-weeks total. Each week has ONE primary produced-skill focus plus ONE interleaved reading-thread touch - never multiple new reading threads in the same week for the same course. Reading threads ramp in a fixed order (git -> asserts -> file I/O exposure -> errors -> AI-verification -> documentation -> decomposition-reading -> git history depth) and the SAME thread touches both courses in the SAME week using different (but comparable) material, which halves the apparent variety students face at any given moment - they're applying the same new tool to two parallel examples, not learning two unrelated things.

This looks fittable. The main remaining risk is week 8's integrative assessment in both courses simultaneously - that's a real crunch point (two capstone-of-the-block assessments due the same week) worth flagging.

## ROUND 7: Service-course constraint

New constraint: some courses must be offerable as SERVICE COURSES to other departments. Named examples: "Relational Databases", "Networking Fundamentals". Requirement: structure topic coverage so it can ALSO map to a traditional course = two back-to-back blocks, same semester, forming one coherent recognizable unit.

Key tension: internal model is decoupled 1-credit parallel chains; service model needs coherent self-contained sequential-feeling courses with a recognizable name and no assumed dependencies on OUR program's other content (a stats major taking "Relational Databases" hasn't taken our CS-101). So a service-mappable pair must be:
1. Two blocks back-to-back in the SAME semester (so it fits a normal 16-week term for the visiting student)
2. Internally coherent as a standalone topic (recognizable traditional course name)
3. Minimally dependent on OUR program-specific prior courses (a visiting student should be able to take it cold, or with only generic prerequisites like "intro programming" or "college algebra")

Let me check the named examples against current placement:

### RELATIONAL DATABASES (service course candidate)
Current relevant courses:
- CS-201 SQL Fundamentals (Block 5, Y2 Fall first half)
- CS-202 Database Design (Block 5, Y2 Fall first half)
PROBLEM: both are in Block 5 (same 8-week block, run in parallel), not back-to-back blocks. For a service course we'd want them SEQUENTIAL (SQL Fundamentals block -> Database Design block) across Blocks 5 and 6, forming a 16-week "Relational Databases" course.
But Block 6 is currently Testing/Security/Collaboration (the "everything formalizes" block). Moving Database Design to Block 6 would either add a 4th course to Block 6 or displace something.
Alternative: keep both in the same semester (Y2 Fall = Blocks 5+6) but sequence them: SQL Fundamentals in Block 5, Database Design in Block 6. A visiting student enrolls in both halves = a full-semester "Relational Databases (CS-2xx)" service course. Internally our students take them possibly in either arrangement. This works IF Block 6 can absorb Database Design.
Dependencies check: Relational Databases as a service course needs ~intro programming as a prereq at most. SQL Fundamentals doesn't deeply depend on our CS-101/102/104 etc. - SELECT/INSERT/JOIN can be taught relatively cold. GOOD service candidate. Data minimization/schema justification embedded content is paradigm-neutral and fine for visiting students.

### NETWORKING FUNDAMENTALS (service course candidate)
Current relevant courses:
- CS-106 Web Foundations (Block 2) - has "consuming a basic web API" but is mostly HTML/CSS/accessibility, NOT networking per se
- CS-111 APIs & Data Visualization (Block 4) - building/consuming APIs, but bundled with SVG visualization
PROBLEM: there isn't actually a clean "Networking Fundamentals" pair right now. Networking content is scattered and entangled with web-presentation (HTML/CSS) and visualization (SVG) content. To offer "Networking Fundamentals" as a service course we'd need to consolidate the networking/protocol/API-communication content into a coherent back-to-back pair, separated from the HTML/CSS/SVG presentation content.
This is a real restructuring question, not just a relabeling. Options:
(a) Create a networking-focused pair somewhere: e.g. "how computers communicate" (protocols, client-server, HTTP, request/response) + "working with APIs" (consuming, building, error handling across network boundary). That's a coherent 2-block "Networking Fundamentals" service course.
(b) But our current Block 2 / Block 4 placement splits these across DIFFERENT semesters (Block 2 = Y1 Fall, Block 4 = Y1 Spring) - violates the same-semester requirement. Would need both networking blocks in the SAME semester to be service-offerable.

This reveals a genuine conflict: the spiral design deliberately SPREAD networking (consume early in B2, build later in B4) for good pedagogical spiral reasons, but service-course-ability wants it CONSOLIDATED into one semester. These goals fight each other.

Possible resolutions:
1. Accept that not every topic can be both spiraled AND service-offerable; pick which topics are service courses and consolidate ONLY those, letting them be less-spiraled in exchange. Networking becomes a consolidated Y_ semester pair; databases similarly.
2. Offer the service course as a DIFFERENT packaging of content that internally is still spiraled - i.e., a visiting student takes a dedicated 2-block "Networking Fundamentals" that is SEPARATE from how our students encounter networking woven through B2/B4. (This means MORE total course development, essentially a parallel service-only offering - probably too expensive/duplicative.)
3. Identify which blocks can be SEQUENED in one semester to form the service course AND still serve our students' spiral - i.e. find a semester where putting two related blocks back-to-back doesn't hurt the spiral much.

Resolution 3 is the sweet spot where achievable. Let me assess which named service courses can fit it:
- Relational Databases: ACHIEVABLE via Res.3 - SQL Fundamentals (B5) -> Database Design (B6), both Y2 Fall, if B6 absorbs Database Design. Spiral impact low (databases weren't a big multi-block spiral anyway; they're fairly self-contained).
- Networking Fundamentals: HARDER - current B2/B4 split is cross-semester AND the content is entangled with HTML/CSS/SVG. Would need (a) consolidating networking into 2 same-semester blocks and (b) disentangling from presentation content. This likely means pulling networking OUT of CS-106 (leave CS-106 as pure HTML/CSS/accessibility) and OUT of CS-111 (leave it as visualization + the building side), and creating a dedicated networking pair. Where? If we want it as a service course it needs its own 2 blocks in one semester.

Hmm - this is getting into real restructuring. Rather than unilaterally redesign, I should surface this conflict clearly and get direction. The databases case is nearly free; the networking case forces real tradeoffs against the spiral and against the HTML/CSS/SVG threads we just carefully built.

Also worth noting: making something a service course has an UPSIDE for the spiral tension - if Networking Fundamentals becomes a coherent consolidated course, the "APIs & Networked Systems" spiral (B2 consume -> B4 build -> B5/7 integrate -> B8 operate) loses its early two passes as DISTRIBUTED touchpoints. But maybe that's OK if networking is consolidated early and then still REVISITED at B5/7/B8 for integration/operation. Consolidation early + revisit later is still a spiral, just front-loaded.

Need user input on:
1. Confirm databases consolidation (SQL B5 -> Design B6) is acceptable, accepting Block 6 load implications
2. Networking: is it worth the restructuring to make it service-offerable, given it fights the HTML/CSS/SVG entanglement and the cross-semester spiral split? Or focus service-course-ability on the cleaner candidates (databases) and a couple others?
3. Are there OTHER intended service courses beyond the two named, so I can check them too?

## ROUND 8: Networking Fundamentals = OSI-model theory course (NEW content, not a relabel)

Critical reframe: Networking Fundamentals is a THEORETICAL intro organized around the OSI 7-layer model, intended as a shared trunk that 3 departments build on (CompE = low-level implementation; CS = ?; Business = network administration). This is NOT the API/web-communication content in CS-106/111 - that content stays put in the spiral, untouched. This resolves the earlier conflict entirely: we are not disentangling anything, we're ADDING a distinct course.

Implications:
1. This is NEW content. Current budget is fully allocated (22 CS + 4 discrete = 26). Adding a 2-block Networking Fundamentals (2 credits) requires either (a) growing past 26, or (b) cutting/displacing 2 credits of existing CS content. Need user decision on this - it's a real budget question.
2. As a service course it needs to be 2 back-to-back blocks, same semester, self-contained, minimal prereqs. OSI model theory fits this perfectly - it's conceptual, needs basically no programming prerequisite, could even be taken by a business student in their first year.
3. Where does it go? Since it's largely self-contained and prerequisite-light, it has placement freedom. Options:
   - Could anchor a semester as the "theory" counterpart to more hands-on blocks
   - Pedagogically, OSI layering (physical -> data link -> network -> transport -> session -> presentation -> application) is a GREAT fit with the "notional machine" expansion in the program's philosophy (the layered model of the whole computational system: People -> Requirements -> ... -> Networks -> Users). OSI is literally a layered-abstraction model, which reinforces the systems-thinking spine. Could even be positioned EARLY as a systems-thinking scaffold rather than late.
   - But it also connects naturally to the APIs/networked-systems spiral (understanding HTTP at the application layer is richer if you know what's underneath). Placing it BEFORE or DURING the networking-adjacent spiral passes (B2 consume APIs, B4 build APIs) would enrich them. That argues for Year 1.
   - Counter: as a 2-block same-semester service course, it needs two consecutive blocks. Year 1 Fall (B1+B2) and Year 1 Spring (B3+B4) are options. B1 is already very dense (just analyzed). B2 has the HTML/CSS/Code Archaeology load. 

4. How does OSI-as-2-blocks split? Natural division:
   - Block A: Lower layers (Physical, Data Link, Network, Transport) - how bits physically move and get routed reliably end to end
   - Block B: Upper layers (Session, Presentation, Application) + integrative review of the full stack - how applications actually use the stack; this is where it connects to HTTP/APIs that CS students see elsewhere
   This is a clean, recognizable, traditional split and maps to "one semester of Networking Fundamentals."

5. CS-specific follow-on: user said CompE does low-level, Business does network admin - what's the CS follow-on that builds on this trunk? Probably the existing API/distributed-systems/networked-applications content (CS-106/111 and later integration work). So for OUR students, Networking Fundamentals (OSI theory) becomes a conceptual UNDERPINNING that the existing spiral passes then build on - meaning if we place it Year 1, the existing B2/B4 API work becomes the CS-specific application of the shared trunk. Clean.

## Budget options to present
Option A: Grow to 28 credits (26 + 2 for Networking Fundamentals). Simplest, but breaks the "26 credit" constraint established earlier - may have KBOR/degree-total implications.
Option B: Displace 2 existing CS credits. What could go? Candidates for cutting/compressing:
   - The program is tight; everything's there for a reason. Hard cuts.
   - Possible: CS-112 Data Persistence I (1cr, Block 4) is partly a "bridge/motivation" course (files, CSV/JSON, "why we need a database") - some of this could potentially fold into CS-111 or into the Block 5 databases sequence, freeing ~1 credit. 
   - Possible: one of the Year 2 courses could compress, but those are all carrying distinct weight.
   - This needs faculty/user judgment, not something I should unilaterally decide.
Option C: Networking Fundamentals is offered as a service course / elective that ISN'T required in the core 26 for our CS majors - i.e., our students might take it as one of their gen-ed "Natural Science" (4cr) or "Institutionally Determined" (6cr) KBOR slots, OR it lives outside the 2-year core as a 3rd-year course. This avoids the budget conflict entirely by NOT putting it in the first-two-year CS 26. But then it's not part of the spiral for our students in years 1-2. Tradeoff.
Option D: Cross-list / double-count - if a student takes Networking Fundamentals, it satisfies both a CS requirement AND could be structured to satisfy part of an institutionally-determined gen-ed block. Depends on institutional rules.

This is fundamentally a budget/institutional-policy decision, not a curriculum-design decision. I should present the options clearly and get direction rather than guessing.

## ROUND 9: Statistics foundations for ML (new external 1-credit course strand)

User direction: add statistical foundations sufficient to set the stage for machine learning, as additional 1-credit courses from the STATISTICS dept, following the MATH model (external, co-designed, 1-credit, 8-week, loosely paired/parallel, prereq college algebra-ish). Budget left soft for now.

Parallel to discrete math: discrete math = 4x 1-credit (MATH-101..104). Statistics likely a similar small sequence (STAT-1xx). Question: how many, and what content, to "set the stage for ML"?

What does "enough to set the stage for ML" actually require? Working backward from intro ML prerequisites:
- Descriptive statistics (mean, variance, std dev, distributions) - foundational
- Probability (basic probability, conditional probability, Bayes) - critical for ML
- Random variables & common distributions (normal, binomial, etc.)
- Sampling & sampling distributions, central limit theorem
- Inference (confidence intervals, hypothesis testing) - useful but arguably less critical for ML specifically than probability
- Correlation & regression (linear regression especially) - this is the DIRECT on-ramp to ML (regression IS a supervised learning method)
- Possibly: intro to linear algebra concepts (vectors, matrices) - but that's MATH not STAT, and is also an ML prereq. Worth flagging that ML readiness needs SOME linear algebra that neither the current discrete math sequence NOR a stats sequence necessarily covers. Gap to flag.

Reasonable 4-course STAT sequence mirroring the discrete math model:
- STAT-101: Descriptive Statistics & Data Summarization (mean/median/variance/distributions/visualization of data) - pairs naturally with the data work (CS-112 persistence, CS-111 visualization, or the Block 5 databases/data-investigation)
- STAT-102: Probability (basic -> conditional -> Bayes) - foundational, pairs with discrete counting (MATH-102) nicely since counting underlies discrete probability
- STAT-103: Random Variables & Distributions / Sampling (normal, binomial, CLT, sampling distributions)
- STAT-104: Correlation & Regression (linear regression as the ML on-ramp) - this is the capstone of the stats sequence and the direct bridge to ML

Pairing/sequencing with existing content (loose parallel, per the established model):
- STAT-101 (descriptive) pairs well with data-heavy blocks - Block 4 (data persistence/visualization) or Block 5 (databases/data investigation). Probably Block 4 or 5.
- STAT-102 (probability) pairs conceptually with MATH-102 (counting, Block 3) - counting -> probability is the classic progression. But that might crowd Block 3. Could be slightly later.
- This raises a sequencing question: discrete math occupies the "external 1-credit course" slot in Blocks 1,3,5,7 (one per... actually let me check - MATH-101 B1, MATH-102 B3, MATH-103 B5, MATH-104 B7). So external math courses are in the ODD blocks (1,3,5,7), none in even blocks (2,4,6,8). 
- If stats follows the same "one external course per block" rhythm, stats courses could go in the EVEN blocks (2,4,6,8) OR could extend into year 2 / overlap. But 4 stats + 4 discrete = 8 external courses across 8 blocks = exactly one external course per block. That's clean IF it fits the load.
  - But wait - some blocks are already dense (B1 has 4 courses incl MATH-101; B2 has 3 CS; etc). Adding a stats course to every even block makes B2,4,6,8 also 4-course blocks. Combined with the service-course database resequencing (Database Design possibly -> B6) and the soft-budget OSI networking addition, Year 2 especially is getting crowded. This is exactly the "optimize later, block by block" work the user flagged. For now: NOTE that stats adds ~4 credits and the external-course rhythm COULD be one-per-block but load needs checking.

Actually, ML readiness might not need all 4 stats in the first two years - some could be deferred. But user said "set the stage for ML" and the ML-adjacent specializations (AI Systems, Data Science) are post-foundation. So the FOUNDATION needs enough stats that a student ENTERING those specializations is ready. That probably means at least descriptive + probability + regression (3 courses minimum); the 4th (inference/sampling) is valuable but could potentially be early in the specialization rather than the foundation. Flag this as a scoping question.

Linear algebra gap: ML needs vectors/matrices/dot products. Neither discrete math (logic/counting/recursion/graphs) nor this stats sequence covers it. This is a real gap for ML-readiness. Options: add a MATH linear algebra 1-credit course, or fold basic linear algebra into one of the existing math courses, or defer to the specialization. Worth flagging explicitly - it's the most likely thing to be missed.

## Questions to surface
1. How many stats courses (3 vs 4)? Is inferential statistics (hypothesis testing/CI) needed in the foundation or deferrable to the ML specialization?
2. Linear algebra gap for ML - address in the 2-year foundation, or defer to specialization?
3. Do stats courses follow the "one external per block" rhythm in even blocks, or cluster nearer the data-heavy/Year-2 content where they pair best?

## ROUND 10: Linear algebra, probability ownership, data viz, optimization

### Decisions recorded
1. LINEAR ALGEBRA: add as MATH-105 (5th math course) for now, FLAG that it may need a different approach. Rationale for the flag: the other 4 math courses are discrete math (logic/counting/recursion/graphs), pitched at first-year-calc level, prereq college algebra. Linear algebra is a different beast - it's not discrete, it's arguably MORE foundational to ML than any single discrete course, and cramming it into one 1-credit/8-week course is tight (most LA courses are 3-credit). "Different approach" candidates to note: might need to be 2 blocks (like the service courses), might need to be a different prereq level, might overlap with the graph adjacency-matrix content (MATH-104) as a bridge in. Don't over-decide now - just place + flag.

2. PROBABILITY OWNERSHIP: cross-department co-design flag. Don't resolve unilaterally. NOTE for that discussion: the discrete draft's Course 2 modules 7-8 already cover finite probability, conditional, Bayes, random variables, expected value, variance. If STAT also covers probability there's duplication. Cleanest likely outcome: discrete OWNS discrete/finite probability (counting-based), STAT owns continuous probability + distributions + inference. But that's for the co-design meeting. Just flag clearly.

3. DATA VISUALIZATION -> folds into the HCI thread, embedded throughout (NOT a standalone stats topic, NOT just the CS-111 SVG moment).

### Data viz as part of HCI thread - rework
Currently HCI thread (Type A spiral) is:
- B2: HTML/CSS + accessibility (static page, checklist compliance)
- B4: SVG visualization (dynamic, data-driven)
- B7: Design Review (justify to others)
- B8: formal UX/requirements

Data viz currently appears as a SINGLE point (B4, SVG). User wants it embedded THROUGHOUT the HCI thread like accessibility is. So data viz should become a recurring concern across the HCI passes, with escalating sophistication, NOT a one-time B4 topic. Reworked HCI thread now carries TWO embedded throughlines (accessibility AND data viz/visual communication), which actually fit together well - both are about "communicating to a human effectively and honestly."

Reworked HCI thread with viz embedded:
- B2: HTML/CSS + accessibility + FIRST viz idea: visual hierarchy/typography as VISUAL COMMUNICATION (this is proto-dataviz - using visual design to aid comprehension, already in the CS-106 description as "CSS for visual hierarchy and comprehension"). So viz starts here, not B4.
- B4: SVG data visualization - charting actual data (the current explicit pass). Now framed as "honest visual representation of data" - escalation from B2's general visual communication to specific DATA representation. Tie-in to descriptive stats (STAT) if/where it lands - visualizing distributions, etc.
- B5/7: when working with databases/data integration, viz of QUERY RESULTS and integrated data - viz as a tool for DATA INVESTIGATION (signature assessment), not just presentation. Escalation: viz as analysis tool, not just output.
- B8: viz in the context of formal UX + the data analysis course (CS-210) - viz for an AUDIENCE with needs, honest representation, avoiding misleading charts (ethics tie-in). Plus notebook-based viz in CS-210.
This is a clean embedded throughline. Data viz now spirals B2->B4->B5/7->B8 alongside accessibility, both under HCI. Good.
Also connects to the "what data to collect / how to present honestly" ethics thread already running. Honest visualization (not misleading with axes/scales) is an ethics-of-representation point - converges HCI + ethics threads nicely.

### Optimization in the spiral - where?
User: "Optimization should appear in the spiral at appropriate points." Optimization is an AI-degree need. What are the natural foundation-level touchpoints where optimization arises ORGANICALLY (not forced)?
Optimization = finding the best solution under constraints. Where does this naturally arise in the existing spiral?
- Algorithmic Thinking & Complexity thread (B3 Big-O, B7 graphs, B8 real bottleneck): optimization is NATIVE here. 
  - B3: complexity analysis IS about efficiency - "can this be done faster" is the seed of optimization thinking. Choosing a better algorithm = optimization. Light, implicit.
  - B7: graph algorithms include SHORTEST PATH (already in MATH-104 and CS-206!) - shortest path IS a classic optimization problem. This is a natural, organic optimization touchpoint already present in the content - just needs NAMING as optimization. Also: weighted graphs, minimum spanning trees (optimization over graphs).
  - B8: performance optimization of a real deployed system - "make this faster/cheaper under real constraints" - applied optimization.
- Data structures thread: choosing the right structure to optimize for a given operation (optimize for lookup vs insertion vs memory) - B3/B4 - this is optimization-as-tradeoff-reasoning, very foundational.
- Database thread (B5): query optimization (indexes, query plans) was mentioned in the ORIGINAL project summary's "Later: Performance, Indexes, Query plans" SQL progression! So query optimization is already anticipated - a natural optimization touchpoint in the data thread.
- The "tradeoff analysis" that appears in the AI-assisted-development and design threads is optimization-adjacent (optimizing across competing quality attributes).

So optimization isn't a NEW thread - it's a LENS/naming that can be applied to existing points where "find the best X under constraints" already occurs:
  - B3: algorithmic efficiency, data structure tradeoffs (optimize for which operation?)
  - B5: query optimization (indexes/query plans)
  - B7: shortest path, MST, weighted graph optimization (NATIVE - strongest organic point)
  - B8: real system performance optimization
This mirrors how Security was handled - a lens applied where relevant content already exists, with escalating sophistication, rather than a separate spiral. Mathematical optimization proper (gradient descent, convex optimization for ML) is deferred to the specialization, but the CONCEPT and reasoning pattern ("optimize this under these constraints") is seeded organically at these 4 points so students arrive at the ML specialization already thinking in optimization terms.

Should optimization be: (a) its own named lens like Security/Documentation, or (b) just embedded naming within the Algorithmic Thinking spiral + Data thread? 
Given it spans BOTH the algorithmic thinking thread AND the data thread AND touches design tradeoffs, it's probably cleanest as a lightweight LENS (Type B) - "optimization reasoning" - that surfaces the common pattern across these otherwise-separate threads. That also matches its eventual importance in the AI degree (where it becomes central). Flag as a 3rd lens alongside Security/Privacy/Ethics and Documentation.

## ROUND 11: Block 2 reframe — "computation as modifying data"; push heavy OOP to Block 3

User decisions:
1. Block 2 cognitive frame = understanding computation as MODIFYING DATA (not the "read others / write for others" duality)
2. Push heavy OOP (CS-104 OOP I) OUT of Block 2, into Block 3.

This is a strong reframe. New conceptual spine across blocks:
- Block 1: READING computation (two paradigms, comprehension focus)
- Block 2: MODIFYING data/state (transformation, mutation, the act of CHANGING things)
- Block 3: STRUCTURING data (OOP + data structures now together - organizing data, not just modifying it)
This is cleaner than the old Programming Fundamentals I/II -> Data Structures progression. Read -> Modify -> Structure is a real conceptual escalation.

### What "computation as modifying data" pulls together (the frame's natural content)
This frame unifies what looked like a grab-bag:
- Debugging/repair = modifying broken code to fix data flow (Code Archaeology + repair fits PERFECTLY - you read code (B1 skill) then MODIFY it)
- The git commit/revert safety net = managing the HISTORY of modifications (now thematically core, not bolted on - version control IS "tracking how data/code changes over time")
- Tests-for-regression = verifying your modifications didn't break existing behavior (core to the frame - "did my modification preserve what should be preserved")
- Data transformation (functional) and mutation (imperative) from B1 now get APPLIED - B1 read these, B2 does them
- Async/event-loop via fetch = modifying program state in response to events arriving over time (fits "modifying data" - state changes triggered by async events)
- Error/failure = what happens when a modification goes wrong (failed fetch, bad input) - fits the frame
- Data-minimization in forms = WHAT data you collect/modify and why (fits "modifying data" via the ethical lens - which data should you even be touching)

### What gets PUSHED OUT or recedes
- Heavy OOP (encapsulation/inheritance/abstraction/classes) -> Block 3. This is "structuring data," not "modifying data" - correct to move. Block 3 becomes OOP + data structures = "organizing/structuring data" which is a coherent frame for block 3.
- HTML/CSS/accessibility (CS-106): does this fit "modifying data"? Partially. HTML/CSS is REPRESENTATION/presentation, not really modification. BUT - consuming an API and populating a page IS taking data and transforming it into a visual representation = a kind of data modification (data -> DOM). The web work could be reframed as "modifying what the user sees based on data" rather than "web foundations." OR web/HTML could itself move. NEED TO THINK: does CS-106 stay in B2 under this frame, or does it also move?
  - Argument to KEEP in B2: fetch->render is literally "modify the page based on data arriving" - fits async/event-loop + modifying-data frame well. The accessibility/viz angle (HCI thread pass 1) is valuable here.
  - Argument to MOVE: if B2 is tightly "modifying data/state," the HTML/CSS *representation* content (semantic markup, visual hierarchy) is more about presentation than modification, and could go with the OOP "structuring" block or later. But that would delay the HCI thread's first pass (B2 currently = HCI pass 1).
  - Tentative resolution: SPLIT CS-106. The DATA->rendering / dynamic-update part (fetch, populate, update the DOM as data changes) stays in B2 (fits "modifying what's shown based on data"). The static HTML/CSS/semantic-markup/accessibility-foundation part could either stay lightly in B2 or move. But splitting a 1-credit course is awkward. ALTERNATIVELY keep CS-106 mostly intact in B2 but reframe its emphasis toward dynamic/data-driven rendering rather than static page construction, with static HTML/CSS as the necessary substrate taught lightly. This keeps HCI pass 1 in B2 and fits the frame. LEAN: keep CS-106 in B2, reframe emphasis to data-driven rendering.

### Block 2 revised course set (3 courses, 1 credit each)
Given OOP I leaves, B2 has an open slot. Options:
(a) CS-105 Code Reading & Debugging (Code Archaeology) - STAYS, it's the centerpiece, fits "modify broken code" perfectly
(b) CS-106 Web Foundations, reframed toward data-driven rendering - STAYS (HCI pass 1, fits frame)
(c) NEW 3rd course to fill OOP I's slot, fitting "modifying data" frame. Candidates:
    - A "Data Transformation" course: applying B1's imperative-mutation and functional-transformation skills to actually TRANSFORM data (parse, filter, reshape, aggregate small datasets - CSV/JSON in, transformed data out). This is a GREAT fit for the frame, sets up later data work (B4 persistence, B5 databases, stats), and gives the functional skills from B1 a real application (map/filter/reduce as data transformation). 
    - This "Data Transformation" course also is a natural home for: more data-minimization/ethics (what data, transformed how), early descriptive-stats touch if STAT-101 pairs here, proto-data-viz (transformed data -> simple visual).
    - LEAN: replace OOP I slot with "Data Transformation & Manipulation" (CS-104 renumbered/retitled)

So revised Block 2:
- CS-104 (retitled): Data Transformation & Manipulation — parsing, filtering, reshaping, aggregating data; applies B1 imperative+functional skills; CSV/JSON handling (the file I/O that was "read only" in B1 now gets USED to transform)
- CS-105: Code Reading & Repair — Code Archaeology signature assessment; debugging AS data-flow modification
- CS-106: Web Foundations & Data-Driven Rendering — semantic HTML/CSS/accessibility substrate + fetch-and-render (modify the page as data arrives); HCI thread pass 1 + data viz proto-pass + async/event-loop computational-models pass
- (+ possibly an external STAT or MATH course per the even-block rhythm question - deferred to cross-block optimization)

Frame check: all three courses now genuinely about modifying/transforming data and state. Code Archaeology (modify broken code), Data Transformation (modify data shape), Web rendering (modify display from data). Coherent single frame. 

### Thread touches now land MORE naturally (re-mapping to the frame)
- Git commit/revert: managing modification history - CORE to frame now, lands in CS-105 (repair work) - strong fit
- Tests-for-regression: verifying modifications preserve behavior - lands in CS-105 - strong fit
- Async/event-loop: lands in CS-106 (fetch-driven rendering) - strong fit
- Documentation: document a bug fix (CS-105), document a data transformation's contract (CS-104) - fits
- AI-as-explainer: still supports Code Archaeology in CS-105
- Data-minimization/ethics: lands in CS-104 (what data, transformed how) and CS-106 (form fields) - fits
- HCI accessibility + proto-viz: lands in CS-106 - fits
- APIs (consume): lands in CS-106 (fetch) - fits

Everything still fits, and arguably fits BETTER than before because the frame gives each thread touch a reason to be there. OOP-related thread touches (none major were B2-specific) move to B3 with the OOP content.

### Ripple to Block 3
B3 now gains OOP I (was B3 already had OOP II + data structures). So B3 = OOP I + OOP II + data structures (linear) + complexity? That might OVERLOAD B3. Need to check B3 when we get there - pushing OOP I into B3 may require pushing something ELSE from B3 to B4, cascading. FLAG: B2 reframe has a downstream cost at B3 that needs reconciling when we do B3. Specifically B3 might become: OOP I, OOP II (or a merged "OOP" pair), Linear Data Structures, + MATH-102. Complexity (CS-109) might need to slide to B4. Note and defer to B3 analysis.

## ROUND 12: Block 3 reframe — "modeling and abstraction"

User frame for B3: MODELING AND ABSTRACTION. OOP natural fit, plus structured/modular programming principles, plus INTRODUCE BOUNDARIES AND CONTRACTS.

Current B3 base: CS-107 OOP II (exceptions/collections/iterators), CS-108 Linear Data Structures, CS-109 Algorithmic Complexity, MATH-102 Counting.
Plus from Block 2 reframe: OOP I pushed DOWN into B3.

So naive B3 load = OOP I + OOP II + Linear Data Structures + Algorithmic Complexity + MATH-102 = 4 CS + 1 math = 5 courses. OVERLOADED (vs typical 3 CS). Must shed.

### Does the "modeling and abstraction" frame tell us what BELONGS vs what should leave?
Frame = modeling a domain + drawing boundaries + defining contracts + structured/modular decomposition. Test each candidate course against it:
- OOP I (encapsulation, inheritance, abstraction, classes): CORE to frame. Encapsulation IS boundary-drawing; abstraction IS the frame's name; classes ARE domain models. PERFECT fit. Belongs.
- OOP II (exceptions, collections, iterators, OOP design principles): "OOP design principles" = modeling/abstraction core. Collections/iterators = abstraction over data access. Exceptions = ... actually exceptions belong more to the Error Handling thread than to modeling/abstraction. Iterators = abstraction over traversal (contract: "give me the next thing"). Mostly fits, but exceptions are a slightly awkward guest.
- Linear Data Structures (lists/linked-lists/stacks/queues): do these fit "modeling and abstraction"? Stacks/queues are ABSTRACT DATA TYPES - defined by their CONTRACT (LIFO/FIFO) independent of implementation. That's LITERALLY boundaries-and-contracts! A stack is "push/pop, last-in-first-out" as a contract; the linked-list vs array implementation is hidden behind that boundary. So data structures, taught as ADTs (contract first, implementation behind a boundary), fit the frame EXTREMELY well. Belongs - and the frame actually improves how they're taught (ADT contract before implementation).
- Algorithmic Complexity (Big-O, sorting/searching): does this fit "modeling and abstraction"? Big-O is itself an ABSTRACTION (abstracting away constants/hardware to model growth). But it's a different KIND of abstraction (quantitative/performance) than the structural modeling the rest of the block is about. It's a somewhat awkward fit - complexity is more about ANALYSIS than MODELING. This is the candidate to MOVE OUT to relieve overload. It also pairs with MATH-102 counting, so if complexity moves, does counting follow? 

### Resolution: move Algorithmic Complexity to Block 4
- Complexity (CS-109) -> Block 4. Frees B3 to be tightly about modeling/abstraction (OOP I, OOP II, Data Structures as ADTs).
- But CS-109 was paired with MATH-102 (counting underlies complexity). If CS-109 moves to B4, either MATH-102 moves with it, or the pairing is loosened (they're in adjacent blocks, same semester, so "loosely paired" still roughly holds - counting in B3, complexity in B4, one block apart, same semester = acceptable under the loose-pairing philosophy).
- LEAN: complexity -> B4, counting (MATH-102) stays B3 (or also slides - minor, decide at B4). The loose-pairing philosophy tolerates one-block separation.

### Revised Block 3 (modeling and abstraction)
- CS-104 -> wait, renumbering. Let me keep it conceptual not numbered for now:
- OOP I — encapsulation, inheritance, abstraction, classes (boundary-drawing, domain modeling)
- OOP II — collections, iterators, OOP design principles (abstraction over data access/traversal; SOLID-ish design principles = modeling discipline). Exceptions could move to the Error Handling thread's natural home or stay lightly.
- Data Structures as ADTs — lists/linked-lists/stacks/queues taught CONTRACT-FIRST (the ADT's interface/boundary) then implementation behind the boundary. This reframing is the key insight - data structures become the concrete vehicle for "boundaries and contracts."
- MATH-102 Counting (stays, loosely pairs with complexity now in B4)
That's 3 CS + 1 math = 4 courses. Matches B1's load (4). Acceptable.

### "Boundaries and contracts" - the NEW conceptual introduction, and its thread implications
This is a genuinely important new seed. "Contract" = a promise about behavior at a boundary, independent of implementation. Where does this thread go LATER (it's being INTRODUCED here, so it should spiral)?
- B3: INTRODUCE - ADT contracts (stack promises LIFO), class interfaces/encapsulation (public contract vs private implementation), function contracts (preconditions/postconditions - TIES BACK to B1's informal pre/post-condition reasoning in the Verification thread!). 
  - Big convergence: the Verification thread's B1 seed (informal pre/post-condition reasoning) now gets a NAME and a home in B3 as "contracts." Contracts ARE pre/post-conditions made into a design principle. This retroactively strengthens the Verification thread - B1 informal reasoning -> B3 contracts as design -> B6 formal verification. The contract idea is the bridge between informal B1 reasoning and formal B6 verification.
- B4 (APIs): API contracts - an API endpoint is a contract (request shape -> response shape). The boundary is now a NETWORK boundary. Natural escalation of the contract idea across a process/network boundary.
- B5 (databases): schema as a contract (table structure is a contract about what data looks like); transactions as contracts (all-or-nothing promise). 
- B6 (testing/security): testing AGAINST a contract (does the implementation honor its contract?); security trust boundaries (a contract about what's trusted on each side). Contracts + verification converge formally here.
- B7 (design review): defending the boundaries/contracts you designed.
- B8 (deployment): service contracts / API versioning (semantic versioning RETURNS here - a version number is a contract about compatibility - ties back to B1 git/semver!).

So "Boundaries and Contracts" is potentially a NEW THREAD (Type A spiral) introduced at B3, spiraling B3->B4->B5->B6->B7->B8. It also CONNECTS several existing threads (Verification's pre/post-conditions, APIs, semantic versioning from Git, security trust boundaries). It might be better understood as a UNIFYING thread that ties others together rather than a standalone - it's the abstraction that several concrete threads are instances of. This is conceptually rich - arguably one of the more sophisticated systems-thinking ideas in the whole curriculum, and it fits the program's "systems thinking" emphasis strongly.

FLAG for user: "boundaries and contracts" could be (a) a contained B3 topic, or (b) a new spiraling thread that recurs and ties together APIs/verification/security/versioning. (b) is more powerful and fits the systems-thinking ethos but adds another thread to track. Worth asking.

### Ripple summary
- B3 sheds Algorithmic Complexity -> B4. 
- B4 currently: Trees/Hashing/Hierarchies, APIs & Data Viz, Data Persistence I. Adding Complexity makes B4 = 4 courses. AND data viz rework + stats pairing might also want B4. B4 is getting heavy - will need its own careful pass. FLAG.
- The "structuring data" frame I proposed for B3 in round 11 is now REPLACED by user's "modeling and abstraction" frame - which is broader and better (structuring data is a subset of modeling/abstraction). Good.
- Conceptual spine now: B1 read computation -> B2 modify data -> B3 model & abstract (boundaries/contracts) -> B4 ? (needs a frame; currently the structural-data/performance content). 

## ROUND 13: Boundaries & Contracts promoted to spiraling thread; ADT-first adopted

DECISIONS:
1. Boundaries & Contracts = new Type A spiraling thread, introduced B3, unifying idea across APIs/schemas/testing/security/versioning.
2. Data structures taught contract-first (ADT interface before implementation) in B3.

### Updated thread taxonomy (now 9 spirals + 3 lenses + 1 bounded practice = 13 threads)
TYPE A - CLASSIC SPIRALS (9):
1. Data Structures & Representation
2. Program Correctness / Code Comprehension
3. APIs & Networked Systems
4. HCI / Accessible & Human-Centered Design (now carries TWO embedded throughlines: accessibility + data viz)
5. Algorithmic Thinking & Complexity
6. Git & Version Control
7. Computational Models & Error Handling (flagship)
8. Testing & Formal Verification
9. Boundaries & Contracts (NEW - and partially a META-thread: it names the common structure under APIs, schemas, trust boundaries, versioning, verification)

TYPE B - LENSES (3):
1. Security, Privacy & Ethical Reasoning
2. Documentation Practice
3. Optimization Reasoning

TYPE C - BOUNDED PRACTICE (1):
1. AI-Assisted Development

### Boundaries & Contracts full spiral trace (the canonical definition for the map)
Core idea: a contract is a promise about behavior at a boundary, honored regardless of what's hidden behind it. Each pass introduces a new KIND of boundary the contract spans.

- B3 INTRODUCE: the boundary is an INTERFACE within a single program.
  - ADT contracts: stack = {push, pop, LIFO promise}, queue = {enqueue, dequeue, FIFO promise} - the contract is the interface, the linked-list/array choice is hidden implementation
  - Class encapsulation: public interface = contract, private members = hidden implementation
  - Function pre/post-conditions: the contract of a function (names B1's informal verification reasoning - THE BRIDGE)
  - Lens: "what does this promise, and what does it hide?"
- B4 ESCALATE: the boundary becomes a PROCESS/NETWORK boundary.
  - API contract: request shape -> response shape; the server's implementation is hidden and on another machine
  - Same idea (contract over a boundary) but now the boundary is bigger and the other side is untrusted/unseen
- B5 ESCALATE: the boundary becomes a DATA/PERSISTENCE boundary.
  - Schema as contract (what shape data must have to be stored/retrieved)
  - Transaction as contract (atomicity: all-or-nothing promise)
- B6 CONVERGE: contracts meet verification AND security.
  - Testing = checking an implementation honors its contract
  - Formal verification = proving it does
  - Security trust boundary = a contract about what each side is allowed to assume/trust (and what happens when the contract is violated maliciously - input validation as contract enforcement)
- B7 DEFEND: Design Review - students defend the boundaries they drew and the contracts they specified (why this interface, why this much hidden)
- B8 VERSION: service contracts over TIME.
  - API versioning / semantic versioning returns (callback to B1 Git/semver): a version number is a contract about backward compatibility
  - Breaking vs non-breaking changes = contract violations vs contract-preserving changes
  - This CLOSES a loop opened in B1 (semver was introduced as "what a version communicates" - now students understand it communicates a COMPATIBILITY CONTRACT)

This thread is special: it's both a spiral (escalating boundary types) AND a meta-thread that retroactively unifies Git/semver (B1), Verification (B1 pre/post seed), APIs (B4), Databases (B5), Testing+Security (B6), and versioning (B8). It's arguably the strongest expression of the program's systems-thinking ethos. In the map it should be presented with explicit "this connects to thread X here" cross-references.

### ADT-first teaching note (for B3 design + the map)
Data Structures & Representation thread's B3 pass changes: instead of "lists, linked lists, stacks, queues" as implementations to learn, it's "abstract data types as contracts, then implementations behind the contract." Concretely:
- Introduce each structure by its CONTRACT first (what operations, what guarantees) 
- THEN show 1+ implementations and how they honor the same contract differently (e.g. stack via array vs linked list - same contract, different performance characteristics - which FORESHADOWS the complexity analysis now in B4: "these honor the same contract but differ in cost")
- This creates a beautiful handoff to B4: B3 establishes "same contract, different implementations," B4's complexity analysis answers "so how do we CHOOSE between implementations honoring the same contract?" - complexity becomes the tool for choosing among contract-satisfying options. The B3->B4 move (which I worried was just overload-shedding) is actually a clean conceptual handoff: contracts (B3) -> choosing implementations by cost (B4).

This RESOLVES my earlier worry that moving complexity to B4 was just load-balancing - it's actually pedagogically motivated. B3 "here are the contracts and that multiple implementations satisfy them"; B4 "here's how to analyze and choose among them." 

### Revised conceptual spine
- B1: READ computation (two paradigms)
- B2: MODIFY data & state
- B3: MODEL & ABSTRACT (boundaries & contracts; ADTs; OOP)
- B4: (emerging frame) CHOOSE & STRUCTURE FOR COST? - data structures' implementations, complexity, performance, persistence. Maybe frame = "representation choices and their consequences" or "structure and cost." TBD at B4.

## ROUND 14: Block 4 reframe — "structure & representation across scales" (data, systems, networks, humans)

User frame: structure/representation, but NOT just data structures - structure of SYSTEMS (networks, containers, even humans/organizations). Cross-scale structural thinking.

Current B4 base: CS-110 Trees/Hashing/Hierarchies, CS-111 APIs & Data Viz, CS-112 Data Persistence I.
Plus inbound from B3 reframe: CS-109 Algorithmic Complexity (moved here).
Plus: data viz rework (now embedded HCI throughline, but B4 was its anchor pass), possible STAT-101 pairing (descriptive stats near data work), the checkpoint (end of Year 1).

Naive load = Trees/Hashing + APIs/Viz + Persistence + Complexity = 4 CS + maybe STAT = 5. OVERLOADED again. Same pattern as B3. Need the frame to reorganize, not just accumulate.

### The frame is BIGGER than the current content - does that help or hurt?
"Structure across scales: data, systems, networks, humans" is a UNIFYING frame. The insight: trees/hashing (data structure), API/client-server (system structure), networks (network structure), containers (deployment structure), org charts/teams (human structure) are ALL the same cognitive move - decomposing something into parts + relationships. This is the "modeling and abstraction" of B3 APPLIED UP THE SCALE LADDER from in-program structures to whole-system and human structures.

This actually gives a reason for the OSI networking content to live here (deferred from earlier!) - OSI is literally "network structure as layered abstraction," a perfect instance of cross-scale structure. The deferred Networking Fundamentals question may have found its home: B4's frame WANTS network structure.

But careful: can't cram OSI (2 blocks) + 4 CS courses + stats into B4. The frame is unifying CONCEPTUALLY but B4 is one 8-week block with room for ~3 courses. Need to choose which INSTANCES of "structure across scales" actually get course-time here vs which are touched lightly vs which live in adjacent blocks under the same frame.

### What the cross-scale frame suggests for course allocation
Think of B4 as teaching ONE big idea (structure = parts + relationships, at every scale) through a few concrete instances:
1. DATA structure: Trees/Hashing/Hierarchies (CS-110) - hierarchical & associative structure. KEEP - it's the in-program-scale instance, continues the Data Structures spiral (B3 linear -> B4 hierarchical/associative), and now taught as "structure" not just "data structures."
2. SYSTEM structure: client-server, APIs (part of CS-111) - how a system decomposes across a boundary (ties to Boundaries & Contracts thread B4 pass = network boundary!). KEEP the API/system-structure part.
3. The COMPLEXITY content (CS-109 inbound) - this is "the COST of structural choices" - how does structure affect performance. Fits the frame as the analytical lens on structure. But it's a 4th course. 

Tension: data viz (was CS-111's other half) + persistence (CS-112) + complexity (CS-109 inbound) + trees (CS-110) + system/network structure = too much.

### Reorganization options
The frame lets us see that some current B4 content is actually about DIFFERENT things wearing a "B4" label:
- Data viz: per round 10, this is now an EMBEDDED HCI throughline, NOT a standalone B4 topic. So "APIs & Data Visualization" (CS-111) splits: API/system-structure stays in B4 (fits frame), data-viz becomes embedded practice (the B4 viz pass happens, but woven into whatever course shows data, not its own course slot). This frees roughly half a course.
- Data Persistence I (CS-112): "files, CSV/JSON, why we need a database." Is persistence "structure across scales"? Persistence is more about TIME/durability than structure. It's a bridge-to-B5 motivator. Under the structure frame, persistence is a weaker fit. CANDIDATE TO MOVE or compress: persistence could fold into B5 (databases) where it naturally belongs - "why we need a database" is literally the B5 intro. Moving CS-112's content into B5's front end frees a B4 slot AND tightens B5. This was flagged way back (CS-112 as a possible cut/compress candidate for the OSI budget). The structure frame confirms persistence doesn't really belong in B4.
- That leaves B4 = Trees/Hashing (data structure) + APIs/system-structure + Complexity (cost of structure) = 3 CS courses, all tightly on-frame. Data viz embedded (not a slot). Persistence -> B5.

### Where does "systems, networks, containers, humans" structure get its due?
The frame explicitly names networks, containers, humans. But B4 as 3 courses (trees, API/system, complexity) only lightly touches those. Resolution:
- NETWORKS: this is where OSI Networking Fundamentals connects. If OSI lands in Year 1 Spring (B3+B4) or as a 2-block sequence, B4 could host one OSI block as the "network structure" instance. BUT that's additional credit (soft budget). Alternatively, network structure is touched via the API/client-server content (CS-111) lightly, and OSI-proper is its own service course placed during cross-block optimization. DEFER per earlier user call, but NOTE B4's frame is the natural conceptual host for network structure.
- CONTAINERS: container/deployment structure is really a B8 (deployment) topic. In B4 it can be FORESHADOWED ("a container is another boundary with a contract" - ties Boundaries thread) but containers proper = B8. Don't force into B4.
- HUMANS/ORGANIZATIONS: structure of teams/orgs. This is interesting - it connects to the Collaboration thread (B6 team project) and Professional Practice. In B4 it could appear as a light CONCEPTUAL parallel ("the same decomposition thinking applies to how teams are structured - Conway's Law: systems mirror the orgs that build them"). Conway's Law is a GREAT B4 seed - it explicitly links system structure and human structure, which is exactly the cross-scale frame. Light touch, big idea, no new course needed - could be a discussion/reading woven into the API/system-structure course. Then it spirals to B6 (when teams actually form) and B7/B8.

### Revised Block 4 (structure & representation across scales)
- Trees, Hashing & Hierarchies — in-program data structure (Data Structures spiral pass; taught as "structure," contracts from B3 continue: a tree/map has a contract too)
- Systems & APIs — client-server decomposition, API as system structure across a network boundary (APIs spiral pass + Boundaries & Contracts B4 pass + Conway's Law seed linking system & human structure + light network-structure touch)
- Algorithmic Complexity — the cost of structural choices; how to choose among contract-satisfying implementations (Algorithmic Thinking spiral; clean handoff from B3 contracts; pairs loosely with MATH-102 counting one block back)
- Data viz: EMBEDDED (HCI throughline pass) - woven into Trees (visualize a tree?) or Systems (visualize API data) - not a course slot
- Persistence: MOVED to B5 front-end
- (external pairing: STAT-101 descriptive stats is a candidate here - "describing the shape/structure of data" fits the structure frame and pairs with any data-handling; or it slots B5 with databases. DEFER exact stats placement to cross-block optimization, but NOTE B4 is a reasonable home for STAT-101 thematically.)
3 CS + possibly 1 stat. On-frame and not overloaded.

### Checkpoint note
B4 is the end-of-Year-1 checkpoint. Under the reframe, what has a student who exits after B4 got? Read computation (B1), modify data (B2), model/abstract with contracts (B3), structure across scales + cost analysis (B4). Plus the transfer-aligned core (prog fundamentals, OOP, data structures). That's STILL a coherent, defensible exit point - arguably MORE coherent now (the read->modify->model->structure spine is a clean story). Moving persistence to B5 means the exiting student hasn't done databases - but they were never going to finish databases by B4 anyway (DB was B5). The "why we need a database" motivator moving to B5 is fine for the checkpoint - an exiting student has files/CSV/JSON from B2's data transformation work, which is enough.

### Conceptual spine (updated)
- B1 READ computation
- B2 MODIFY data & state
- B3 MODEL & ABSTRACT (contracts, ADTs, OOP)
- B4 STRUCTURE across scales (data/system/network/human; cost of structure)
- [END YEAR 1 CHECKPOINT]
- B5 onward: Year 2...

### Open items from this round
1. STAT-101 placement (B4 vs B5) - defer to optimization
2. OSI networking - B4 is conceptual host for "network structure" but credit is soft - defer
3. Persistence moving B4->B5 - confirm with user (it's a real content move, affects B5)
4. Conway's Law / human-structure seed - confirm user wants the "structure of humans/orgs" thread actually seeded here (they NAMED humans in the frame, so likely yes, but it's a non-obvious inclusion worth confirming)

## ROUND 15: Persistence split (representation vs durability) + human/org structure thread confirmed

### DECISION 1: Files/CSV/JSON split into two distinct ideas
- FILE FORMATS AS DATA REPRESENTATION (encountered, not taught as topic): appears naturally across early blocks
  - B1: files/CSV/JSON as representations of data we CONSUME/read (already consistent with B1's "reading" frame + file I/O "appears in code students read" decision from round 5). Reinforce: CSV/JSON are just more representations to read, alongside the imperative/functional code.
  - B2: files/CSV/JSON as SOURCES and SINKS of data transformations (consistent with B2 "modifying data" frame + the new CS-104 Data Transformation course - parse CSV in, transform, write JSON out). Natural fit, already implied.
  - B3: files/CSV/JSON when considering HOW TO REPRESENT data (consistent with B3 "modeling/abstraction" - choosing a representation IS a modeling decision; "should this be CSV or JSON" is a representation/contract question). 
  - This means by the time persistence-proper comes in B5, students have informally USED file formats for 4 blocks - classic spiral (practice before formalize). The B5 persistence content isn't "here's CSV" (they know it), it's "why are files INSUFFICIENT - why do we need a database" (durability, concurrent access, querying, integrity).
- PERSISTENCE AS DURABILITY/DATABASE-MOTIVATOR (taught topic): moves to B5 front-end. The "why we need a database" motivator. NOT in B4.

This is cleaner than original CS-112. Original CS-112 conflated "here are file formats" (which students now meet incrementally B1-B3) with "why we need a database" (B5 motivator). Splitting them removes the redundancy and frees the B4 slot legitimately.

CONSISTENCY CHECK against prior block decisions:
- B1 round 5: file I/O "appears in code students read, not separately taught" - CONSISTENT (CSV/JSON as readable representations)
- B2 round 11: CS-104 Data Transformation parses/reshapes CSV/JSON - CONSISTENT (sources/sinks)
- B3 round 12-13: modeling/abstraction, representation choices - CONSISTENT (representation decisions)
All consistent. No contradictions introduced. Good.

### DECISION 2: Human/Organizational Structure = real thread, seeded B4 via Conway's Law
New thread. Where does it sit in taxonomy? It's about how systems and human orgs mirror each other and how to structure collaborative work. Candidate type:
- Not a classic data/code spiral (Type A in the technical sense)
- It's closer to Professional Practice. But it does ESCALATE in depth across blocks (Conway's Law concept -> actual team structure -> defending/operating as a team), so it's spiral-shaped.
- Probably belongs as a Type A spiral but in the "professional/human" family rather than technical family. Or could be seen as part of a broader Professional Practice thread.

Let me define its passes:
- B4 SEED: Conway's Law - "systems mirror the organizations that build them." Conceptual. Students observe the parallel between system decomposition (which they're learning) and org decomposition. Light - a reading + discussion woven into the Systems & APIs course. Connects system structure (technical) to human structure (social).
- B6 ENACT: Team Software Project begins. NOW students ARE an organization building a system. Conway's Law becomes lived - how they divide the work shapes what they build. Team structure, roles, communication overhead (Brooks's Law - adding people to a late project makes it later - another classic). Collaboration thread (git collaborative) converges here.
- B7 DEFEND: Design Review - defending not just technical structure but how the team organized to produce it; team retrospective on whether their structure helped or hurt.
- B8 OPERATE/REFLECT: operating a system as a team; reflection on the system-team mirror over the whole project. Postmortem culture (blameless postmortems - a human/org practice for handling failure, ties to Error Handling thread's "errors are normative" stance - blameless postmortem is the ORG-level expression of "errors are normal, not shameful").

Beautiful convergence at B8: Error Handling thread (errors normative) + Human/Org thread (blameless postmortem) meet - the org-culture expression of the technical stance on errors. 

This thread also retroactively enriches the Collaboration/Git thread (they were going to cover team practices at B6 anyway) - now there's a CONCEPTUAL spine (Conway -> lived team -> defend -> reflect) underneath the practical git-collaboration skills. The two complement: Git-collaboration = the TOOL, Human/Org structure = the WHY/the social reality the tool serves.

Naming: "Systems & Human Organization" or "Sociotechnical Structure" or "Teams & Conway's Law" - the idea is sociotechnical: systems and the humans building them are one structural fabric. This is sophisticated systems-thinking and strongly fits the program ethos (the notional machine's top layer is "Users"/"People" - and now the BUILDERS are also modeled structurally, not just the users).

### Updated thread taxonomy (now 10 spirals + 3 lenses + 1 bounded practice = 14 threads)
Added: Sociotechnical Structure (Conway's Law / human-org) as a spiral (professional/human family).
Note: getting to a LOT of threads (14). At some point worth checking this isn't over-engineered - but each was user-driven and they do interconnect rather than fragment. The convergence points (B6, B8 especially) are where many threads meet, which is the sign they're well-integrated rather than scattered. Worth a future "is 14 threads too many to track / how do we keep this legible to faculty" meta-check, but not now.

### Block 4 final shape (structure & representation across scales)
- Trees, Hashing & Hierarchies (data-scale structure; Data Structures spiral; carries B3 contracts)
- Systems & APIs (system structure across network boundary; APIs spiral + Boundaries & Contracts B4 pass + Conway's Law seed for Sociotechnical thread + light network-structure touch)
- Algorithmic Complexity (cost of structural choices; Algorithmic Thinking spiral; handoff from B3 contracts; loose pair w/ MATH-102)
- Data viz: embedded HCI pass (not a slot)
- Persistence: NOT here (moved to B5); file formats appear as representation only
- STAT-101 descriptive stats: candidate external pairing (defer)
3 CS courses. On-frame, not overloaded.

### Conceptual spine (stable through end of Year 1)
- B1 READ computation (two paradigms)
- B2 MODIFY data & state
- B3 MODEL & ABSTRACT (contracts, ADTs, OOP)
- B4 STRUCTURE across scales (data/system/network/human; cost)
- [END YEAR 1 CHECKPOINT]

## ROUND 16: Block 5 — frame + resolve the service-course sequencing tension

### Two unresolved tensions sitting in B5:
TENSION A: Service course wants SQL (B5) -> Database Design (B6) SEQUENTIAL. But that pushes Database Design into already-dense B6. Alternatively keep both in B5 (parallel) and the service course is "both halves of B5's data content" but then it's not two-back-to-back-blocks, it's one block's worth = only 8 weeks = only 1-2 credits, too small for a recognizable "Relational Databases" semester course.
   - Actually reconsider: a service "Relational Databases" course = 2 credits (2 x 1-credit blocks) if SQL + Design are sequential across B5+B6. OR could it be SQL(B5) + Design(B5) both in B5 = 2 credits in ONE block (parallel) - a visiting student takes both 1-credit courses simultaneously in the first 8 weeks. That's 2 credits in 8 weeks = a half-semester intensive. Recognizable? Less so than a full semester, but possible as a 2-credit service offering. Hmm.
   - The cleanest service-course shape is a full semester (16wk). That REQUIRES sequential across B5+B6. So the service-course goal and the B6-density goal genuinely conflict. Must pick.

TENSION B: Math sequencing. MATH-103 (Recursive & Modular Computation) is in B5. But CS needs recursion informally back in B3/B4 (trees, hierarchies). And modular arithmetic in MATH-103 sets up crypto for B6 security. So MATH-103's placement is fine for the crypto handoff (B5->B6) but LATE for recursion (CS needed it B3/B4). Already flagged as "informal before formal" so probably OK, but worth noting recursion's formal treatment trails its first CS use by 1-2 blocks.

### Block 5 frame
Original question: "how do we store and reason about information at scale." Given Year 1 spine (read->modify->model->structure), Year 2 should escalate. B5 natural frame candidates:
- "PERSISTENCE & QUERYABLE DATA" - storing and asking questions of data that outlives the program
- "INFORMATION AT REST vs DATA IN MOTION" - Year 1 was mostly data in motion (transform, render); B5 is data at rest (stored, queried)
- Given the cross-scale/structure frame of B4, B5 could be "structure that PERSISTS and that many agents share" - the schema is a SHARED structure (multiple programs/users agree on it = a contract), persistent over time, queryable. This connects B4 (structure) -> B5 (shared persistent structure) nicely.
LEAN: frame = "Information at rest: shared, persistent, queryable structure." Emphasizes (a) persistence (vs Year 1's transient data), (b) SHARED (multiple agents - ties to concurrency/Computational Models pass + the schema-as-contract Boundaries pass), (c) queryable (the new capability - asking questions of data).

This frame absorbs the inbound threads coherently:
- Persistence motivator ("why files aren't enough") = the frame's opening
- Schema as contract (Boundaries thread) = "shared structure multiple agents agree on"
- Concurrent access/transactions (Computational Models thread) = "shared" implies concurrency
- Query optimization (Optimization lens) = "queryable" implies "queryable EFFICIENTLY"
- Data minimization + access control (Security lens) = "shared" implies "who can see/touch what"
- Data Investigation signature assessment = "reason about information" = querying as investigation
- Data viz pass (HCI) = visualizing query results = the output side of querying
All on-frame. Good.

### Resolving Tension A (service course vs B6 density)
Decision needs user input, but let me frame the options clearly:
Option 1: SQL (B5) + Database Design (B6) sequential. Service course = clean full-semester "Relational Databases." Cost: B6 gets a 4th course (Database Design) on top of Testing/Security/Collaboration - and B6 is the "everything formalizes / team project begins" block, already the 2nd densest. Bad for B6.
Option 2: SQL + Database Design both in B5 (parallel, as originally). Service course = 2-credit half-semester intensive (less ideal shape, but offerable). B5 then has SQL + Design + persistence-intro + MATH-103 = could be 3 CS-ish + 1 math if persistence folds into SQL or Design rather than being its own course. B6 stays clean.
Option 3: Rethink what the service course IS. Maybe "Relational Databases" service course = SQL Fundamentals (B5) + a B6 course that ISN'T the same as our majors' Database Design - i.e. the service course's second half is lighter/applied (e.g. "Querying & Reporting for [non-majors]") while our majors get Database Design (schema/normalization, more rigorous) integrated differently. But this = more course development (separate service second-half). Probably too costly.
Option 4: Persistence-intro folds into the front of SQL Fundamentals (not a separate course). B5 = SQL Fundamentals (incl. persistence motivator) + Database Design + MATH-103 = 2 CS + 1 math. Lighter than feared. Then for the SERVICE course, offer SQL+Design as B5's two courses = a 2-credit intensive OR stretch to 16 weeks for visiting students as a differently-paced section. Keeps B6 clean. This is basically Option 2 refined - persistence doesn't need its own course, it's the first week or two of SQL Fundamentals.

LEAN: Option 4. Persistence motivator = opening of SQL Fundamentals, not a separate course. B5 = SQL Fundamentals + Database Design (both, in B5) + MATH-103. Service "Relational Databases" = those two CS courses, offered to visiting students as a paired 2-credit unit (or a 16-week paced section if registrar prefers). B6 stays unburdened. The service course being 2 credits rather than 3-4 is a minor downside but acceptable - many service courses are modest.

This also means the earlier "Database Design -> B6" idea (round 7) is REVERSED - keep it in B5. Need to flag this reversal to user clearly since they may remember the round-7 framing.

### Block 5 final shape (proposed)
- SQL Fundamentals — persistence motivator (why files aren't enough) as the opener, then SELECT/INSERT/UPDATE/DELETE/JOIN. Queryable data. Query optimization SEED (indexes/query plans - light, the Optimization lens pass). 
- Database Design — schema design, normalization, relational modeling. Schema-as-contract (Boundaries pass). Data minimization + access-control-as-schema-dimension (Security pass). Documentation: schema-decision docs. Transactions/concurrency (Computational Models pass - "shared" data). Data Investigation signature assessment anchored here.
- MATH-103 Recursive & Modular Computation (external; modular arithmetic sets up B6 crypto)
- Data viz: embedded HCI pass (visualize query results as investigation) - woven in, not a slot
- STAT-101 descriptive stats: STILL a candidate external pairing for B5 (describing data you're now storing/querying) vs B4. Defer, but B5 is arguably the BETTER home now (you have real stored data to describe). Lean B5 for STAT-101.
- Solo Git branching: embedded practice (Git thread pass 3) - woven into Database Design (branch to try a schema alternative)
- AI design-discussion (medium stakes): woven into Database Design (discuss schema alternatives w/ AI, justify own choice)
2 CS + 1 math (+ possibly STAT-101). On-frame.

Note: B5 at 2 CS courses is LIGHTER than other blocks (most have 3 CS). This is fine and maybe good - it leaves room for STAT-101 here, and Year 2 Fall (B5+B6) balances if B6 is the dense one. But worth noting the asymmetry - could also pull something INTO B5 to balance B6. That's cross-block optimization, defer.

## ROUND 17: B5 decisions locked + service-course model generalized

DECISIONS:
1. Keep BOTH SQL Fundamentals + Database Design in Block 5 (round-7 push-to-B6 REVERSED). Block 6 stays unburdened.
2. STAT-101 Descriptive Statistics pairs in Block 5.

### Service-course model - GENERALIZED INSIGHT (important, applies beyond B5)
User reframe: the 2-credit "Relational Databases" service unit is EXPECTED to be followed by a DEPARTMENTAL domain-application course (in the visiting student's home dept). So:
  Service progression for a visiting student = [our shared foundational unit] + [their department's domain-application course] = one semester.
This means our service courses are intentionally MODEST shared foundations (2 credits), NOT full standalone semesters. The domain application is owned by the partner department, not us. This is a clean division of labor:
  - We provide: rigorous, domain-neutral foundation (relational databases; OSI networking; etc.)
  - They provide: domain application (business data apps; network administration; CompE low-level implementation)
This GENERALIZES to all service courses:
  - Relational Databases (our 2cr foundation) -> e.g. Business Data Applications (business dept) 
  - OSI Networking Fundamentals (our foundation) -> Network Administration (business), low-level implementation (CompE), etc. [exactly what user said in round 8!]
So the round-8 OSI model and the round-17 databases model are THE SAME PATTERN. Consistent. This pattern should be stated explicitly in the curriculum doc as "the service-course model": we own shared theoretical/foundational units; partner departments own domain application; together they form a one-semester progression for the visiting student. This also bounds OUR development cost (we don't build domain-specific variants) and clarifies what makes a good service-course candidate: domain-neutral, foundational, recognizable, prerequisite-light.

This also retroactively clarifies the OSI networking budget question (still soft): OSI as a 2-credit foundation unit (lower layers + upper layers, the 2-block split from round 8) parallels the databases 2-credit unit exactly. Both are 2-credit shared foundations. Good structural consistency.

### Block 5 final shape (locked)
- CS-201 SQL Fundamentals — persistence motivator (why files aren't enough) as opener; SELECT/INSERT/UPDATE/DELETE/JOIN; query optimization seed (indexes/query plans, Optimization lens, light)
- CS-202 Database Design — schema design, normalization, relational modeling; schema-as-contract (Boundaries pass); data minimization + access control (Security pass); transactions/concurrency (Computational Models pass); schema-decision docs (Documentation); Data Investigation signature assessment anchored here; solo Git branching + AI design-discussion embedded
- MATH-103 Recursive & Modular Computation (external; modular arithmetic -> B6 crypto)
- STAT-101 Descriptive Statistics (external; describe the data you now store/query; pairs with Data Investigation; feeds data-viz HCI pass)
- Data viz: embedded HCI pass (visualize query results as investigation)
= 2 CS + 2 external (1 math, 1 stat). 

Load note: 2 CS + 2 external = 4 courses, matches B1's 4-course load. The two external courses (MATH-103 + STAT-101) both landing in B5 is the first time two externals share a block. Is that too much external load at once? MATH-103 (recursion/modular) and STAT-101 (descriptive stats) are different enough in kind that it's probably OK, and both are 1-credit/8-week. But FLAG: B5 now has the "two externals" property - worth noting for the external-course-rhythm question (originally posited externals alternate odd/even blocks; now B5 has both a math AND a stat). The clean "one external per block" rhythm is broken here. Acceptable but note it.

### Year 2 spine so far
- B5 INFORMATION AT REST: shared, persistent, queryable structure (+ describing it statistically)
- B6 onward TBD
Year 1 was: read -> modify -> model -> structure (data in motion mostly)
Year 2 opens: data at rest / stored / shared / queried. Good escalation.

### Carry-forward flags
- B6 density still the big open question (testing + security + collaboration + team project START). Now at least NOT also absorbing Database Design. Next block to tackle.
- Two-externals-in-B5 breaks the clean external rhythm (minor)
- STAT sequence: STAT-101 now in B5. STAT-102 (probability - contested ownership w/ discrete), 103, 104 still unplaced. Probability ownership still flagged for cross-dept co-design.
- Recursion formal (MATH-103, B5) trails CS informal use (B3/B4) - informal-before-formal, acceptable.

## ROUND 18: Block 6 reframe — "Responsible Development" (was "Security & Engineering")

User: increasingly thinks of B6 as "Responsible Development" rather than "Security & Engineering."

Current B6 base: CS-203 Testing & Validation, CS-204 Security Fundamentals, CS-205 Collaborative Development. Question already is "how do we build software others can trust?" - which is ALREADY a responsibility framing, the rename just makes it explicit.

### Does "Responsible Development" unify the block, or just rename it?
Test: does the frame give each course a reason to be there UNDER ONE IDEA?
"Responsible Development" = building software responsibly: to others (teammates), for others (users), and accountably (it works, it's safe, you can stand behind it).

- Testing & Validation: responsibility for CORRECTNESS - "I verified it works, I don't just hope it does." Testing IS the practice of taking responsibility for your claims about your code. Formal verification (added round earlier) = the strongest form of that responsibility. FITS - testing reframed from "a skill" to "how you take responsibility for correctness."
- Security Fundamentals: responsibility for SAFETY/HARM - "I considered how this could be misused or breached, who could be hurt." Security as a responsibility to users/society, not just a technical add-on. FITS strongly.
- Collaborative Development: responsibility TO TEAMMATES - code review, clear commits, not breaking the build for others. FITS - collaboration reframed as the social responsibilities of shared work.
- Team Software Project (signature assessment): the integrative context where all three responsibilities are exercised at once. FITS - it's literally where you're responsible to a team, for a working product, safely.

So the frame genuinely unifies - all three courses become facets of one stance (responsibility: for correctness, for safety, to others). This is BETTER than "Security & Engineering" which just listed two topics. The rename is a real conceptual upgrade.

### The frame ALSO helps with density - here's how
B6 was the dreaded "everything formalizes at once" overload block. Reframing as Responsible Development reveals that the convergence is NOT incidental overload - it's the POINT. Testing, security, and collaboration formalize together here BECAUSE they're three faces of the same competency (responsibility), and that competency can only really be exercised in an integrative, team-based, building-real-things context - which is exactly what B6 is (Team Software Project). So the density is pedagogically justified: you can't learn "responsible development" as three separate isolated skills; it has to converge. The block's identity REQUIRES the convergence.

That said, justified-density is still density. The frame doesn't reduce the WORKLOAD, it just makes it coherent. Mechanical load check still needed (like B1). But the threads converging here now have a NARRATIVE reason, which helps students (and faculty) see it as one thing with facets rather than three unrelated demands.

### Threads converging at B6 (from earlier rounds) - re-examined under the frame
- Testing & Formal Verification (formal pass): responsibility for correctness. CORE.
- Security/Privacy/Ethics (lens, formalizes here): responsibility for safety/harm. CORE.
- Git collaborative / PRs / conflicts (Git thread pass 4): responsibility to teammates. CORE.
- Sociotechnical/Conway's Law (thread pass 2 - ENACT): team IS an org now; Brooks's Law, communication overhead. CORE - the team project makes Conway's lived.
- Documentation (lens, team-facing register): responsibility to teammates (docs others depend on). FITS.
- Boundaries & Contracts (pass: testing against a contract, security trust boundary): responsibility = honoring contracts. FITS.
- Computational Models/Error Handling (pass: errors as attack surface): responsible handling of failure. FITS.
- AI-assisted (pass: AI code review as ONE input, not a replacement): responsible use of AI in review. FITS - and notably "responsible" is literally the frame, so AI-responsibility fits perfectly here.
- Optimization lens: not a strong B6 touch, mostly absent here (it's B5/B7). Fine.

Nearly every thread that touches B6 is genuinely an instance of "responsibility." The frame is remarkably cohesive - more so than any block except maybe B1. This is a sign the original architecture had B6 right thematically but mis-NAMED it.

### Ethics gets a real home (was previously thin/embedded-only)
Earlier rounds noted Ethics was only ever a lens (embedded in Security/Privacy), never with a strong dedicated moment. "Responsible Development" as a block FRAME gives ethics its strongest home - not as a separate ethics course (which the program philosophy rejects - competencies embedded not siloed), but as the EXPLICIT ORGANIZING PRINCIPLE of an entire block. Ethics/responsibility stops being a footnote in the security course and becomes the lens through which the whole block is understood. This likely satisfies ABET's ethics/professional-responsibility outcomes strongly (worth noting for accreditation mapping - ABET wants "recognize professional responsibilities and make informed judgments... considering... ethical principles"). FLAG: B6 as Responsible Development is probably a key ABET-outcomes anchor - note for the accreditation mapping.

### Does anything need to MOVE in or out given the frame?
- The frame doesn't pull anything NEW in that isn't already here. 
- Does anything leave? All three courses fit. No.
- One consideration: should there be an explicit "responsibility/ethics" reflective element as the block's INTEGRATIVE thread - e.g., the Team Software Project includes a responsibility retrospective (did we test enough? did we consider misuse? did we communicate well as a team?). This makes the frame's stance assessable rather than just thematic. LEAN yes - the Team Software Project should carry an explicit responsibility-reflection component (ties Reflection recurring experience + ethics + Conway retrospective together). Low cost (it's a reflection layer on the existing project), high coherence payoff.

### Block 6 shape (frame: Responsible Development)
- CS-203 Software Testing & Validation (responsibility for correctness; testing AND formal verification formalized together; testing-against-a-contract Boundaries pass)
- CS-204 Security Fundamentals (responsibility for safety/harm; authn/authz, threat modeling, applied crypto from MATH-103; errors-as-attack-surface; trust boundaries; least privilege + least collection)
- CS-205 Collaborative Development (responsibility to teammates; collaborative git/PRs/code review; Conway's Law ENACTED; Brooks's Law; team-facing documentation; Team Software Project begins; AI-as-one-review-input)
- Integrative: Team Software Project carries a RESPONSIBILITY RETROSPECTIVE (reflection: correctness, safety, teamwork) - makes the stance assessable
3 CS courses. No external (B6 is even block; if stats follows even-rhythm a STAT could land here, but B5 already took STAT-101 and broke the rhythm; B6 staying 3 CS / no external is fine and helps density). 

Density verdict: still the heaviest block by thread-count, but now thematically unified and pedagogically justified. Mechanical week-by-week check advisable (defer to when we do schedules). The frame is a clear win.

### Year 2 spine
- B5 INFORMATION AT REST (store/share/query/describe data)
- B6 RESPONSIBLE DEVELOPMENT (build software you can stand behind: correct, safe, collaborative)
- B7, B8 TBD

## ROUND 19: Block 7 frame

Current B7: CS-206 Graphs & Network Algorithms, CS-207 Document Databases & Data Integration, MATH-104 Graphs/Trees/Networks. Signature assessment: Design Review. Original question "how do structure and connectivity shape systems?"

### Observation: B7 is where DEFENSE/JUSTIFICATION clusters
Nearly every thread's B7 pass is a "justify under scrutiny" moment:
- Design Review (signature assessment) = defend structural choices
- Boundaries & Contracts B7 pass = defend the boundaries/contracts you designed
- Sociotechnical B7 pass = defend/retrospect how the team organized
- HCI B7 pass = defend usability/accessibility choices (Design Review should include usability defense)
- Security B7 pass = defend your handling of re-identification risk in combined data
- Data Structures B7 pass = graphs as most-general representation (defend representation choice)
This clustering suggests the frame is about JUDGMENT/DEFENSE - "can you justify what you built to a skeptical audience?"

But there's ALSO a strong CONTENT throughline: graphs + NoSQL + data integration are all about CONNECTING things that weren't designed to connect - arbitrary relationships (graphs), flexible/irregular data (NoSQL), combining disparate sources (integration). That's a "connectivity / integration / the messy real world" content theme.

So B7 has TWO candidate frames:
(a) JUDGMENT & DEFENSE - "justify your design decisions under scrutiny" (the Design Review/assessment lens)
(b) CONNECTION & INTEGRATION - "connecting things not designed to connect; the irregular real world" (the content lens)

Are these compatible? Yes, beautifully: B7 is where students INTEGRATE messy real-world systems (graphs, NoSQL, multi-source data) AND defend their integration decisions (Design Review). The content (integration of the messy/arbitrary) NATURALLY demands judgment/defense (there's no single right answer when integrating messy data, so you must DEFEND your choices). The two frames are the same coin: when the problem stops having clean answers (integration of irregular real-world data), the skill becomes JUDGMENT and the assessment becomes DEFENSE.

Possible unified frame: "INTEGRATION & JUDGMENT" or "CONNECTING THE MESSY REAL WORLD" or "DESIGN UNDER UNCERTAINTY" - the block where problems stop having single right answers and you must integrate disparate things and DEFEND your choices.

Contrast with earlier blocks to check escalation:
- B3 MODEL & ABSTRACT: clean modeling, contracts (right answers exist)
- B4 STRUCTURE across scales: structural analysis (cost has right answers via Big-O)
- B5 INFORMATION AT REST: store/query (SQL has right answers)
- B6 RESPONSIBLE DEVELOPMENT: build it right (testing has pass/fail)
- B7 INTEGRATION & JUDGMENT: messy connection, no single right answer, defend your call <- this is a real escalation into AMBIGUITY. First block where "it depends / defend your reasoning" dominates.
- B8 TBD (deployment/operation - real world stakes)

This is a strong escalation: B7 is where the curriculum first seriously confronts AMBIGUITY and PROFESSIONAL JUDGMENT (vs earlier blocks' more-determinate problems). That fits the program's "graduate archetype" (systems thinker, product owner, professional - not just coder) and the Design Review signature assessment perfectly. It also pairs with the "requirements are ambiguous" idea I'd earlier flagged as out-of-scope - a LIGHT version of design-under-ambiguity fits here, full version in capstone.

### Does the frame pull anything in/out?
- CS-206 Graphs & Network Algorithms: graphs = arbitrary connection (integration of any-to-any relationships); shortest path/MST = optimization (defend the "best" path under a metric). FITS both frames. Keep.
- CS-207 Document Databases & Data Integration: NoSQL (data that doesn't fit clean relational models) + integration (combining sources). LITERALLY the integration frame. Keep. This is the core of frame (b).
- MATH-104 Graphs/Trees/Networks: external, pairs w/ CS-206. Keep.
- Design Review: the judgment/defense assessment. Core to frame (a). Keep.
Nothing needs to move. The frame is descriptive of what's already well-clustered here - B7 was already coherent, it just needed naming. (Unlike B2/B3/B4 which needed real reorganization.)

### One enrichment the frame suggests
The "design under uncertainty / no single right answer" character means B7 is the natural home for a light treatment of TRADEOFF REASONING as an explicit skill - which connects to Optimization lens (optimizing across COMPETING objectives, not one metric - e.g. integrate for speed vs completeness vs privacy). Multi-objective tradeoff (you can't maximize everything) is a sophisticated judgment skill that fits "integration & judgment" and sets up the AI-degree's optimization needs. Light touch, woven into Design Review (defend your tradeoff, not just your structure). LEAN: name tradeoff reasoning explicitly in the Design Review here.

### Block 7 shape (frame: Integration & Judgment / Design Under Uncertainty)
- CS-206 Graphs & Network Algorithms (arbitrary connection; shortest-path/MST as optimization; graphs as most-general representation; Data Structures spiral terminal pass)
- CS-207 Document Databases & Data Integration (NoSQL = data that resists clean models; multi-source integration; re-identification privacy pass = Security; data-viz-as-investigation = HCI)
- MATH-104 Graphs, Trees, and Networks (external)
- Design Review (signature assessment): defend structures, contracts, team org, usability, AND tradeoffs under scrutiny. The convergence point for the "defense" passes of Boundaries, Sociotechnical, HCI threads. Tradeoff reasoning named explicitly.
3 CS-ish (2 CS + 1 math). On-frame, NOT overloaded (unlike B6). B7 is lighter than B6 - good rhythm (intense B6 -> judgment-focused B7).

### Year 2 spine
- B5 INFORMATION AT REST
- B6 RESPONSIBLE DEVELOPMENT
- B7 INTEGRATION & JUDGMENT (design under uncertainty; defend your calls)
- B8 TBD (deployment/operation/capstone-bridge)

## ROUND 20: Block 8 — frame + honest overload check

Current B8: CS-208 Deployment & Operations, CS-209 Accessible & Human-Centered Design, CS-210 Data Analysis & AI-Assisted Development. System Integration Project bridges to capstone. Question "how do we deliver, deploy, and stand behind our work?"

### Frame
B8 is the terminus + capstone bridge. Threads landing final passes here: Computational Models (prod concurrency), Algorithmic Thinking (real bottleneck), Error Handling (prod fault-tolerance, OTP comparison), Security (harden-before-live), HCI (requirements-driven UX), Boundaries&Contracts (versioning closes B1 loop), Sociotechnical (blameless postmortem), AI (high-stakes verification), Documentation (operational runbooks), Testing/Verification (harder cases).

Common element: ALL of these are about the system meeting the REAL WORLD - real users, real load, real failure, real consequences, real time (versioning/operations). Year 1-B7 was building/judging in a relatively controlled setting; B8 is "it's live, people depend on it, things break, you're accountable."

Frame candidates:
(a) "DELIVERY & OPERATION" - shipping and running real systems (current, descriptive)
(b) "IN PRODUCTION / MEETING THE REAL WORLD" - the system leaves the lab; real stakes
(c) "ACCOUNTABILITY / STANDING BEHIND YOUR WORK" - the responsibility frame of B6 escalated to live-system stakes

(b) and (c) combine well: B8 = where systems meet the real world AND you remain accountable once they do. This is the natural terminal escalation:
- B6 RESPONSIBLE DEVELOPMENT = build it responsibly (controlled setting)
- B8 = ...now it's LIVE and real people depend on it; operate it accountably, and bridge to the capstone
The distinction B6 vs B8: B6 is responsibility BEFORE release (test, secure, collaborate); B8 is responsibility AFTER release / in operation (deploy, monitor, handle real failure, maintain, version, reflect via postmortem). Pre-release vs post-release responsibility. Clean pairing - B6 and B8 are the two halves of professional accountability, bracketing B7's judgment block.

LEAN frame: "IN PRODUCTION: meeting the real world, staying accountable." Or "DELIVERY, OPERATION & ACCOUNTABILITY."

### Conceptual spine COMPLETE
- B1 READ computation
- B2 MODIFY data & state
- B3 MODEL & ABSTRACT (contracts)
- B4 STRUCTURE across scales
- [YEAR 1 CHECKPOINT]
- B5 INFORMATION AT REST (store/query/describe)
- B6 RESPONSIBLE DEVELOPMENT (build it right - pre-release accountability)
- B7 INTEGRATION & JUDGMENT (design under uncertainty)
- B8 IN PRODUCTION (deliver/operate; post-release accountability; capstone bridge)
This is a genuinely coherent two-year narrative arc: read -> modify -> model -> structure -> store -> build-responsibly -> judge -> operate. Each verb escalates. Strong.

### HONEST OVERLOAD CHECK
B8 has 3 courses (CS-208/209/210). The 8 thread final-passes - are they NEW CONTENT or REFRAMES of existing skills at higher stakes?
- Computational Models/prod concurrency: REFRAME (concurrency seeded B2/B4/B5/7) + a bit new (OTP/supervision comparison is genuinely new conceptual content). ~20% new.
- Algorithmic/real bottleneck: REFRAME (Big-O from B3/B4 applied to real system). Mostly not new.
- Error Handling/prod fault-tolerance: PARTLY NEW - the OTP/supervision-tree/circuit-breaker comparison is new conceptual material (flagged as distinctive). This is real new content.
- Security/harden-before-live: REFRAME (security from B6 applied). Not new.
- HCI/requirements-driven UX: PARTLY NEW - formal requirements gathering is a new skill vs B2's accessibility-compliance. Real new content (it's CS-209's core).
- Boundaries/versioning: REFRAME (semver from B1, contracts from B3-7). Closing a loop, not new.
- Sociotechnical/postmortem: light REFRAME (Conway from B4/B6). Not heavy.
- AI/high-stakes verification: PARTLY NEW - critiquing AI-generated code as a subject is the new explicit skill (CS-210 core). Real new content.
- Documentation/runbooks: REFRAME (docs from B1 onward, new register). Light.
- Data analysis (notebook-based): NEW - CS-210 core, notebook data analysis hasn't appeared before. Real new content.

So the genuinely NEW content concentrates in: CS-209 (formal UX/requirements) and CS-210 (notebook data analysis + AI verification + the data-ethics framing) and part of CS-208 (OTP/fault-tolerance comparison). The 3 courses DO carry real new content, not just reframes. 

Verdict: B8 is NOT overloaded by course count (3, normal), BUT CS-210 is carrying a LOT (notebook data analysis AS A NEW SKILL + AI verification AS A NEW SKILL + data ethics). CS-210 is the overloaded UNIT, not the block. 
This is a real problem: "Data Analysis & AI-Assisted Development" crams two substantial new things (data analysis workflow; AI output verification) into one 1-credit course, plus ethics. 
Options:
1. Split CS-210 into two 1-credit courses (Data Analysis; AI Verification) -> B8 becomes 4 courses. Possible but makes B8 the densest block (bad for a capstone-bridge that should leave room for the integration project).
2. Move notebook data analysis EARLIER - it could pair with STAT-101 (B5, descriptive stats) since data analysis IS applied descriptive stats. Then CS-210 in B8 is just AI verification + ethics, lighter. This ALSO strengthens B5 (stats + analysis together) and de-loads B8. LEAN: move notebook data analysis to B5 area (pair w/ STAT-101), leave B8's CS-210 as focused AI-verification/responsible-AI capstone-prep.
   - But wait - B5 is already 2 CS + 2 external. Adding data analysis there... maybe data analysis IS the natural CS companion to STAT-101 and could even BE a CS course in B5 replacing nothing (B5 has only 2 CS, room for a 3rd). B5 = SQL, DB Design, + Data Analysis (notebook, applied stats) = 3 CS + 2 external = 5. Too much for B5.
   - Alternative: data analysis pairs into B7 (Integration & Judgment - analyzing integrated data IS data investigation/analysis, fits the Data Investigation assessment that started B5 and the integration theme of B7). Hmm. Or stays B8 but CS-210 sheds AI-verification to... no, AI-verification is core to B8's capstone-prep.
3. Accept CS-210 is dense but note it for the week-by-week check; possibly the data analysis is LIGHT (using stats they have, in a notebook) rather than a full new skill, if STAT-101 + the embedded data-viz throughline already built the foundation. Under this view, CS-210's "data analysis" is the CULMINATION of the data-viz + stats threads (not new), and the genuinely new part is just AI-verification + ethics, which is manageable. This may be the cleanest read: CS-210 = capstone of the data/viz/stats threads (reframe) + AI verification (new) + ethics framing. Less overloaded than it first looks BECAUSE the data analysis rests on STAT-101 (B5) + data-viz throughline (B2/4/5/7).

LEAN: Option 3 with explicit framing - CS-210's data-analysis component is the CULMINATION of prior stats+viz threads, not new content; the new content is AI-verification + data-ethics. Reframe the course description to make clear data analysis here is integrative (pulling together STAT-101 + viz throughline) rather than from-scratch. This keeps B8 at 3 courses and is honest about load. FLAG for week-by-week check anyway.

### Block 8 shape (frame: In Production / Delivery, Operation & Accountability)
- CS-208 Deployment & Operations — deploy, monitor; performance analysis as REAL-bottleneck (Algorithmic final pass); production fault-tolerance with comparative models try/catch vs OTP supervision vs circuit-breaker (Error Handling flagship final pass - the distinctive content); concurrency-at-scale (Computational Models final pass); containers (the deferred-from-B4 deployment structure); harden-before-live (Security final pass); operational runbooks (Documentation final register); API versioning = compatibility contract (Boundaries final pass, closes B1 semver loop)
- CS-209 Accessible & Human-Centered Design — formal requirements gathering + UX (HCI final pass: checklist-compliance B2 -> requirements-driven design); light design-under-ambiguity (requirements are messy)
- CS-210 Data Analysis & Responsible AI — notebook-based analysis as CULMINATION of STAT-101 + data-viz throughline (integrative, not new); honest visualization/data ethics; high-stakes verification of AI-generated code (AI bounded-practice final pass, prep for Year 3-4 Agentic AI specialization)
- System Integration Project — capstone bridge; blameless postmortem (Sociotechnical final pass, converges with Error-Handling "errors normative")
3 CS courses. Frame-coherent. CS-210 load flagged for week-by-week.

### Year 2 + full arc COMPLETE. All 8 blocks now framed.

## ROUND 21: External (math/stats) pacing — one course per block

Concern: math/stats pacing doesn't work. Consider ONE external course per block.

### Current state (the problem made visible)
- 4 discrete math placed: B1, B3, B5, B7 (odd blocks only)
- STAT-101 placed: B5 (so B5 has TWO externals; B2/B4/B6/B8 have ZERO)
- Agreed-in-principle but UNPLACED: STAT-102, 103, 104 (3 more stats) + linear algebra (MATH-105) = 4 more external courses
- So committed external total = 4 math + 4 stat + 1 lin-alg = 9 external courses (was 4)

### The pacing problem
9 external courses across 8 blocks. Currently they're bunched into odd blocks (and B5 doubled). Even blocks carry zero. That's lumpy: a student in B5 takes 2 CS + 2 external = 4; a student in B2 takes 3 CS + 0 external = 3. And we haven't even placed the 4 unplaced ones.

If we want a smooth "one external per block" rhythm:
- 8 blocks x 1 external = 8 slots. But we have 9 external courses committed (4 math + 4 stat + 1 lin alg). 9 > 8. So one-per-block ALMOST works but is over by one.

### Options to make one-per-block work
Option A: 8 externals, one per block. Requires dropping/merging one of the 9. Candidates:
  - Linear algebra is the awkward one (not discrete, flagged as needing different treatment). Could be deferred to specialization, leaving 8 (4 math + 4 stat) = exactly one per block. BUT user earlier wanted lin alg IN (ML readiness). Tension.
  - OR merge two stats (e.g. distributions+sampling into one) to get stats down to 3, total 4+3+1=8.
  - OR one of the discrete courses merges (unlikely - they're Kansas-transfer aligned, probably fixed).

Option B: Keep 9, accept that one block has 2 externals (back to lumpy) - rejected, that's the current problem.

Option C: Re-examine whether all 9 belong in the 2-year FOUNDATION vs some sliding to year 3. E.g. STAT-104 regression or lin alg could be early-specialization rather than foundation. If 1 slides out, 8 remain = one per block.

### What ONE-PER-BLOCK would look like (sequencing by pairing logic)
Need to honor pedagogical pairings established earlier:
- MATH-101 Logic & Sets -> B1 (pairs w/ Boolean/representation) [FIXED, good]
- MATH-102 Counting -> B3 (pairs w/ complexity/ADTs; counting underlies complexity) [was B3, complexity moved to B4 - so counting could move to B4 to stay w/ complexity, OR stay B3]
- MATH-103 Recursive & Modular -> needs to be ~B5 for crypto handoff to B6 security; recursion needed informally B3/B4
- MATH-104 Graphs -> B7 (pairs w/ graph algorithms) [FIXED, good]
- STAT-101 Descriptive -> pairs w/ data (B4/B5)
- STAT-102 Probability -> pairs w/ counting (after MATH-102)
- STAT-103 Distributions/Sampling -> after probability
- STAT-104 Regression -> late (ML bridge), ~B8
- MATH-105 Linear Algebra -> ML bridge, flexible

A clean one-per-block sequence (8 externals, lin-alg deferred OR stats merged):
  B1: MATH-101 Logic & Sets
  B2: STAT-101 Descriptive Statistics (NEW position - B2 "modify data" + data transformation is a fine home for descriptive stats; describing data you're transforming)
  B3: MATH-102 Counting
  B4: STAT-102 Probability (counting just happened in B3; probability follows counting; B4 structure/cost has prob-adjacent reasoning)
  B5: MATH-103 Recursive & Modular (crypto -> B6)
  B6: STAT-103 Distributions & Sampling (or lin-alg) 
  B7: MATH-104 Graphs
  B8: STAT-104 Regression (ML on-ramp, capstone-adjacent) OR lin-alg
This gives EXACTLY one external per block, alternating MATH/STAT, with pairings mostly honored:
  - Logic@B1 ✓, Counting@B3 ✓, Recursive/Modular@B5 ✓ (crypto->B6), Graphs@B7 ✓ — discrete stays in odd blocks, pairings intact
  - Stats fills even blocks: Descriptive@B2, Probability@B4, Distributions@B6, Regression@B8 — a clean stats progression in even blocks
  - This is ELEGANT: discrete math = odd blocks, statistics = even blocks, one per block, both sequences internally ordered.

But where's linear algebra? This 8-slot scheme has NO room for it. Options:
  - Lin alg deferred to specialization (cleanest for pacing, but reduces foundation ML-readiness)
  - Lin alg replaces one stat in foundation (e.g. drop STAT-103 distributions to specialization, put lin-alg@B6) - judgment call about which ML-prereq matters more in foundation
  - Lin alg as a 9th, doubling up one block (breaks one-per-block) 
  - Lin alg folded across existing math (e.g. vectors/matrices touched in MATH-104 graphs via adjacency matrices + elsewhere) rather than its own course - reduces to 8

### Recommendation to surface
The clean design is: discrete math in odd blocks (B1,3,5,7), statistics in even blocks (B2,4,6,8), one external per block, 8 total. Linear algebra is the odd-one-out that doesn't fit 8 slots - needs an explicit decision (defer to specialization / displace a stat / fold into existing courses / accept a 9th that doubles a block).

This also FIXES the lumpiness AND gives every block exactly 1 external = predictable, even load. And it means every block is either (3 CS + 1 ext) or (2 CS + 1 ext) - very regular. Need to check CS-count per block supports adding an external to the currently-zero-external blocks (B2,4,6,8 currently have 3 CS each -> would become 3 CS + 1 ext = 4-course blocks).

Load consequence: EVERY block becomes 4 courses (3 CS + 1 ext), except B5/B7 where CS=2 (-> 3 courses) ... let me check actual CS counts:
  B1:3CS B2:3CS B3:3CS B4:3CS B5:2CS B6:3CS B7:2CS B8:3CS
  + 1 ext each = B1:4 B2:4 B3:4 B4:4 B5:3 B6:4 B7:3 B8:4
  So most blocks = 4 courses, two = 3. Fairly even. 4 one-credit courses/block = 4 credits/8 weeks. Reasonable full-time-ish pace.

## ROUND 22: Alternative — 4 math in B1-B4, 4 stats in B5-B8

Proposal: MATH in first four blocks (B1-B4), STAT in last four (B5-B8). Clean Year1=discrete, Year2=stats split.

### Mapping
  B1: MATH-101 Logic & Sets
  B2: MATH-102 Counting
  B3: MATH-103 Recursive & Modular
  B4: MATH-104 Graphs, Trees, Networks
  B5: STAT-101 Descriptive
  B6: STAT-102 Probability
  B7: STAT-103 Distributions & Sampling
  B8: STAT-104 Regression

### Check against established pedagogical pairings
- MATH-101 Logic & Sets @ B1: pairs w/ Boolean/representation (CS-103). STILL GOOD. ✓
- MATH-102 Counting @ B2: previously paired w/ complexity (counting underlies Big-O). Complexity is now in B4. So counting (B2) now PRECEDES complexity (B4) by two blocks instead of pairing. Counting-before-complexity still works (you want counting first), just not adjacent. Acceptable, mild loosening. ~OK
- MATH-103 Recursive & Modular @ B3: 
    * Recursion: CS uses recursion informally in B3/B4 (ADTs, trees). Having recursion formalized AT B3 is BETTER than the old B5 placement - now formal recursion arrives JUST as ADTs/trees need it, instead of trailing by 2 blocks. IMPROVEMENT. ✓✓
    * Modular arithmetic: was placed B5 to hand off to B6 crypto (security). At B3, modular arithmetic now PRECEDES B6 crypto by 3 blocks. Gap widens. The crypto handoff was a nice adjacency; now it's distant. This is the COST. Security crypto in B6 would have to re-activate modular arithmetic taught back in B3. Minor but real.
- MATH-104 Graphs @ B4: previously B7 (paired w/ graph algorithms CS-206). Now graphs-math @ B4 but graph-algorithms-CS @ B7 = separated by 3 blocks. This BREAKS a clean pairing. Graph theory (math) taught B4, graph algorithms (CS) taught B7 - big gap. The math would be cold by the time CS graph algorithms arrive. This is the biggest COST of the front-load.

### Net assessment of front-loading math
GAINS:
  + Year 1 = all discrete math done; Year 2 = all stats. Clean mental model, easy to explain, easy to schedule.
  + Recursion formalized at B3 (improvement - arrives when ADTs/trees need it)
  + Stats runs as an uninterrupted 4-course sequence in Year 2 (good for stats pedagogy - descriptive->probability->distributions->regression flows without gaps)
  + Stats in Year 2 sits closer to where data-heavy CS work is (B5 databases, B7 integration, B8 data analysis) - stats pairs with DATA, which is mostly Year 2. STRONG: descriptive stats (B5) right when databases give real data; regression (B8) right at the data-analysis course. Stats-data adjacency is BETTER than the alternating scheme.
COSTS:
  - Graph theory (MATH-104 @ B4) decoupled from graph algorithms (CS-206 @ B7) by 3 blocks. Biggest loss.
  - Modular arithmetic (B3) decoupled from crypto (B6) by 3 blocks.
  - Counting (B2) decoupled from complexity (B4) by 2 blocks (minor).

### The graph problem is the crux
Front-loading math is clearly BETTER for stats (stats wants to be in Year 2 near data) but WORSE for graphs (graph math wants to be near graph algorithms in B7).
Tension: graph math naturally wants B7, but front-loading puts it at B4.

Possible fix: DON'T strictly front-load all 4 math. Keep 3 math in Year 1 (Logic@B1, Counting@B2 or B3, Recursive/Modular@B3) and let GRAPHS (MATH-104) stay at B7 where it pairs with CS graph algorithms. Then Year 1 has 3 math + ? , Year 2 has graphs-math (B7) + stats.
But that breaks the clean "Year1=math, Year2=stats" symmetry and leaves a hole in Year 1 (only 3 externals) and crowds Year 2 (4 stats + 1 graph-math = 5 externals across 4 blocks = one block doubles).

Alternatively accept the graph decoupling: maybe graph THEORY at B4 (math: what graphs ARE, properties, representations) and graph ALGORITHMS at B7 (CS: traversal, shortest path) is actually a fine SPIRAL - math introduces the structure, CS applies it 3 blocks later with the math as foundation. The "gap" could be reframed as "math foundation early, CS application later" which is the same informal-before-formal / foundation-before-application pattern used elsewhere. Under that reframe the decoupling isn't a bug, it's the same spiral logic. Hmm - but graph theory taught with NO nearby application may not stick. Risk.

### Comparison: alternating (round 21) vs front-load (round 22)
Alternating (MATH odd / STAT even):
  + every pairing adjacent (counting near complexity-ish, graphs@B7 w/ CS graphs, modular@B5 near crypto@B6)
  + smooth one-per-block
  - stats scattered, descriptive stats earlier (B2) before much data exists - weaker stats-data adjacency
  - probability@B4 ok, but stats sequence interrupted by being spread across whole 2 years
Front-load (MATH B1-4 / STAT B5-8):
  + clean Year1/Year2 split, recursion improves, STATS-DATA adjacency strong, stats sequence uninterrupted
  - graph math decoupled from graph algorithms (biggest cost), modular from crypto

### Lin algebra in each scheme
Still the 9th. Both schemes are 8 slots. Same options as round 21 (defer/displace/fold).
In front-load scheme, lin-alg most naturally appends to the stats/Year-2 side (it's an ML prereq w/ stats) - could be a 5th Year-2 external (doubling a Year-2 block) or replace a stat.

### What to ask the user
The choice is essentially: optimize externals for STATS-data adjacency (front-load math, stats in Y2) or for math-CS pairing adjacency (alternating). Front-load is cleaner organizationally and better for stats; its main cost is graph-math/graph-CS separation. Worth asking whether they'll accept the graph decoupling (or reframe it as foundation-early/application-later), since that's the hinge.

## ROUND 23: Graphs become their own spiral (resolves the front-load graph problem)

User: spiral graphs. First experience B3 (graphs as a MODEL for certain data), building/representing B4, Neo4j B5 (graphs as another persistent store), ... -> deepening through to B7 graph algorithms + MATH-104.

This dissolves the round-22 graph-decoupling problem: there's no "graph theory cold at B4, applied cold at B7" gap because graphs now recur continuously B3->B7 with deepening purpose. The MATH-104 graph course at B7 is no longer the FIRST encounter (cold) - it's the formalization of something students have used for 4 blocks. Classic spiral (practice before formalize), consistent with everything else.

### Graph spiral passes
- B3 MODEL: graphs as a way to model certain data/relationships. First encounter - conceptual. "Some data is naturally a network: people and friendships, pages and links, tasks and dependencies." Fits B3 "model & abstract" frame perfectly - a graph is a MODEL of relationship structure. Light, no algorithms yet.
- B4 REPRESENT/BUILD: representing graphs (adjacency list/matrix), building them, basic traversal. Fits B4 "structure across scales" - graphs ARE arbitrary structure; and adjacency MATRIX is a nice touch-point that connects to the linear-algebra question (matrices appear here naturally). Fits B4 perfectly.
- B5 PERSIST: Neo4j / graph databases as another persistent store. Fits B5 "information at rest" - graphs as a STORED, queryable structure alongside relational (SQL) and document (NoSQL is B7). Actually this enriches B5: B5 now shows TWO+ storage models (relational + graph), foreshadowing B7 document. Nice. Graph queries (Cypher) as another query language alongside SQL.
- B6 ?: does graphs touch B6 (responsible dev)? Possibly light - graph of dependencies for security (attack graphs / dependency analysis) or social graph privacy. Optional, probably skip to avoid overloading B6.
- B7 ALGORITHMS + THEORY: CS-206 graph algorithms (traversal, shortest path, MST) + MATH-104 graph theory, NOW formalizing 4 blocks of informal graph use. This is the deep pass. By now students have modeled with graphs (B3), built/represented them (B4), persisted/queried them (B5) - so the algorithms and formal theory land on rich prior experience. MUCH better than cold.

### Consequences for placements
1. MATH-104 (graph theory) STAYS at B7 (formalizes the spiral) - so the front-load is NOT a strict "all 4 math in B1-B4." It's "3 math in B1-B3, graph-math stays B7." 
   - Wait - reconcile with round 22 front-load. The user's graph-spiral implies MATH-104 stays B7, NOT moved to B4. So the math placement becomes:
     B1: MATH-101 Logic & Sets
     B2: MATH-102 Counting
     B3: MATH-103 Recursive & Modular
     B7: MATH-104 Graphs, Trees, Networks (stays - formalizes the graph spiral)
   - That's 3 math in B1-B3, 1 math in B7. Year 1 has math in B1,B2,B3 (not B4). B4 has no math.
2. Stats then fills: B4, B5, B6, B8? Let's see. Externals one-per-block, 8 slots:
     B1: MATH-101
     B2: MATH-102
     B3: MATH-103
     B4: STAT-101 Descriptive (B4 has graph-build CS work + now descriptive stats - describing data, fine)
     B5: STAT-102 Probability? OR keep stats near data... 
     B6: STAT-103
     B7: MATH-104 Graphs
     B8: STAT-104 Regression
   - That leaves B5 with no external? No: B5 needs one. Let me recount. 8 blocks, externals: MATH-101,102,103,104 (4) + STAT-101,102,103,104 (4) = 8. One per block:
     B1: MATH-101
     B2: MATH-102
     B3: MATH-103
     B4: STAT-101
     B5: STAT-102
     B6: STAT-103
     B7: MATH-104
     B8: STAT-104
   - Check: B7 = MATH-104 (graphs, formalizing spiral) ✓. Stats run B4,B5,B6,B8 - mostly contiguous (gap at B7 where graph-math sits). Stats-data adjacency: STAT-101 descriptive @ B4 (data from B4 structure work), STAT-102 probability @ B5, STAT-103 @ B6, STAT-104 regression @ B8 (data analysis). Decent.
   - This is a HYBRID of front-load and alternating: math B1-B3 + B7, stats B4-B6 + B8. Honors graph-spiral (MATH-104@B7), honors recursion-early (MATH-103@B3), honors stats-in-Y2-ish (mostly B4-B8), one per block. 
   - Modular arithmetic (B3) -> crypto (B6): 3-block gap remains. Minor, accept.
3. Counting (B2) -> complexity (B4): counting B2, complexity B4, 2-block gap, counting-before-complexity preserved. OK.

### This hybrid looks best
  B1 MATH-101 Logic & Sets
  B2 MATH-102 Counting
  B3 MATH-103 Recursive & Modular
  B4 STAT-101 Descriptive
  B5 STAT-102 Probability
  B6 STAT-103 Distributions & Sampling
  B7 MATH-104 Graphs (formalizes the graph spiral B3->B7)
  B8 STAT-104 Regression
One external per block ✓. Graph spiral honored (MATH-104@B7 caps it) ✓. Recursion early (B3) ✓. Stats mostly Year 2, near data ✓. Lin-alg still the 9th (defer/fold/displace - unchanged question, and note adjacency matrices now appear in B4 graph-representation, a natural fold-in point for SOME linear algebra).

### Graphs spiral is a NEW thread to add to taxonomy
Graphs were PART of "Data Structures & Representation" thread (terminal pass). Now graphs get their own explicit sub-spiral B3-B7. Could either (a) be a distinct thread, or (b) be an explicit multi-pass strand WITHIN Data Structures & Representation. Given Data Structures already spirals primitive->...->graph->document, breaking graphs into their own thread overlaps. BETTER: enrich the Data Structures thread to show graphs as a spiral-within-the-spiral (B3 model, B4 represent, B5 persist via Neo4j, B7 algorithms+theory) rather than a single terminal "graph" pass. This keeps thread count at 14 (doesn't add a 15th) and just deepens an existing thread's graph treatment. LEAN: enrich Data Structures thread, don't add a new thread.
   - Note: adding Neo4j/graph-db at B5 is genuinely new content (wasn't there before) - B5 gains a graph-database touch alongside relational. Small addition to B5 (probably embedded in/adjacent to the existing DB work, not a new course).

### Lin algebra note
Adjacency matrices now explicitly appear at B4 (graph representation). That's a natural seed for basic linear algebra (matrices, matrix-vector products as graph operations). Strengthens the "fold lin-alg into existing courses" option: some lin-alg could live at B4 (matrices via graphs) + elsewhere, rather than a standalone course. Doesn't fully solve lin-alg (ML needs more than adjacency matrices) but is a real partial home.

## ROUND 24: Revisit thread taxonomy; create "Professional Practices" thread

User: move Documentation + Git into a "Professional Practices" thread, along with continued education, reflection (team+self), code style, other related ideas. Offer critique + counterproposals.

### Critique of the current 14-thread taxonomy (accreted, not designed)
Current: 10 spirals (incl Sociotechnical) + 3 lenses (Security, Documentation, Optimization) + 1 bounded (AI).
Problems I see:
1. INCONSISTENT GRANULARITY. Some threads are big ideas (Boundaries & Contracts, Computational Models) and some are single practices (Git, Documentation). Git as a top-level peer of "Computational Models & Error Handling" is a category error - one's a tool-practice, the other's a deep conceptual spiral. User's instinct to bundle the practice-level ones is CORRECT.
2. DOCUMENTATION is currently a LENS, GIT is a SPIRAL. They're actually the same KIND of thing (professional practices that recur and mature). Splitting them across two categories was inconsistent. Bundling fixes this.
3. SOCIOTECHNICAL (Conway/teams/reflection) overlaps heavily with what the user now wants in "Professional Practices" (reflection team+self). Need to decide: does Professional Practices SUBSUME Sociotechnical, or sit beside it? They're cousins.
4. "Continued education / lifelong learning" and "code style" aren't currently threads at all - they're new additions. Both are genuinely professional-practice material and have no other home. Good additions.

### What belongs in "Professional Practices"
User's list: Documentation, Git/version control, continued education (lifelong learning), reflection (team + self), code style, "other related."
Other related candidates that currently have weak/no homes:
  - Code style / readability / linting conventions (NEW - genuinely missing, fits)
  - Estimation / scoping (flagged as a gap way back in round, never homed - fits here)
  - Giving/receiving code review feedback (currently scattered in Git collaborative + B6 - the INTERPERSONAL skill of review, distinct from the git mechanics)
  - Professional communication (writing clearly for an audience - overlaps documentation)
  - Time/work management, working with ambiguity (professional maturity)
  - Ethics of practice (overlaps Security/Privacy/Ethics lens - careful not to double-home)

### The tension to surface: Professional Practices vs Sociotechnical vs Reflection
"Reflection (team and self)" the user wants in Professional Practices. But:
  - Sociotechnical thread (Conway's Law) already culminates in B8 blameless postmortem = team reflection.
  - The B6 "responsibility retrospective" = team+self reflection.
  - Reflection is ALSO one of the 8 recurring developmental experiences (Read/Repair/.../Reflect) from the original program design.
So "reflection" lives in at least 3 places. Consolidating it into Professional Practices is reasonable, but we must decide what happens to Sociotechnical. Options:
  (a) Professional Practices and Sociotechnical are SEPARATE: Professional Practices = individual professional habits (docs, git, style, self-reflection, continued ed); Sociotechnical = the structural idea that systems mirror orgs (Conway, team structure). Reflection-as-SELF goes to Prof Practices; reflection-as-TEAM (postmortem) stays in Sociotechnical. Clean-ish but splits reflection.
  (b) MERGE Sociotechnical INTO Professional Practices as the "teamwork/collaboration" facet. Professional Practices becomes the big "how to be a professional" thread covering individual habits AND team habits AND Conway. Simpler taxonomy (one fewer thread) but Professional Practices becomes large/sprawling.
  (c) Professional Practices = individual; a separate "Teamwork & Collaboration" thread (renamed Sociotechnical) = collective. Two clean threads split by individual vs collective.

I lean (a) or (c) - keep individual-professional and team/collective conceptually distinct, because they're assessed differently (self-reflection vs team retrospective) and Conway's Law is a genuinely different (structural/systems) idea than "keep good code style." Merging everything into one mega-thread (b) loses the systems-thinking edge of Conway.

Actually - cleanest: 
  - "Professional Practices" (individual craft + habits): documentation, version control, code style/readability, self-reflection, continued learning, estimation. The habits of an individual professional.
  - Keep "Sociotechnical Structure" but maybe RENAME to "Collaboration & Sociotechnical Structure" to house: teamwork, code review as interpersonal practice, team reflection/postmortem, Conway's Law. The collective/social dimension.
This splits the user's "reflection (team and self)": SELF-reflection -> Professional Practices; TEAM-reflection -> Collaboration thread. That's defensible (they ARE different practices) but I should flag it since the user grouped them together.

### Counterproposal on thread COUNT / structure
With this move:
  - REMOVE: Git (spiral) and Documentation (lens) as standalone threads
  - ADD: Professional Practices (spiral) absorbing them + code style + continued ed + self-reflection + estimation
  - Sociotechnical stays (possibly renamed to foreground collaboration)
New taxonomy:
  Spirals: Data Structures, Program Correctness, APIs, HCI, Algorithmic, Computational Models, Testing/Verification, Boundaries & Contracts, Professional Practices, Collaboration & Sociotechnical = 10 spirals
  Lenses: Security/Privacy/Ethics, Optimization = 2 lenses (Documentation removed from lenses -> folded into Prof Practices)
  Bounded: AI = 1
  Total = 13 threads (down from 14). 
Net: cleaner (practice-level items consolidated), one fewer thread, granularity more consistent.

BUT does Professional Practices as a "spiral" work? It's really a BUNDLE of parallel practices each with their own mini-progression, not a single escalating concept. It's more like a "lens" (standing practice applied throughout) than a "spiral" (single concept deepening). Hmm. Maybe Professional Practices is best understood as its own THIRD category alongside the bounded practice, or as a lens. Actually it fits the LENS definition well: a standing set of practices applied wherever relevant, scope growing with capability. Documentation was already a lens; Git was mis-categorized as a spiral. So:
  Professional Practices = a LENS (or a "practice bundle"), not a spiral.
Revised taxonomy:
  Spirals (8): Data Structures, Program Correctness, APIs, HCI, Algorithmic, Computational Models, Testing/Verification, Boundaries & Contracts
  + Sociotechnical/Collaboration: spiral OR fold into Prof Practices? If Prof Practices is a lens and includes teamwork, Sociotechnical/Conway could be the systems-thinking part that stays a spiral, while teamwork-as-practice goes to the Prof Practices lens. OR Sociotechnical folds in.
  Lenses (3): Security/Privacy/Ethics, Optimization, Professional Practices
  Bounded (1): AI
This is getting complicated - need user input on the key forks rather than deciding alone.

### Key forks for user
1. Is "Professional Practices" a SPIRAL (single deepening arc) or a LENS/bundle (many parallel practices applied throughout)? I lean LENS/bundle - it's not one concept.
2. Does Professional Practices ABSORB the team/collaboration/Conway material (Sociotechnical), or does that stay a separate thread? I lean SEPARATE (individual craft vs collective/systems), but it splits "reflection" into self (Prof Practices) and team (Collaboration).
3. Confirm new additions: code style, continued education, estimation, self-reflection all join Prof Practices.

## ROUND 25: Professional Practices lens locked; new taxonomy

DECISIONS:
1. Professional Practices = a LENS (bundle of parallel practices applied throughout).
2. Kept SEPARATE from Sociotechnical/Conway. Professional Practices = INDIVIDUAL craft; Sociotechnical = COLLECTIVE + structural. Reflection splits: SELF-reflection -> Professional Practices; TEAM-reflection (postmortem/retro) -> Sociotechnical.
3. Contents: Documentation, Git/version control, code style/readability, continued education (lifelong learning), self-reflection, estimation/scoping, interpersonal code-review skill, professional communication.

### NEW TAXONOMY (13 threads, down from 14; granularity consistent)
SPIRALS (9) - single concept deepening:
1. Data Structures & Representation (now includes the graph sub-spiral B3->B7)
2. Program Correctness / Code Comprehension
3. APIs & Networked Systems
4. HCI / Accessible & Human-Centered Design (accessibility + data viz throughlines)
5. Algorithmic Thinking & Complexity
6. Computational Models & Error Handling (flagship)
7. Testing & Formal Verification
8. Boundaries & Contracts (meta-thread)
9. Sociotechnical Structure (Conway's Law; collective/team: teamwork, code review as collective practice, team reflection/postmortem)

LENSES (3) - standing practice/question applied throughout, scope grows with capability:
1. Security, Privacy & Ethical Reasoning
2. Optimization Reasoning
3. Professional Practices (NEW) - individual craft bundle

BOUNDED PRACTICE (1):
1. AI-Assisted Development

Total: 9 + 3 + 1 = 13 threads. (Was 14: removed Git-spiral and Documentation-lens as standalone = -2; added Professional Practices lens = +1; net -1.)

### Note on Git/Documentation: thread vs constituent
Git and Documentation no longer standalone threads, but their PER-BLOCK progressions still exist as constituents of Professional Practices. The detailed git progression (B1 read history -> B2 commit/revert -> B5 solo branch -> B6 collaborative) and doc progression (B1 inline+doc -> ... -> B8 runbooks) are now sub-strands within the Professional Practices lens. The collaborative-git and team-facing-doc passes (B6) sit at the boundary with Sociotechnical (collaborative git is BOTH a git-practice and a team practice) - note the overlap, attribute git-mechanics to Prof Practices and team-coordination to Sociotechnical.

### Professional Practices lens - constituent sub-strands and their arcs
- DOCUMENTATION: B1 (inline + explanatory doc) -> B2 (docstrings/API, bug-fix docs) -> B3 (justification: why this design) -> B5 (schema decisions) -> B6 (team-facing: PRs, review comments) -> B8 (operational runbooks). [register escalates: self->reviewer->teammate->operator]
- VERSION CONTROL (Git): B1 (read history: log/diff/blame, semver) -> B2 (commit/revert safety net) -> B5 (solo branching) -> B6 (collaborative: PRs, conflicts). [mechanics; B6 collaborative overlaps Sociotechnical]
- CODE STYLE / READABILITY: NEW. Where? B1-B2 (writing readable code as you first write/modify) -> B3 (style as part of good modeling/naming) -> B6 (style consistency matters for a TEAM; linting conventions; style as a shared contract) -> ongoing. Seed early (readable code from the start), formalize team-style at B6.
- CODE REVIEW (interpersonal skill): primarily B6 (giving/receiving feedback constructively) but the READING-others'-code groundwork is B2 (Code Archaeology). So: B2 (read others' code - precondition for reviewing it) -> B6 (review as interpersonal practice: how to give/receive feedback). Distinct from git-mechanics-of-PRs and from Sociotechnical's team-coordination.
- PROFESSIONAL COMMUNICATION: overlaps documentation but broader (explaining to non-technical audiences, Design Review presentation B7, writing clear issue reports). Touches: B1 (explain code in writing) -> B6 (communicate within a team) -> B7 (Design Review: present/defend to an audience) -> B8 (operational comms).
- SELF-REFLECTION: B6 (responsibility retrospective - self portion) -> B8 (personal reflection on the integration project / what I learned). Lighter than team reflection (which is Sociotechnical). Could also have a light touch each block (a brief "what did I learn / what would I do differently" habit) - that's the "applied throughout" lens character.
- ESTIMATION / SCOPING: NEW, was a long-standing gap. Primarily emerges with the Team Software Project (B6) and Integration Project (B8) - "how long will this take, how do we scope the work." Light; foundation-level awareness, not rigorous estimation (that's professional experience). B6 seed -> B8 practice.
- CONTINUED EDUCATION / LIFELONG LEARNING: the most diffuse. Less a per-block skill, more a STANCE cultivated throughout - "the field changes, you'll always be learning, here's how to learn a new tool/language/framework independently." Could be explicitly named where students must pick up something not formally taught (e.g. a new library in a project). Touch: anywhere students self-teach; named explicitly maybe at B8 (preparing to leave the foundation / enter specialization - "you now know how to learn the next thing"). 

### Consequence for files
- Documentation lens file (lens-documentation.md): SUPERSEDED - becomes part of Professional Practices.
- Git thread file (thread-git.md): SUPERSEDED - becomes part of Professional Practices.
- NEW: Professional Practices lens file needed.
- Sociotechnical thread file: needs slight update (it now explicitly OWNS team-reflection, code-review-as-team-coordination; gives up nothing it had - it didn't have docs/git).
- Data Structures thread file: needs the graph sub-spiral added (from round 23, still pending).
- Overview + block files: thread taxonomy references update (14->13; Git/Doc no longer standalone; Prof Practices added).
- Block "threadTouches" in supplement.js: relabel Git/Documentation touches as "Professional Practices (Git)" / "Professional Practices (Documentation)" etc.

This is a fair amount of regeneration. The content.js (course/block structure) does NOT change from this - threads are a separate layer (supplement.js + the thread/lens files + overview prose). So this is a "thread-layer" refactor, not a course-structure change. Good - course grid is stable.

## ROUND 26: "Humanistic Computing" thread/lens proposal

Proposal: a thread or lens capturing accessibility, requirements gathering, UX design, A/B + acceptance testing.

### What it would pull from where
- Accessibility: currently in HCI spiral (the accessibility throughline)
- Requirements gathering: currently HCI spiral terminal pass (B8 CS-209)
- UX design: currently HCI spiral (B8 formal UX)
- A/B testing: NOT currently anywhere - NEW. (Experimentation/validation WITH USERS.)
- Acceptance testing: currently implied in Testing/Verification thread (validating against requirements) - but acceptance testing is specifically "does it meet the USER'S needs/criteria" vs unit/integration testing which is "does the code work." So acceptance testing arguably belongs MORE with the human/requirements side than the technical-testing side.

### Critique: is this a new thread, or a renaming/reframing of HCI?
Key observation: "Humanistic Computing" as proposed is ~80% the existing HCI spiral (accessibility, UX, requirements) PLUS two testing-adjacent items (A/B, acceptance) that are about validating-with-humans. So this isn't really a NEW thread competing with HCI - it's a RENAMING and BROADENING of the HCI thread to its proper scope.

The current "HCI / Accessible & Human-Centered Design" thread is arguably MIS-SCOPED / under-named:
- It carries accessibility + data-viz, but "data viz" is really about human COMPREHENSION (a human-centered concern) 
- It culminates in requirements/UX
- The unifying idea is: COMPUTING IN SERVICE OF HUMAN NEEDS - designing for, validating with, and communicating to humans.
"Humanistic Computing" is a BETTER NAME for this whole thread than "HCI / Accessible Design" because it captures the full scope: it's not just interface accessibility, it's the whole stance of building for human needs and verifying you've met them.

### The boundary question: testing
Two pulls proposed, different cleanliness:
- A/B testing + acceptance testing INTO Humanistic Computing: 
  - A/B testing = experimenting to learn what humans actually prefer/need. Clearly human-centered. Clean pull (it's new anyway).
  - Acceptance testing = validating against user-defined acceptance criteria. This is the SEAM. It's "testing" (Testing/Verification thread) but it's testing AGAINST HUMAN REQUIREMENTS (Humanistic). 
  Resolution: there are two distinct testing questions - "does the code do what I intended" (unit/integration/verification = Testing thread) vs "does the system meet the user's actual needs" (acceptance/UAT + A/B = Humanistic thread). This is a REAL and PEDAGOGICALLY USEFUL distinction (correctness vs fitness-for-purpose). So splitting acceptance testing OUT of the technical-testing thread and INTO Humanistic is defensible and even clarifying. The Testing/Verification thread keeps unit/integration/formal-verification (code-correctness); Humanistic gets acceptance/UAT + A/B (human-fitness).
  This actually IMPROVES the Testing thread by sharpening its scope to "is it correct" and giving "is it what they needed" a proper home.

### Spiral or lens?
Like the old HCI thread, this is a SPIRAL (it has a clear deepening arc): 
  perceive/comprehend (B2 accessibility + visual hierarchy) -> represent data honestly for humans (B4 viz) -> investigate via visualization (B5) -> defend human-facing choices (B7 Design Review) -> formal requirements + UX + validate-with-users (B8: requirements, UX, acceptance testing, A/B). 
It deepens from "make it perceivable" to "design from needs and prove you met them." Spiral, not lens. (It REPLACES the HCI spiral slot - not an addition to thread count.)

### Proposed: rename + rescope HCI -> Humanistic Computing
- RENAME "HCI / Accessible & Human-Centered Design" spiral TO "Humanistic Computing"
- KEEP its existing content (accessibility, data viz, requirements, UX)
- ADD: A/B testing + acceptance testing (validating WITH/FOR humans) at the B8 end (and acceptance-criteria thinking could seed earlier, e.g. B7 Design Review defends against user criteria)
- MOVE acceptance testing OUT of Testing/Verification thread INTO Humanistic; Testing/Verification keeps code-correctness testing + formal verification only.
Net thread count: UNCHANGED (13). It's a rename+rescope of an existing spiral plus a small transfer from the Testing thread. Clean.

### New arc for Humanistic Computing spiral
- B2: accessibility basics + visual hierarchy as human comprehension (perceive)
- B4: honest data visualization (represent for humans)
- B5: visualization as investigation (comprehend data)
- B7: Design Review - defend human-facing choices; introduce ACCEPTANCE CRITERIA (what would make this acceptable to the user?)
- B8: formal requirements gathering + UX + ACCEPTANCE TESTING (validate against user criteria) + A/B TESTING (experiment to learn user preference). The "fitness for human purpose" capstone.

### Things to confirm with user
1. Is this a RENAME/RESCOPE of the existing HCI thread (my read) or a genuinely separate thread sitting alongside HCI? I strongly lean rename/rescope - a separate thread would duplicate accessibility/UX.
2. Confirm moving ACCEPTANCE testing out of Testing/Verification into Humanistic (sharpens both). A/B testing is new, goes to Humanistic regardless.
3. Name: "Humanistic Computing" vs "Human-Centered Computing" vs keep "HCI." User said "humanistic" - confirm that exact framing (humanistic has a slightly broader/philosophical connotation than human-centered, which may be intended given the program's systems+people ethos).

## ROUND 27: Human-Centered Computing locked (rename/rescope of HCI)

DECISIONS:
1. RENAME + RESCOPE the HCI spiral to "Human-Centered Computing" (NOT "Humanistic" - user picked Human-Centered). Stays a spiral; thread count unchanged at 13.
2. Scope = accessibility + data viz (comprehension) + requirements + UX + acceptance testing + A/B testing. Unifying idea: computing in service of human needs - design FOR, communicate TO, validate WITH humans.
3. Acceptance testing MOVES from Testing & Verification -> Human-Centered Computing. A/B testing is NEW, also in Human-Centered Computing.
4. Testing & Verification thread now SHARPENED: code-correctness only (unit, integration, formal verification). It answers "is it correct"; Human-Centered Computing answers "is it what they needed" (fitness for purpose). This correctness-vs-fitness distinction is pedagogically clarifying.

### Human-Centered Computing spiral arc (final)
- B2: accessibility basics + visual hierarchy as human comprehension (PERCEIVE)
- B4: honest data visualization - represent data for humans (REPRESENT)
- B5: visualization as investigation - comprehend data (COMPREHEND)
- B7: Design Review - defend human-facing choices; introduce ACCEPTANCE CRITERIA ("what would make this acceptable to the user?")
- B8: formal requirements gathering + UX + ACCEPTANCE TESTING (validate against user criteria) + A/B TESTING (experiment to learn user preference). FITNESS-FOR-HUMAN-PURPOSE capstone.

### Testing & Verification thread arc (sharpened - correctness only)
- B1: asserts/logs + informal pre/post-condition reasoning
- B2: tests for regression
- B3: recursion correctness; contracts as pre/post-conditions
- B6: testing AND formal verification, named/contrasted (code-correctness)
- B8: both applied to harder cases (deployed systems) - still code-correctness; acceptance/fitness now lives in Human-Centered Computing
NOTE: B8 is where BOTH threads have a pass - Testing/Verification (is the deployed code correct) AND Human-Centered (does it meet user acceptance criteria, A/B). They're adjacent at B8 but answer different questions. Worth an explicit cross-reference: "two kinds of 'does it work' converge at B8 - correctness and fitness."

### New content introduced by this round
- A/B testing (B8) - NEW, didn't exist in any prior thread
- Acceptance testing as an explicit, named practice (B8, seeded B7 via acceptance criteria) - was implicit, now explicit and rehomed
- Both are small additions at the B8 end; CS-209 (Accessible & Human-Centered Design) is the natural host course - its scope broadens slightly to include validate-with-users (acceptance + A/B), not just design. Possibly retitle CS-209 to reflect this (e.g. "Human-Centered Design & Validation"). Course-structure note: this touches content.js (CS-209 desc/title), unlike the round-25 thread refactor which didn't.

### CURRENT TAXONOMY (13 threads) - updated names
SPIRALS (9):
1. Data Structures & Representation (+ graph sub-spiral B3->B7)
2. Program Correctness / Code Comprehension
3. APIs & Networked Systems
4. Human-Centered Computing (RENAMED from HCI; now incl. acceptance + A/B testing)
5. Algorithmic Thinking & Complexity
6. Computational Models & Error Handling (flagship)
7. Testing & Formal Verification (SHARPENED to code-correctness only)
8. Boundaries & Contracts (meta-thread)
9. Sociotechnical Structure (Conway's Law; collective/team)
LENSES (3):
1. Security, Privacy & Ethical Reasoning
2. Optimization Reasoning
3. Professional Practices (individual craft bundle)
BOUNDED (1):
1. AI-Assisted Development

### Pending regeneration (accumulated across rounds 23-27)
Thread-layer (supplement.js, thread/lens files, overview, block files):
- Data Structures file: add graph sub-spiral (round 23)
- Remove Git thread file + Documentation lens file; add Professional Practices lens file (round 25)
- Sociotechnical file: add team-reflection + code-review-as-coordination ownership (round 25)
- Rename/rescope HCI -> Human-Centered Computing file; add acceptance + A/B (round 27)
- Testing/Verification file: sharpen to correctness-only, note acceptance moved out (round 27)
- Overview: taxonomy 14->13, renames, Professional Practices, Human-Centered (round 25, 27)
- Block files threadTouches: relabel per new taxonomy
Course-structure (content.js):
- CS-209 desc/title broaden to include validation (acceptance + A/B) (round 27) - the ONLY content.js change from rounds 24-27

## ROUND 28: Computational Models - surface declarative models; find homes for logic/constraint/actor

User: explicitly surface DECLARATIVE models via HTML + SQL. Is there a home for logic, constraint, actor, other models?

### Reframe: the thread has an implicit imperative bias
Current Computational Models & Error Handling thread passes:
- B1: imperative/sequential vs functional (two models named)
- B2: async/event-loop
- B3: try/catch (control-flow error model)
- B4: network failures
- B5: transactional rollback
- B6: errors as attack surface
- B8: fault tolerance comparison (try/catch vs OTP vs circuit-breaker)
Observation: after B1's imperative-vs-functional, almost everything is about CONTROL FLOW and FAILURE handling. The thread quietly assumes the imperative paradigm and explores how control/failure work within it. Declarative computation (state WHAT you want, not HOW) is underrepresented - yet the curriculum is FULL of declarative models students already use without naming them as such:
  - HTML: declarative UI (describe the structure/content, browser figures out rendering) - B2/CS-106
  - CSS: declarative styling (describe desired appearance, engine computes layout) - B2
  - SQL: declarative querying (describe WHAT data you want, query planner figures out HOW) - B5
  - Regex (if used): declarative pattern matching
  - Build/config files, etc.
These are ALREADY in the curriculum but not NAMED as "a different computational model." Surfacing them is high-value and nearly free - it's naming something students already do.

### The deeper taxonomy of computational models (what's the full space?)
A cleaner organizing idea for the thread: computational models answer "what does a program SAY and how does computation happen?"
1. IMPERATIVE / sequential - steps that change state (B1)
2. FUNCTIONAL - composition of transformations, values not state (B1)
3. DECLARATIVE - state WHAT, not HOW; a system resolves it:
   - markup/structural: HTML (B2)
   - query: SQL (B5)
   - styling/constraint-ish: CSS (B2)
   - logic programming: facts + rules + queries (Prolog-style) - NOT currently anywhere
   - constraint programming: state constraints, solver finds solution - NOT anywhere
4. CONCURRENT / reactive - many things at once, responding to events:
   - async/event-loop (B2)
   - actor model (message-passing, isolated state) - Erlang/OTP is touched at B8 for FAULT TOLERANCE but the ACTOR MODEL itself (as a computational model) isn't named
   - dataflow/reactive
5. (failure handling cuts across all of these - the existing thread strength)

### Homes for logic, constraint, actor
- ACTOR MODEL: already HALF-present. B8 discusses Erlang/OTP supervision for fault tolerance. The actor model (isolated processes communicating by messages) is the SUBSTRATE of that OTP discussion. So actors have a natural home at B8 - just need to NAME the actor model explicitly as a computational model (not only as a fault-tolerance mechanism). Also: async/event-loop (B2) is actor-adjacent (message-driven). Could foreshadow B2, name at B8. LOW cost - it's already lurking there.
- DECLARATIVE (HTML/SQL): name explicitly where they already occur - HTML@B2, SQL@B5. Add a connective "these are declarative - you state what, not how" framing. Near-free.
- LOGIC PROGRAMMING (Prolog-style facts/rules/queries): NOT currently anywhere. Genuinely new. Does it have a natural home? 
  - It connects to: MATH-101 Logic & Sets (B1 - propositional/predicate logic is the foundation of logic programming), SQL (B5 - SQL is logic-programming-adjacent; a query is essentially a logical statement; relational algebra has logic roots), and constraint solving.
  - Possible home: a light touch at B5 (SQL as declarative/logical querying -> "there's a whole paradigm where you program by stating logical facts and rules") or B7 (graphs + logic - querying relationships is logic-flavored; Datalog/Cypher are logic-query-adjacent). 
  - But full logic programming (Prolog) is arguably a SPECIALIZATION topic, not foundation. In the foundation, logic programming might just be NAMED as "another declarative model exists" rather than taught. Flag: is logic programming foundation or specialization?
- CONSTRAINT PROGRAMMING (state constraints, solver finds solutions): connects to optimization (Optimization lens!) and to the B7 "design under uncertainty / tradeoffs." Constraint satisfaction is optimization-adjacent. 
  - Possible home: conceptual mention at B7 (constraints + optimization) or with logic programming. Like logic programming, full constraint programming is likely SPECIALIZATION; foundation just NAMES it exists.

### Proposal: restructure the thread's spine around the SPACE of models
Rename/reframe the thread so the SPINE is the taxonomy of models, with failure-handling woven through (not the dominant axis it accidentally became):
  - B1: imperative & functional (two foundational paradigms) - errors as ordinary
  - B2: declarative (HTML/CSS - state what not how) + concurrent/reactive (async/event-loop) - failure looks different across models
  - B3: (control-flow & exceptions in the imperative model - try/catch)
  - B5: declarative querying (SQL as "state what data, planner finds how") - name it as the SAME declarative idea as HTML, now for data; transactional failure
  - B7: (optional) constraint/logic flavor - querying relationships, constraints + tradeoffs; "models where you state rules/constraints and a solver works it out" - NAMED, lightly
  - B8: concurrent/distributed models at scale - actor model named explicitly (Erlang/OTP as actors, not just fault tolerance); fault-tolerance comparison
This makes the thread genuinely about "the landscape of computational models" with error-handling as a cross-cutting property of each - which is RICHER and fixes the imperative bias. The flagship status is even more justified.

### What's foundation vs specialization (the scoping call)
- NAME and USE (foundation): imperative, functional, declarative-markup (HTML), declarative-query (SQL), concurrent/async, actor (at least named via OTP).
- NAME ONLY / awareness (foundation edge): logic programming, constraint programming - "these paradigms exist, here's the flavor" without teaching Prolog/MiniZinc.
- TEACH DEEPLY (specialization): full logic programming, full constraint solving, advanced actor systems.
This keeps foundation load sane while surfacing the full landscape conceptually. Matches the program's pattern (name/expose broadly, teach deeply where it counts, defer specialization).

### Questions for user
1. Reframe the thread spine around the model TAXONOMY (imperative/functional/declarative/concurrent) with failure woven through, rather than the current control-flow-biased spine? (I recommend yes - fixes a real bias.)
2. Logic & constraint programming: NAME-only in foundation (B7 light touch), or leave entirely to specialization?
3. Actor model: explicitly name at B8 (it's already there implicitly via OTP)? (Recommend yes.)
4. Does this change the thread NAME? "Computational Models & Error Handling" still fits, but if the model-landscape becomes the spine, maybe "Computational Models" with error-handling as an explicit sub-theme. Minor.

## ROUND 29: Computational Models reframe locked

DECISIONS:
1. Reframe spine around model TAXONOMY (imperative / functional / declarative / concurrent), error-handling woven through as a property of each. Fixes the imperative bias.
2. Logic & constraint programming: NAME + LIGHT TOUCH = see and explore a small EXAMPLE (not just named in passing, not taught deeply). Students run/read a small Prolog-ish or constraint example to feel the paradigm. Light, exploratory.
3. Actor model: explicitly NAMED at B8 (already present via OTP).

### Reframed Computational Models thread - final spine
Core question of the thread: "What does a program SAY, how does computation happen, and how does each model handle failure?"
- B1: IMPERATIVE (steps that change state) & FUNCTIONAL (composition of transformations). Two foundational paradigms named. Errors as ordinary (read a stack trace).
- B2: DECLARATIVE introduced (HTML/CSS: state WHAT, not HOW - browser/engine resolves it) + CONCURRENT/REACTIVE (async/event-loop). Failure looks different across models (rejected promise vs sequential crash).
- B3: control flow & exceptions within the imperative model (try/catch named).
- B4: network failures/timeouts - errors you don't control.
- B5: DECLARATIVE QUERYING (SQL = the same "state what, not how" idea as HTML, now for data; query planner finds the how). Transactional rollback (a failure model). 
- B7: LOGIC & CONSTRAINT models - light touch: see and explore a small example (a few Prolog-style facts/rules + a query; or a small constraint problem a solver resolves). Connects to MATH-101 predicate logic, to SQL's logical character, and to the Optimization lens / tradeoff reasoning (constraint satisfaction). Framed as "models where you state facts/rules/constraints and a system derives/solves."
- B8: CONCURRENT & DISTRIBUTED models at scale - ACTOR MODEL named explicitly (isolated processes, message passing; Erlang/OTP as actors, not only as fault tolerance). Fault-tolerance comparison (try/catch vs OTP supervision vs circuit-breaker).

Error-handling is now woven through (B1 stack trace, B2 cross-model failure, B3 try/catch, B4 network, B5 transactional, B8 fault tolerance) as a PROPERTY of each model rather than the spine itself. Richer, bias fixed.

### Model taxonomy made explicit (the thread's organizing map)
1. Imperative (B1) | 2. Functional (B1) | 3. Declarative: markup HTML/CSS (B2), query SQL (B5), logic/constraint (B7 light) | 4. Concurrent/reactive: async (B2), actor (B8)
Failure handling: cross-cutting property of all (woven B1->B8).

### Scoping (foundation vs specialization) - confirmed
- USE deeply: imperative, functional, declarative-markup (HTML), declarative-query (SQL), concurrent/async.
- SEE + EXPLORE AN EXAMPLE: logic programming, constraint programming (B7), actor model (B8 - named, explored via OTP example).
- DEFER to specialization: full Prolog/logic programming, full constraint solving, building real actor/distributed systems.

### Content/host notes
- B7 light logic/constraint example needs a host. CS-206 Graphs & Network Algorithms (B7) is a candidate - querying graph relationships is logic-flavored (Datalog/Cypher); a small logic/constraint example fits the "design under uncertainty / rules & constraints" B7 frame. OR woven into the Design Review context. Small addition - an example + discussion, not a course. Touches content.js lightly (B7 course desc) or just the thread file.
- B8 actor naming: already in CS-208 desc (OTP). Minor desc tweak to name "actor model" explicitly.
- Declarative naming at B2 (HTML) and B5 (SQL): connective framing in those course descs - near-free, light desc edits.

### Thread name
"Computational Models & Error Handling" still fits and is accurate (error-handling is now explicitly a woven property). Keep the name. (Considered "Computational Models" alone, but error-handling is a deliberate co-equal theme - keep both.)

### Accumulated content.js edits now pending (rounds 27 + 29):
- CS-209: broaden to include validation (acceptance + A/B testing) [round 27]
- CS-201 (SQL): name SQL as declarative querying [round 29]
- CS-106 (HTML): name HTML/CSS as declarative [round 29]
- CS-206 or B7: add light logic/constraint example [round 29]
- CS-208: name actor model explicitly [round 29]
All small description edits; no course added/removed/moved. Course grid still stable at 30 credits.

## ROUND 30: Thread name review (all 13)

User: rename "Computational Models & Error Handling" -> "Computational Models" or "Models of Computation". Review other names.

Naming standard to apply: short, parallel in form, names the IDEA not a list of contents, no stale framing, distinguishable from each other at a glance. Avoid "&"-lists where one noun captures it.

### Current 13 names + assessment

SPIRALS:
1. "Data Structures & Representation"
   - Now includes graph sub-spiral; covers representation broadly (bits->graphs->documents). "Data Structures" undersells the representation/encoding breadth. "& Representation" is doing real work. Could go to just "Representation" (broader, captures bits, structures, persistence formats, graphs) but "Data Structures" is the recognizable transfer-aligned term. KEEP "Data Structures & Representation" - or consider "Representation & Data Structures" (lead with the bigger idea). Mild. LEAN keep.
2. "Program Correctness / Code Comprehension"
   - Slash name = two ideas bolted. The thread arc is: make it work -> read others' -> organize -> verify -> defend. The through-line is really UNDERSTANDING/REASONING ABOUT programs (yours and others'). "Code Comprehension" alone misses the correctness/verification angle; "Correctness" alone misses the reading-others' angle. Candidate single name: "Reading & Reasoning About Code" or "Program Comprehension & Correctness". The slash is ugly. LEAN rename -> "Reading & Reasoning About Code" (captures comprehend-others + reason-about-correctness). Flag for user.
3. "APIs & Networked Systems"
   - Fine. Maybe "Networked Systems & APIs". Minor. KEEP.
4. "Human-Centered Computing" (just renamed)
   - Good. KEEP.
5. "Algorithmic Thinking & Complexity"
   - Fine, parallel, clear. Could shorten to "Algorithms & Complexity" but "Algorithmic Thinking" signals it's about the THINKING not just cataloguing algorithms - intentional. KEEP.
6. "Computational Models & Error Handling" -> USER WANTS RENAME
   - error-handling now woven as a property, not co-headline. Drop it from the name. "Models of Computation" vs "Computational Models": 
     - "Models of Computation" has a formal-CS-theory connotation (Turing machines, lambda calculus, automata) - might over-promise theory we don't teach.
     - "Computational Models" is broader/softer - fits "imperative/functional/declarative/concurrent paradigms" better.
   - LEAN "Computational Models". (Recommend over "Models of Computation" to avoid the automata-theory connotation.) Confirm with user.
7. "Testing & Formal Verification"
   - Just sharpened to code-correctness only (acceptance moved out). Name is accurate. Maybe "Testing & Verification" (drop "Formal" - we do informal verification too, from B1). "Formal" might overstate. LEAN "Testing & Verification". Mild.
8. "Boundaries & Contracts"
   - Excellent, distinctive, captures the meta-thread. KEEP.
9. "Sociotechnical Structure"
   - After round 25 it owns: teamwork, collaboration, code-review-as-coordination, team reflection, Conway's Law. "Sociotechnical Structure" is academically precise but jargony; might not signal "teamwork & collaboration" to faculty at a glance. Candidates: "Teams & Sociotechnical Structure", "Collaboration & Sociotechnical Structure", "Sociotechnical Systems". The Conway's-Law/systems-mirror-orgs idea is the distinctive core (don't lose it to a generic "Teamwork"). LEAN "Collaboration & Sociotechnical Structure" (signals both the practice and the systems idea). Flag.

LENSES:
1. "Security, Privacy & Ethical Reasoning"
   - Three-item name but each is distinct and all genuinely covered. Could shorten to "Security, Privacy & Ethics". "Ethical Reasoning" emphasizes the THINKING (parallel to keeping "Algorithmic Thinking"). Mild. LEAN "Security, Privacy & Ethics" for parallelism/brevity, or keep. Minor.
2. "Optimization Reasoning"
   - "Reasoning" suffix fits (it's a reasoning pattern, not a math course). Could be just "Optimization" but that over-promises mathematical optimization (which is deferred). "Optimization Reasoning" honestly signals "the reasoning pattern." KEEP.
3. "Professional Practices"
   - Good, clear, captures the bundle. KEEP.

BOUNDED:
1. "AI-Assisted Development"
   - Accurate. Given the bounded/comprehension-protective character, maybe "Responsible AI Use" or "AI as a Learning Tool"? But "AI-Assisted Development" is the recognizable industry term and the B8 course is "Data Analysis & Responsible AI". KEEP "AI-Assisted Development" (recognizable; the bounded character is explained in the thread, not the name).

### Summary of proposed changes (for user confirmation)
DEFINITE (user-requested): 
  - "Computational Models & Error Handling" -> "Computational Models"
PROPOSED (review):
  - "Program Correctness / Code Comprehension" -> "Reading & Reasoning About Code" (kill the slash)
  - "Testing & Formal Verification" -> "Testing & Verification" (drop "Formal")
  - "Sociotechnical Structure" -> "Collaboration & Sociotechnical Structure" (signal teamwork)
  - "Security, Privacy & Ethical Reasoning" -> "Security, Privacy & Ethics" (brevity/parallel) [very minor]
KEEP AS-IS:
  - Data Structures & Representation, APIs & Networked Systems, Human-Centered Computing, Algorithmic Thinking & Complexity, Boundaries & Contracts, Optimization Reasoning, Professional Practices, AI-Assisted Development

### Parallelism note
Names mix forms: some "X & Y", some single concept, some "X-ing". That's OK if each is the clearest for its thread - forcing uniform grammar can hurt clarity. But the SLASH name (#2) is the clear outlier and should go regardless.

## ROUND 31: Name refinements

- #1 CONFIRMED: "Program Correctness / Code Comprehension" -> "Code Comprehension". Clean, captures the understand-programs through-line.
- #2 PUSHBACK: user suggested "Trustworthy Computing" for the testing/verification thread. PROBLEM: rounds 26-27 deliberately narrowed this thread to CODE-CORRECTNESS only (moved acceptance/fitness to Human-Centered Computing). "Trustworthy" re-broadens to security/privacy/reliability/fitness - exactly what we separated out - and collides with the Security/Privacy/Ethics lens (which owns "trust"). Recommend a correctness-scoped name instead. Candidates: "Software Correctness", "Correctness & Verification", "Verification" alone. LEAN "Correctness & Verification" (testing + formal/informal verification, both about correctness). Flag the collision to user.
- #3 sociotechnical: user wants to keep the connotation (systems mirror the orgs that build them; team structure shapes system structure) without the jargony "sociotechnical structure". Generate alternatives:
  - "Teams & Systems" - too vague
  - "Conway's Law" - too inside-baseball as a thread title
  - "How Teams Build Systems" - descriptive, accessible, keeps the team<->system link
  - "Collaboration & System Structure" - signals teamwork + the structural mirror
  - "Team & System Structure" - parallel, compact, keeps the mirror idea (team structure <-> system structure)
  - "Building Together" - warm but loses the structural/Conway edge
  - "Teamwork & System Design" - clear but loses the MIRROR (Conway) idea slightly
  - "Collaboration & Conway's Law" - names the law for those who know it
  - LEAN: "Team & System Structure" (compact, parallel, preserves the structural-mirror connotation that IS Conway's Law without the word 'sociotechnical') OR "Collaboration & System Structure" (foregrounds the teamwork practice). The core connotation to preserve: team structure and system structure mirror each other. "Team & System Structure" holds both halves and implies the mirror by juxtaposition.

### Updated name slate (pending #2 and #3 confirmation)
SPIRALS:
1. Data Structures & Representation [keep]
2. Code Comprehension [CONFIRMED rename]
3. APIs & Networked Systems [keep]
4. Human-Centered Computing [keep]
5. Algorithmic Thinking & Complexity [keep]
6. Computational Models [CONFIRMED rename]
7. (testing/verification) - PENDING: recommend "Correctness & Verification", user proposed "Trustworthy Computing" (flagged collision)
8. Boundaries & Contracts [keep]
9. (sociotechnical) - PENDING: recommend "Team & System Structure" or "Collaboration & System Structure"
LENSES:
1. Security, Privacy & Ethics [user picked from earlier? not confirmed - leave as Security, Privacy & Ethical Reasoning unless confirmed]
2. Optimization Reasoning [keep]
3. Professional Practices [keep]
BOUNDED:
1. AI-Assisted Development [keep]

## ROUND 32: Final name slate LOCKED

DECISIONS:
- Testing/verification thread -> "Correctness & Verification" (protects the narrow code-correctness scope)
- Sociotechnical thread -> KEEP "Sociotechnical Structure" (user keeps the precise term)
- Security/Privacy/Ethics lens -> "Trustworthy Computing" (user's reassignment - and it FITS here: trustworthiness is the umbrella over security+privacy+ethics; "can people trust this system and its builders". The connotation that was WRONG on the correctness thread is RIGHT here.)

### FINAL 13-THREAD NAME SLATE
SPIRALS (9):
1. Data Structures & Representation
2. Code Comprehension
3. APIs & Networked Systems
4. Human-Centered Computing
5. Algorithmic Thinking & Complexity
6. Computational Models
7. Correctness & Verification
8. Boundaries & Contracts
9. Sociotechnical Structure
LENSES (3):
1. Trustworthy Computing  (was "Security, Privacy & Ethical Reasoning")
2. Optimization Reasoning
3. Professional Practices
BOUNDED PRACTICE (1):
1. AI-Assisted Development

### Note: "Trustworthy Computing" as the lens name
Scope unchanged - still security, privacy, ethical reasoning, data minimization, harm consideration. The NAME now frames them under their unifying purpose (trust) rather than listing them. Good: a lens is a standing QUESTION, and "is this trustworthy / can people trust us with this" is exactly the standing question. Arguably the best-named lens now. The B6 "Responsible Development" block frame aligns with it (responsible dev produces trustworthy software).

### Naming coherence check (full slate)
- No slashes. ✓ (killed Program Correctness / Code Comprehension)
- No stale framing. ✓ (Computational Models dropped error-handling; Correctness & Verification dropped Formal/acceptance)
- Each names an idea, not a content list (mostly). The "& " names (Data Structures & Representation, APIs & Networked Systems, Algorithmic Thinking & Complexity, Correctness & Verification, Boundaries & Contracts) pair two facets of one idea - acceptable, each pair is genuinely one concept.
- Distinguishable at a glance. ✓
- Mixed grammatical form retained intentionally (clarity over uniformity).
- Trustworthy Computing / Computational Models / Human-Centered Computing all end in a noun-phrase; nice informal rhythm among the conceptual ones.

This slate is stable. Next regeneration should use these names throughout.

## ROUND 33: Mapping the curriculum to two new service consumers (Geography/GIS, Communications/Digital Media)

Two real downstream degrees:
- GEOGRAPHY (GIS degree): uses us for SCRIPTING SKILLS
- COMMUNICATIONS (Digital Innovation in Media): uses us for FOUNDATIONAL DEV KNOWLEDGE

### Recall our service-course model (round 17)
"We own a domain-neutral foundational UNIT; the partner owns the domain-application course; together = a one-semester progression." Established examples: Relational Databases (2cr unit) + partner's domain app; OSI Networking (2cr) + partner's domain course. Good candidates = domain-neutral, foundational, recognizable, prerequisite-light.

### The problem: our curriculum is now a TIGHTLY SPIRALED, INTERDEPENDENT design
The whole strength of what we built is that competencies spiral and threads interconnect across 8 blocks. That's GREAT for our majors but creates FRICTION for service consumers, who want to extract a SLICE without taking the whole interdependent thing. A GIS student doesn't want "read->modify->model->structure->store->responsible->judge->operate" as a 2-year arc; they want enough Python/scripting to automate GIS workflows. Our courses are 1-credit, 8-week, and deliberately decoupled into "short parallel chains" - which actually HELPS here (small units are extractable) - but the spiral means later courses assume earlier competencies.

### Map each consumer against our actual blocks/courses

GEOGRAPHY / GIS - wants SCRIPTING:
- What they need: variables, control flow, functions, data types, file I/O (read/write spatial data files), data transformation (reshape/filter datasets), maybe basic API consumption (pull from geo services), maybe basic data viz. NOT: OOP depth, data structures theory, networking theory, databases-design, testing/verification rigor, team software eng.
- Our courses that fit: CS-101 Imperative Programming (core scripting!), CS-102 Functional Programming (transformation - maps well to data pipelines), CS-104 Data Transformation & Manipulation (parse/filter/reshape - EXACTLY GIS scripting), maybe CS-106 (consuming an API for geo data). 
- So GIS scripting = roughly CS-101 + CS-104 (+ maybe CS-102 or CS-106). That's a coherent 2-3 credit "Scripting for [domain]" foundation unit. Maps cleanly! These are Block 1-2 courses - early, prerequisite-light, domain-neutral. GOOD service candidate.
- Tension: CS-104 (Data Transformation) in our design assumes B1 (both paradigms) as background. For GIS we'd want CS-101 + CS-104 as a pair, skipping the functional depth or including just enough. Mostly works.

COMMUNICATIONS / Digital Innovation in Media - wants FOUNDATIONAL DEV KNOWLEDGE:
- What they need: broader than GIS. Probably: basic programming, web foundations (HTML/CSS/JS - building web things), consuming APIs, maybe basic data-driven interactivity, accessible/human-centered design (VERY relevant to media!), maybe a bit of data viz. NOT: deep data structures, complexity, databases-design rigor, networking theory, formal verification.
- Our courses that fit: CS-101 Imperative, CS-106 Web Foundations & Data-Driven Rendering (PERFECT for digital media - HTML/CSS/accessibility/fetch-render), CS-104 Data Transformation, maybe CS-111 Systems & APIs (consuming/building simple APIs), and notably our HUMAN-CENTERED COMPUTING thread is highly relevant to media (accessibility, UX, design).
- So Digital Media = roughly CS-101 + CS-106 (+ maybe CS-104, CS-111). A "Foundations of Media Development" unit. These span Block 1-4. Slightly broader/later than GIS but still early-ish. GOOD candidate, especially CS-106 which is almost custom-fit for digital media.

### The gap this exposes in our service model
Our round-17 model assumed service courses are SELF-CONTAINED UNITS (like Relational Databases = SQL+Design, a clean topical block). But GIS and Digital Media don't want a topical block - they want a CURATED PATH through our early courses (scripting path; web/media-dev path). This is a DIFFERENT kind of service offering:
  - Type 1 (round 17): a self-contained topical unit (Relational Databases, OSI Networking) - a coherent subject other depts bolt their domain onto.
  - Type 2 (NEW, GIS/Digital Media): a CURATED SEQUENCE of our early foundational courses, selected for a domain's needs - "scripting track" (CS-101+104), "media-dev track" (CS-101+106+...). Not a new subject, but a PATHWAY through existing courses.
Both are enabled by the 1-credit modular design! Because courses are small and (relatively) decoupled, we can compose different curated paths for different consumers WITHOUT building new courses. This is a STRENGTH of the modular/decoupled architecture we might not have fully exploited.

### But the spiral creates a real constraint
Our courses embed threads that assume continuity. E.g. CS-106 (Web Foundations) carries HCI pass 1, async/event-loop, declarative-models naming, data-minimization - some of which assume CS-104/B2 context or feed forward to courses the service student won't take. For a service student, each borrowed course must function STANDALONE (or with only the other borrowed courses as prereqs). Question: are our early courses written to stand alone, or do they lean on the spiral so heavily they don't transplant? 
  - CS-101 (Imperative): essentially standalone. ✓
  - CS-104 (Data Transformation): assumes B1 paradigms lightly; mostly standalone if paired with CS-101. ~✓
  - CS-106 (Web Foundations): standalone-ish, but carries threads (async, declarative naming) that are richer-in-context; for a service student those become self-contained intro topics rather than spiral passes. Works but loses the spiral payoff. ~✓
  - CS-111 (Systems & APIs): assumes more (data structures B3/4 context, Boundaries thread). Less standalone. Harder to transplant.
So: the EARLIER the course, the more transplantable (less spiral history assumed). GIS/Digital Media both draw from early courses - which is exactly why they work. A consumer wanting a LATE course (e.g. someone wanting our deployment course) would face heavy prereq/spiral baggage.

### Design principle this surfaces
"Service-extractability decays with block depth." Early blocks (1-2) are highly extractable (little spiral history); late blocks (7-8) are deeply embedded (assume the whole arc). Service offerings should be built mostly from early courses. GIS (scripting, B1-2) and Digital Media (B1, B2, some B4) both honor this naturally. Good.

### Two service TYPES to name in the model
1. Topical Unit (round 17): self-contained subject, partner adds domain app. (Relational DB, OSI)
2. Curated Foundational Path (round 33): a domain-selected sequence of early courses. (GIS scripting path, Digital Media dev path)
Both exploit the 1-credit modular design. Type 2 needs each constituent course to function with only its fellow-borrowed courses as prereqs - achievable for early courses.

### Open questions for user
1. Do we want to formally support Type 2 (curated foundational paths) as a service model alongside Type 1 (topical units)?
2. For GIS: is the target literally "scripting" = CS-101 + CS-104 (imperative + data transformation), or do they want more (functional, API consumption)? Need geography's actual ask.
3. For Digital Media: CS-106 (Web Foundations) is almost custom-fit. Is the target web/interactive-media dev (CS-101+106+maybe 111) or broader? Need communications' actual ask.
4. Do our early courses need a "standalone-capable" design constraint added (each early course must function with only other early courses as prereqs), so they transplant cleanly to service paths? This is a real design requirement if we commit to Type 2.
5. Should there be a domain-neutral "scripting" course distinct from CS-101 Imperative (which is paradigm-focused for our majors)? GIS scripting might want a more applied, less paradigm-conscious intro. Tension between our majors' framing (imperative-as-one-paradigm) and a service student's need (just teach me to script).

## ROUND 34: Service model decisions

DECISIONS:
1. Support BOTH service types: Topical Units (self-contained subject + partner domain app) AND Curated Foundational Paths (domain-selected sequence of early courses). The 1-credit modular design enables both.
2. DO NOT add a "standalone-capable" design constraint. Borrowed courses lose some spiral payoff out of context, and that's ACCEPTED. The design stays optimized for OUR majors' spiral; service consumers get courses as-is.
3. GIS/scripting reconciliation: undecided pending Geography's actual ask.

### Why decision #2 is the right discipline (and its consequence)
This is a priority statement: the spiral integrity for OUR majors is NOT compromised to make courses more transplantable. We don't water down CS-106's threads so a media student gets a cleaner standalone course. Service consumers take our courses as they are; if a course carries spiral context a service student lacks, that context becomes (for them) either harmless richness or a self-contained intro - but we don't REMOVE it.
Consequence: service students occasionally encounter forward/backward references to threads they're not following ("as you'll see when you build APIs in a later course..."). For a service student that's mild noise, not a blocker, IF courses are written so the core competency is deliverable without the spiral. So decision #2 implies a SOFT expectation (not a hard constraint): a course's CORE skill should be learnable standalone, even though its spiral enrichments assume continuity. We just won't engineer the courses around service needs.
This keeps the design honest: built for majors, lent to others. The modular 1-credit structure makes lending feasible without redesign.

### The two service types - formalized for the doc
TYPE 1 - TOPICAL UNIT
  - A self-contained subject (e.g. Relational Databases = SQL Fundamentals + Database Design; OSI Networking Fundamentals).
  - Domain-neutral, recognizable, prerequisite-light.
  - Partner department supplies the domain-application course; together = one-semester progression.
  - Consumers so far: (business -> databases, network admin; CompE -> networking low-level)
TYPE 2 - CURATED FOUNDATIONAL PATH
  - A domain-selected SEQUENCE of our early (Block 1-2, sometimes B4) courses, composed for a domain's needs. No new courses built.
  - Each course taken as-is (spiral enrichments may be lost on the service student - accepted).
  - Best drawn from EARLY blocks (extractability decays with block depth).
  - Consumers so far:
    * Geography/GIS -> "scripting": candidate path CS-101 (+ CS-104, possibly CS-102/CS-106). Exact set pending Geography's ask.
    * Communications/Digital Media -> "foundational dev": candidate path CS-101 + CS-106 (+ possibly CS-104, CS-111). CS-106 and the Human-Centered Computing thread are especially relevant.

### Principle: service-extractability decays with block depth
Early courses (B1-2) transplant cleanly (little assumed spiral history). Late courses (B7-8) are deeply embedded. Service offerings should draw mostly from early blocks. Both new consumers do. This also means our late courses are essentially NOT service-extractable - they're for majors (and specialization students) only. That's fine and worth stating.

### Still-open: GIS scripting vs CS-101's paradigm framing
Pending Geography's actual requirements. Two scenarios:
  (a) If Geography wants light automation/scripting: CS-101 (imperative) alone may suffice; its paradigm framing is harmless background ("this is one way to tell a computer what to do") and the core skill (write scripts that manipulate data/files) is fully there. CS-101 wears both hats fine.
  (b) If Geography wants real data-pipeline/automation depth: CS-101 + CS-104 (Data Transformation) is the better path - CS-104 is literally "parse/filter/reshape data," the heart of GIS scripting. 
  Either way, no new course needed yet. Only if Geography wants something neither course delivers (e.g. heavy spatial-specific scripting) would a dedicated course arise - and that domain-specific part is THEIRS to build (Type 1/2 model: we provide foundational scripting, they provide spatial application).
ACTION: get Geography's actual learning outcomes before deciding. Likely CS-101 (+CS-104) suffices.

### Net: no curriculum CHANGES from this round
This round is about SERVICE STRATEGY, not curriculum content. No blocks/courses/threads change. The output is: a formalized two-type service model + a "extractability decays with depth" principle + candidate paths for two consumers + a flagged need for the partner departments' actual requirements. Document-level addition (overview's service-course section gains Type 2), not a structural change.

## ROUND 35: Dataflow models + geospatial data/algorithms

Three additions:
1. DATAFLOW models -> Computational Models thread (web server request/process pipelines + D3 operations)
2. GEOSPATIAL data -> Data Structures & Representation thread (representing data)
3. GEOSPATIAL algorithms -> Algorithmic Thinking & Complexity thread

### 1. Dataflow models in Computational Models
Current Computational Models taxonomy: imperative, functional, declarative (markup/query/logic-constraint), concurrent/reactive (async, actor).
DATAFLOW is a distinct model: computation as data flowing through a pipeline of transformations; each stage transforms and passes along. It's RELATED to functional (composition) and to reactive (streams) but distinct - the mental model is "data moves through stages" not "call functions" or "react to events."
User's two anchors:
  - WEB SERVER REQUEST/PROCESS PIPELINES: a request flows through middleware/handlers (parse -> auth -> route -> handler -> serialize -> respond). This is a dataflow pipeline. Natural home: B4 (Systems & APIs - building APIs) or B8 (deployment/server operation). B4 is where students BUILD APIs, so the request-pipeline mental model fits there - "a request flows through stages." Good B4 fit, extends the APIs work.
  - D3 OPERATIONS: D3's data-join + method-chaining is a dataflow/pipeline model (data -> scale -> shape -> render, chained). D3 lives in the data-viz throughline (Human-Centered Computing, B4 SVG viz). So D3-as-dataflow naturally co-locates with the B4 viz pass. NICE convergence: B4 already has SVG viz (HCI) AND API-building (APIs) - BOTH are dataflow examples. B4 becomes the natural DATAFLOW home: request pipelines (server side) + D3 data-join pipelines (client/viz side). Two concrete dataflow instances in one block.
  - Also functional pipeline (map/filter/reduce as a data pipeline) was already in B1/B2 (CS-102 functional, CS-104 transformation) - that's PROTO-dataflow. So dataflow can SEED at B2 (transformation pipelines: parse->filter->reshape is a dataflow) and get NAMED as a model at B4 (request pipelines + D3).
Dataflow passes (added to Computational Models thread):
  - B2 (seed): CS-104 data transformation as a pipeline (parse -> filter -> reshape -> output) - proto-dataflow, not yet named
  - B4 (named): dataflow model named explicitly via TWO anchors - web server request pipelines (CS-111 Systems & APIs) and D3 data-join/method-chaining (the B4 viz pass). "Computation as data flowing through transformation stages."
  - Possibly B8: streaming/real-time dataflow at scale (if relevant) - optional, light
This ENRICHES B4 nicely and gives the functional-pipeline work from B1/B2 a named destination. Low new content - mostly naming + the D3/server-pipeline framing. Updated model taxonomy: imperative, functional, declarative, concurrent/reactive, DATAFLOW.

### 2. Geospatial data in Data Structures & Representation
Representing geospatial data = points, lines, polygons (vector); rasters (grids); coordinate systems; spatial relationships. This is a RICH representation topic and directly serves the GIS service consumers (round 33!) - double benefit (enriches majors + serves GIS).
Where in the Data Structures spiral?
  - The thread: primitive (B1) -> ADTs (B3) -> trees/hashing (B4) -> relational/graph (B5) -> graph/document (B7).
  - Geospatial fits as a REPRESENTATION case study, most naturally where spatial data structures live: 
    * Points/coords as primitive-ish tuples - could touch B1/B3
    * Spatial data as a representation choice - B3 (modeling: how do you represent a map/region?)
    * Spatial INDEXING (quadtrees, R-trees, geohashing) - these are TREE/HASH structures - fits B4 (Trees, Hashing & Hierarchies)! Quadtrees and R-trees are literally trees; geohashing is spatial hashing. PERFECT fit - B4 already does trees/hashing, geospatial indexing is a natural application.
    * Spatial data in databases (PostGIS, spatial queries) - B5 (databases) as a representation/storage case
  - LEAN: geospatial representation seeds at B3 (how to model spatial data - points/lines/polygons/rasters as representation choices) and deepens at B4 (spatial indexing = quadtrees/R-trees/geohashing, riding the existing trees/hashing content). This makes B4's trees/hashing richer (real-world spatial application) AND serves GIS.
  - This is genuinely NEW content (spatial representation + indexing wasn't there) but it RIDES existing structure (trees/hashing already taught) - so it's an enrichment/application layer, modest addition, not a new course.

### 3. Geospatial algorithms in Algorithmic Thinking & Complexity
Spatial algorithms: nearest-neighbor, range queries, spatial joins, point-in-polygon, shortest-path-on-road-networks (which is GRAPH shortest path - ties to graph spiral!), convex hull, etc.
Where in the Algorithmic thread? Thread: complexity/sorting/searching (B4) -> graph algorithms (B7) -> real bottleneck (B8).
  - Spatial NEAREST-NEIGHBOR / RANGE QUERIES: use the spatial indexes from the geospatial-representation addition (B4) - so spatial search algorithms fit B4 (searching, now spatial) or B7.
  - Spatial SHORTEST PATH (routing on road networks): this IS graph shortest-path applied to geospatial graphs - fits B7 (graph algorithms) PERFECTLY. Road network = weighted graph; routing = Dijkstra/A*. A* (heuristic search) is a nice geospatial-motivated addition to B7's graph algorithms. Strong fit.
  - LEAN: geospatial algorithms primarily at B7 (spatial graph algorithms - routing/shortest-path on road networks, A* as geospatially-motivated; spatial joins/queries using B4 indexes). Lighter touch at B4 (spatial search using spatial indexes). Ties beautifully to the graph sub-spiral (round 23) - road-network routing is the geospatial face of graph algorithms.

### Convergence/coherence note
Geospatial threads through: B3 (represent spatial data) -> B4 (spatial indexing via trees/hashing + spatial search) -> B5 (spatial data in databases, optional) -> B7 (spatial graph algorithms / routing). It becomes a SUB-THEME riding multiple threads (Data Structures + Algorithms + graph sub-spiral), much like graphs themselves. It also is the CONTENT that makes the GIS service path (round 33) substantive - a GIS student drawing CS-101/104 for scripting could ALSO benefit from the geospatial representation/algorithm content if it's in courses they take. Note: geospatial content lands in B3/B4/B7 (mid-to-late), while GIS service students draw from B1-2 (early). So geospatial-for-majors (B3-7) and GIS-scripting-service (B1-2) are DIFFERENT - the service students get scripting, not the deep geospatial CS. The deep geospatial CS serves OUR majors (e.g. those heading toward data science / GIS-adjacent work) and possibly an advanced GIS service path. Worth noting the distinction.

### Scope check - is this too much new content?
- Dataflow: mostly naming + D3/server-pipeline framing. Low.
- Geospatial representation: new but rides trees/hashing (B3/B4). Modest.
- Geospatial algorithms: new but rides graph algorithms (B7) + spatial indexes. Modest.
All three are ENRICHMENTS riding existing thread structure, not new courses. They add CONTENT DEPTH to existing courses (CS-109/110 for spatial rep, CS-111 for dataflow, CS-206 for spatial algorithms, B4 viz for D3-dataflow). No credit/course changes. But they do ADD to the content load of those courses - worth flagging that B4 especially is accumulating (trees/hashing + spatial indexing + dataflow naming + D3 + APIs) - B4 load should be watched.

### Course-desc edits needed (content.js)
- CS-109 (ADTs, B3): add geospatial representation seed (points/lines/polygons/rasters as representation choices)
- CS-110 (Trees/Hashing, B4): add spatial indexing (quadtrees, R-trees, geohashing)
- CS-111 (Systems & APIs, B4): add dataflow model - request/process pipelines
- B4 viz (embedded, CS-110 or CS-111): D3 data-join as dataflow
- CS-206 (Graphs, B7): add spatial graph algorithms (routing/shortest-path on road networks, A*)
- Computational Models thread: add dataflow (B2 seed, B4 named)
- Data Structures thread: add geospatial representation sub-theme
- Algorithmic thread: add geospatial algorithms

### Question for user
- B4 is accumulating a lot (trees/hashing, spatial indexing, dataflow, D3, API-building). Is that too much for B4, or acceptable as "B4 is the rich application block"? May need to watch/rebalance. Flag.

## ROUND 36: Computer Engineering service mapping (12 credits: CS0, CS1, Data Structures, OOP)

CompE currently takes 12 credits from us as 4 traditional courses:
- CS0 (intro/pre-programming - often pseudocode, problem solving, basic concepts; sometimes a "preparation for CS1")
- CS1 (first real programming - variables, control, functions, basic data, intro problem solving)
- Data Structures (lists/stacks/queues/trees/hashing/graphs + complexity)
- OOP (encapsulation, inheritance, polymorphism, classes)
Traditional = 3-credit, 16-week courses. 4 x 3 = 12 credits.

### The core tension
Our redesign DISSOLVED these monolithic courses into spiraled 1-credit pieces distributed across blocks AND reorganized by paradigm/concept rather than the traditional sequence. CompE wants the TRADITIONAL shape (recognizable CS0/CS1/DS/OOP on a transcript, ABET-mapped). This is the HARDEST service case yet:
- GIS/Digital Media wanted EARLY courses as a curated path (Type 2) - our early courses map to their needs fairly directly.
- CompE wants RECOGNIZABLE TRADITIONAL COURSES - which we specifically deconstructed. They want the OLD packaging.

### Can our 1-credit pieces REASSEMBLE into the 4 traditional courses?
Let me map traditional-course content to our pieces:

CS1 (first programming): variables, control, functions, arrays, basic problem solving
  - Our pieces: CS-101 Imperative Programming (variables/state/control) + CS-102 Functional Programming + CS-104 Data Transformation (functions, data manipulation)
  - A traditional CS1 is mostly IMPERATIVE. Our CS-101 alone = ~core CS1 imperative content. CS-101+CS-104 ~ a fuller CS1. But our split puts functional (CS-102) as co-equal, which traditional CS1 doesn't. For CompE, CS1 = CS-101 (+ maybe CS-104). ~3 credits if we count CS-101+102+104 but that includes functional they may not want.
  - REASSEMBLY: CS1-equivalent ~ CS-101 + CS-104 (+ CS-102 optional) = 2-3 of our credits. Reasonable.

CS0 (pre-programming/intro): 
  - We don't really HAVE a CS0 - our B1 jumps into imperative+functional programming directly (no pre-programming course). Our "reading first" B1 philosophy is actually CS0-adjacent (read/comprehend before produce) but it's woven INTO CS-101/102, not a separate CS0.
  - GAP: there's no clean CS0 in our design. CompE wanting CS0 is a real mismatch. Options: (a) CS-103 Computational Representation (boolean/number systems/bits) could serve as a CS0-ish "foundations" course - it's conceptual, pre-heavy-programming. (b) Or the reading-oriented early parts. (c) Or we say "our model doesn't have CS0; here's what covers that ground." 
  - This is the WEAKEST mapping. Flag.

Data Structures (lists/stacks/queues/trees/hashing/graphs/complexity):
  - Our pieces: CS-109 Abstract Data Types (lists/stacks/queues, contract-first) + CS-110 Trees, Hashing & Hierarchies + CS-112 Algorithmic Complexity + graph content (CS-206 B7, + graph sub-spiral)
  - REASSEMBLY: Data-Structures-equivalent ~ CS-109 + CS-110 + CS-112 = 3 of our credits. Maps WELL (these three are basically a distributed data structures course). Graphs are later (B7/CS-206) - traditional DS includes graphs, ours defers full graph algorithms to B7. So a CompE "Data Structures" = CS-109+110+112 covers most; graph algorithms would need CS-206 too (but that's B7, later, and bundled with other things). Minor gap on graphs.

OOP (encapsulation/inheritance/polymorphism/classes):
  - Our pieces: CS-107 OOP I + CS-108 OOP II
  - REASSEMBLY: OOP-equivalent ~ CS-107 + CS-108 = 2 credits. Maps CLEANLY. (We kept OOP I/II as a recognizable pair.)

### Reassembly summary
  CS1 ~ CS-101 (+CS-104, +CS-102 optional): 2-3 cr
  CS0 ~ ??? (CS-103 partial; no clean match): GAP
  Data Structures ~ CS-109 + CS-110 + CS-112: 3 cr (graphs partial via CS-206)
  OOP ~ CS-107 + CS-108: 2 cr
  Total clean mappings ~ 9-10 of our credits map to CS1+DS+OOP. CS0 is the gap.

### The deeper question: do they want our COURSES or our COMPETENCIES?
CompE's 12 credits could be satisfied two ways:
  (a) PACKAGE our 1-credit pieces into 4 transcript-courses that LOOK like CS0/CS1/DS/OOP (administrative repackaging - bundle our pieces under traditional course numbers/names for CompE students). The 3-layer model from the original design (transcript courses / developmental experiences / competencies) ALREADY anticipated this - transcript courses are administrative containers. So we could expose a CompE-facing transcript VIEW that bundles pieces into CS0/CS1/DS/OOP while the actual learning is our spiraled pieces. This is elegant - it uses the existing 3-layer separation.
  (b) Or CompE accepts our actual course structure (8-week 1-credit pieces) and re-maps their degree to it. Harder for them (changes their degree structure, ABET re-mapping).
Option (a) is almost certainly what they want and what the 3-layer design enables: KEEP our pedagogical structure, EXPOSE a traditional-looking transcript packaging for service consumers who need it. The "transcript course" layer was DESIGNED to be administrative/flexible - this is exactly its use case.

### But there's a sequencing/timing problem with packaging
Our pieces are distributed across blocks/semesters with the spiral. A traditional "Data Structures" course is one semester. Our DS pieces: CS-109 (B3), CS-110 (B4), CS-112 (B4). B3=Y1 Spring first half, B4=Y1 Spring second half. So CS-109+110+112 all fall in Y1 Spring (one semester!) - they could be packaged as a one-semester "Data Structures" for CompE. GOOD - the DS pieces happen to co-locate in one semester.
  OOP: CS-107+108 both in B3 (Y1 Spring first half). One block. Packageable. GOOD.
  CS1: CS-101 (B1) + CS-104 (B2) - both Y1 Fall. Packageable as Y1 Fall "CS1". GOOD.
  CS0: gap - and timing-wise, if it existed it'd want to be Y1 Fall or a prereq.
So the timing actually WORKS for packaging because related pieces tend to co-locate in semesters (we designed the spiral so related content clusters). Nice unintended benefit.

### Recommendation
- CompE = a THIRD service type, or a variant of Type 1: "Traditional-Course Repackaging" - we expose a transcript VIEW that bundles our 1-credit pieces into recognizable CS0/CS1/DS/OOP courses, leveraging the 3-layer (transcript/experience/competency) design. Pedagogy unchanged; packaging adapts.
- CS0 is the one real gap - need to resolve: does CS-103 (Computational Representation) + the reading-first early material constitute a CS0-equivalent, or does CompE's CS0 cover ground we genuinely don't (e.g. they may want pseudocode/problem-solving-only pre-programming)? Need CompE's CS0 outcomes.
- Graphs in Data Structures: ours defers full graph algorithms to B7; if CompE's DS needs graphs, either include a graph-intro in the packaged DS (we have graph-as-model B3, represent B4) or note graph algorithms come slightly later.

### Service model now has THREE patterns
1. Topical Unit (round 17): self-contained subject + partner domain app. (DB, Networking)
2. Curated Foundational Path (round 33): domain-selected sequence of early courses. (GIS, Digital Media)
3. Traditional-Course Repackaging (round 36): bundle 1-credit pieces into recognizable traditional transcript courses via the 3-layer design. (CompE: CS0/CS1/DS/OOP)
All three exploit the modular 1-credit design + the transcript/competency layer separation. The architecture is proving FLEXIBLE for service - the modular+layered design pays off.

### Questions for user
1. Confirm the "traditional-course repackaging" approach (expose CS0/CS1/DS/OOP transcript bundles over our pieces) - using the 3-layer design's administrative transcript layer?
2. CS0 gap: what does CompE's CS0 actually cover? (pseudocode/problem-solving pre-programming, OR boolean/number-systems foundations [=our CS-103], OR something else). Determines if we have a match.
3. Graphs: is graph content required in CompE's Data Structures? If so, packaging must pull from B7 (later) or include the early graph passes.
4. Does packaging for CompE risk diverging the service students' experience from majors (they take the same pieces, just labeled differently - should be fine, but confirm the pieces aren't reordered in a way that breaks the spiral for them)?

## ROUND 37: CompE resolutions + build CompE file (both options)

RESOLUTIONS:
1. Present BOTH options in a CompE markdown file (repackaging vs re-map).
2. CS0 = gentle intro to programming -> overlaps CS-101. The "CS0 gap" largely closes: CS0+CS1 together map to our CS-101 + CS-102 + CS-104 region (gentle intro through first real programming). CompE's CS0/CS1 split can be drawn across our early programming pieces.
3. Graphs = introduction only in their DS -> our B3 graph-as-model + B4 represent passes SUFFICE. No need to pull B7/CS-206 into the DS package. Clean.

### Refined reassembly (with resolutions)
- CS0 (gentle intro to programming): maps to CS-101 Imperative Programming (early weeks / the gentle on-ramp). Possibly the reading-first framing of B1. CS0 ~ CS-101 (or first half) (+ conceptual CS-103 representation if they want digital foundations too).
- CS1 (first real programming): CS-101 + CS-104 Data Transformation (+ CS-102 functional optional). 
  - Tension: CS0 and CS1 both lean on CS-101. If CS0=CS-101-gentle-intro and CS1=CS-101-fuller, they overlap. Cleaner split: CS0 ~ CS-101 (imperative basics) ; CS1 ~ CS-102 (functional) + CS-104 (data transformation) + CS-103 (representation)? But that makes CS1 not-very-CS1 (CS1 is traditionally imperative). 
  - Better: CS0 ~ a gentle subset (CS-101 first portion + reading framing) ; CS1 ~ CS-101 full + CS-104. Some sharing of CS-101 across the CS0/CS1 boundary is fine in a packaging view (the transcript bundles can overlap-source from the same pieces or split CS-101's weeks). 
  - Cleanest for packaging: treat CS-101 + CS-102 + CS-104 (3 credits, all Y1 Fall/early) as the raw material for BOTH CS0 and CS1, and draw the CS0/CS1 transcript boundary wherever CompE's outcomes split. Since CS0+CS1 traditionally = ~6 credits and we have CS-101+102+104 = 3 credits... MISMATCH IN CREDIT VOLUME.

### CREDIT VOLUME PROBLEM (important)
CompE takes 12 credits currently (4 x 3-credit courses). Our reassembly:
  CS0+CS1 ~ CS-101+102+104 (+103?) = 3-4 of our credits
  Data Structures ~ CS-109+110+112 = 3 credits
  OOP ~ CS-107+108 = 2 credits
  TOTAL ~ 8-9 of our credits to cover what CompE currently gets as 12.
So our content is DENSER / our credits cover MORE per credit? Or our coverage is LIGHTER in raw hours? 
  - Our 1-credit/8-week courses: 1 credit each. 8-9 credits.
  - CompE's 12 traditional credits.
  - The 12-vs-8/9 gap: either (a) our pieces cover the same competencies in fewer credit-hours (denser/more efficient - plausible given focused 1-credit design), or (b) there's genuinely less seat-time and CompE would be getting fewer hours, or (c) CompE's 12 includes content we don't cover (e.g. their CS0 is a full 3-credit course; their DS includes more graph/advanced content).
  - This matters for ABET (contact hours) and for CompE's degree credit count. If we give them 8-9 credits where they had 12, their degree is 3-4 credits short unless backfilled.
  - LIKELY RESOLUTION: the credit MAPPING isn't 1:1 by competency - our spiral means data structures competency is ALSO developed in courses beyond CS-109/110/112 (it spirals into B5/B7). For CompE's purposes, the TRADITIONAL-COURSE-equivalent might bundle MORE of our pieces than the minimal mapping (e.g. their "Data Structures" credit could include CS-109+110+112 PLUS the relevant graph pieces PLUS complexity-adjacent work = more credits). The repackaging can be SIZED to match 12 credits by including the appropriate spiral pieces.
  - This is a real design question for the packaging: which/how-many of our pieces roll up into each traditional course to hit the credit target AND the competency target.

### This actually strengthens the "two options" framing
- Option A (Repackaging): we define 4 transcript bundles (CS0/CS1/DS/OOP) that roll up a SET of our 1-credit pieces summing to ~12 credits, mapped to traditional course outcomes + ABET. The challenge: our pieces are distributed across blocks/semesters, so a bundle may span semesters (a CompE "Data Structures" drawing from B3+B4 is one semester - OK; but if it needs B7 graph pieces, it spans into Y2 - problematic for a Y1 course). With graphs being intro-only (resolved), DS stays in Y1 Spring (B3+B4) - clean. Credit-sizing to 12 needs care.
- Option B (Re-map): CompE adopts our actual 1-credit structure and re-maps their degree + ABET to our competencies. More work for them, but no artificial repackaging; they get our actual (arguably better) pedagogy. The credit-volume question still applies (they'd take ~8-9 of our credits, or more if they want full coverage).

### CompE file should present:
1. Context (what they take now: 12 cr, CS0/CS1/DS/OOP)
2. How the content maps to our pieces (the reassembly table)
3. Option A: Traditional-Course Repackaging (transcript bundles, pros/cons, the credit-sizing note, semester-coherence note)
4. Option B: Re-map to modular structure (pros/cons)
5. Open issues: credit volume (12 vs ~8-9), CS0/CS1 boundary, graph-intro sufficiency (resolved-light), ABET contact-hour mapping
6. Recommendation / what we need from CompE

No curriculum changes this round - it's a service-mapping analysis + a new artifact.

## ROUND 38: K-State actual degree mapping (replace CIS <500 with the new two-year core)

ACTUAL K-State BS CS (Fall 2026), 120 hrs. CS Requirements = 41 cr. The CIS courses:
SUB-500 CIS (to be REPLACED by our two-year core):
- CIS 115 Introduction to Computing Science (2)
- CIS 116 Introduction to Programming (1)
- CIS 200 Programming Fundamentals (4)
- CIS 300 Data and Program Structures (3)
- CIS 301 Logical Foundations of Programming (3)
- CIS 308 C/C++ Programming Laboratory (1)
- CIS 400 Object-Oriented Design, Implementation and Testing (3)
- CIS 415 Ethics and Conduct for Computing Professionals (3)
- CIS 450 Computer Architecture and Operations (3)
Sub-500 CIS total = 2+1+4+3+3+1+3+3+3 = 23 credits

500+ CIS (STAY - these are upper division, not replaced):
- CIS 501 Software Architecture and Design (3)
- CIS 505 Introduction to Programming Languages (3)
- CIS 560 Database System Concepts (3)
- CIS 575 Introduction to Algorithm Analysis (3)
- (Capstone CIS 598/599/643 (3))
- Restricted/Technical electives (500+)
Plus non-CIS in the CS Requirements block: ECE 241 Intro to Computer Engineering (3) - NOT a CIS course, stays.

So: replacing sub-500 CIS = 23 credits being replaced by our 2-year core.

### CRITICAL FINDINGS - the sub-500 CIS courses are NOT all "intro programming"
Our two-year core was designed to replace intro programming + data structures + OOP (the CS0/CS1/DS/OOP world). But K-State's sub-500 CIS includes THREE courses that are NOT that:
1. CIS 301 Logical Foundations of Programming (3) - this is logic/formal methods/proofs. Does our core cover it? We have MATH-101 Logic & Sets (external) + the Correctness & Verification thread (pre/post-conditions, formal verification) + Boundaries & Contracts. PARTIAL overlap but CIS 301 is a dedicated formal-logic-of-programming course. Gap risk.
2. CIS 415 Ethics and Conduct for Computing Professionals (3) - dedicated ethics course. Our core has the Trustworthy Computing lens (ethics woven throughout) + B6 Responsible Development frame. But ours is EMBEDDED, not a standalone 3-credit ethics course. K-State currently has a DEDICATED ethics course. Replacing it with embedded ethics = a philosophy difference. Gap/tension.
3. CIS 450 Computer Architecture and Operations (3) - computer architecture (organization, assembly, memory, etc). Our core has CS-103 Computational Representation (boolean/number systems/bits) but NOT full computer architecture. And we CUT HDL/FPGA earlier. ECE 241 (Intro to Computer Engineering) also covers some hardware. CIS 450 architecture is LARGELY NOT in our core. Big gap.
Also:
4. CIS 308 C/C++ Programming Laboratory (1) - specific C/C++ skills. Our core is paradigm/language-agnostic (we don't commit to C/C++). Gap - they may want specific C/C++ exposure.

### So the replacement is NOT clean 1:1
Our 2-year core (26-30 cr) was scoped to replace: intro programming, data structures, OOP, + our broader systems-thinking additions (databases, testing, security, HCI, etc - which actually go BEYOND what sub-500 CIS covers and into 500-level territory like CIS 560 databases, CIS 575 algorithms).

Mismatch analysis:
- Things our core covers that map to sub-500 CIS: CIS 115/116/200 (intro/programming) -> our B1-B2; CIS 300 (data structures) -> our B3-B4; CIS 400 (OOP) -> our B3. CLEAN.
- Things sub-500 CIS has that our core covers DIFFERENTLY/PARTIALLY: CIS 301 (logic) -> partial (MATH-101 + verification thread); CIS 415 (ethics) -> embedded not standalone; CIS 450 (architecture) -> mostly NOT covered; CIS 308 (C/C++) -> not language-specific.
- Things our core covers that are CURRENTLY 500-level at K-State: databases (CIS 560 is 500!), algorithm analysis (CIS 575 is 500!), software arch (CIS 501 is 500!). Our core INCLUDES database design, algorithmic complexity, etc. that K-State currently teaches at 500-level. So our core REACHES UP into 500-level content.

### This is the key insight for the analysis
Our two-year core is NOT a drop-in replacement for the 23 credits of sub-500 CIS. It's a DIFFERENT SHAPE:
- It COVERS most sub-500 CIS (intro, programming, data structures, OOP)
- It does NOT fully cover: computer architecture (CIS 450), dedicated formal logic (CIS 301), dedicated ethics (CIS 415), C/C++ specifics (CIS 308)
- It REACHES INTO 500-level content (databases, algorithm analysis, software design, testing, security, HCI) that K-State currently teaches above 500
So replacing "all sub-500 CIS" with our core LEAVES GAPS (architecture, maybe logic/ethics/C++) AND OVERLAPS UPWARD (our core duplicates parts of CIS 560/575/501).

### Credit reconciliation
- Sub-500 CIS being removed: 23 cr
- Our core: 26-30 cr (currently ~30 with full stats; CS-only is 22)
- If our 22 CS credits replace 23 sub-500 CIS credits: roughly even on CS credits (22 vs 23). But our core ALSO includes 4-8 external math/stat credits that overlap with K-State's existing MATH 510 Discrete (3) + STAT 510 (3) requirements! K-State already requires MATH 510 Discrete Math and STAT 510 Probability/Stats separately. Our core's embedded discrete (MATH-101..104) and stats (STAT-101..104) would DUPLICATE or REPLACE those. Need to reconcile our external courses with K-State's existing MATH 510/STAT 510.

### Questions I need answered (for the markdown file)
1. SCOPE of replacement: "all CIS under 500" = the 9 courses / 23 credits listed. Confirm. Does it include the non-programming ones (CIS 301 logic, CIS 415 ethics, CIS 450 architecture, CIS 308 C/C++)? Or only the programming-sequence ones (115/116/200/300/400)?
2. COMPUTER ARCHITECTURE (CIS 450): our core doesn't cover this. Does it move to a 500-level course, stay as a separate requirement, get added to our core, or get dropped? Big gap.
3. ETHICS (CIS 415): replace the dedicated 3-cr ethics course with our embedded Trustworthy Computing lens + B6 frame? Or keep a standalone ethics course? Philosophy decision.
4. FORMAL LOGIC (CIS 301): our MATH-101 + verification thread partially covers; is that enough, or is dedicated logic-of-programming needed?
5. C/C++ (CIS 308): our core is language-agnostic. Does the program need specific C/C++ exposure (relevant for systems/CompE-adjacent)? 
6. EXTERNAL COURSE OVERLAP: K-State requires MATH 510 Discrete (3) + STAT 510 (3) in the Math block (separate from CS Requirements). Our core embeds its own discrete (4 x 1cr) + stats (4 x 1cr). Do our embedded math/stats REPLACE MATH 510/STAT 510, or duplicate? Reconcile.
7. 500-LEVEL OVERLAP: our core covers databases, algorithm analysis, testing, software design - which K-State teaches at 500 (CIS 560/575/501). Does our core let students SKIP those 500-levels, or is there intended overlap/reinforcement? Affects total credit count.
8. The 41-credit CS Requirements block: if 23 sub-500 replaced by ~22-30 of our core, and 500-levels stay, what's the new CS Requirements total? Need target.

This is a substantial analysis - the file should map old->new course by course, flag the 4 gap areas (architecture, logic, ethics, C++), flag the external-course overlap (MATH510/STAT510), flag the upward 500-level overlap, and ASK the questions above.

## ROUND 39: K-State reconciliation answers

ANSWERS:
1. Discrete math + stats: the new core's embedded sequences REPLACE K-State's MATH 510 Discrete + STAT 510. Collision resolved - our MATH-101..104 + STAT-101..104 ARE the discrete/stats requirement now. (No duplication.)
2. CIS 450 Computer Architecture: it's PROGRAMMING-CENTRIC (stack/heap, cache misses, memory model from a programmer's view - NOT digital logic/hardware design). This content is ABSORBED by the core. Gap CLOSES - and this tells us WHERE: stack/heap/memory model fits the Computational Models thread + CS-103 representation + B8 performance (cache misses -> real bottleneck/performance pass). So architecture-as-programming-concern is already in our wheelhouse; just need to make sure stack/heap/cache are explicitly named.
3. CIS 301 Logical Foundations: ABSORBED by the core (MATH-101 Logic & Sets + Correctness & Verification thread + Boundaries & Contracts). Gap CLOSES - user confirms distributed coverage is sufficient.
4. CALCULUS: pushed to THIRD YEAR; Calc 2 may not be required. (Calc currently MATH 220 Calc I + MATH 221 Calc II in years 1-2.)

### What the architecture/301 absorption requires (small additions to name explicitly)
- Stack & heap (memory model): name explicitly. Natural home: CS-103 Computational Representation (B1) introduces it (how memory is laid out) OR Computational Models. Actually stack/heap connects to: function calls (stack frames - B1 imperative/functional, recursion B3), dynamic allocation (heap - data structures B3/B4). Could seed at B1 (CS-103: memory model alongside representation) and reinforce where recursion/data-structures need it.
- Cache misses / performance from hardware: fits B8 (real-bottleneck performance pass, Algorithmic thread) + the "why slow under load" Computational Models B8. Name cache/memory-hierarchy effects there.
- These are ENRICHMENTS to existing courses (CS-103, B8 performance), not new courses. Light. Confirm naming.

### CALCULUS - the bigger ripple
Currently MATH 220 Calc I (4, counts under KSC-3 core) + MATH 221 Calc II (4) in the math block. Pushing calc to year 3, Calc 2 maybe not required.
Implications:
- Our 2-year core's MATH/STAT sequence (discrete + stats, 8 x 1cr) does NOT include calculus. Good - calc was separate (MATH 220/221). Pushing calc out of years 1-2 means our 2-year math footprint = just our 8 embedded credits (discrete + stats). Clean.
- BUT: our STAT sequence (probability, distributions, regression) traditionally assumes SOME calculus (continuous probability, integration for distributions, etc). If calc is pushed to year 3 and our stats is in years 1-2 (B4-B8), our stats courses CANNOT assume calculus. This constrains the stats sequence design:
  * STAT-101 Descriptive: no calc needed. Fine.
  * STAT-102 Probability: discrete probability fine without calc; CONTINUOUS probability/distributions traditionally uses integration. Without calc, must be taught at a pre-calc/conceptual level (which is actually common for intro stats - "intro stats" courses are often non-calculus). 
  * STAT-103 Distributions/Sampling: same - can be done non-calculus (intro level) but loses rigor.
  * STAT-104 Regression: regression can be taught conceptually/computationally without calculus (least squares geometrically/numerically). Fine.
  So our stats sequence must be NON-CALCULUS (intro-stats style), which is consistent with it being foundational/early. The CALCULUS-BASED probability/stats (for ML rigor) would come LATER (year 3+, after calc). This actually aligns: foundation stats = conceptual/computational (no calc); specialization stats = calculus-based rigor. Flag this explicitly - our STAT sequence is intro/non-calculus by necessity and design.
- ML readiness: ML needs calculus (gradients!) + linear algebra + probability. If calc is year 3, then full ML-prep (calculus-based) is year 3+, and our foundation provides the CONCEPTUAL/computational groundwork (stats reasoning, the optimization LENS, linear algebra question still open). This is fine - foundation seeds, specialization (with year-3 calc) does the rigor. Consistent with everything.
- Calc 2 maybe not required: affects downstream (some math electives/specializations need Calc 2). Not our 2-year core's concern directly, but worth noting our core doesn't depend on Calc 2.

### Linear algebra (still the open 9th external)
Recall lin-alg was the unplaced 9th external (ML prereq). With calc pushed to year 3, the math landscape in years 1-2 is: our discrete (4) + stats (4) = 8, no calc, no lin-alg. If lin-alg is also ML-prep, it could join calc in year 3, OR stay in the foundation. With calc gone from years 1-2, is there ROOM/rationale for lin-alg in the foundation? The adjacency-matrix seed (B4) gives partial lin-alg. Full lin-alg could now naturally sit in year 3 WITH calc (both ML-prereqs, both pushed later). LEAN: lin-alg follows calc to year 3 (or a dedicated math course there), foundation keeps only the B4 adjacency-matrix seed. This RESOLVES the long-open lin-alg question cleanly - it goes to year 3 with calc, not crammed into the 8-slot foundation. Confirm with user.

### Net effect on the core
- Discrete/stats: now officially REPLACE MATH 510/STAT 510 (no change to our design, just confirms our embedded sequence IS the requirement).
- Architecture (programming-centric): absorbed - add explicit naming of stack/heap (CS-103/B1) + cache/memory-hierarchy (B8 performance). Small enrichment.
- Logic (301): absorbed - no change needed (already covered).
- Calculus: not in our 2-year core anyway (was separate MATH 220/221); pushing it to year 3 means our STAT sequence is confirmed NON-CALCULUS/intro-level. Document this constraint.
- Lin-alg: likely resolves to year 3 with calc (foundation keeps adjacency-matrix seed only). Confirm.

### Questions for user
1. Confirm: add explicit stack/heap naming (CS-103/B1) + cache/memory-hierarchy performance (B8) to absorb CIS 450's programming-centric architecture? (Small enrichment.)
2. Confirm: our STAT sequence is intentionally NON-CALCULUS (intro-stats level), with calculus-based statistical rigor deferred to year 3+ (after calc)? 
3. Lin-alg: does it follow calculus to year 3 (foundation keeps only the B4 adjacency-matrix seed), or stay as a foundation course? (Pushing calc later makes "lin-alg in year 3" natural.)

## ROUND 40: Resolutions folded; constraints recorded

FOLDED into content.js:
- CS-103 (B1): stack/heap memory model named (absorbs CIS 450 programmer-facing architecture)
- CS-208 (B8): cache misses / memory-hierarchy / locality in the performance pass (absorbs CIS 450 cache concerns)

CONSTRAINTS now locked (document these):
1. STATISTICS SEQUENCE IS NON-CALCULUS. STAT-101..104 taught at intro/conceptual/computational level, no calculus assumed. Calculus-based statistical rigor deferred to year 3+ (after calc moves to year 3). This is a co-design constraint for the statistics department: do NOT assume calculus in the foundation stats courses.
2. LINEAR ALGEBRA -> YEAR 3 (with calculus). Foundation keeps only the B4 adjacency-matrix seed (in CS-110, graph representation). The long-open "9th external" question is RESOLVED: lin-alg is NOT a foundation course; it joins calc in year 3 as ML-prep. This removes the budget pressure the 9th external created.
3. CALCULUS -> YEAR 3 (Calc 2 maybe not required). Not part of the 2-year core (was always separate MATH 220/221 at K-State). Confirms the foundation math footprint = 8 embedded credits (4 discrete + 4 stats), no calc, no lin-alg.

### Updated external/math picture for the foundation
Foundation math/stats = 8 one-credit embedded courses (MATH-101..104 discrete + STAT-101..104 non-calculus stats). 
NOT in foundation: calculus (year 3), linear algebra (year 3), calculus-based stats (year 3+).
This is CLEAN and final for the 2-year core. The earlier "9 externals, doesn't fit 8 slots" tension is GONE - it's 8 externals, one per block, exactly.

### Credit picture now
Core = 22 CS + 8 external = 30 credits. This REPLACES:
- 23 cr sub-500 CIS (all of it - architecture/logic absorbed, ethics embedded, C++ still a question)
- 6 cr of K-State math block (MATH 510 Discrete 3 + STAT 510 Stats 3) that our embedded sequences replace
So core replaces ~29 K-State credits (23 CIS + 6 math) with 30 of ours. Much closer to even now (was 22-vs-23 CS-only; now 30-vs-29 including the math reconciliation). The credit picture is nearly balanced - GOOD. The earlier "30 vs 26 over budget" worry dissolves because the 8 external credits aren't ADDITIONAL - they REPLACE K-State's existing MATH 510 + STAT 510 (6 cr) plus absorb distributed math need. Net new burden is minimal.

### Remaining open from K-State analysis
- C/C++ (CIS 308, 1cr): still open - does the program need language-specific C/C++ exposure? Only remaining true gap.
- Ethics (CIS 415): embedded vs standalone - philosophy choice, still worth explicit confirmation (user implied absorption by saying "as with 301" for architecture, but ethics wasn't explicitly confirmed - though the trajectory suggests embedded is accepted).
- 500-level upward overlap (CIS 560 databases, CIS 575 algorithms): do students place out or take both? Affects total.
- Calc 2 requirement: downstream, not core.
- ECE 241 (Intro to Computer Engineering, stays): unaffected.

### Files to update
- content.js: DONE (stack/heap, cache)
- K-State analysis file: update to show architecture/logic/discrete-stats RESOLVED; remaining opens = C++, ethics-confirmation, 500-overlap. Add the non-calculus-stats + lin-alg-to-year-3 + calc-to-year-3 resolutions.
- Thread files: CS-103 stack/heap touches Computational Models (memory model) + the B8 cache touches Algorithmic/Computational Models performance. Minor - could note in those threads. Low priority.
- Overview: external picture now firmly 8 (4+4), lin-alg/calc explicitly year-3. Minor update to open questions (#6 lin-alg resolved, #1 budget eased).

## ROUND 41: 500-level overlap, language certificates, ethics

ANSWERS:
1. CIS 560 (Databases): NARROWS scope - spirals deeper on relational databases + relational algebra; LIKELY becomes an ELECTIVE. So our core's database coverage (B5 SQL+Design) becomes the FOUNDATION, and CIS 560 becomes an optional deeper dive (relational algebra, advanced relational theory). Not required, not placed-out-of - it becomes an elective building on our core. Clean relationship: core = foundational databases; 560 = elective depth.
2. CIS 575 (Algorithm Analysis): LIKELY similar - narrows/becomes elective. Our core's algorithmic coverage (B4 complexity, B7 graph algorithms) = foundation; 575 = optional deeper algorithm analysis. Same pattern.
3. LANGUAGE CERTIFICATES (new idea): outside the core, teach a SPECIFIC language deeply, ~1 credit each. This is the answer to the C/C++ gap (CIS 308)! Instead of forcing C/C++ into the language-agnostic core, offer language certificates (C, C++, Python, etc.) as separate 1-credit modules. Students/programs needing specific languages take the cert. CompE-adjacent or systems students take C/C++ cert. ELEGANT - keeps core language-agnostic AND serves specific-language needs.
4. ETHICS: MAYBE keep standalone ethics at year 3, BUT ethics faculty retiring - uncertain. So: core has embedded ethics (Trustworthy Computing lens + B6); a standalone year-3 ethics course is possible but at risk. Plan for embedded-as-primary, standalone-as-uncertain-supplement.

### The emerging pattern: core as FOUNDATION, upper-division as ELECTIVE DEPTH
560 and 575 both narrowing to electives reveals the structural relationship: our 2-year core establishes FOUNDATIONAL competency across many areas (databases, algorithms, etc.); the former-required 500-levels become ELECTIVE deeper spirals on specific areas. This is exactly the spiral philosophy extended UP: the core spirals broadly, electives spiral DEEPER on chosen topics. 
- Core: relational databases foundation (B5) -> Elective CIS 560: relational algebra + advanced relational theory (deeper spiral)
- Core: algorithmic complexity + graph algorithms (B4/B7) -> Elective CIS 575: deeper algorithm analysis (deeper spiral)
This is COHERENT and good - it means the core doesn't make 560/575 redundant, it makes them OPTIONAL DEPTH. Students who want database/algorithm specialization take the deeper elective; others get solid foundations from the core. The spiral metaphor now spans the WHOLE degree: broad foundation (years 1-2) -> chosen depth (years 3-4 electives + specialization).

### LANGUAGE CERTIFICATES - design implications
- ~1 credit each, outside the core, teach a specific language deeply.
- WHY this works with our design: our core teaches CONCEPTS/PARADIGMS (imperative, functional, declarative...) language-agnostically. A student who's learned the concepts can then learn a SPECIFIC language deeply via a cert - the cert is "apply what you know in language X with X's idioms/ecosystem/tooling." 
- Candidates: C, C++, Python, JavaScript, Rust, Java, SQL(? - though SQL is in core), etc.
- Serves: C/C++ gap (CIS 308 replacement), specific-language job-readiness, CompE/systems needs (C/C++), data science (Python), web (JS).
- Relationship to core: core gives paradigm fluency + reading ability (Code Comprehension thread - reading unfamiliar code in any language); certs give deep single-language fluency. Complementary.
- These are NOT service courses per se - they're optional add-ons for our own students AND potentially service offerings (a CompE student takes the C cert). Could be Type-2-ish (curated) or standalone modules.
- Are they part of the 120-cr degree (electives) or truly outside (micro-credentials)? "Certificate" suggests possibly stackable micro-credentials, maybe even non-credit or unrestricted-elective credit. Flag - need to know if they count toward the degree or are supplementary.

### C/C++ gap RESOLVED
CIS 308 C/C++ Lab -> replaced by a C and/or C++ language certificate. The core stays language-agnostic; students needing C/C++ take the cert. Gap closes cleanly without compromising the core's paradigm-focus.

### Updated K-State reconciliation status
- Discrete/stats: core replaces MATH 510/STAT 510. DONE.
- Architecture (450): absorbed (stack/heap, cache). DONE.
- Logic (301): absorbed. DONE.
- C/C++ (308): language certificate. RESOLVED.
- Databases (560): narrows to elective. RESOLVED (core = foundation, 560 = elective depth).
- Algorithms (575): likely narrows to elective. RESOLVED (same pattern).
- Ethics (415): embedded primary + uncertain standalone year-3 (faculty retiring). SOFT-RESOLVED (embedded is the plan; standalone is bonus-if-available).
- Calculus: year 3. Lin-alg: year 3. DONE.
So ALL sub-500 CIS replacement questions are now resolved or soft-resolved. The core cleanly replaces sub-500 CIS, with: architecture/logic absorbed, ethics embedded, C/C++ to certificates, and the former-500-level databases/algorithms becoming electives that the core feeds.

### Questions for user
1. Language certificates: do they count toward the 120-cr degree (as electives/unrestricted), or are they supplementary micro-credentials outside the degree credit? 
2. Confirm the "core = foundation, former-required-500s = elective depth" relationship for 560/575 - and are there OTHER currently-required 500-levels that should similarly become electives now the core covers their foundations (e.g. CIS 501 Software Arch - our core has Boundaries/design/HCI; CIS 505 Prog Languages - our core has Computational Models/paradigms)?
3. Should I update the K-State analysis file to reflect all these resolutions (most gaps now closed)?

## ROUND 42: Cybersecurity degree - shaping the specialization approach

K-State BS Cybersecurity (Fall 2026), 120 hrs. Cybersecurity Requirements = 56 credits (vs CS's 41). 

### The crucial observation: SAME foundation as CS
The cyber degree's first chunk is IDENTICAL to the CS sub-500 CIS block:
- CIS 115 (2), 116 (1), 200 (4), 300 (3), 301 (3), 308 (1, here "C Language Lab"), 400 (3), 415 (3), 450 (3) = same 23 cr sub-500 CIS foundation
Then it SHARES several 500-levels with CS:
- CIS 501 (3), 505 (3), 560 (3), 575 (3) - same as CS
Then ADDS security-specific + extra:
- CIS 525 Network Programming (3)
- CIS 551 Fundamentals of Computer and Information Security (3)
- CIS 553 Fundamentals of Cryptography (3)
- CIS 599 Cybersecurity Project (capstone) (3)
- CRIM 550 Cybercrime, Security, and Society (3) [also satisfies a core req]
- ECE 241 (3)
- SOCIO 211 Intro Sociology (3) [core req]
- Restricted elective: CIS 655 Security/Reliability OR CIS 755 Systems Security (3)

So the cyber degree = [SAME 2-year foundation as CS] + [shared 500 core: 501/505/560/575] + [security specialization: 525/551/553/655-or-755/599 capstone] + [context courses: CRIM 550, SOCIO 211, ECE 241].

### THIS IS THE SPECIALIZATION MODEL, REVEALED
The original project premise: a common 2-year foundation, then specialization degrees (Cyber, Data Science, AI, Software Arch). K-State's actual cyber degree CONFIRMS the structure:
- Common foundation (years 1-2) = our two-year core (replaces the shared sub-500 CIS that BOTH CS and Cyber currently duplicate)
- Specialization (years 3-4) = security-specific courses + shared upper-division core + domain context
So our two-year core SERVES the cyber degree the SAME way it serves the CS degree - it's the COMMON foundation. The cyber degree just swaps the CS upper-division for a security upper-division. EXACTLY the project's original vision.

### What this tells us about specialization design
1. The 2-year core is genuinely COMMON - both CS and Cyber (and presumably DS, AI, SW Arch) share it. The core replaces the duplicated sub-500 CIS across ALL these degrees. HUGE win - currently every degree re-lists the same 23 sub-500 CIS credits; the core unifies them.
2. Specializations = a SHARED upper-division core (501/505/560/575 appear in both CS and Cyber) + DEGREE-SPECIFIC courses (security ones for cyber).
3. Our core's SECURITY thread (Trustworthy Computing lens + B6 Responsible Development) is the FOUNDATION that the cyber specialization builds on. The cyber degree's CIS 551 (Info Security), 553 (Crypto), 525 (Network Programming) are the DEEP SPIRAL of what our core SEEDS:
   - Core seeds: Trustworthy Computing lens (security/privacy/ethics woven), B6 dedicated security (authn/authz/threat modeling/applied crypto via modular arithmetic), least privilege, data minimization, security as attack surface (errors), trust boundaries.
   - Cyber specialization deepens: CIS 551 (full info security), CIS 553 (full cryptography - our modular-arithmetic crypto seed at B6 -> deep crypto course), CIS 525 (network security/programming), CIS 655/755 (systems security).
   - PERFECT spiral continuation: our B6 applied-crypto (grounded in MATH-103 modular arithmetic) is the SEED; CIS 553 Fundamentals of Cryptography is the DEEP DIVE. The spiral philosophy spans into the specialization.

### Mapping cyber degree to new structure
Cyber Requirements (56 cr) restructured:
- Common 2-year core (replaces CIS 115/116/200/300/301/308/400/415/450 = 23cr): our core (~22 CS + relevant)
  * Note 308 here is "C Language Lab" -> our C language CERTIFICATE (micro-credential) - cyber students likely need C (systems security). 
  * 415 ethics -> embedded (Trustworthy Computing) + maybe standalone
  * 450 architecture -> absorbed
  * 301 logic -> absorbed
- Shared upper-division (501/505/560/575): becomes electives/required-depth per the CS analysis (TBD, ABET)
- Security specialization (525/551/553/655-or-755): the cyber-specific upper division - these are NEW relative to our core, they're the SPECIALIZATION proper
- Capstone CIS 599 Cybersecurity Project
- Context: CRIM 550, SOCIO 211 (social science core), ECE 241

### Key design questions this raises
1. Does our 2-year core REPLACE the shared sub-500 CIS in the CYBER degree too (not just CS)? Almost certainly YES - that's the whole "common foundation" premise. Confirm.
2. The security specialization (525/551/553/655/755): how does it relate to our core's security thread? Our core SEEDS security comprehensively (it's a whole lens + a dedicated B6 block). Does that mean cyber students arrive at CIS 551/553 BETTER PREPARED (the core's security foundation), allowing those courses to go DEEPER? Likely yes - the core raises the security floor for cyber students. Worth articulating: the core's security emphasis is PARTICULARLY valuable for the cyber pipeline.
3. Does the strong security thread in our CORE mean some cyber-specialization content could move EARLIER (into the core) or that the specialization can assume more? E.g. our B6 already does authn/authz/threat-modeling/applied-crypto - does CIS 551 Fundamentals of Computer and Information Security now START from a higher baseline?
4. Cyber has 56 cr requirements vs CS's 41 - cyber is a "fuller" major (more required, fewer free electives). The common core (same for both) + bigger specialization stack for cyber. Confirm the core is identical across both and the difference is purely upper-division.
5. SPECIALIZATION MODEL GENERALIZATION: if Cyber = core + security upper-division, then DS = core + data upper-division, AI = core + AI upper-division, SW Arch = core + architecture upper-division. Each specialization = SAME core + a distinct upper-division stack (+ shared upper-division core like 501/505/560/575?). This is the model to formalize. The core's THREADS pre-position students for each: Trustworthy Computing -> Cyber; Data Structures + stats + data viz -> DS; Computational Models + AI-assisted + optimization -> AI; Boundaries & Contracts + Sociotechnical + HCI -> SW Arch. Our core's threads are SPECIALIZATION ON-RAMPS.

### The beautiful structural result
Our 13 threads aren't just pedagogy - they're SPECIALIZATION PIPELINES. Each thread, spiraled through the 2-year core, pre-positions students for a specialization:
- Trustworthy Computing lens + B6 -> Cybersecurity specialization (CIS 551/553/525/655/755)
- Data Structures + Human-Centered (data viz) + STAT sequence + Optimization -> Data Science specialization
- Computational Models + AI-Assisted Development + Optimization + (year-3 calc/lin-alg) -> AI Systems specialization
- Boundaries & Contracts + Sociotechnical + APIs + Correctness -> Software Architecture specialization
This is worth making EXPLICIT in the specialization model: the common core's threads are deliberately the seeds of the four specializations. A student leans toward a specialization by which threads resonated.

### Deliverable
A specialization-model analysis (markdown), using Cyber as the worked example, that:
- Shows the common-core-replaces-shared-foundation structure
- Maps cyber's security courses to the core's security thread (seed -> deep spiral)
- Generalizes the model to all 4 specializations (threads as on-ramps)
- Flags the shared-upper-division question (501/505/560/575) pending the ABET 500-level analysis
- Asks the open questions above

## ROUND 43: Specialization model decisions + build file

DECISIONS:
1. Core is IDENTICAL across all 5 degrees (CS + 4 specializations). Only upper division differs. CONSEQUENCE: students defer specialization choice to year 3 penalty-free; free transfer between specializations; ONE foundation maintained, not five. Major institutional win + matches CBE/flexibility goals.
2. "Threads as specialization on-ramps" = FORMAL design principle. Each of the 13 threads deliberately pre-positions students for specialization(s).
3. Per-security-course baseline analysis (551/553/525 - what the core now lets them assume): worth doing, included as a worked sub-analysis in the cyber file.

### Threads -> specialization on-ramp mapping (formalized)
CYBERSECURITY: Trustworthy Computing (lens, primary), B6 Responsible Development, Correctness & Verification (secure code), Boundaries & Contracts (trust boundaries), Computational Models (attack surface/error handling), APIs & Networked (network security base).
DATA SCIENCE: Data Structures & Representation (incl. geospatial), Human-Centered (data viz throughline), STAT sequence (4 courses), Optimization Reasoning, Computational Models (dataflow/declarative-SQL), AI-Assisted (data analysis).
AI SYSTEMS: Computational Models (flagship - paradigms), AI-Assisted Development (bounded->specialization), Optimization Reasoning, Algorithmic Thinking, + year-3 calc/lin-alg prereqs, STAT sequence (probability).
SOFTWARE ARCHITECTURE: Boundaries & Contracts (meta-thread, primary), Sociotechnical Structure, APIs & Networked Systems, Correctness & Verification, Human-Centered Computing (UX/requirements), Code Comprehension.
Note: threads serve MULTIPLE specializations (Optimization -> DS+AI; Computational Models -> AI+DS+Cyber). The core is genuinely common; specialization is about which DEEPEN, not which were taught.

### Per-security-course baseline analysis (what the core lets cyber upper-division assume)
- CIS 551 Fundamentals of Computer and Information Security: core B6 already does authn/authz, threat modeling, least privilege, trust boundaries. 551 can now ASSUME these basics and go deeper (security architecture, defense-in-depth, advanced threat models) rather than re-teaching fundamentals. Core RAISES the floor.
- CIS 553 Fundamentals of Cryptography: core B6 does applied crypto grounded in MATH-103 modular arithmetic (conceptual public-key). 553 can assume the conceptual base + modular arithmetic and go to real cryptographic rigor (formal schemes, protocols, attacks). The MATH-103->B6->553 chain is a clean 3-stage spiral.
  * BUT: 553 likely needs MORE number theory than MATH-103 provides (modular arithmetic is a start; full crypto needs more). Year-3 math (the MATH 506 Number Theory elective option!) could feed 553. Note the math dependency.
- CIS 525 Network Programming: core APIs & Networked Systems (consume->build->integrate->operate) + the (deferred) OSI networking unit. 525 can assume networked-systems fluency + OSI theory and focus on the SECURITY/programming of networks. Core + OSI unit = strong base.
- CIS 655/755 Systems Security: assumes the above + systems knowledge (the absorbed architecture - stack/heap/memory). Core's programming-centric architecture (CS-103 stack/heap, B8 memory hierarchy) gives a base.

### Specialization model - the general structure
EVERY degree = [Common 2-year core: 30cr, identical] + [Shared upper-division core: 501/505/560/575-ish, TBD by ABET analysis] + [Specialization stack: degree-specific courses] + [Capstone: degree-specific] + [Context/gen-ed courses].
Specializations differ ONLY in the specialization stack + capstone + some context. The core and (likely) shared upper-division are common.

### Open questions
1. Shared upper-division (501/505/560/575): are these common across ALL specializations or do some specializations drop some? (Cyber HAS all four; does DS? does AI?) - pending per-specialization + ABET analysis.
2. The C Language Lab (CIS 308) in cyber is "C Language Laboratory" specifically (CS version was "C/C++") - cyber needs C (systems/security). The language CERTIFICATE model serves this - cyber students take the C certificate. Confirm certs satisfy this for cyber.
3. Per-security-course redesign (551/553/525 starting higher): worth a deeper future pass with the security faculty; flagged.
4. Number theory for crypto: CIS 553 may need more number theory than MATH-103 modular arithmetic. The year-3 MATH 506 Number Theory option could feed it. Flag the math dependency.

### Deliverable: specialization-model.md
- The common-core + specialization-stack structure (general)
- Cyber as worked example (course-by-course: core-replaces-foundation, security-stack-is-specialization, seed->deep-spiral)
- "Threads as on-ramps" formalized with the 4-specialization mapping
- Per-security-course baseline analysis (what the core raises)
- Open questions (shared upper-division/ABET, number theory for crypto, certs for C)

## ROUND 44: AI & Data Science specialization recommendation files

NOTE: AI and Data Science specialization DEGREES DON'T EXIST YET at K-State. Task: create recommendation .md for EACH, from the shared core + AVAILABLE courses. Advanced-search URL robots-blocked; used catalog content pages + web search.

### REAL K-State CIS courses found (relevant to AI/DS)
UNDERGRAD-accessible (from earlier search):
- CIS 530 Introduction to Artificial Intelligence (undergrad intro AI)
- CIS 560 Database System Concepts (3)
- CIS 575 Introduction to Algorithm Analysis (3)
GRADUATE (700/800 - some cross-listed/accessible to advanced undergrads or accelerated BS/MS):
- CIS 730 Principles of Artificial Intelligence (3) [grad version of 530]
- CIS 732 Machine Learning and Pattern Recognition (3) [prereq for many]
- CIS 831 Deep Learning (3) [prereq CIS 732]
- CIS 833 Information Retrieval and Text Mining (3) [prereq 732]
- CIS 834 Machine Learning for Bioinformatics (3) [prereq 732/734]
- CIS 832 Knowledge Representation for Semantic Web (3) [prereq CIS 300]
- CIS 835 Neuro-Symbolic AI (3)
- CIS 836 Knowledge Graphs (3)
- CIS 761 Database Management Systems (3) [prereq 560]
- CIS 764 Database Design (3) [prereq 501]
- CIS 860 Advanced Database Systems (incl data mining/warehousing) (3)
- CIS 861 Data Science in Practice (3)
- CIS 864 Data Engineering (3) [prereq 761/764]
- CIS 810 Logic Programming (3)
- CIS 770 Formal Language Theory (3)
- CIS 775 Analysis of Algorithms (3)
K-State has a Data Analytics M.S. and strong AI/data-mining/KDD research group (Hsu et al).
NOTE: K-State undergrad AI/data offerings are THIN at the 500-level (mainly CIS 530); depth is at grad level (730/732/831...). An undergrad specialization would lean on 500-level + accessible grad courses (accelerated BS/MS path exists) + likely NEW 500-level courses the dept would create.

### KEY HONEST CONSTRAINT
These degrees DON'T EXIST. The recommendation must:
- Build on the shared 2-year core (the on-ramp threads)
- Use AVAILABLE real courses where they exist (530, 560, 575, and grad 730/732/831/861/864 etc via accelerated/cross-listing)
- HONESTLY FLAG where K-State lacks undergrad-level courses and would need to CREATE them (e.g. undergrad ML, undergrad data science practicum) - the 500-level undergrad AI/DS offering is thin
- Map the year-3 math (calc, lin-alg) that AI especially needs
- Reference the specialization model (core + shared upper-division + specialization stack + capstone)

### AI SYSTEMS specialization - recommended structure
On-ramp threads (from core): Computational Models (flagship), AI-Assisted Development (bounded->deepens here), Optimization Reasoning, Algorithmic Thinking, STAT sequence (probability).
Year-3 prereqs: Calculus (I, maybe II), Linear Algebra (both pushed to year 3 - AI NEEDS these: gradients, vectors/matrices), calculus-based probability/statistics.
Specialization stack (from available + to-create):
- CIS 530 Introduction to AI (exists, undergrad) - foundational
- CIS 732 Machine Learning (grad, accessible via accelerated; or create undergrad 5xx ML) - CORE of AI
- CIS 831 Deep Learning (grad; prereq 732)
- Electives from: 833 IR/Text Mining, 835 Neuro-Symbolic, 836 Knowledge Graphs, 810 Logic Programming (connects to core's logic/constraint see-and-explore!)
- Capstone: AI project
GAPS to flag: undergrad-level ML course likely needs creating (732 is grad); the math sequence (calc+linalg+prob) must be solidly in place by year 3; agentic AI (the core's AI-Assisted bounded practice points to a year 3-4 Agentic AI specialization - mentioned in core design) - is there a course? Likely NEW.

### DATA SCIENCE specialization - recommended structure
On-ramp threads (from core): Data Structures & Representation (incl geospatial), Human-Centered Computing (data viz throughline), STAT sequence (all 4: descriptive/probability/distributions/regression), Optimization Reasoning, Computational Models (declarative SQL, dataflow), AI-Assisted (data analysis at B8/CS-210).
Year-3 prereqs: Linear algebra (for ML/dimensionality), calculus-based stats, more statistics (STAT 511 Prob & Stats II option exists).
Specialization stack (from available + to-create):
- CIS 560 Database System Concepts (exists) - foundation already in core (B5), 560 = depth
- CIS 732 Machine Learning (grad/accessible) - shared with AI
- CIS 861 Data Science in Practice (grad) - capstone-like practicum
- CIS 864 Data Engineering (grad; prereq 761/764) - pipelines/scale
- CIS 833 Information Retrieval & Text Mining (grad)
- CIS 860 Advanced DB (data mining/warehousing/OLAP)
- Stats dept courses (STAT 511+, regression, etc.) - data science is stats-heavy
- Capstone: Data science practicum (CIS 861-style)
GAPS to flag: undergrad-level data science courses thin (861/864 are grad); heavy reliance on STAT dept (cross-dept coordination needed); data viz - core has the throughline but a dedicated viz course may be wanted; the CORE's data-science on-ramp is STRONG (data structures + 4 stats + viz + dataflow + SQL) so DS students are well-prepared by the core - emphasize this.

### Both files should note
- These are RECOMMENDATIONS for degrees that don't exist - proposals, not mappings of existing degrees.
- The core does heavy lifting (on-ramp threads pre-position students).
- K-State's real course depth is at GRADUATE level; undergrad specialization needs either accelerated-BS/MS access, cross-listed 5xx versions, or NEW 500-level courses.
- Shared upper-division (501/505/560/575) + ABET still pending.
- Math (calc/linalg year 3) is a hard prereq for AI especially.
- Cross-dept (STAT, MATH) coordination essential, esp for DS.

## ROUND 45: ABET data science requirements -> Data Science specialization

ABET DS requirements: >=45 SCH of data science coursework covering:
LIFECYCLE: data acquisition/representativeness, data management, data prep/integration, data analysis, model dev/deployment, visualization & communication
SPANNING CONCEPTS: data ethics (legit use, algorithmic fairness), governance (privacy/security/stewardship), applied stats/math (inference, modeling, linear algebra, probability, optimization), computing (data structures & algorithms)
+ advanced DS coursework (depth)
+ >=1 application area (context)
+ major project (integration capstone)

### Map ABET DS requirements against what we have (core + proposed specialization)
LIFECYCLE:
- Data acquisition/representativeness: core touches (CS-104 data transformation, B2; API data B4; data investigation B5). Representativeness/sampling -> STAT-103 (sampling). PARTIAL in core; representativeness bias is a DS-specific concept needing explicit coverage. Flag.
- Data management: core B5 (databases SQL+design), CIS 560 depth, CIS 864 data engineering. COVERED well.
- Data prep/integration: core CS-104 (transformation), CS-207 (data integration B7). COVERED.
- Data analysis: core CS-210 (notebook analysis B8), STAT sequence. COVERED.
- Model dev/deployment: ML course (732/new) + deployment (core B8 CS-208 deployment!). Model DEPLOYMENT interestingly maps to core's B8 operations. COVERED via specialization ML + core deployment.
- Visualization & communication: core Human-Centered Computing viz throughline + Professional Practices communication. COVERED (a real core strength). Maybe dedicated viz course for depth.
SPANNING CONCEPTS:
- Data ethics (legit use, algorithmic fairness): core Trustworthy Computing lens + CS-210 Responsible AI (data ethics, honest viz). ALGORITHMIC FAIRNESS specifically - core touches responsible AI but algorithmic fairness as a named topic may need explicit specialization coverage. Mostly covered, fairness needs naming. Flag.
- Governance (privacy/security/stewardship): core Trustworthy Computing (privacy, security, data minimization), B5 access control. Data STEWARDSHIP (lifecycle data governance) less explicit. Mostly covered; stewardship flag.
- Applied stats/math (inference, modeling, lin alg, probability, optimization): 
  * Inference: STAT sequence + year-3 calc-based stats. Core stats is DESCRIPTIVE/non-calc; INFERENCE (hypothesis testing, confidence intervals) needs the year-3 calc-based stats. Flag - inference is year-3.
  * Modeling: ML course + regression (STAT-104). COVERED.
  * Linear algebra: YEAR 3 (deferred). COVERED at year 3.
  * Probability: STAT-102 (core, non-calc) + year-3 calc-based. COVERED (conceptual core + year-3 rigor).
  * Optimization: Optimization Reasoning lens + year-3. COVERED (lens seeds, specialization deepens).
- Computing (data structures & algorithms): core Data Structures thread + Algorithmic Thinking thread. COVERED STRONGLY (this is our home turf).
ADVANCED DS COURSEWORK (depth): specialization stack (732, 861, 864, 860, 833). COVERED (pending undergrad-level availability).
APPLICATION AREA (context): NEW requirement - DS must be applied to a domain (e.g. bioinformatics, business, geospatial!). Our GEOSPATIAL content + the service-dept relationships (geography/GIS) could provide application context. Also CIS 834 (bioinformatics ML). Need a named application area. Flag - decide application area(s).
MAJOR PROJECT (integration capstone): CIS 861 Data Science in Practice OR a new capstone. COVERED via capstone.

### The 45-SCH floor - big implication
ABET requires >=45 SCH of DATA SCIENCE coursework. How does our structure stack up?
- Core contributes DS-relevant credits: stats (4) + data structures-ish (CS-109/110/112 ~3) + databases (CS-201/202 ~2) + data transformation/integration (CS-104, CS-207 ~2) + viz (embedded) + CS-210 analysis (1) + ... maybe ~12-15 core credits are "data science coursework" by ABET's definition.
- Specialization stack: ML, data eng, advanced DB, practicum, viz, stats-dept courses... ~15-21 credits.
- Year-3 math (lin alg, calc-based stats/prob, optimization): counts toward "applied stats/math" - ~9-12 credits.
- Total DS-relevant: ~12-15 (core) + ~15-21 (spec) + ~9-12 (math) = ~36-48. POSSIBLY meets 45 but TIGHT. Need careful accounting - the 45 SCH is a real constraint that shapes how many specialization + math credits are required.
- KEY: ABET counts "data science coursework" - does our CORE count fully? The core is general CS+foundations; ABET DS wants DS-specific. Some core (stats, data structures, databases, data transformation) clearly counts; some (B1 imperative/functional, B6 security, B3 OOP) is general CS that may NOT count as "data science coursework." So the EFFECTIVE core contribution to the 45 might be LESS than total core credits. This TIGHTENS the requirement - the specialization + math must carry more of the 45. Flag clearly.

### This is actually a GOOD fit overall
ABET DS criteria map remarkably well onto the core's data-science on-ramp (data structures, stats, viz, databases, dataflow, analysis) + the proposed specialization. The lifecycle and spanning-concepts are nearly all present. Real gaps to flag:
1. Representativeness/sampling bias (DS-specific) - needs explicit coverage
2. Algorithmic fairness (named topic) - needs explicit coverage in specialization
3. Data stewardship/governance lifecycle - partially covered, needs strengthening
4. Statistical INFERENCE - is year-3 (calc-based stats), confirm sequencing
5. Application area - must NAME one+ (geospatial via geography? bioinformatics via 834? business?)
6. 45 SCH floor - careful credit accounting; core may not all count as "DS coursework"; specialization+math must be sized to clear 45

### Update the DS recommendation file with an ABET section
Add: a dedicated ABET-mapping section showing lifecycle + spanning concepts against core+specialization, the 45-SCH accounting note, the named gaps (representativeness, fairness, stewardship, inference-sequencing, application-area), and application-area options.

## ROUND 46: ABET AI criteria -> AI Systems specialization

ABET AI (proposed): >=42 SCH AI coursework covering:
FUNDAMENTAL AI: AI foundations (reasoning, heuristic search, knowledge representation); programming/data structures/algorithms; data & knowledge engineering; machine learning incl deep learning; design & implementation of AI solutions; AI system architecture & infrastructure; ethics & responsible AI
+ advanced AI topics (depth)
+ >=1 application area using AI
+ major project (integration)
SEPARATE: >=9 SCH math/stats: statistical inference & modeling, linear algebra, probability, data visualization, optimization

### Map against core + proposed AI specialization
FUNDAMENTAL AI:
- AI foundations (reasoning, heuristic search, knowledge representation): 
  * Heuristic search: A* is in core B7 (geospatial routing/graph algorithms)! Heuristic search literally present. 
  * Reasoning/knowledge representation: core's logic/constraint see-and-explore (B7) seeds this; CIS 530/730 (AI), 832 (KR for semantic web), 835/836 (knowledge graphs, neuro-symbolic) deepen. Core SEEDS, specialization deepens. COVERED via 530 + KR electives. Note: symbolic AI is well-served by K-State (832/835/836 knowledge graphs/neuro-symbolic) - a strength.
- Programming/data structures/algorithms: core Data Structures + Algorithmic threads. COVERED STRONGLY (home turf).
- Data & knowledge engineering: CIS 864 data engineering, 832/836 knowledge graphs. COVERED via specialization.
- ML incl deep learning: CIS 732 ML + 831 Deep Learning. COVERED (pending undergrad-level; 732/831 are grad).
- Design & implementation of AI solutions: specialization project courses + capstone. COVERED.
- AI system architecture & infrastructure: THIS IS A GAP. "AI system architecture and infrastructure" = MLOps, model serving, pipelines, scaling AI systems. Core B8 (deployment/operations) touches infrastructure generally; but AI-SPECIFIC infrastructure (model serving, ML pipelines, GPU/compute, vector DBs) is NOT in core or clearly in K-State's course list. Flag - likely needs a new course or explicit coverage. K-State's distributed systems (720/825) touch infra but not AI-specific.
- Ethics & responsible AI: core Trustworthy Computing lens + CS-210 Responsible AI (B8) + AI-Assisted Development bounded practice (responsible AI use is LITERALLY the through-line). COVERED STRONGLY - this is a core strength, the AI-Assisted bounded practice + Responsible AI course directly serve this.
ADVANCED AI (depth): 730, 831, 833, 834, 835, 836, 810. COVERED (grad-level, pending undergrad access).
APPLICATION AREA using AI: NEW requirement. Options: bioinformatics (834 ML for Bioinformatics!), NLP/text (833 IR/text mining), robotics (K-State has robotics research), knowledge graphs/semantic web. Need to NAME one. Flag.
MAJOR PROJECT: AI capstone (+ possibly the Agentic AI capstone idea). COVERED.

MATH/STATS (>=9 SCH separate): inference & modeling, linear algebra, probability, data viz, optimization
- Statistical inference & modeling: year-3 calc-based stats (inference); regression (STAT-104). Core stats non-calc; inference is year-3. Same as DS - inference needs year-3.
- Linear algebra: YEAR 3. COVERED.
- Probability: STAT-102 (core) + year-3. COVERED.
- Data visualization: core Human-Centered viz throughline. COVERED (interesting that AI criteria explicitly want viz - our core provides it).
- Optimization: Optimization Reasoning lens + year-3. COVERED.
- So the >=9 SCH math/stats = year-3 (calc, lin alg, calc-stats) + core stats + optimization. EASILY met by the year-3 math block + core. The 9 SCH floor is LOWER than DS's math expectation and easily cleared. GOOD.

### Two real gaps for AI (vs DS's gaps)
1. AI SYSTEM ARCHITECTURE & INFRASTRUCTURE: genuinely thin. Core B8 has general deployment/ops but not AI-specific (MLOps, model serving, ML pipelines, vector stores, GPU). K-State lacks an obvious course. NEEDS new course or explicit coverage. This is the standout AI gap.
2. APPLICATION AREA using AI: must name one (bioinformatics via 834 is the readiest, given the course exists).
Minor: AI system infra connects to core B8 + the Computational Models actor/distributed pass (B8) - some foundation exists but AI-specific layer missing.

### Comparison to DS ABET mapping
- Both need: application area (new), inference-is-year-3, ML-course-is-grad-level.
- AI-specific strength: ethics/responsible AI is a STANDOUT core strength (AI-Assisted bounded practice + Responsible AI course directly map). Symbolic AI well-served by K-State (knowledge graphs/neuro-symbolic).
- AI-specific gap: AI system architecture/infrastructure (MLOps) - the clearest new-course need.
- AI math floor (9 SCH) is EASILY met (lower bar than DS); the year-3 math block clears it.
- 42 SCH AI coursework floor: similar accounting issue as DS - core general-CS may not all count as "AI coursework"; specialization + math must carry. But AI foundations (search/reasoning/KR), data structures/algorithms (core), ethics (core) DO count, so core contributes meaningfully.

### Heuristic search nice catch
ABET wants "heuristic search" as an AI foundation - our core literally has A* in B7 (geospatial routing). So an AI foundation topic is already seeded in the COMMON core via the geospatial-algorithms addition (round 35). Nice unintended coverage.

### Update AI recommendation file with ABET section
Add ABET-mapping section: fundamental AI topics table, math/stats (9 SCH) note, the two gaps (AI infra/MLOps, application area), the heuristic-search/A* nice-catch, ethics/responsible-AI as standout strength, 42-SCH accounting note.

## ROUND 47: ABET CS criteria -> the CS degree (the deferred big analysis)

ABET CS criteria:
CS (>=40 SCH):
- Substantial coverage: algorithms & complexity, CS theory, concepts of programming languages, software development
- Substantial coverage of >=1 general-purpose programming language
- EXPOSURE to: computer architecture & organization, information management, networking & communication, operating systems, parallel & distributed computing
- Study of computing-based systems at varying levels of abstraction
- Major project (integration capstone)
MATH/STATS (>=15 SCH): discrete math, probability, statistics; rigor >= introductory calculus
SCIENCE: scientific method in a non-computing area

### This is the BINDING analysis - the required path must satisfy ALL of this on its own
Recall the scope escalation: required 500-levels (501/505/560/575) becoming electives means the REQUIRED path = core + capstone + whatever stays required. That required path must independently satisfy ABET CS. Let's check.

### SUBSTANTIAL COVERAGE requirements
- Algorithms & complexity: core Algorithmic Thinking thread (B4 complexity, B7 graph algorithms, B8 real bottleneck) + Data Structures. SUBSTANTIAL? Core gives a solid foundation but "substantial" may want more depth - CIS 575 (algorithm analysis) was the depth course, now becoming elective. QUESTION: does core algorithmic coverage alone meet "substantial," or must 575-level stay required? Likely core is substantial ENOUGH for the floor, with 575 as elective depth. Flag - needs faculty judgment on "substantial."
- CS theory: HMMMM. "Computer science theory" = formal languages, automata, computability, complexity theory. Core has: Computational Models (paradigms - not formal automata theory), Boundaries & Contracts, complexity (Big-O). But FORMAL CS THEORY (automata, computability, formal languages - CIS 570/770) is NOT really in the core. The core is PRACTICAL/applied, deliberately. CS THEORY IS A GAP. This is the biggest finding - our applied core is light on classical CS theory. Flag prominently.
- Concepts of programming languages: core Computational Models (imperative/functional/declarative/concurrent/dataflow/logic) is LITERALLY "concepts of programming languages" - paradigms, models. STRONG coverage actually. CIS 505 (prog languages) was the course; core's Computational Models thread covers the CONCEPTS well. COVERED (core strength - the flagship thread).
- Software development: core has tons - Code Comprehension, Correctness & Verification, Professional Practices, Sociotechnical, B6 Responsible Development (team project), B8 (deployment). SUBSTANTIAL. COVERED STRONGLY.
- >=1 general-purpose language substantial coverage: core is language-AGNOSTIC (paradigm-focused). The language CERTIFICATES are outside the degree. PROBLEM: ABET wants substantial coverage of >=1 general-purpose language IN the degree. Our language-agnostic core + outside-degree certs may NOT satisfy this! If certs are outside the 120 credits, they may not count for ABET. This is a REAL tension between our language-agnostic philosophy + cert model and ABET's "substantial coverage of a language" requirement. BIG FLAG. Options: (a) certs count for ABET even if outside degree credit (unlikely), (b) one language gets substantial in-core coverage (but core is deliberately multi-paradigm/agnostic), (c) a required language course in the degree. Tension with our design philosophy. MUST resolve.

### EXPOSURE requirements (lower bar than "substantial")
- Computer architecture & organization: core absorbs programming-centric architecture (stack/heap B1, cache B8). "Exposure" bar - probably MET (we have programmer-facing arch). But ABET architecture exposure might want organization (assembly, ISA, etc) we don't have. Marginal - the absorbed CIS 450 was programming-centric; ABET "exposure" likely satisfied but verify.
- Information management: core B5 (databases, SQL, schema). COVERED (exposure easily met, arguably substantial).
- Networking & communication: core APIs & Networked Systems thread + the (deferred) OSI Networking unit. Exposure MET (APIs, network boundaries); OSI unit would strengthen. COVERED.
- Operating systems: GAP? Core has B8 (deployment/operations - but that's ops not OS), concurrency (Computational Models), memory model (stack/heap). But classical OS (processes, scheduling, virtual memory, file systems) is NOT really in core. OS EXPOSURE may be thin. Flag - core has concurrency + memory + ops but not classical OS. "Exposure" bar is lower though - maybe the concurrency/memory/process touches suffice. Marginal flag.
- Parallel & distributed computing: core Computational Models (concurrent, actor model B8, distributed) + B8 fault tolerance. Exposure MET (actor model, concurrency, distributed touches). COVERED.
- Varying levels of abstraction: core is LITERALLY built on this (representation primitive->graph, boundaries/contracts meta-thread, abstraction spiral). COVERED STRONGLY (core philosophy).
- Major project: capstone + B6 team project + B8 integration project. COVERED.

### MATH/STATS (>=15 SCH, rigor >= intro calculus)
- Discrete math: core MATH-101..104 (4 cr). COVERED.
- Probability: STAT-102 + year-3. COVERED.
- Statistics: STAT-101..104 (4 cr). COVERED.
- "Rigor >= introductory calculus": HERE'S THE TENSION. We made the foundation stats NON-CALCULUS deliberately. ABET wants math/stats rigor "at least equivalent to introductory calculus." Our discrete (4) + stats (4) = 8 cr in foundation, non-calculus. Plus year-3 calculus + lin-alg. Does the 15 SCH need calculus-level rigor? 
  * The 15 SCH = discrete (4) + stats (4) + year-3 calc (4-ish) + lin-alg (3) = ~15. The CALCULUS is in year 3 - so the 15 SCH math/stats INCLUDES calculus (year 3) which provides the rigor. 
  * BUT "rigor >= introductory calculus" for the discrete/stats specifically? The non-calculus stats might not meet "calculus-level rigor" on its own. However, the requirement is for the math/stats BLOCK to have calc-level rigor, and with year-3 calculus IN the block, the block meets it. The NON-calculus foundation stats is fine AS LONG AS calculus is in the 15 SCH somewhere (year 3). So: confirm calculus (year 3) counts in the 15 SCH math/stats. Likely YES. Then satisfied. But the timing (calc in year 3) means the 15 SCH spans into year 3 - fine for a 4-year degree.
  * Flag: ensure the 15 SCH math/stats including year-3 calc meets the rigor bar; the non-calc foundation stats is acceptable within a block that also has calculus.

### SCIENCE requirement
- Scientific method in non-computing area: this is a gen-ed/science course (physics, bio, chem). NOT our concern (it's outside CS coursework) - K-State already has science requirements. NOTE only - unaffected by our redesign.

### THE THREE REAL CS-ABET GAPS (the important findings)
1. CS THEORY (automata/computability/formal languages): our applied core is LIGHT on classical CS theory. CIS 570/770 (formal language theory) exists but is the depth. Does the required path need formal CS theory? ABET "substantial coverage of CS theory" suggests YES. Our core's theory = complexity (Big-O) + computational models (paradigms) + logic/verification, but NOT automata/computability. GAP - may need a required theory course or core strengthening. PROMINENT FLAG.
2. GENERAL-PURPOSE LANGUAGE (substantial coverage IN degree): our language-agnostic core + outside-degree certs may not satisfy ABET's "substantial coverage of >=1 general-purpose language." TENSION with design philosophy. PROMINENT FLAG.
3. OPERATING SYSTEMS exposure: core has concurrency/memory/ops but not classical OS - "exposure" bar may be marginally met or may need strengthening. MODERATE FLAG.

### Lower-confidence / verify
- "Substantial" algorithms (vs 575 elective): core probably enough, verify.
- Architecture exposure (programming-centric only): likely enough for "exposure," verify.
- 15 SCH math rigor: met if year-3 calc counts in the block, verify.

### The big picture for the CS restructure
Required path = core (30) + capstone + science + remaining-required-courses. To satisfy ABET CS:
- Core covers MOST substantial+exposure requirements WELL (algorithms, prog-language-concepts, software dev, info mgmt, networking, parallel/distributed, abstraction, math/stats).
- Core GAPS for ABET: CS theory (automata/computability), general-purpose language depth, possibly OS.
- These gaps determine what 500-levels MUST stay required (vs elective):
  * CS theory gap -> maybe CIS 570/770 (formal languages) stays required OR core adds theory.
  * Language gap -> maybe a language course stays required OR certs are restructured to count OR one core course goes language-deep.
  * OS gap -> maybe an OS course required OR core strengthens.
- So the ABET analysis DIRECTLY answers "which 500-levels stay required": those covering the core's ABET gaps (theory, OS, language). Others (560 databases, 575 algorithms - core covers their floors) can become electives.

### Deliverable
Update the K-State replacement analysis file (or a new ABET-CS file) with this mapping: the substantial/exposure/math checklist, the 3 real gaps (theory, language, OS), how the gaps determine required-vs-elective 500-levels, and the math-rigor + language-philosophy tensions. This is the "largest open piece" - now addressed.

## ROUND 48: ABET Cybersecurity criteria -> Cyber specialization (and promote to its own file)

ABET Cyber: >=45 SCH computing+cyber coursework covering:
CROSSCUTTING CONCEPTS (applied throughout): confidentiality, integrity, availability, risk, adversarial thinking, systems thinking
8 FUNDAMENTAL AREAS (CSEC2017 knowledge areas): Data Security, Software Security, Component Security, Connection Security, System Security, Human Security, Organizational Security, Societal Security
+ advanced cyber topics (depth)
SEPARATE: >=6 SCH math: discrete math + statistics

### Map crosscutting concepts against core
- Confidentiality, Integrity, Availability (CIA triad): core B6 Security Fundamentals (authn/authz), Trustworthy Computing lens, B5 access control. CIA covered conceptually. COVERED.
- Risk: core has threat modeling (B6), design-under-uncertainty (B7). Risk-thinking present. COVERED (B6 threat modeling = risk).
- Adversarial thinking: core B6 (threat identification, errors-as-attack-surface), security mindset. COVERED - B6 explicitly does adversarial/threat thinking.
- Systems thinking: core is BUILT on systems thinking (Sociotechnical, Boundaries & Contracts, "structure across scales" B4). STANDOUT - systems thinking is a core ethos, not just a topic. COVERED STRONGLY.
So crosscutting concepts map well - the core's security thread + systems-thinking ethos cover them. These are applied THROUGHOUT (like the core's lens approach) - philosophically aligned.

### Map 8 fundamental areas
- Data Security (at rest/processing/in transit): core B5 (data at rest - DB security, access control), B6 (applied crypto - in transit/processing), data minimization. COVERED across core + cyber spec (CIS 553 crypto deepens).
- Software Security (secure software dev): core B6 Responsible Development (secure coding), Correctness & Verification, CS-204 Security Fundamentals. COVERED + CIS 551 deepens.
- Component Security (design/procure/test/analyze/maintain components): core Boundaries & Contracts (component interfaces), testing. PARTIAL - "component security" specifically (supply chain, component analysis) is more specialized. Core touches via boundaries/testing; cyber spec deepens. Flag - component security as a NAMED area may need explicit coverage.
- Connection Security (connections between components, physical+logical): core APIs & Networked Systems (network boundaries, trust boundaries B6) + OSI unit (deferred). CIS 525 Network Programming deepens. COVERED via core networking + cyber spec.
- System Security (systems of components+connections): core B8 (systems in production, hardening), Sociotechnical (systems), CIS 655/755 Systems Security. COVERED + spec deepens.
- Human Security (human behavior re: data protection, privacy, threat mitigation): core Human-Centered Computing (human-centered) + Trustworthy Computing (privacy). PARTIAL - "human security" in cyber = social engineering, usable security, human factors in security. Core has HCI + privacy but not security-specific human factors. Flag - human security needs explicit cyber coverage. CRIM 550 (cybercrime/society) touches.
- Organizational Security (protecting orgs, risk mgmt, mission): core Sociotechnical (orgs) but org-security-specific (governance, risk mgmt, policy) is specialized. PARTIAL/GAP - organizational security (governance, compliance, risk management) is a cyber-specialization topic not in core. CRIM 550 + cyber courses. Flag.
- Societal Security (broad societal impact): core Trustworthy Computing (ethics, societal), CRIM 550 Cybercrime Security & Society (literally this!), SOCIO 211. COVERED via core ethics + CRIM 550.

### The 8 areas - summary
Core + cyber spec (CIS 525/551/553/655/755) + context (CRIM 550, SOCIO 211) cover MOST areas. The cyber degree's existing structure (which we mapped round 42) ALREADY has the context courses (CRIM 550 cybercrime/society, SOCIO 211) that serve Human/Organizational/Societal security - the "softer" security areas. Real gaps/flags:
- Component Security (named area) - supply chain, component analysis - may need explicit coverage
- Human Security (security-specific human factors, social engineering, usable security) - core HCI + privacy partial; needs cyber-specific
- Organizational Security (governance, risk mgmt, compliance) - partial; CRIM 550 + needs cyber-specific
These 3 "softer"/named areas are where pure-CS cores typically underserve cyber - our core is no exception, but the cyber DEGREE's context courses (CRIM 550, SOCIO 211) + specialization courses help. Flag that the cyber specialization must explicitly cover Component/Human/Organizational security.

### MATH (>=6 SCH: discrete + statistics)
- Discrete math: core MATH-101..104 (4). COVERED.
- Statistics: core STAT-101..104 (4). COVERED.
- 6 SCH easily met by core's 8 embedded math/stats. EASILY CLEARED (lowest math bar of all 4 ABET criteria - cyber needs least math).
- Note: cyber's crypto (CIS 553) needs number theory (flagged round 42-43) - but that's beyond the ABET 6 SCH minimum; it's a specialization prereq (year-3 MATH 506).

### 45 SCH cyber+computing coursework
- Core contributes heavily (it's computing coursework + strong security thread): much of the core counts as "computing and cybersecurity coursework" since ABET cyber allows COMPUTING + cyber (broader than DS's "data science coursework" or AI's "AI coursework"). So the core counts MORE generously here - "computing and cybersecurity" is broad. 45 SCH likely easier to clear than DS's 45 or AI's 42, because more of the core qualifies.
- Core (30, much counts as computing) + cyber spec (525/551/553/655 ~12) + context. Clears 45 comfortably.

### Cyber is the BEST-FIT specialization for ABET
- Crosscutting concepts (CIA, risk, adversarial, systems thinking) - core security thread + systems-thinking ethos cover well; SYSTEMS THINKING is a standout (core ethos).
- Most of 8 areas covered (Data/Software/Connection/System/Societal strong; Component/Human/Organizational need explicit spec coverage).
- Math bar lowest (6 SCH, easily met).
- 45 SCH easiest to clear (computing+cyber is broad).
- The core's SECURITY EMPHASIS (Trustworthy Computing lens + dedicated B6) was always the strongest specialization on-ramp - confirmed by ABET fit.

### Promote cyber to its own recommendation file (like AI/DS)
Currently cyber is only the worked example INSIDE specialization-model.md. Create specialization-cybersecurity-recommendation.md matching the AI/DS file structure: premise, on-ramps, specialization stack (from the REAL cyber degree courses 525/551/553/655/755 + capstone 599), ABET mapping (crosscutting + 8 areas + math), gaps (component/human/org security, number theory for crypto), bottom line. This makes the 3 specialization rec files parallel (AI, DS, Cyber) + the general model file.

## ROUND 49: Surface OS grounding (processes/threads) + memory-hierarchy reality (page thrashing)

Two related gaps where the core teaches concepts that SECRETLY depend on OS/systems mechanism:
1. CONCURRENT computational models (threads/green threads/actors) REQUIRE OS process/thread grounding - otherwise the distinctions are meaningless. Currently B8 names actor model + concurrency but assumes no process/thread foundation.
2. PAGE THRASHING / memory hierarchy can TRUMP Big-O in practice - real systems constraint. Currently B8 has cache misses (round 39) but page thrashing/virtual memory is deeper and can invert algorithmic predictions.

Both connect to the ABET OS-exposure gap (round 47). Surfacing these may convert OS from "marginal" to "covered."

### Issue 1: Concurrent models need OS process grounding
The Computational Models thread (B8) names: threads vs green threads vs actor model, fault-tolerance comparison. BUT:
- Threads = OS-scheduled, preemptive, kernel-level, share memory
- Green threads = runtime-scheduled, cooperative, lightweight, user-space
- Actor model = isolated state, message-passing, no shared memory
The DISTINCTIONS between these REQUIRE understanding: what an OS process is, what a thread is (vs process), kernel vs user space, preemptive vs cooperative scheduling, shared vs isolated memory. WITHOUT this grounding, "green threads vs OS threads vs actors" is just vocabulary - students can't reason about WHY you'd choose one.
So: the concurrent-models pass needs an OS-PROCESS/THREAD foundation FIRST. Where?
- The concurrency spiral: async/event-loop (B2), server concurrency conceptual (B4), transactions (B5), B8 (the big concurrent-models comparison).
- OS process/thread grounding should come BEFORE B8's model comparison. Natural spot: B8 itself (introduce process/thread/scheduling as the GROUNDING right before comparing thread/green-thread/actor models). OR earlier seed.
- Actually the memory model (stack/heap, round 39) is at B1 (CS-103). Processes/threads are a natural EXTENSION of "how programs run" - could seed at B1 (a program runs as a process; the OS schedules it) and deepen at B8 (multiple threads/processes, scheduling, the concurrent models). 
- LEAN: seed OS process/execution model at B1 (CS-103, alongside stack/heap - "a running program is a process the OS manages; it has a stack and heap") -> B8 deepens to threads/scheduling/green-threads/actors with the process foundation in place.
- This GROUNDS the concurrent computational models properly AND adds real OS exposure (processes, threads, scheduling, kernel/user space) = directly addresses ABET OS gap.

### Issue 2: Page thrashing / memory hierarchy trumping Big-O
Algorithmic Thinking thread: Big-O (B4), graph algorithms (B7), real bottleneck (B8). Round 39 added cache misses at B8. But:
- PAGE THRASHING (virtual memory, working set exceeds RAM, constant paging to disk) can make a "good Big-O" algorithm catastrophically slow - a real-world constraint that INVERTS algorithmic predictions.
- Cache misses (round 39) are one level; page thrashing (virtual memory/disk) is a deeper, more dramatic level.
- The LESSON: Big-O assumes uniform memory access; real memory hierarchy (registers->cache->RAM->disk) means CONSTANT FACTORS and ACCESS PATTERNS can dominate. A theoretically-worse algorithm with good locality can beat a theoretically-better one that thrashes.
- This is the "Big-O is necessary but not sufficient" lesson - profound for the Algorithmic thread. 
- Home: B8 (real bottleneck pass) - already has cache misses; ADD page thrashing / virtual memory as the dramatic case where systems reality trumps asymptotic analysis. The memory hierarchy (cache + virtual memory/paging) is the full picture.
- Requires: understanding virtual memory, paging, working set = OS memory management. So this ALSO needs OS grounding (virtual memory).
- LEAN: B8 Algorithmic pass explicitly contrasts asymptotic analysis vs systems reality (cache + paging/thrashing); requires the OS virtual-memory grounding (which pairs with the process grounding from issue 1).

### Both issues share a root: the core needs MORE EXPLICIT OS GROUNDING
- Processes, threads, scheduling (for concurrent models)
- Virtual memory, paging (for the memory-hierarchy/thrashing lesson)
- These are CLASSICAL OS topics. Surfacing them:
  a. GROUNDS the concurrent computational models (threads/green/actors meaningful)
  b. GROUNDS the systems-reality-trumps-Big-O lesson (thrashing)
  c. ADDRESSES the ABET OS-exposure gap (round 47) - converts "marginal" to real exposure
So this is ONE coherent addition: a thread of OS-systems grounding (process/execution model + memory management) woven where it's NEEDED (B1 seed: process + stack/heap; B8 deepen: threads/scheduling/virtual-memory/paging), serving concurrent-models + algorithmic-reality + ABET-OS simultaneously.

### Where does OS grounding live - new thread, or woven?
Option A: a new explicit "Systems & OS" thread. But we just settled at 13 threads; adding one re-opens that.
Option B: weave OS grounding into EXISTING threads as the mechanism they depend on:
  - Process/execution model -> Computational Models thread (the concurrent models need it) + the B1 memory model
  - Virtual memory/paging -> Algorithmic Thinking thread (the thrashing/reality lesson) + memory hierarchy
  - This treats OS not as a separate thread but as the MECHANISM LAYER beneath Computational Models (how computation actually runs) and Algorithmic (what really costs).
  - LEAN Option B - weave, don't add a thread. OS grounding is the "how it actually runs on real hardware/OS" layer that the Computational Models and Algorithmic threads have been IMPLICITLY assuming. Make it explicit within them. Consistent with "absorbed CIS 450 programming-centric architecture" (round 39) - OS-as-programming-concern, woven, not a hardware course.
  - Note: this stays true to the deliberate choice NOT to have a full classical-OS course (no scheduling-algorithm deep dives, no filesystem internals) - we surface the OS CONCEPTS that GROUND other learning (process/thread/scheduling-existence, virtual-memory/paging-existence), at the depth needed to make concurrent models + algorithmic reality meaningful. Programming/programmer-facing OS, not OS-implementation.

### Proposed additions (woven, programmer-facing depth)
B1 (CS-103 Computational Representation): seed the EXECUTION MODEL - a running program is a PROCESS the OS schedules; it has a stack and heap (already added round 39); single-threaded for now. Names "process," "the OS runs your program."
B8 (CS-208 Deployment & Operations / Computational Models + Algorithmic passes): 
  - Process/thread/scheduling grounding: threads vs processes (shared vs isolated memory), preemptive (OS threads) vs cooperative (green threads) scheduling, kernel vs user space - JUST ENOUGH to make threads/green-threads/actors a meaningful CHOICE (Computational Models concurrent pass).
  - Virtual memory/paging: working set, paging, thrashing - the memory hierarchy's deepest level; the case where systems reality (locality, paging) trumps Big-O (Algorithmic real-bottleneck pass).
This is programmer-facing OS grounding woven into B1 (seed) + B8 (depth), serving 3 goals at once.

### ABET OS-gap status update
Round 47 flagged OS as a moderate gap ("marginal exposure"). With explicit process/thread/scheduling + virtual-memory/paging grounding woven into B1+B8, OS EXPOSURE is now genuinely present (processes, threads, scheduling, virtual memory, paging - the core OS concepts). Likely converts the ABET OS-exposure gap from "marginal/flag" to "covered" (at exposure level - not a full OS course, but ABET asks EXPOSURE for OS, not substantial). Update the ABET-CS analysis to reflect this.

### Content/thread edits needed
- CS-103 (B1): add process/execution-model seed (a running program is a process; OS schedules it).
- CS-208 (B8): add process/thread/scheduling grounding (for concurrent models) + virtual-memory/paging/thrashing (for memory hierarchy reality).
- Computational Models thread: note OS process/thread grounding enables the concurrent-models distinctions (B8).
- Algorithmic Thinking thread: add the "systems reality (cache + paging/thrashing) trumps Big-O" lesson explicitly (B8), requiring virtual-memory grounding.
- B1, B8 block files regen.
- ABET-CS analysis: update OS-exposure from gap to covered.

### Question for user
- Confirm: weave OS grounding (process/thread/scheduling + virtual-memory/paging) into existing threads (Computational Models + Algorithmic) at programmer-facing depth, B1 seed + B8 depth - NOT a new thread, NOT a full OS course?
- Confirm this is meant to convert the ABET OS-exposure gap to covered?

## ROUND 50: Surface OS message queues + event loops + browser-as-mini-OS

User: surface OS message queues; ties into event processing loops; the browser is a 'mini-OS'.

### The unifying insight
Message queues / event loops are NOT just a B8 OS topic - the SAME mechanism already runs under the async/event-loop work at B2 (CS-106 fetch/promises). Students use the event loop in B2 without seeing it's the same message-queue/event-processing idea that the OS uses. Surfacing message queues UNIFIES:
- B2 async/event-loop (browser event loop, callback/promise queue) - already in core
- B8 concurrent models + OS grounding (message passing between processes/threads/actors)
- The ACTOR MODEL (B8) - actors communicate via message queues/mailboxes! Message queue IS the actor substrate.
- Event-driven/reactive model (Computational Models taxonomy) - event loop processing a message/event queue

So message queues are a THROUGH-LINE connecting: browser event loop (B2) -> OS message passing / IPC (B8) -> actor mailboxes (B8) -> event-driven model. It's the mechanism beneath the concurrent/reactive model family.

### Browser as 'mini-OS' - a powerful framing
The browser IS a mini-OS: it schedules tasks (event loop), manages memory (GC), isolates processes (tabs/origins = sandboxing), handles I/O (network/DOM events), runs concurrent work (web workers = threads), passes messages (postMessage between workers/frames = IPC). 
This framing is PEDAGOGICALLY GOLD because students MEET the browser early (B2 web foundations) - so the browser is a concrete, already-familiar mini-OS that introduces OS concepts (scheduling, message passing, isolation, concurrency) BEFORE the formal OS grounding at B8. The browser becomes the gentle on-ramp to OS concepts:
- B2: browser event loop = task scheduling; message/callback queue = how async work is ordered; (later) postMessage/web workers = message passing + threads.
- B8: generalize from "the browser does this" to "operating systems do this" - processes, threads, scheduling, message queues/IPC, isolation. The browser was a mini-OS all along.
This is a beautiful spiral: concrete familiar instance (browser, B2) -> general principle (OS, B8). Consistent with the whole "practice/concrete before formal/general" approach.

### Where message queues land
COMPUTATIONAL MODELS thread (the concurrent/reactive + dataflow + actor family):
- B2: event loop + message/callback queue NAMED (the browser's event loop processes a queue of events/callbacks) - already have async here, now NAME the queue mechanism + browser-as-mini-OS framing.
- B8: OS message queues / IPC as the general mechanism; actor mailboxes ARE message queues; the event-loop model generalizes. Ties the actor model (already at B8) to its message-queue substrate, and back to the B2 browser event loop.
- This makes the concurrent/reactive/actor/dataflow models COHERENT - they all rest on message-passing/event-queue mechanics, concretely met in the browser (B2), generalized at the OS level (B8).

### Browser-as-mini-OS also enriches B2 / web foundations
CS-106 Web Foundations already does HTML/CSS/accessibility/fetch/async. Adding the "browser as mini-OS" framing:
- The browser schedules your code (event loop), isolates origins (security - ties to Trustworthy Computing!), runs workers (concurrency), passes messages (postMessage).
- This makes CS-106 richer WITHOUT new heavy content - it's a FRAMING that connects web work to systems concepts. And it foreshadows B8's OS grounding.
- Light touch at B2 (name the event loop + queue, note the browser-as-mini-OS idea); deeper at B8 (generalize to OS).

### Connection to event-driven / reactive model
The Computational Models taxonomy has "concurrent/reactive (async, actor)". Message queues + event loops are the MECHANISM of the reactive/event-driven model. Surfacing them makes the reactive model concrete: "event-driven = a loop processing a queue of events." Browser (B2) and OS (B8) and actors (B8) are all instances.

### Edits
- CS-106 (B2): name the event loop + message/callback queue; introduce "browser as a mini-OS" framing (schedules, isolates, messages, concurrency via workers) - light, a framing that foreshadows B8 OS grounding and connects to security (origin isolation).
- CS-208 (B8): OS message queues / IPC as the general mechanism; actor mailboxes ARE message queues; generalize the browser event loop (B2) to OS-level message passing.
- Computational Models thread: message-queue/event-loop through-line (B2 browser event loop -> B8 OS message queues/IPC + actor mailboxes); browser-as-mini-OS as the concrete on-ramp to OS concepts.
- Possibly note in CS-106/B2 block: browser-as-mini-OS.
- Regen B2, B8 blocks + Computational Models thread.

### This strengthens the OS-exposure story further
Round 49 added process/thread/scheduling/virtual-memory grounding. Adding message queues / IPC + the browser-as-mini-OS on-ramp makes OS exposure even more solid AND better-motivated (students meet OS concepts concretely in the browser at B2, formally at B8). The ABET OS-exposure is now well-covered with a clean pedagogical arc (concrete B2 -> general B8). Message passing/IPC is a classic OS topic now explicitly present.

### Question for user
- Confirm: name event loop + message queue at B2 with the browser-as-mini-OS framing (concrete OS on-ramp), generalize to OS message queues/IPC + actor mailboxes at B8?

## ROUND 51: Hugo site structure expansion (chapters)

User wants additional top-level chapters in the Hugo site:
1. Competency-based ASSESSMENT (the assessment system wrapping the structure) - NEW chapter
2. Pedagogical & instructional APPROACH - NEW chapter
3. Individual COURSE DESIGNS - NEW chapter
4. Promote SPECIALIZATIONS to their own chapter (out of analyses)

### Reasoning about chapter ORDER (story for a faculty reader)
The site should read as a coherent argument. Proposed narrative order:
1. Core Design (the structure) - what the curriculum IS (blocks/threads/lenses). [exists]
2. Competency-Based Assessment - how we ASSESS against the structure (competencies are program-level, courses are evidence contexts; grades vs competency status parallel tracks). This WRAPS the structure - belongs right after it.
3. Pedagogical Approach - HOW we teach (spiral pedagogy, practice-before-formal, the 8 recurring developmental experiences Read/Repair/.../Reflect, AI-assisted discipline, signature assessments). The teaching philosophy.
4. Course Designs - the concrete individual courses (the 22 CS + 8 external, each course's design). The instantiation. [the actual courses, distinct from block summaries]
5. Specializations - the upper-division degrees built on the core (Cyber/DS/AI/SW-Arch + the model). [promoted from analyses]
6. Analyses - accreditation (ABET), K-State replacement, service mappings. The external-facing justification. [exists, trimmed]

This order = structure -> assessment -> pedagogy -> courses -> specializations -> analyses. Reads as: here's what it is, how we judge it, how we teach it, the actual courses, where it leads, and how it satisfies external requirements. Coherent.

### Chapter numbering (weights, gaps of 10)
1. Core Design (weight 10, ordinal 1)
2. Competency-Based Assessment (weight 20, ordinal 2)
3. Pedagogical Approach (weight 30, ordinal 3)
4. Course Designs (weight 40, ordinal 4)
5. Specializations (weight 50, ordinal 5)
6. Analyses (weight 60, ordinal 6)

### Content status of new chapters
- Core Design: HAVE content (overview, blocks, threads, lenses).
- Assessment: PARTIAL - competency principles are in planning notes (competencies program-level, courses=evidence, parallel grade/competency tracks, signature assessments like Code Archaeology/Data Investigation/Design Review) but NO dedicated assessment document written. Chapter is mostly STUB + a landing page summarizing what we know. Real content TBD.
- Pedagogical Approach: PARTIAL - spiral philosophy, practice-before-formal, 8 developmental experiences, AI-assisted discipline are in planning notes/threads but no dedicated pedagogy doc. STUB + landing summary. TBD.
- Course Designs: HAVE the data (content.js has all 30 courses w/ descriptions) but NOT individual course-design pages. Could GENERATE a stub per course from content.js (code/title/credits/desc) as a starting point. 30 stubs (22 CS + 8 external). Or organize by block. LEAN: generate a course stub per CS course from content.js, grouped by block, as starting points.
- Specializations: HAVE content (model + 3 recommendations: cyber/DS/AI). Missing SW Arch (undrafted). Promote the 4 files; add SW-Arch stub.
- Analyses: HAVE content (ABET-CS, K-State replacement, CompE service). Specializations LEAVE this chapter.

### Course Designs chapter - structure
Option A: flat list of 30 course pages.
Option B: grouped by block (8 block subsections, each with its courses).
Option C: grouped by CS vs external.
LEAN B - grouped by block mirrors the Core Design blocks structure and keeps navigation parallel. Each block subsection in Course Designs has its 3-4 course-design pages. But that DUPLICATES the block nesting from Core Design... Alternatively, Course Designs is flat-by-code (CS-101..CS-210 + externals). 
Actually: the BLOCKS chapter (in Core Design) summarizes blocks; COURSE DESIGNS gives per-course depth. To avoid confusing duplication, Course Designs grouped by block is fine (parallel structure, different depth - block summary vs course detail). Generate per-course stubs from content.js, grouped by block subsections.

### Generate
Rebuild skeleton with 6 chapters, new ordering, course-design stubs generated from content.js (grouped by block), specializations promoted (+ SW-Arch stub), assessment + pedagogy as landing-page + stub chapters.

## Assessment Design Session — 2026-06-24

### Key decisions

**1. Competency assessment is program-level and continuous (Crystalis)**
Assessment operates through the Crystalis platform at the program level. Evidence accumulates through a preponderance across multiple courses. Two tiers: automated telemetry (ceiling: Application) and direct observable assessments via LTI 3.0 rubrics (ceiling: Adaptation through course contexts; Leadership through TA/LA/club roles). Grades and competency levels are parallel tracks — grades live in course containers; competencies live in the Crystalis record. Students graduate with a traditional transcript and a final competency report; the employer-facing version is curated by the student from Crystalis evidence. Target: Adaptation or above, but decoupled from graduation requirements by institutional constraint.

**2. Code Archaeology is a recurring assessment type, not a one-time B2 event**
Code Archaeology deepens across the full program: single-module familiar code (B2) → unfamiliar paradigm/Elixir (B3) → schema archaeology (B5) → git history archaeology (B6) → multi-component system (B7) → production bottleneck diagnosis (B8). The B2 Code Archaeology milestone in the signature-assessments page is the first formal instance; Crystalis tracks the full arc.

**3. 21 recurring assessment types identified and named**
Each type has a longitudinal arc with explicit touchpoints from first appearance to B8. Types are documented in content/assessment/recurring-assessments.md. Three types cross domain boundaries: Design Brief (Develop Abstractions / Design Software Systems / Design Human-Centered Solutions), Algorithm Evaluation Task (Evaluate Algorithmic Solutions / Represent Information), Code Archaeology (Analyze Computational Systems / Maintain Software Systems). Two sub-competencies (Represent Information; Design Software Systems) are fully served by types from other sub-competencies without a dedicated type.

**4. Formal verification additions to CS-107, CS-109, CS-203**
Three formal verification techniques added to existing courses (pending curriculum PR):
- CS-107 (B3): Type annotations explicitly reframed as mechanical verification — the type checker is a theorem prover for a restricted logic
- CS-109 (B3): Pre/post-conditions deepened to include class/loop invariants as proof obligations
- CS-203 (B6): Property-based testing added alongside unit/integration testing

**5. Survey design added to STAT-101 (pending statistics department coordination)**
Requirements Analysis Task needs an early qualitative/quantitative investigation foundation. Survey design (instrument validity, question bias, Likert scales, sampling considerations) is legitimate statistics content and fits in STAT-101. Requires buy-in from the statistics department in co-design. This seeds the B8 CS-209 formal methods toolkit.

**6. Requirements gathering gets explicit B6 touchpoint**
CS-205 Team Software Project scoping becomes an assessed requirements artifact: students conduct a stakeholder interview and produce a documented functional/non-functional requirements brief before implementation begins. This gives the Requirements Analysis Task a meaningful mid-program touchpoint before the B8 formal treatment.

**7. AI-Assisted Practice Task: telemetry gap**
Crystalis captures AI chat prompt/response logs (AI use → Application via automated evidence). But responsible use — verification, judgment, risk awareness — requires direct assessment at every level above Application. This is the one sub-competency with a structurally significant gap between what telemetry proves and what the competency requires.

**8. Reflection Assessment linked to Crystalis evidence record**
At B6 and B8, students can be asked to review their own Crystalis competency trajectory as the evidence base for reflection. The employer-facing competency report (capstone of B8 System Integration Project) is the program's capstone reflection artifact.

## CS-101 Block Design Session — 2026-07-09

Completed `content/course-designs/block-1/cs-101.md` (was a stub with only a working description + Competency Assessments table + a "To develop" TODO list). Added: learning outcomes, an 8-week map, expanded competency-assessment mapping, threads-passing-through with pass depth, prerequisites/standalone-extractability, and a new concurrency seed. Also touched `content/core-design/threads/thread-computational-models.md` (B1 row + Connections clause + a new open question) and `resources/reference/block-inventory.md` (new course-level status section, seeded with CS-101 only).

### Reconciliation flag: Go/CSP concurrency decision not found in this log

My briefing for this session asserted as already-established: "multi-paradigm core: Python/Java/Elixir/Prolog/Go; OS concepts woven throughout; Go/CSP concurrency in CS-101/102, Elixir actor model deferred to year two." I grepped this entire log for "Go," "CSP," and "goroutine" and found **zero** prior mentions. I also found that Round 41 explicitly established what looks like the *opposite* general principle: the core is deliberately **language-agnostic** (concepts/paradigms taught without committing to a language stack; language-specific depth deferred to elective "language certificates," with candidates C, C++, Python, JavaScript, Rust, Java — Go, Elixir, and Prolog were never listed as core languages or certificate candidates). The Elixir mention that does exist in this log (Round: Assessment Design Session, 2026-06-24) places Elixir as an *unfamiliar-paradigm reading substrate* for Code Archaeology at B3 — not as a core teaching language, and not tied to concurrency or the actor model. The actor model itself is logged as arriving at B8 via Erlang/OTP, named explicitly but only as an example/vocabulary moment, not as "Elixir taught as a core language."

The user has confirmed (this session) that a decision to introduce Go-goroutine-*inspired* concurrency at CS-101/102 was made in a conversation outside my visible context, and directed me to treat it as authoritative. I am NOT silently merging this into the log as if it always fit. Two things in the briefing are in real tension with each other and with what's logged:
1. "Concurrency inspired by Go's goroutines, introduced conceptually, not necessarily teaching Go syntax at CS-101" — narrow, concept-level, compatible with the language-agnostic core. **Adopted this session.**
2. "Multi-paradigm core: Python/Java/Elixir/Prolog/Go" as a named five-language core stack — broader, prescriptive, and in direct tension with Round 41's language-agnostic-core-plus-certificates decision (which is otherwise untouched and not contradicted by anything in this session). **NOT adopted.** I did not rewrite CS-101's working description to name Go, Java, Elixir, or Prolog as taught languages; the course still names only Python/JavaScript (already established, acting on the DOM), and the new concurrency content is introduced without committing to any host language's concurrency syntax.

**Open flag for the user/faculty:** is "Python/Java/Elixir/Prolog/Go" meant literally as the languages used for in-class examples throughout the core (a real, substantial reversal of Round 41's language-agnostic decision, which would need its own reconciliation pass across every block file), or was it shorthand for "multi-paradigm exposure via illustrative snippets" (compatible with the existing design)? Left unresolved pending confirmation; flagged in `cs-101.md`'s own open-questions section and in `block-inventory.md`'s course-level status section so it isn't lost.

### The H5P widget: placement and reasoning

Placed the two-step H5P widget (sheet-music → QBASIC `SOUND` command sequence; then multiple independent parallel voices) at CS-101 Weeks 2 and 6 respectively.

- **Week 2** (Step 1): the melody→command translation is the first concrete embodiment of "imperative = an ordered sequence of steps, executed over time, each producing an effect before the next begins" — deliberately contrasted with Week 1's HTML/DOM reading (declarative: structure, no time dimension). This sharpens the declarative/imperative distinction that gets formally named at Week 5's paired CS-101/CS-102 checkpoint.
- **Week 6** (Step 2, parallel voices): this is the concrete, experiential vehicle for the Go-goroutine-inspired concurrency seed — several independent, lightweight sequences of steps, explicitly WITHOUT shared mutable state, so races/locks are out of scope until B8. I folded this into the slot Round 6's draft had already reserved for "reading someone else's decomposition choices," reusing the SAME multi-voice material, rather than adding a new week — the block is already flagged dense in `block-1-read.md`'s open questions, and I didn't want to add net-new instructional time to reconcile an instruction that arrived after that density flag was written.

### CS-101 (Week 6) vs. CS-103's process seed: complementary, not conflicting

Concluded these are complementary passes at different grains, not a contradiction, even though CS-103's seed is explicitly logged as "single-threaded for now" (Round 49/50) while CS-101's Week 6 introduces multiple simultaneous voices in the same block. CS-103's seed is the *formal/OS-level* view: your whole program is one process the OS schedules. CS-101's widget is a *concrete/experiential* seed at a smaller grain: *within* a program, several independent sequences can each make progress "at once." Nothing about "the OS schedules your program as one single-threaded process" is violated by "your program can describe several independent lightweight sequences" — this is exactly the same distinction Go itself draws between an OS thread/process and a goroutine, and it's exactly the distinction B8 (CS-210) already plans to formalize (cooperative/green threads vs. OS-scheduled preemptive threads and processes, per Round 49/50). I recommend CS-103's eventual week-map cross-reference the CS-101 widget by name when it's written — flagged in `block-inventory.md`, not implemented, since CS-103 wasn't in scope for this session.

Also flagged (not implemented): a natural same-block companion pass in CS-102, since functional immutability makes "nothing is shared" the *default* rather than an engineered simplification — a strong paired-comparison extension of the existing Week 5 checkpoint. Flagged in `cs-101.md` and `block-inventory.md` for whoever scopes CS-102 next.

### Spiral spacing judgment for the new concurrency seed (qualitative, per topic)

- B1 → B2 (CS-106 async/event-loop): ~1 block/~8 weeks, contiguous same semester — reasonable short-interval reinforcement for a first-encounter concept.
- B2 → B4 (CS-111 dataflow): ~2 blocks/~16 weeks, crossing a Fall→Spring boundary — acceptable widening since dataflow is an adjacent facet, not a direct rehearsal; recommend B4 explicitly name-check the B1 seed.
- B4 → B8 (CS-210, OS-grounded comparison + actor model + shared-state complexity finally introduced): ~4 blocks, roughly a full academic year — the longest gap and the highest-stakes reinforcement (it's also where the "no shared state" simplification is deliberately lifted). Flagged: recommend CS-210 include an explicit recall bridge back to the B1 music-widget example rather than relying on latent memory of a first-block activity from a year earlier. This is a judgment call (systems-thinking concepts plausibly tolerate longer gaps than syntax skills), not an assertion that the gap is wrong.

### Unresolved discrepancy noted, not resolved: HTML/CSS framing in CS-101 has no logged rationale

`content/course-designs/block-1/cs-101.md` (stub) and `content/core-design/blocks/block-1-read.md` both describe CS-101 opening with HTML/CSS as a reading substrate (trace markup → DOM → rendered page, before writing code). I grepped this entire log for that framing ("reading substrate," "trace a web document," "DOM tree," "rendering pipeline") and found **no session that logged this decision** — Round 6's week-by-week draft (the log's only prior week-map attempt for CS-101) opens Week 1 with "variables, state, basic control structures," no HTML/CSS at all. This looks like a later, unlogged revision (the repo's git history shows a commit titled "Update CS-101 course description"). I treated the currently-committed stub content as authoritative (per instruction to ground sequencing in what's actually there) and merged it with Round 6's reading-thread scaffold (git/asserts/docs/AI-explainer/errors), since the two are content-compatible even though only one was ever logged. Flagging this rather than silently patching the log on its behalf — recommend a future session backfill the missing rationale, or confirm the framing was intentional and log it retroactively.

### Files touched this session
- `content/course-designs/block-1/cs-101.md` — completed per the "To develop" list.
- `content/core-design/threads/thread-computational-models.md` — B1 row rewritten; Connections paragraph and open-questions list each got one clause/item added.
- `resources/reference/block-inventory.md` — new "Course-level status" section added, seeded with CS-101 only; CS-102/CS-103 flagged, not edited.

### Open items for faculty/human review (consolidated)
1. Is "Python/Java/Elixir/Prolog/Go" a literal core language-stack decision (reversing Round 41's language-agnostic-core principle) or shorthand for multi-paradigm exposure? Unresolved.
2. Confirm the HTML/CSS-as-reading-substrate framing for CS-101 was an intentional decision; if so, log it retroactively with rationale.
3. Confirm the Week 6 concurrency-seed addition doesn't tip B1's already-flagged density problem (block-1-read.md open question #1) — I folded it into an existing slot rather than adding a week, but I'm not certain that's sufficient.
4. CS-102 and CS-103 need their own scoping passes; both now have explicit, unresolved cross-references pointing at them from CS-101's file. Neither was edited this session.
5. CS-101's standalone service-extractability claim (in the new file) is my judgment applying the general Round 17/34 service-course principles — it has not been given its own analysis pass the way databases/networking were. Flag before relying on it for a service-course conversation.

## CS-101 Revision Session (follow-on) — 2026-07-09

User-directed revision to `content/course-designs/block-1/cs-101.md`, logged separately from the same-day entry above per instruction (that entry is left unedited).

### 1. HTML/CSS/declarative content removed — resolves last entry's open flag

User confirmed directly: the HTML/CSS-as-reading-substrate content never belonged in CS-101 — it was a misplaced duplication. Checked `content/course-designs/block-2/cs-106.md`: it already fully owns semantic HTML/CSS, DOM, declarative-model naming, async/event-loop, and browser-as-mini-OS framing. Removed the HTML/CSS/declarative-model content entirely from CS-101 (working description, Week 1, learning outcomes, threads table) — pure deduplication, no replacement needed at CS-106 since it's already there. This **resolves** the open flag from the same-day entry above ("HTML/CSS framing has no logged rationale") — it wasn't a missing-rationale problem, it was a duplication error, now corrected by direct instruction. Also lightly corrected `content/core-design/blocks/block-1-read.md`'s Structure-table CS-101 row (which repeated the same HTML/declarative framing) and its Computational Models thread bullet, which had drifted into saying "functional/declarative" was named at B1 — declarative is B2 (CS-106) per `thread-computational-models.md`'s own B1/B2 rows; corrected for internal consistency, not a new decision.

### 2. Language decision: Python primary, Go/C comparative-reading only — stated explicitly

Per instruction, freed the HTML vehicle's Week 1 slot for the widget's melody→QBASIC-command translation (now the block's opener) and committed explicitly to **Python as CS-101's sole produce language**, with **Go and C appearing only as comparative reading material** (same construct, different syntax, no production requirement) threaded through every week. This is a genuinely new, explicit decision — nothing in the log previously named CS-101's produce language this precisely (the removed HTML draft named "JavaScript/Python acting on the DOM," which is now gone along with the DOM vehicle).

Notably, this gives the "Go" part of last entry's unresolved language-stack flag a real, bounded, defensible role for the first time, and it does not contradict Round 41's language-agnostic-core-plus-certificates decision: reading-exposure to a second/third language's syntax is a different claim than deep multi-language production fluency, and doesn't preempt Python/Go/C remaining plausible certificate candidates later. See the consolidated flag-status note below.

### 3. Mutable vs. immutable variable assignment — a real CS-102 pairing point, not just a recommendation

Firmed up last session's "recommended, not yet adopted" CS-102 companion-pass idea into a concrete plan: CS-101 Week 2 introduces mutable variable assignment specifically framed as the same-week counterpart to whatever week CS-102 uses to introduce immutable binding. I did not edit `cs-102.md` (still someone else's scoping pass) but named Week 2 explicitly in CS-101's file and in `block-inventory.md`'s flags so there's a concrete week for that scoping pass to hook into, rather than a vague cross-block gesture.

### 4. GOTO / structured programming — new content, no prior rationale to reconcile

Grepped this log for "goto," "structured programming," and "dijkstra" — zero matches. This is genuinely new content, logged fresh here rather than reconciled against anything. Scoped as a bounded historical aside (Week 3, second use of the QBASIC widget's GOTO capability, refactor GOTO-flow into structured control flow), with Dijkstra's "Go To Statement Considered Harmful" as optional/ungraded reading. It doesn't map onto any of the 13 named spiral threads; I didn't force a mapping — flagged in the file as an unhomed enrichment rather than invented into an existing thread's territory.

### 5. Stack/heap notional machine — new widget, real ownership conflict with CS-103, resolved the same way as the concurrency seed

CS-103's stub already commits to stack/heap content AND a graded assessment row (System Analysis Task — trace stack/heap state through a function call sequence — Analyze System Behavior, SI.1). The user's new CS-101 widget (draw stack/heap/execution-pointer state, used both as demo and as a student assessment) would duplicate that formal claim if added naively. Resolved by applying the same concrete/formative-vs-formal/graded split established last session for the concurrency seed: CS-101 owns the concrete, experiential, *formative* first pass (Tier-1 automated check only, mapped to CR.2 — Develop Abstractions, since drawing a simplified model of program state is abstraction-construction, distinct from CS-103's SI.1 "analyze behavior via observation" framing); CS-103 continues to own the formal, graded instance. This is a recommendation surfaced explicitly in both `cs-101.md` and `block-inventory.md`'s flags, not a unilateral edit to CS-103 — CS-103's stub is unchanged.

Also tied the widget explicitly to the log's own pre-existing "notional machine" framing (the layered People→...→Processes→Memory→...→Networks→Users abstraction, first named around the Computational Models strand's original drafting and reused at the OSI-networking and Sociotechnical-Structure rounds) rather than treating it as an unrelated new idea — per instruction.

The VS Code debugger-visualization plugin was scoped as a same-week tool bridge (steps through the identical worked example), not a separate topic, per instruction.

### 6. Density — an honest read, not forced

Removing HTML freed roughly one week's content. This revision adds back more: per-week Python/Go/C comparison, the mutable/immutable pairing, the GOTO/structured-programming aside, and the new stack/heap widget + VS Code tool + assessment. I fit all of it into 8 weeks by merging the previously-separate "git history applied" week into the errors week (Week 4, via git blame for bug-provenance — a genuine pedagogical fit, not just compression for its own sake) and by keeping GOTO/structured-programming to a bounded discussion rather than a unit. I flagged, rather than asserted, that this fits comfortably: Week 3 (control flow + GOTO + cross-language reading) and Week 6 (wholly new widget + tool + assessment) have little to no slack, and recommended concrete fallback cuts (trim the GOTO discussion further, or move the Week 6 assessment fully to CS-103) if faculty piloting shows either week doesn't fit in the 3-hours/credit-week budget.

### Files touched this session
- `content/course-designs/block-1/cs-101.md` — substantially revised per items 1–6 above.
- `content/core-design/blocks/block-1-read.md` — CS-101 Structure-table row rewritten to match; Computational Models thread bullet corrected (declarative is B2, not B1).
- `resources/reference/block-inventory.md` — flags section updated: HTML flag marked resolved; new flags added for the Week 2 CS-102 pairing point and the Week 6 CS-103 stack/heap split; density flag added.
- `content/core-design/threads/thread-computational-models.md` — assessed, no changes made. HTML was never referenced in this file's B1 row or open questions (checked); the stack/heap and GOTO additions are not part of this thread's own subject matter (paradigm taxonomy, not memory model or control-flow history) — no edit warranted this session.

### Open items for faculty/human review (this session, consolidated; supersedes the density/HTML items in the prior same-day entry)
1. Language-stack flag, **narrowed, not resolved**: Python (produce) and Go (comparative reading only) now have a concrete, bounded, defensible role in CS-101 that doesn't conflict with Round 41's language-agnostic-core principle. Java, Elixir, and Prolog each still have only their own separately-logged, narrow roles elsewhere (Java: certificate candidate; Elixir: B3 unfamiliar-paradigm reading; Prolog: B7 light-touch logic/constraint) — none of which, individually or together, amounts to the originally-asserted "these five languages are the core's teaching stack." Lower-risk than before, still open.
2. CS-103 stack/heap split (concrete/formative in CS-101 vs. formal/graded in CS-103) needs confirmation before CS-103's own scoping pass proceeds on that assumption.
3. Density: Weeks 3 and 6 of the revised CS-101 map have little slack; recommend piloting before treating the map as final.
4. CS-102's scoping pass now has two concrete hooks from CS-101 (Week 2 mutable/immutable pairing; Week 7 concurrency companion pass) — still unaddressed, CS-102's stub is unchanged.
5. CS-103's scoping pass now has two concrete cross-references to address (Week 6 stack/heap split; Week 7 concurrency-seed cross-reference) — still unaddressed, CS-103's stub is unchanged.
6. GOTO/structured-programming content is new and unreviewed by faculty — confirm scope (bounded aside, optional reading) is the right level, not more.

## Block 1 Coordinated Build Session — 2026-07-12

Coordinator asked for block-scale work: deepen CS-101 further, and take CS-102 and CS-103 from bare stubs to complete block files, resolving the cross-references flagged "unaddressed" across the last two sessions. Read all three CS files plus MATH-101's stub before proposing anything, per instruction. MATH-101 was not edited (external, math-department-owned) — confirmed and respected.

### CS-101: two lightweight additions, not a re-scope

Added a recursion cross-reference (Week 6, same worked function as CS-102's new Week 6) and a shared-memory-hazard glimpse (Week 7 closing beat: a hand-traced lost-update example, problem only, no fix). Both are deliberately small — connective tissue and a bounded discussion extension — and I judged neither materially worsens CS-101's own density picture, which was already flagged twice. Resolved (rather than left dangling) two of CS-101's own open questions: the CS-103 stack/heap split is now confirmed by CS-103's actual build, and the CS-102 Week 2 pairing point is now confirmed by CS-102's actual build.

### CS-102: built from a two-sentence stub to a full block file

Distributed core imperative/functional coverage per the established paradigm split: CS-101 = mutable/imperative vehicle, CS-102 = immutable/functional vehicle. Made an explicit, new language decision for CS-102 (not previously stated anywhere): **Python, disciplined to a functional subset, as the produce language; JavaScript as comparative-reading-only.** Deliberately did NOT bring Elixir into CS-102, even though it would be a natural "real functional language" choice, specifically to preserve Elixir's role as an *unfamiliar* paradigm for B3's Code Archaeology pass (`recurring-assessments.md`: "unfamiliar paradigm (Elixir/Chrysalis)," CS-107) — previewing it here would blunt that later novelty. This is a reasoned, flagged decision, not an assumption.

Firmly adopted the concurrency companion pass that was left as "recommended, not yet adopted" in both prior sessions: CS-102's Week 7 now explicitly contrasts CS-101's *engineered* "nothing shared" simplification with functional immutability's *intrinsic* avoidance of the same hazard, extended to sharpen the new shared-memory glimpse (see below).

Recursion (Week 6) is built to share its worked example with CS-101's Week 6 rather than existing as an unrelated topic — same function, two angles (what it does to memory vs. what it lets you express). The specific function is not chosen in either file; flagged as a shared open item.

### The shared-memory surface pass: where it landed, and why I think it strengthens rather than weakens the B4→B8 spacing case

The user wanted concurrency content to go one step further than "no shared state, full stop" — a light, conceptual glimpse of why shared state is hazardous, without teaching synchronization primitives (still B8's job). I placed this as a closing beat in CS-101's Week 7 (a hand-traced example: two independent voices try to update one shared counter "at the same time," one voice's write gets lost) and a matching contrast in CS-102's Week 7 (immutability avoids this because there's nothing shared to race over). This is a real scope addition, not a reframing — logged as new.

This required revisiting the previously-logged B4→B8 spacing judgment, which had partly justified the year-long gap by "B1 deliberately defers ALL shared-state complexity, so there's nothing more to say until B8." That's no longer accurate. My revised judgment, recorded in both CS-101's and `thread-computational-models.md`'s B1/B8 rows: I think this **strengthens** rather than weakens the case for the long gap — a concrete, motivating, unresolved puzzle left open for a year is a recognized desirable-difficulty technique, and B8 still has substantial, genuinely new material to justify its own pass regardless: the OS-level formalization (processes/threads/scheduling), the actual fix mechanisms (synchronization) that resolve the puzzle B1 only posed, and the architectural alternative that sidesteps the whole problem differently (the actor model/message-passing, Erlang/OTP). I recommended CS-210 open its concurrency unit by explicitly recalling the B1 lost-update example, turning the gap into a deliberate payoff rather than a cold start — added as a new open item on `thread-computational-models.md`'s B8 row.

### CS-103: built from a one-paragraph working description to the densest of the three B1 files

New content, in the requested order: (1) Babbage's Difference/Analytical Engines as a bounded historical aside (same treatment as CS-101's GOTO/Dijkstra aside — not a full week) motivating that number representation is a design choice, before (2) binary representation of integers/characters, (3) a simplified 8-bit float worked by hand, and (4) registers/the register-transfer model of basic operations (two weeks, genuinely new, no prior treatment anywhere in the log to calibrate against).

**8-bit float layout — a specific, justified proposal, not left vague:** 1 sign bit + 4 exponent bits (bias 7, IEEE-754-style reserved patterns for zero/subnormal and inf/NaN at toy scale) + 3 mantissa bits with an implicit leading 1. Chosen for a workable dynamic range at a hand-tractable mantissa size; noted to students as structurally similar to real FP8 E4M3-style formats used in ML accelerator hardware, which is a genuine, motivating connection, not just a toy. Flagged for confirmation — a 1-3-4 split (more precision, less range) is equally defensible.

**Registers + VS Code tool — a real capability question, flagged rather than assumed.** CS-101's existing tool bridge works because it debugs Python, and Python debugging in VS Code doesn't meaningfully expose general-purpose CPU registers (CPython execution doesn't map cleanly to hardware registers). A register-level live-tool view is much more plausible against a small **compiled C** example via GDB/LLDB register views in VS Code's C/C++ extension — which is workable since C is already a CS-101 read-comparison language, but is a bigger ask than CS-101's same-language bridge (Python throughout). I could not confirm the actual plugin's capability from available materials; flagged explicitly rather than assumed, per instruction.

**Stack/heap formal assessment:** given its own Week 6 slot, reusing CS-101's Week 6 widget/tool at a longer call sequence, with the existing System Analysis Task row's "This pass" description expanded to also cover the new register tracing — extending an already-committed claim rather than inventing a new one. Process-execution seed shares the same week, with an explicit cross-reference to CS-101's Week 7 (including the new shared-memory glimpse).

**MATH-101 cross-tie:** proposed CS-103's Week 2 (Boolean logic/bitwise) as the pairing week for MATH-101's truth-tables/predicate-logic/sets content. Did not edit `math-101.md`, per explicit instruction — logged as a confirmation ask for the math department's own eventual week-map.

**Density — the honest read the coordinator asked for, not forced:** CS-103 is genuinely the densest of the three files. I used two compression moves to make an 8-week draft plausible: Babbage stays a bounded aside rather than a full week (mirroring CS-101's GOTO treatment), and Week 7 is scoped as pure consolidation/synthesis (source → binary/float → register → stack, reviewing Weeks 1–6) rather than new content, giving a release valve if Weeks 4–5's register content needs more time in practice. Even with those moves, I flagged CS-103 as the file I'd most want piloted before treating as stable — registers (Weeks 4–5) are the single highest-risk item in the whole B1 build, being both genuinely new and dependent on the unconfirmed tool-capability question above.

**Register-transfer model has no identified forward spiral link** — unlike every other new topic this session (recursion, the shared-memory glimpse, Babbage), I could not find a natural later-block reinforcement point for register/ALU content specifically, and did not force one. Flagged in CS-103's own file and in `block-inventory.md` rather than silently left implicit.

### Competency framework: no gaps found, checked explicitly

Per instruction (a competency-architect agent now owns framework extension, not this role), I checked whether any of this session's new content — recursion, the shared-memory hazard glimpse, Babbage/representation history, binary/float representation, registers/ALU — needed a competency ID not already in `resources/reference/competency-framework.md`. It did not: CR.1, CR.2, CR.3, DI.1, SI.1, PP.1, HCP.3, HCP.4, SD.2, PP.2 covered everything mapped in both new files. Stating this explicitly rather than leaving it implicit, since the instruction was to flag gaps, not silently confirm their absence.

### Files touched this session
- `content/course-designs/block-1/cs-101.md` — Week 6/7 rows extended (drag-and-drop naming, recursion cross-reference, shared-memory glimpse); "Concurrency seed" section revised (CS-102 companion firmed up, spacing judgment revisited); new "Recursion: one function, two angles" section added; spiral_links yaml updated; open questions updated (two items resolved, one added).
- `content/course-designs/block-1/cs-102.md` — built in full from stub.
- `content/course-designs/block-1/cs-103.md` — built in full from stub; densest file in this build.
- `content/course-designs/block-1/math-101.md` — **not edited**, per instruction.
- `content/core-design/blocks/block-1-read.md` — CS-102/CS-103 Structure-table rows rewritten; Threads-passing-through list updated (recursion, shared-memory glimpse); new open-question item added.
- `content/core-design/threads/thread-computational-models.md` — B1 row rewritten (recursion, shared-memory glimpse); B8 row extended (explicit recall-and-resolve recommendation); open questions updated.
- `resources/reference/block-inventory.md` — CS-102/CS-103 rows added to the course-level status table; all standing two-session-old flags marked resolved with dated notes; new flags added for this session's open items.

### Open items for faculty/human review (this session, consolidated)
1. CS-103's 8-bit float layout (1-4-3, bias 7) — confirm or propose the 1-3-4 alternative.
2. CS-103's VS Code register-view tool bridge — unconfirmed capability; may require a C debugging target instead of Python for that one week.
3. CS-103's MATH-101 week-pairing proposal (Week 2) — needs confirmation from MATH-101's co-designers.
4. CS-103's register-transfer model has no forward spiral link — may be fine as single-pass content, flagged rather than asserted.
5. The shared recursive function for CS-101/CS-102's Week 6 is not yet chosen — an authoring decision both files depend on.
6. CS-103 is the densest of the three B1 files and the one most in need of piloting before being treated as stable.
7. The revised B4→B8 concurrency spacing judgment (shared-memory glimpse added at B1) — recommend CS-210 (B8) explicitly confirm it will recall/resolve the B1 puzzle rather than introduce synchronization cold; not yet confirmed against CS-210's actual (not-yet-built) content.
8. Carried forward, unchanged: the broader "Python/Java/Elixir/Prolog/Go as the core's language stack" claim remains only partially grounded (see the 2026-07-09 entries) — CS-102's new Python/JS decision doesn't touch this further.
