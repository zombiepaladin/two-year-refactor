+++
title = "The Specialization Model"
weight = 10
ordinal = "5.1"
+++

> *Working draft for faculty review. How the common two-year core relates to the specialization degrees (Cybersecurity, Data Science, AI Systems, Software Architecture), using K-State's Fall 2026 B.S. in Cybersecurity as the concrete case.*
>
> This page is written against the real course sequence and the fleshed-out `content/course-designs/*.md` pages. `cybersecurity.md` and `ai-systems.md` already carry full, real, ABET-mapped degree maps — this page doesn't duplicate that detail, it points to it.

## The structural reveal

K-State's Cybersecurity degree confirms the project's founding premise rather than merely fitting it. Its first ~61 credits (the full two-year core) are **identical** to the Computer Science degree's foundation — the same CIS 115, 116, 120, 200, 220, 225, 251, 260, 300, 301, 308, 320, 400, plus STAT 410 and the MATH discrete sequence (see `cybersecurity.md`'s Degree Map for the full, real course-by-course breakdown). Today, both degrees write out the same foundation separately. The two-year core is therefore not a CS-only replacement; it is the **common foundation both degrees already share**, made explicit and taught once.

The Cybersecurity degree then swaps the CS upper division for a security upper division. That is the entire specialization model, observed in the wild:

> **Every degree = one identical two-year core + a degree-specific upper division.**

## The general structure

| Layer | Content | Common across degrees? |
|---|---|---|
| **Two-year core** (61 cr, Y1–Y2) | The real course sequence — CIS 115/116/120/200/220/225/251/260/300/301/308/320/400, STAT 410, the MATH discrete sequence | **Identical** across CS, Cyber, Data Science, AI, SW Architecture |
| **Shared upper-division core** | CIS 501, 505, 560, 575 — **confirmed common to Cybersecurity and AI Systems** (both `cybersecurity.md` and `ai-systems.md` require all four in Y3) | Common across the two specializations checked so far; Data Science and Software Architecture not yet confirmed against this |
| **Specialization stack** | Degree-specific courses (e.g. security courses for Cyber) | **Differs** — this *is* the specialization |
| **Capstone** | CIS 400 (core-level, Y2S2) **plus** a degree-specific capstone (e.g. CIS 599 for Cyber, CIS 597 for AI) | The core capstone is common; the specialization capstone differs |
| **Context / gen-ed** | Social science, communications, etc. | Mostly common (institution-set) |

Because the core is **identical**, three institutional advantages follow that are worth stating plainly:

- A student can **defer specialization choice until year 3 with no penalty** — the first two years are the same regardless.
- Students can **transfer between specializations** freely (and the Kansas transfer associate degree maps to one core, not five).
- The department maintains **one foundation, not five** — a large reduction in curricular maintenance and a single target for ABET foundation-outcome mapping.

## Cybersecurity, course by course

**Superseded by `cybersecurity.md`'s Degree Map, 2026-08-04** — that page now carries the real, confirmed, semester-by-semester breakdown (all 8 semesters of the core plus the full security upper division), with its own ABET Cybersecurity and ABET Computer Science mapping tables. This page no longer duplicates that table to avoid the two drifting apart; see `cybersecurity.md` directly.

One correction worth noting: **CIS 308 (C Language Laboratory) is real core coursework, required in Y2S2 — not a micro-credential/certificate outside the 120-credit degree.** Both `cybersecurity.md` and `ai-systems.md` confirm it as a shared core course.

**Shared upper-division core, confirmed (not just "pending ABET analysis" as this page previously said):** CIS 501, 505, 560, and 575 are required in Year 3 by both Cybersecurity and AI Systems. Data Science and Software Architecture haven't been checked against this yet.

## The key principle: threads are specialization on-ramps

The core's twelve threads (eight spirals, three lenses, one bounded practice — see `content/core-design/threads/_index.md` and `content/core-design/lenses/_index.md`) are not only pedagogy — each is a deliberate **on-ramp** to one or more specializations. A student gravitates toward a specialization by which threads resonated. This is now an explicit design principle.

| Specialization | Core threads that pre-position the student |
|---|---|
| **Cybersecurity** | Trustworthy Computing lens (primary — formalized in CIS 251); Correctness & Verification (secure code); Boundaries & Contracts (trust boundaries); Computational Models (error handling as attack surface); the `networked-computing` cross-cutting norm (CIS 225, CIS 220/CIS 320) |
| **Data Science** | Data Structures & Representation (incl. the geospatial sub-theme, still a proposed addition — see `cis-300.md`'s "Proposed Changes"); Human-Centered Computing (data-visualization throughline, confirmed at CIS 320); STAT 410; Optimization Reasoning; Computational Models (declarative SQL at CIS 260, dataflow at CIS 300/CIS 320) |
| **AI Systems** | Computational Models (flagship); the AI-Assisted Development bounded practice (CIS 116/200 → CIS 260 → CIS 400 → CIS 141, terminal pass); Optimization Reasoning; Algorithmic Thinking & Complexity; (+ year-3 calculus & linear algebra) |
| **Software Architecture** | Boundaries & Contracts (primary meta-thread); Sociotechnical Structure; the `networked-computing` cross-cutting norm (CIS 220/CIS 300/CIS 320's client-server pairing — the old "APIs & Networked Systems" thread this row used to cite was retired into this norm on 2026-07-15); Correctness & Verification; Human-Centered Computing (UX/requirements, CIS 320's bounded exposure) |

Threads deliberately serve **multiple** specializations (Optimization Reasoning feeds both Data Science and AI; Computational Models feeds AI, Data Science, and Cyber). The core is genuinely common; a specialization is defined by which threads it *deepens*, not by which were taught.

## Seed → deep spiral: what the core lets the cyber upper division assume

Because the core seeds security thoroughly (the Trustworthy Computing lens throughout, formalized in **CIS 251** — authentication, authorization, threat modeling, least privilege, trust boundaries, and applied cryptography building on MATH Recursive and Modular Computation's modular arithmetic), the cyber specialization courses can **start from a higher baseline** and go deeper rather than re-teaching fundamentals. **Caveat, sharpened 2026-08-04 after checking CIS 251's real 7 SLOs and 8-week schedule directly (`content/course-designs/cis-251.md`):** the course is a broad intro-survey — CIA triad (SLO 2), common threat/attacker survey (SLO 3), defensive best practices (SLO 5), risk/incident response (SLO 4, Week 6), ethics/privacy/law (SLO 6, Week 7). Authentication and authorization *are* named explicitly (Week 2), so that part of this framing holds. But **threat modeling as a formal practice, least privilege as a named principle, trust boundaries as a concept, and applied cryptography with any modular-arithmetic tie-in are not in the real course anywhere** — "encryption" appears once, generically, in Week 5's "protecting systems and data" survey, with no cryptographic-math connection at all. The claims below describe original design intent that CIS 251 has not yet been drafted to match, not confirmed content — see `cybersecurity.md`'s own ABET table for the same correction applied row-by-row:

- **CIS 551 Fundamentals of Computer & Information Security** — can assume authn/authz, threat modeling, least privilege, and trust boundaries from CIS 251, and move directly to security architecture, defense-in-depth, and advanced threat modeling. The core raises the floor.
- **CIS 553 Fundamentals of Cryptography** — can assume the conceptual public-key treatment and modular arithmetic from MATH Recursive and Modular Computation → CIS 251, and proceed to formal schemes, protocols, and attacks. This is a clean three-stage spiral: MATH (modular arithmetic, Y1 Spring) → CIS 251 (applied/conceptual crypto, Y2 Fall) → CIS 553 (cryptographic rigor, Y4). **Caveat:** full cryptography needs more number theory than the core's MATH sequence provides; the year-3 MATH 506 (Number Theory) elective is the natural feeder, so there is a math dependency to plan.
- **CIS 525 Network Programming** — can assume the `networked-computing` norm's consume/build/integrate/operate escalation (CIS 200/300 consume, CIS 300 build, CIS 220/320 integrate, CIS 400 operate) and CIS 225's OSI-layer/protocol content, and focus on the security and programming of networks rather than networking basics. **Note:** `cybersecurity.md`'s degree map requires CIS 525 directly rather than the general Systems Elective choice (CIS 520/525/625) — see the Open Questions section below for why that matters for ABET OS/parallel-computing coverage specifically.
- **CIS 655 / 755 Systems Security** — can assume CIS 450 (Computer Architecture and Operations) as a base for systems-level security. **Deep OS/concurrency formalization (processes vs. threads, scheduling, kernel/user space) has no confirmed home in the core itself** — see `resources/reference/spiral-threads.md`'s 2026-08-04 correction note — so this course may need to assume less than the old framing implied, pending that placement decision.

A fuller per-course redesign (what each security course can now drop and what depth it can add) is worth a dedicated pass with the security faculty.

## Open questions

1. **Shared upper-division core — partially confirmed.** CIS 501/505/560/575 are required by both Cybersecurity and AI Systems (`cybersecurity.md`, `ai-systems.md`), so it's common across at least those two; Data Science's own page doesn't yet carry a full degree-map table to check against, and Software Architecture is still a stub. Confirm across all four before calling this settled.
2. **Number theory for cryptography.** CIS 553 likely needs more number theory than the core's MATH sequence provides. Plan the MATH 506 (Number Theory) feeder, or strengthen the relevant math, before finalizing the crypto sequence.
3. ~~C for cyber.~~ **Resolved 2026-08-04** — CIS 308 is confirmed required core coursework (Y2S2), not a certificate.
4. **Per-security-course redesign.** A deeper pass with security faculty on exactly what 551/553/525/655 can assume and how much further they can go, given the core's raised security floor — and CIS 251's real content needs to catch up to the depth this page assumes before that's fully true.
5. **ABET.** Whichever upper-division courses become required vs elective, the *required* path for each specialization must independently satisfy ABET outcomes — the binding constraint for the whole restructure.
6. **New, 2026-08-04 — Cybersecurity's OS/parallel-computing ABET coverage may be thinner than AI Systems'.** `ai-systems.md`'s degree map uses the flexible Systems Elective (choose one of CIS 520/525/625), which `cs.md` explicitly ties to ABET's OS/networking requirement. `cybersecurity.md`'s map instead hard-codes CIS 525 (Network Programming) alone, without also getting CIS 520 or CIS 625. Since the underlying core content this requirement used to lean on was found to have no confirmed home either (see `resources/reference/spiral-threads.md`'s correction note), this is worth a direct check: does CIS 525 alone still clear the ABET OS-exposure bar for Cybersecurity, or does that degree need a second required course from the Systems Elective list too?

## Why this matters beyond Cybersecurity

Cyber is the worked example, but the model generalizes: **Data Science = core + data upper-division; AI Systems = core + AI upper-division; Software Architecture = core + architecture upper-division.** Each reuses the identical core and the threads that pre-position students for it. `cybersecurity.md` and `ai-systems.md` now carry the full real analysis; `data-science.md` has a partial analysis (no full degree-map table yet); `software-architecture.md` remains an undrafted stub. The next step is bringing those last two up to the same standard — a real degree-map table, ABET mapping, and faculty-concerns section, matching the two that are done.
