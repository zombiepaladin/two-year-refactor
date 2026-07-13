+++
title = "Block 8 — Operate"
weight = 80
ordinal = "1.1.8"
+++

**Year 2, Spring · Weeks 9–16 · 8-week block · 3 credits**

> *Working draft for faculty review. Course codes are placeholders. This block is one of eight; it is best read alongside the two-year arc below.*

**Two-year arc:** Read (B1) → Modify (B2) → Model (B3) → Structure (B4) → Store (B5) → Build responsibly (B6) → Judge (B7) → **➤ Operate (B8)**

---

## Purpose

**Cognitive frame:** IN PRODUCTION: delivery, operation & accountability — the system meets the real world. Closes the two-year arc and bridges to the capstone.

**Essential question:** *It's live and people depend on it — how do we operate it and stay accountable?*

In Production: delivery, operation & accountability — the system meets the real world. Pairs with B6 as the two halves of professional accountability (B6 pre-release, B8 post-release), bracketing B7's judgment block. Terminal pass for many threads: production concurrency, real-bottleneck performance, comparative fault-tolerance (try/catch vs OTP supervision vs circuit-breaker), security hardening, requirements-driven UX, API versioning (closes the B1 semantic-versioning loop), blameless postmortem. System Integration Project bridges to the capstone. Closes the two-year arc: read → modify → model → structure → store → build-responsibly → judge → operate.

## Structure

Computer science courses (3):

| Code | Course | Cr | Focus |
|---|---|---|---|
| CS-210 | **Deployment & Operations** | 1 | Deploy, monitor, and operate a live system. Performance analysis on a REAL bottleneck (Algorithmic final pass), including the full memory hierarchy — cache misses and locality, and (the dramatic case) virtual memory, paging, and THRASHING, where systems reality can TRUMP Big-O: a theoretically-worse algorithm with good locality can beat a theoretically-better one that thrashes. Asymptotic analysis is necessary but not sufficient. Grounded in the B1 stack/heap/process model and requiring virtual-memory grounding. Operating-system grounding (programmer-facing): processes vs threads (isolated vs shared memory), preemptive (OS threads) vs cooperative (green threads) scheduling, kernel vs user space, and MESSAGE QUEUES / inter-process communication — generalizing the browser event loop from B2 (the browser was a mini-OS all along). Actor mailboxes ARE message queues, which ties the actor model to its substrate. Just enough to make the concurrent-model choice meaningful. Production fault-tolerance compared across models — try/catch vs the ACTOR MODEL (Erlang/OTP: isolated processes, message passing, supervision trees) vs circuit-breakers. The actor model is named explicitly as a concurrent/distributed computational model, not only a fault-tolerance mechanism (Computational Models flagship final pass; conceptual). Concurrency at scale; containers as deployment structure; harden-before-live (Security final pass); operational runbooks (Documentation); API versioning as a compatibility contract (Boundaries final pass, closes the B1 semver loop). |
| CS-211 | **Human-Centered Design & Validation** | 1 | Formal requirements gathering, UX, and VALIDATION-WITH-USERS — the Human-Centered Computing final pass, escalating from B2's accessibility-checklist compliance to requirements-driven design and fitness-for-purpose. Acceptance testing (does it meet the user's criteria?) and A/B testing (experiment to learn user preference) live here — distinct from code-correctness testing (Correctness & Verification thread). Light design-under-ambiguity. The System Integration Project carries a blameless postmortem (Sociotechnical final pass). |
| CS-212 | **Data Analysis & Responsible AI** | 1 | Notebook-based data analysis as the CULMINATION of the STAT-101 statistics foundation and the data-visualization throughline (B2/B4/B5/B7) — integrative, not new-from-scratch. Honest visualization and data ethics. The genuinely new skill: high-stakes verification and critique of AI-generated code for correctness and security (AI bounded-practice final pass; prerequisite for the Year 3–4 Agentic AI specialization, which this course precedes but does not duplicate). |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| STAT-104 | **Correlation & Regression** | 1 | (External/co-designed, stats dept. Linear regression as the direct on-ramp to machine learning; capstone of the statistics sequence.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 3 credits.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Computational Models** — FLAGSHIP terminal pass: production concurrency at scale; comparative fault-tolerance — try/catch vs Erlang/OTP supervision trees vs circuit-breakers (conceptual). Genuinely distinctive content.
- **Algorithmic Thinking & Complexity** — Performance analysis on a REAL bottleneck, not toy Big-O (terminal pass).
- **Trustworthy Computing (lens)** — Harden a system before it goes live — a real assessed task.
- **Human-Centered Computing** — Requirements-driven UX — escalation from B2's checklist compliance to designing from others' needs (terminal pass).
- **Boundaries & Contracts** — API versioning as a compatibility contract — closes the Block-1 semantic-versioning loop (terminal pass).
- **Sociotechnical Structure** — Blameless postmortem — the org-culture expression of "errors are normative"; converges with the Error-Handling thread (terminal pass).
- **Professional Practices — documentation (lens)** — Operational runbooks — documentation for a future on-call person.
- **AI-Assisted Development (bounded)** — High-stakes verification/critique of AI-generated code for correctness and security — prerequisite skill for the Year 3–4 Agentic AI specialization (terminal pass).

## Open questions for faculty review

1. CS-212 was the most overloaded single unit — it tried to carry notebook data analysis AND AI verification AND data ethics. Resolved by framing data analysis as the CULMINATION of STAT-101 + the data-viz throughline (integrative, not new), leaving AI-verification + ethics as the genuinely new content. Still flagged for the week-by-week check.
2. Pairs with Block 6 as the two halves of professional accountability (B6 pre-release, B8 post-release), bracketing B7's judgment block.
3. Containers arrive here (the deployment-structure topic foreshadowed in Block 4).

---

*Spine position: **Operate**. Builds on Block 7.*
