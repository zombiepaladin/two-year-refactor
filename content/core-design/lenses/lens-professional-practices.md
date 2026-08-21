+++
title = "Professional Practices"
weight = 30
ordinal = "1.3.3"
+++

> *Working draft for faculty review. A **lens** is a standing question or practice applied across the two-year core, scope growing with capability — not a topic taught in one place. One of three lenses (with eight spirals and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** The individual craft of being a professional: documentation, version control, code style, code review, communication, self-reflection, estimation, and continued learning — each maturing as it recurs.

---

## Why this is a lens, not a spiral

A bundle of parallel practices applied throughout, not a single deepening concept — so it is a lens, not a spiral. Covers the individual dimension; the collective/team dimension (teamwork, team reflection, Conway's Law) lives in the Sociotechnical Structure thread. The two meet at a deliberate seam in CIS 400.

This lens's course mapping is the most directly confirmed of any in this chapter — it's carried over unchanged from the re-homing table the user approved when the "Communication Elective" requirement was cut (`resources/reference/spiral-threads.md`, 2026-07-13), on the condition that communication and version-control practice got genuinely embedded throughout the core instead of living in one bolted-on course.

## Where it touches the curriculum

Each touch is woven into the host course — not separately credit-bearing. Touches escalate across the two years.

| Course | The standing question / practice |
|---|---|
| **CIS 115** (Y1 Fall) — Introduction to Computing Science | Professional communication: the "Topic Research and Wiki Article" assignment (20% of grade) is a real, graded writing-for-an-audience artifact. Added 2026-08-04 — a genuine touchpoint the lens previously didn't claim. |
| **CIS 116** (Y1 Fall) — Introduction to Programming | Documentation: inline comments + a standalone explanatory doc (two registers). Version control: git as a history-reading tool (log/diff/blame, semantic versioning). Code style: readable code from the start. **Unconfirmed** — the course's real Topics/Assignments sections are still "TBD," so this can't yet be checked against drafted content. |
| **CIS 200** (Y1 Spring) — Programming Fundamentals | Documentation: docstrings/API conventions (ties naturally to CIS 301's contracts framing). Version control: commit/revert as a safety net. Code-review groundwork: reading others' code. **Unconfirmed** — same TBD-schedule situation as CIS 116; the real SLOs (OOP, error handling, class design) don't mention docs/git/review yet. |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | Documentation: schema-decision docs. Version control: solo feature branching (escalation from CIS 116's read-only git use). Confirmed design intent (2026-07-13 re-homing table), but not yet drafted into the real (SQL-only) schedule/SLOs — see `cis-260.md`'s "Proposed Changes." |
| **CIS 300** (Y2 Fall) — Data and Program Structures | Documentation-as-justification: why this data structure, not that one — a direct tie-in to KBOR CSC1040 outcome 2 ("explain how performance changes based on the data structure chosen"), not an add-on. **Confirmed** against the real course (SLO 3). |
| **CIS 400** (Y2 Spring) — capstone of the core | Version control: collaborative git mechanics (PRs, conflicts) — the seam with Sociotechnical Structure (team coordination). Documentation: team-facing register. Code style: shared conventions/linting as a team contract. Code review as interpersonal skill (give/receive feedback). Self-reflection: an individually-written responsibility retrospective. Estimation/scoping. **Confirmed**, now written into `cis-400.md`'s "Confirmed Design Intent" section almost verbatim — not yet drafted into a real schedule. |
| **CIS 501** (Y3 Fall) — Software Architecture and Design | Professional communication: present and defend a design to an audience, individually assessed even if the design was a team effort. **Confirmed** — `cis-501.md` itself cross-references this lens directly. |
| **Year 3–4 Capstone** | Documentation: operational runbooks (a new register). Estimation practiced against the real project. Continued learning named explicitly: "you now know how to learn the next thing." Out of scope for this pass — no core course-design page covers the Year 3–4 capstone yet. |

## Convergences with other threads

- CIS 400 seam with Sociotechnical Structure: git collaboration mechanics and individual self-reflection are here; team coordination and team reflection are Sociotechnical.
- Documentation-as-justification (CIS 300) pairs with the Boundaries & Contracts thread (a contract documents a promise).
- Professional communication (CIS 501) supports the design-defense pattern CIS 400 establishes earlier.

## Open questions for faculty review

1. A broad bundle — confirm faculty can see/assess each sub-strand (documentation, version control, code style, review, communication, self-reflection, estimation, continued learning) without a dedicated course.
2. Continued education / lifelong learning is the most diffuse sub-strand — confirm it has enough concrete anchoring (named explicitly at the Year 3–4 capstone) rather than being only aspirational.
3. Self-reflection (here) vs. team reflection (Sociotechnical Structure) is a deliberate split — confirm it's legible.
4. **Re-checked against fleshed-out course-design pages, 2026-08-04.** CIS 116 and CIS 200's rows are unconfirmed (both courses' schedules are still TBD); CIS 260's row is confirmed intent but undrafted (now the fifth logged item accumulating on that course — see `cis-260.md`). CIS 300, CIS 400, and CIS 501 all confirmed cleanly against real content; CIS 115 gained a new confirmed touchpoint (Topic Research and Wiki Article).

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
