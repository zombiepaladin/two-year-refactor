+++
title = "Block 2 — Modify"
weight = 20
ordinal = "1.1.2"
+++

**Year 1, Fall · Weeks 9–16 · 8-week block · 3 credits**

> *Working draft for faculty review. Course codes are placeholders. This block is one of eight; it is best read alongside the two-year arc below.*

**Two-year arc:** Read (B1) → **➤ Modify (B2)** → Model (B3) → Structure (B4) → Store (B5) → Build responsibly (B6) → Judge (B7) → Operate (B8)

---

## Purpose

**Cognitive frame:** MODIFY data & state. Computation understood as the act of changing data.

**Essential question:** *What does it mean to change code and data we didn't write?*

MODIFY data & state. Cognitive frame: computation as the modification of data. Heavy OOP pushed to B3. Code Archaeology (modify broken code) is the centerpiece; data transformation (CSV/JSON as sources and sinks); data-driven web rendering (modify what the user sees as data arrives). Git commit/revert and regression tests introduced together as two safety nets the moment students start changing code.

## Structure

Computer science courses (3):

| Code | Course | Cr | Focus |
|---|---|---|---|
| CS-104 | **Data Transformation & Manipulation** | 1 | Parsing, filtering, reshaping, aggregating data; applies B1 imperative-mutation and functional-transformation skills. CSV/JSON as sources and sinks (file formats used, not taught). Embedded data-minimization: what data, transformed how. |
| CS-105 | **Code Reading & Repair** | 1 | Code Archaeology signature assessment; debugging reframed as modifying data flow. Git commit/revert and regression tests introduced together as two safety nets for changing code. AI-as-explainer, verified empirically. |
| CS-106 | **Web Foundations & Data-Driven Rendering** | 1 | Semantic HTML/CSS + accessibility substrate; emphasis on fetch-and-render (modify the page as data arrives). HTML/CSS declarative model formalized (state what, not how; the engine resolves layout) — deepening B1's shallow first encounter; Computational Models pass. Human-Centered Computing pass 1 (accessibility) + proto-visualization (visual hierarchy). Async/event-loop introduced via fetch — the event loop processes a QUEUE of callbacks/events (first encounter with message-queue/event-processing mechanics). Framing: the browser is a MINI-OS (it schedules your code via the event loop, isolates origins as a security boundary, runs concurrent work via web workers, and passes messages via postMessage = IPC) — a concrete, familiar on-ramp to the OS concepts formalized at B8. Data-minimization in form fields. |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| MATH-102 | **Discrete Math: Counting Finite Configurations** | 1 | (External/co-designed. Counting precedes Algorithmic Complexity in B4.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 3 credits.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Code Comprehension** — Code Archaeology signature assessment formalizes here; "understand it before judging it" (pass 2).
- **Professional Practices — version control (lens)** — Commit/revert as a safety net for repair work (pass 2).
- **Correctness & Verification** — Tests for regression — verify a change didn't break prior function, before the vocabulary exists (pass 2).
- **Computational Models** — Async/event-loop via fetch; failure looks different here than B1's sequential crash (pass 2).
- **Human-Centered Computing** — HTML/CSS + accessibility, checklist-compliance level; visual hierarchy as proto-visualization (pass 1).
- **APIs & Networked Systems** — Consume a basic, read-only API (pass 1).
- **Professional Practices — documentation (lens)** — Docstrings/API docs as you build; document a bug fix (what was broken, why, what changed).
- **Trustworthy Computing (lens)** — Data minimization in form fields: why are we asking for this?
- **Algorithmic Thinking & Complexity** — Big-O and memory constraints seeded conceptually in CS-105: cost recognized while reading slow code, before formal notation (pass 1).
- **AI-Assisted Development (bounded)** — AI as explainer continues, supporting Code Archaeology.

## Open questions for faculty review

1. CS-106 (Web Foundations & Data-Driven Rendering) is the weakest fit for the "modifying data" frame — HTML/CSS is fundamentally representation, not modification. It's kept in by emphasizing the dynamic fetch-and-render side (data → DOM as a transformation) and treating static markup as lightly-taught substrate. If Block 2 should be tight on the frame, CS-106 is the candidate to reconsider; doing so would move the HCI thread's first pass elsewhere.
2. This reframe pushed heavy OOP out of Block 2 into Block 3, which is the source of Block 3's load pressure (see Block 3 notes).

---

*Spine position: **Modify**. Builds on Block 1. Leads into Block 3.*
