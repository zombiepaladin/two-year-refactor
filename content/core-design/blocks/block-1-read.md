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
| CS-101 | **Imperative Programming** | 1 | State, mutation, control structures — the sequence-of-steps-that-change-things paradigm. HTML and CSS as the initial reading substrate — trace a web document (DOM tree, browser rendering) before writing Python or JavaScript; HTML/CSS named as a DECLARATIVE model (first encounter, shallow). State, mutation, control structures via JavaScript/Python acting on the DOM. Lists at shallow depth. |
| CS-102 | **Functional Programming** | 1 | Functions as values, composition, immutability, basic recursion — the describe-the-result-as-composed-transformations paradigm. Paired solve-it-both-ways exercise with CS-101 names the idea of more than one computational model. |
| CS-103 | **Computational Representation** | 1 | Boolean logic, number systems, bitwise operations — applied counterpart to Discrete Math Logic & Sets. Light home for the representation/hiding security question. Programming-centric memory model named: the stack and the heap (stack frames for calls/recursion; heap for dynamic allocation) — absorbing the programmer-facing part of computer architecture. Execution-model seed: a running program is a PROCESS the operating system schedules (single-threaded for now) — the grounding the concurrent models will need later. HDL/FPGA intentionally not produced. |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| MATH-101 | **Discrete Math: Logic and Sets** | 1 | (External/co-designed. Pairs with Boolean logic/representation in CS-103.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 4 credits.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Data Structures & Representation** — Bits, booleans, numbers — the most primitive representation (pass 1 of the spiral).
- **Code Comprehension** — Write small correct programs; "make it work" (pass 1).
- **Computational Models** — Name that there is more than one model (imperative/sequential vs functional/declarative); read your first stack trace — errors are ordinary, not shameful (pass 1).
- **Professional Practices — version control (lens)** — Git as a history-reading tool: log, diff, blame; semantic versioning as "what a version communicates" (pass 1).
- **Correctness & Verification** — Asserts/logs to explore code; informal pre/post-condition reasoning (pass 1).
- **Professional Practices — documentation (lens)** — Inline comments AND a standalone explanatory document — two registers introduced together.
- **AI-Assisted Development (bounded)** — AI as explainer for unfamiliar code; student verifies the explanation against actual behavior using the same block's asserts/logs.
- **Trustworthy Computing (lens)** — Light: how a representation choice affects what can be hidden or obscured (homed in CS-103).

## Open questions for faculty review

1. Block 1 is dense — four converging "reading tools" (git history, asserts/logs, documentation, computational-model naming) plus two paradigms. Coherent in framing (all are ways to read code you didn't write), but the week-by-week schedule must confirm three 1-credit courses can actually hold it. A draft week-map exists and looks fittable; the Week-8 integrative assessment in both CS-101 and CS-102 simultaneously is a real crunch point to resolve (stagger one?).
2. Imperative/functional split is genuinely parallel (no dependency either direction), which the old Programming Fundamentals I/II ordering was not. Confirm the two-paradigm approach is acceptable to faculty as a first-block model.
3. Produce vs. read distinction: only imperative basics, functional basics, and shallow lists are PRODUCED; file I/O, richer control flow, and paradigm idioms only need to APPEAR in code students read. Confirm this scoping holds.

---

*Spine position: **Read**. Leads into Block 2.*
