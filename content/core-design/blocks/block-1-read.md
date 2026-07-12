+++
title = "Block 1 — READ"
weight = 10
ordinal = "1.1.1"
+++

**Year 1, Fall · Weeks 1–8 · 8-week block · 4 credits**

> *Working draft for faculty review. Course codes are placeholders. This block is one of eight; it is best read alongside the two-year arc below.*

**Two-year arc:** **➤ Read (B1)** → Modify (B2) → Model (B3) → Structure (B4) → Store (B5) → Build responsibly (B6) → Judge (B7) → Operate (B8)

---

## Purpose

**Cognitive frame:** READ computation. The first encounter with code is reading it, across two paradigms, before producing much.

**Essential question:** *How does information become computation — and how do we read it?*

READ computation. The block establishes multiple ways to read code you didn't write — across two paradigms (imperative and functional) taught in parallel, plus git history, asserts/logs, documentation, and AI-as-explainer, all converging on the Code Archaeology assessment that formalizes in B2. File formats appear as data representations to read, not taught as a skill. First naming of "more than one computational model."

## Structure

Computer science courses (3):

| Code | Course | Cr | Focus |
|---|---|---|---|
| CS-101 | **Imperative Programming** | 1 | State, mutation, control structures — the sequence-of-steps-that-change-things paradigm. Opens with a scaffolded H5P widget (sheet music → ordered sequence of QBASIC `SOUND` commands) as the first concrete embodiment of "imperative = ordered steps over time," then moves rapidly to real practice: Python as the primary produce language, with Go and C used for comparative reading of the same constructs. Mutable variable assignment paired explicitly against CS-102's immutability. Lists at shallow depth. The same widget returns for a GOTO/structured-programming historical aside and, later, a no-shared-state multi-voice concurrency seed. A separate new H5P widget + VS Code plugin introduce the stack/heap as a "notional machine." (HTML/CSS/declarative-model content lives in CS-106, B2 — not here.) |
| CS-102 | **Functional Programming** | 1 | Functions as values, composition, immutability (paired same-week against CS-101's mutable assignment), basic recursion — the describe-the-result-as-composed-transformations paradigm. Recursion (Week 6) shares its worked function with CS-101's stack/heap widget — elegance/composition angle here, memory-trace angle there. A firmly-adopted concurrency companion pass (Week 7) contrasts CS-101's engineered "nothing shared" simplification with functional immutability's intrinsic answer, and sharpens CS-101's shared-memory-hazard glimpse: immutability avoids it by construction. Python (disciplined functional subset) is the produce language; JavaScript is comparative reading only (Elixir deliberately withheld to preserve its B3 novelty). Paired solve-it-both-ways exercise with CS-101 (Week 5) names the idea of more than one computational model. |
| CS-103 | **Computational Representation** | 1 | Opens with Babbage's Difference/Analytical Engines (bounded historical aside) motivating why representation is a design choice, before binary representation of integers/characters. A simplified 8-bit float (1-4-3, worked by hand) follows. Boolean logic, bitwise operations — applied counterpart to Discrete Math Logic & Sets (MATH-101), proposed same-week pairing. Registers and the register-transfer model of basic operations (new, two weeks) — the programmer-facing ALU level. Programming-centric memory model: the stack and the heap — the FORMAL, graded pass (System Analysis Task), reusing CS-101's Week 6 widget/tool at greater depth, now also covering register tracing. Execution-model seed: a running program is a PROCESS the OS schedules (single-threaded for now), explicitly cross-referenced with CS-101's concurrency seed. Light home for the representation/hiding security question. HDL/FPGA intentionally not produced. |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| MATH-101 | **Discrete Math: Logic and Sets** | 1 | (External/co-designed. Pairs with Boolean logic/representation in CS-103.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 4 credits.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Data Structures & Representation** — Bits, booleans, numbers, binary primitives, and a simplified 8-bit float — the most primitive representations (pass 1 of the spiral, substantially deepened in CS-103).
- **Code Comprehension** — Write small correct programs; "make it work" (pass 1).
- **Computational Models** — Name that there is more than one model (imperative/sequential vs functional); recursion given two angles across CS-101/CS-102 (memory-trace vs. elegance); a first, concrete, no-shared-state concurrency seed with a bounded shared-memory-hazard glimpse (CS-101's music widget, sharpened by CS-102's immutability contrast, paired with CS-103's OS-process seed); read your first stack trace — errors are ordinary, not shameful (pass 1). (Declarative is named at B2, CS-106 — not here.)
- **Professional Practices — version control (lens)** — Git as a history-reading tool: log, diff, blame; semantic versioning as "what a version communicates" (pass 1).
- **Correctness & Verification** — Asserts/logs to explore code; informal pre/post-condition reasoning (pass 1).
- **Professional Practices — documentation (lens)** — Inline comments AND a standalone explanatory document — two registers introduced together.
- **AI-Assisted Development (bounded)** — AI as explainer for unfamiliar code; student verifies the explanation against actual behavior using the same block's asserts/logs.
- **Trustworthy Computing (lens)** — Light: how a representation choice affects what can be hidden or obscured (homed in CS-103).

## Open questions for faculty review

1. Block 1 is dense — four converging "reading tools" (git history, asserts/logs, documentation, computational-model naming) plus two paradigms. Coherent in framing (all are ways to read code you didn't write), but the week-by-week schedule must confirm three 1-credit courses can actually hold it. A draft week-map exists and looks fittable; the Week-8 integrative assessment in both CS-101 and CS-102 simultaneously is a real crunch point to resolve (stagger one?).
2. Imperative/functional split is genuinely parallel (no dependency either direction), which the old Programming Fundamentals I/II ordering was not. Confirm the two-paradigm approach is acceptable to faculty as a first-block model.
3. Produce vs. read distinction: only imperative basics, functional basics, and shallow lists are PRODUCED; file I/O, richer control flow, and paradigm idioms only need to APPEAR in code students read. Confirm this scoping holds.
4. **All three CS courses now have full block files** (`content/course-designs/block-1/cs-101.md`, `cs-102.md`, `cs-103.md`), each with its own honest density read. CS-103 in particular (Babbage, binary, 8-bit float, two weeks of registers, the formal stack/heap+register assessment, process seed, MATH-101 pairing, git-history capstone) is flagged as the densest of the three and the one most in need of piloting before being treated as stable — see its own open questions.

---

*Spine position: **Read**. Leads into Block 2.*
