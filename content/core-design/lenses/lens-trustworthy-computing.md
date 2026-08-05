+++
title = "Trustworthy Computing"
weight = 10
ordinal = "1.3.1"
+++

> *Working draft for faculty review. A **lens** is a standing question or practice applied across the two-year core, scope growing with capability — not a topic taught in one place. One of three lenses (with eight spirals and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** Can people trust this system, and the people who built it? — security, privacy, and ethical reasoning asked wherever content raises it, formalized once.

---

## Why this is a lens, not a spiral

Trustworthiness is the unifying purpose under security, privacy, and ethics. A lens, not a spiral, because making it a spiral produced fake "light touches" in late courses. It is a standing question asked wherever relevant content appears, formalized and systematized once (CIS 251), but never confined there. Avoids the failure mode the program rejects (security becoming isolated or disappearing).

## Where it touches the curriculum

Each touch is woven into the host course — not separately credit-bearing. Touches escalate across the two years.

| Course | The standing question / practice |
|---|---|
| **CIS 115** (Y1 Fall) — Introduction to Computing Science | Light: how does a representation choice affect what can be hidden or obscured? Confirmed, long-standing design intent; softly supported by the real course (its Course Topics list "computational representation" and "cybersecurity" as separate bullets, not yet explicitly connected). |
| **CIS 120** (Y1 Fall) — Web Foundations | Privacy-by-design in data collection: why are we asking for this field? Data minimization. **Narrowed from a prior three-course claim (CIS 200/CIS 120/CIS 220) to CIS 120 alone**, 2026-08-04 — CIS 120 is the real successor to the old "Web Foundations" design intent this traces to, and its "Web Forms" topic is the plausible carrier; CIS 200's and CIS 220's real drafted content don't fit. Proposed, not yet drafted — see `cis-120.md`'s "Proposed Changes." |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | Data minimization as a schema decision; access control as a property of the schema (who sees what). Confirmed design intent (2026-07-13 re-homing table), but not yet drafted into the real (SQL-only) schedule/SLOs — see `cis-260.md`'s "Proposed Changes." |
| **CIS 251** (Y2 Fall) — Foundations of Cybersecurity — FORMALIZED | Authentication, authorization, threat modeling, applied cryptography (building on MATH — Recursive and Modular Computation's modular arithmetic, correctly sequenced before this course). Least privilege extended to least data collection. This is the program's primary ABET ethics anchor — confirmed as this lens's formalized capstone, not its first appearance (see `cs.md`'s CIS 251 entry). **Note:** the real drafted SLOs are thinner/more generic than this row (CIA triad, authn/authz, threats, risk, ethics/law, incident response) — the crypto/modular-arithmetic and least-privilege/least-data-collection framing specifically isn't spelled out yet, though it fits the course's scope. |
| **CIS 220 / CIS 320** (Y1 Spring / Y2 Fall) | Re-identification risk from combined datasets — a specific, real privacy question arising from APIs used as structural boundaries, defended as part of CIS 400's design-defense assessment. **Proposed, not yet built, and with no confirmed course to carry it** — same finding as the Optimization Reasoning lens's matching row. The confirmed real content for this pairing is a single-API client/server boundary, not multi-source integration. Logged in both `cis-220.md`'s and `cis-320.md`'s "Proposed Changes"; needs a course-designer/faculty decision. |
| **CIS 400** (Y2 Spring) — capstone of the core | Harden a system before it goes live — a real, assessed task, part of the course's deployment/operations content. Poorly-handled errors as attack surface. Long-confirmed design intent, now written into `cis-400.md`'s "Confirmed Design Intent" section — not yet drafted into a real schedule. |

## Convergences with other threads

- CIS 251: converges with Computational Models — errors as attack surface.
- CIS 251: converges with Boundaries & Contracts — a trust boundary is a contract about what each side may assume.
- Throughout: the ethical/honesty strand surfaces in Human-Centered Computing's data-visualization throughline (honest, non-misleading charts).

## Open questions for faculty review

1. Confirmed as the primary ABET anchor for professional-responsibility and ethical-judgment outcomes (`cs.md`, CIS 251 entry) — still needs a formal pass in the accreditation mapping itself.
2. No course of its own beyond CIS 251's formalized pass (by design) — confirm faculty can see/assess that the trust questions were actually raised in each host course.
3. **Re-checked against fleshed-out course-design pages, 2026-08-04.** Three of six touchpoints (CIS 120's narrowed privacy-by-design row, CIS 260's access-control row, CIS 220/CIS 320's re-identification row) are confirmed intent but not yet drafted; the CIS 220/CIS 320 item specifically traces to a retired pre-refactor course design and needs a real decision, not just drafting.

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
