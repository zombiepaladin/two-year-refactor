# Cybersecurity

This is a proposed degree map swapping the new two-year core into the current official B.S. in Cybersecurity requirements (effective Fall 2026, https://www.cs.ksu.edu/academics/undergraduate/cybersecurity/), using Cybersecurity's required upper-division courses to fill the elective slots the shared core already has. **First step toward regenerating `content/specializations/cybersecurity.md`, which is still written against the retired v1 block structure — per direct instruction, that file is not being touched again until the open questions below are resolved.**

**Dual-ABET framing, per direct instruction:** a Cybersecurity student earns *two* bachelor's degrees (Computer Science and Cybersecurity), so this map must independently satisfy both `resources/reference/abet/cs.md` and `resources/reference/abet/security.md` — not just the Cybersecurity criteria alone. See the Dual ABET Check section near the end.

**Years 1–2 are identical to `cs.md`** — per the standing rule that the core doesn't vary by degree, this section is not reproduced in full here (avoids two copies drifting apart). Compact reference table below; see `cs.md` for the full annotated version, including all the redesign-direction notes, open flags, and ABET-gap-closing rationale that apply here exactly as written there.

## Years 1–2 (= `cs.md`, not reproduced)

| Semester | Courses | Credits |
|---|---|---|
| Y1S1 | CIS 115, CIS 116, DEN 161, CIS 120, MATH XXX Logic and Sets, MATH XXX Counting Finite Configurations, ENGL 100, Core Communication Requirement (KSC 020) | 14 |
| Y1S2 | CIS 260, CIS 220, CIS 200, ECE 241, Calculus Slot, MATH XXX Recursive and Modular Computation, MATH XXX Graphs/Trees/Maps, ENGL 200 | 17 |
| Y2S1 | CIS 300, CIS 320, CIS 301, Linear Algebra Slot, CIS 225, CIS 251, KSC 040 | 15 |
| Y2S2 | CIS 141, CIS 308, CIS 400, KSC 060, STAT 410, Social & Behavioral Sciences (KSC 050) | 15 |

**Note on ECE 241**: already required in the shared core (Y1S2) — independently validates the CompE-alignment finding from `service-computer-engineering.md`; no Cybersecurity-specific action needed.

**Note on CIS 400 (Y2S2), resolved 2026-07-14**: not a conflict. CIS 400 (capstone-of-the-core, Y2S2) and CIS 599 (Cybersecurity's own specialized capstone, Y4S2) are confirmed as the intended two-tier structure — Cybersecurity students keep their own capstone, and CIS 400 serves as a "mid-tier" capstone experience along the way. This also directly validates `cs.md`'s own original hedge on CIS 400 ("likely will become mid-tier capstone course"), written before the redesign, now confirmed rather than superseded. No change needed to the official list's course title for this to hold — the title is stale, but the two-tier structure it implicitly assumed still works.

## Years 3–4 — Cybersecurity-specific

All eighteen of Cybersecurity's required upper-division/context courses fit **exactly** into `cs.md`'s existing Year 3–4 elective-slot architecture, at the same 15-credits-per-semester totals as the general CS map — no new rows, no trims, no additions. See the Additional Requirements section below for the items that needed a decision but didn't end up costing any credits.

### Year 3, Semester 1 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| CIS 450 | CIS 450 (Computer Architecture and Operations) | Direct match — required here regardless of `cs.md`'s general "may become an elective" hedge |
| CIS 501 | CIS 501 (Software Architecture and Design) | Direct match |
| CIS 505 | CIS 505 (Introduction to Programming Languages) | Direct match — validates `cs.md`'s 2026-07-14 "leaning required" decision |
| Technical Writing Requirement | ENGL 415 or ENGL 516 | Direct match |
| Social & Behavioral Sciences (KSC 050, 2nd of 2) | **SOCIO 211** (Introduction to Sociology) | Cybersecurity-required, and the official list confirms it "also satisfies KSC-5" — a clean substitution, not an addition |

### Year 3, Semester 2 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| CIS 560 | CIS 560 (Database System Concepts) | Direct match — required here regardless of `cs.md`'s general elective hedge |
| CIS 575 | CIS 575 (Introduction to Algorithm Analysis) | Direct match — same hedge situation |
| CIS 415 | CIS 415 (Ethics and Conduct for Computing) | Direct match, at the **full 3 credits** — Cybersecurity's list doesn't hedge this the way `cs.md`'s general "may reduce to 1" note does; flagged as a tension in the Additional Requirements section |
| Unrestricted Elective | **Cybersecurity Elective** — CIS 655 or CIS 755 (choose one, per the official restricted-elective requirement) | Fits the "any course" rule cleanly |
| Free Elective (KSC 070) | Stays generic | Nothing in the official Cybersecurity list specifically satisfies this K-State Core bucket; unchanged |

**MATH 510 / STAT 510, resolved 2026-07-14**: confirmed — the shared core's discrete-math sequence (MATH XXX ×4, already in Years 1–2) and STAT 410 (Y2S2, already in Years 1–2) **replace** MATH 510 and STAT 510 directly. Not additional requirements; already fully covered within the shared-core credit count. Removed from the Additional Requirements list below.

### Year 4, Semester 1 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| Systems Elective | **CIS 525** (Introduction to Network Programming) | Already one of the three choices in the general slot — Cybersecurity pins it specifically, as expected |
| Required Technical Elective #1 | **CIS 551** (Fundamentals of Computer and Information Security) | Satisfies the slot's own "CIS 500-level or above" rule |
| Required Technical Elective #2 | **CIS 553** (Fundamentals of Cryptography) | Same — satisfies the slot's own rule |
| Arts & Humanities (KSC 060, 2nd of 2) | Stays generic | Nothing in the official list specifically satisfies this bucket |
| Unrestricted Elective | **CRIM 550** (Cybercrime, Security, and Society) | Fits the "any course" rule cleanly |

### Year 4, Semester 2 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| Required Technical Elective | Stays generic | All CIS-course-list requirements already placed above |
| Capstone | **CIS 599** (Cybersecurity Project) | Replaces the generic CIS 598/643/DEN 591 choice — Cybersecurity's own specialized capstone, confirmed distinct from and complementary to CIS 400's mid-tier core-capstone role (resolved 2026-07-14, see above) |
| Upper Division Elective ×3 | Stay generic | All Cybersecurity-specific requirements are already placed; these remain true free upper-division electives. **Restored to all 3, 2026-07-14** — the earlier 2-slot trim was working around the MATH 221 overage below, which is now dropped, so the trim is no longer needed. |

**Years 3–4 subtotal: 60 credits — identical to `cs.md`'s own Year 3–4 total**, with zero net credits added anywhere for Cybersecurity-specific requirements.

## Additional requirements beyond the standard slot grid

**MATH 221 (Analytic Geometry and Calculus II) — dropped entirely, 2026-07-14.** Direct instruction: ABET requires neither degree to include Calc II specifically (the CS math floor is a credit-hour count with a calculus-rigor requirement, satisfied by MATH 220 already in the shared core; the Cybersecurity math floor is just 6 SCH of discrete + statistics). Cybersecurity's official published list includes MATH 221, but since it's not accreditation-load-bearing for either degree and nothing else in this map depends on it as a prerequisite, it's cut from this redesigned map rather than given a credit-costly home. This is a real, deliberate departure from the currently-published official list, not an oversight — flag it as such if this map goes to faculty review.

**MATH 510 / STAT 510 — resolved, not additional** (see the Y3S2 note above): the shared core's discrete-math sequence and STAT 410 replace both directly.

**Required Communications Elective — resolved, not additional.** Direct instruction, 2026-07-14: Cybersecurity's official list includes this course *because the Computer Science degree required it*, not as a Cybersecurity-specific addition. Since the shared core cut the Communication Elective (2026-07-14, embedding argument), the cut applies uniformly to both degrees — Cybersecurity does not get it added back. No credit consequence.

**Math elective — likely already covered, worth confirming.** Cybersecurity's own math-elective menu includes MATH 515 and MATH 551, both already offered as choices in the shared core's Linear Algebra Slot (Y2S1). If a Cybersecurity student picks one of those two (not MATH 350, which isn't on Cybersecurity's approved list), the shared core's requirement and Cybersecurity's math elective are satisfied by the same course. Worth stating explicitly in advising materials rather than leaving implicit.

## Credit total (2026-07-14, final)

With MATH 221 dropped and the Upper Division Elective trim reversed, **this map no longer diverges from `cs.md`'s own credit structure at all** — every Cybersecurity-specific requirement fits into the shared core's existing slot architecture at exactly matching credit sizes, semester by semester:

| | Y1S1 | Y1S2 | Y2S1 | Y2S2 | Y3S1 | Y3S2 | Y4S1 | Y4S2 | **Total** |
|---|---|---|---|---|---|---|---|---|---|
| Credits | 14 | 17 | 15 | 15 | 15 | 15 | 15 | 15 | **121** |

This is identical to `cs.md`'s own already-accepted per-semester distribution and program total (121 — see `design-log.md`, 2026-07-14 credit-balancing pass). Y1S2's 17 is the same structural floor already accepted there (Calculus + ECE 241 + CIS 200/220/260 + two MATH XXX courses, none movable); nothing about Cybersecurity's own requirements makes it worse. **121 is 1 credit hour above the officially-published 120** — the same 1-credit gap the general CS map already carries, not a new or Cybersecurity-specific overage.

**ABET threshold check after dropping MATH 221, per instruction to watch this:**
- CS ABET math/stat floor (≥15 SCH): MATH 220 (4) + the discrete-math sequence (4) + STAT 410 (4) + the Linear Algebra/math-elective slot (3) = **exactly 15 SCH**. This clears the floor but with **zero margin** — worth flagging plainly, since MATH 221 had been providing 4 credits of buffer above this line. Any future credit reduction anywhere in this math block would need to be checked against this floor specifically.
- Cybersecurity math floor (≥6 SCH discrete + statistics): 8 SCH (4 + 4), comfortably clear.
- Computing floors (CS ≥40 SCH CS-specific; Cybersecurity ≥45 SCH computing+cybersecurity): unaffected by dropping MATH 221 (it's a math course, not computing) — both still clear at 56 SCH as before.

## Dual ABET check

Since a Cybersecurity graduate earns both degrees, both criteria documents apply.

**Against `resources/reference/abet/cs.md` (CS criteria):** this map is the full shared core (all four ABET gaps closed this week — operating systems, parallel/distributed computing, computer architecture, computer science theory) plus Cybersecurity's upper division layered on top, removing nothing from the shared core. The CS-specific 40 SCH floor (cleared at 56 SCH, see the Credit Total section above), the ≥1 general-purpose-language depth requirement, and the math floor all hold — the math floor at exactly 15 SCH, zero margin, per the ABET threshold check above. **Major project, resolved 2026-07-14**: direct instruction confirms CIS 599 (or CIS 400) can serve as the CS degree's own capstone as well as Cybersecurity's — the two-tier structure satisfies both degrees' major-project requirements through the same coursework, not two separate projects.

**Against `resources/reference/abet/security.md` (Cybersecurity criteria):** the crosscutting concepts and most of the eight fundamental areas are addressed per `content/specializations/cybersecurity.md`'s 2026-07-14 regeneration (Component, Human, and Organizational Security remain flagged as partial there — unaffected by this degree-map exercise, still open). The math floor (≥6 SCH discrete + statistics) clears comfortably at ~19 SCH.

## Open questions

All items resolved 2026-07-14 except the three still marked open in `content/specializations/cybersecurity.md` (Component/Human/Organizational Security ABET gaps — unaffected by this degree-map exercise). This map itself has no remaining open structural questions:

1. ~~**CIS 400**~~ — resolved: CIS 400 (core) and CIS 599 (specialization) are the intended two-tier capstone structure, and either can anchor the CS ABET major-project requirement too.
2. ~~**MATH 510 / STAT 510 substitution**~~ — resolved: the new core's discrete-math sequence and STAT 410 replace both directly, no additional credits.
3. ~~**Communications Elective**~~ — resolved: cut uniformly across both degrees, consistent with the general core's 2026-07-14 cut.
4. ~~**CIS 599 as the CS ABET major-project anchor**~~ — resolved, see above.
5. ~~**Published 120-credit-hour total**~~ — resolved: MATH 221 dropped (not ABET-required for either degree), landing at **121 credits** — identical to `cs.md`'s own total, 1 credit hour above the published 120, the same known gap the general CS map already carries. The CS math floor now clears with zero margin (exactly 15 SCH) — worth watching if anything else in that block changes later.

**Remaining, not part of this document**: `content/specializations/cybersecurity.md` can now be regenerated to match this map — all the issues that instruction was waiting on are resolved.
