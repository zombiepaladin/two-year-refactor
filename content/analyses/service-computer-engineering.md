+++
title = "Service: Computer Engineering"
weight = 30
ordinal = "6.3"
+++

# Service Mapping: Computer Engineering

> *Working draft for faculty review. Regenerated 2026-07-14 against the new course-container structure (`resources/reference/degree-maps/cs.md`) — the prior version of this analysis was written against the retired 8-week-block structure and is no longer current. Course codes for the new core are the working CIS numbers in `cs.md`; several are still placeholders (CIS XXX) pending official assignment.*

## Context — this is a deeper relationship than a typical service case

The relationship with Computer Engineering is not a simple "CompE takes N credits of service courses from us" arrangement, and the redesign has made that more true, not less. Two things established directly, 2026-07-14:

- **Computer Engineering majors take most of the core CS courses** — not a curated subset, the bulk of the two-year core itself.
- **ECE 241 (Introduction to Electrical and Computer Engineering) sits inside our own required core** (Y1S2, 3 credits) — its placement was confirmed to stay put specifically *because* it aligns with Computer Engineering's own degree map, and moving it would work against that alignment (see `resources/design-log.md`, 2026-07-14 credit-balancing entry).
- **A CS + CE dual-degree pathway (out-of-department specialization) is under consideration** as a *potential* future direction — not yet a decision, but the shared-foundation size of the overlap is why it's plausible at all.

This reframes the analysis. The prior version of this document treated Computer Engineering as a service-course consumer of four traditional 3-credit courses (CS0/CS1/Data Structures/OOP, 12 credits total) bundled from spiraled 1-credit pieces. That framing is now largely obsolete for two reasons: **the new core's courses are already traditionally sized** (CIS 116 at 2 credits, CIS 200 and CIS 300 at 3 credits each — not 1-credit slivers needing repackaging), and **the actual relationship is broader than four courses** — it's most of the shared foundation, with ECE 241 as a two-way anchor point rather than a one-way service delivery.

## How the content maps to our pieces

| Traditional course (as previously understood) | New core course(s) | Fit |
|---|---|---|
| **CS0** (gentle intro) | CIS 115 (Introduction to Computing Science — history + "how digital computers work" content: number representation, Boolean logic/bitwise, a worked 8-bit float format, the register/register-transfer model) | Good — CIS 115 carries the digital-foundations content CS0 needs; credit hedge (1 or 2, trending toward 2) still open, see `cs.md` |
| **CS1** (first real programming) | CIS 116 (Introduction to Programming, Python, 2 credits — KBOR CSC1020-equivalent) | Good — direct overlap; CIS 116 is now sized close to a traditional CS1 rather than a 1-credit fragment |
| **Data Structures** | CIS 300 (Data and Program Structures, 3 credits — KBOR CSC1040-equivalent: lists, linked lists, stacks, queues, trees, hash tables, sets, dictionaries, heaps, graphs; sorting/searching/tree/graph algorithms; complexity analysis) | Strong — CIS 300 alone is now a traditionally-shaped Data Structures course, not a distributed set of 1-credit pieces. **New in this course, not in the old mapping**: concurrent algorithms and thread-safe data structures are now explicitly part of CIS 300's purview (2026-07-13 redesign — see `cs.md`), motivated by its server-layer practice vehicle. This is a genuine addition CompE should be aware of, not a gap. |
| **OOP** | CIS 200 (Programming Fundamentals, 3 credits — KBOR CSC1030-equivalent: encapsulation, inheritance [now required, not optional], abstraction, exception handling, collections, generics/interfaces) | Strong — direct overlap, and inheritance being made explicitly required (it was optional in the current Fall 2024 offering) closes a real gap CompE's own outcomes likely need |

**What's materially different from the prior analysis, not just relabeled:**

- **No more repackaging problem.** The prior analysis spent most of its length on "Option A: bundle 1-credit pieces into recognizable transcript courses" vs. "Option B: have CompE re-map to the modular structure." That tension is largely dissolved — CIS 116/200/300 are already close to traditional course shapes. The credit-volume question shrinks accordingly: CIS 116 (2) + CIS 200 (3) + CIS 300 (3) = 8 credits, plus CIS 115's CS0-adjacent content, against CompE's historically-stated 12. This gap is smaller than before but not resolved — see Open Issues.
- **Windows Forms and Visual Studio are dropped entirely from CIS 200 and CIS 300** (2026-07-13, program-wide decision) — if Computer Engineering's own outcomes or downstream courses assumed a Windows Forms/desktop-GUI deliverable from either course, that assumption no longer holds. GUIs across the core are HTML-based instead (CIS 120, and the new client-side course sequence below). **This needs explicit confirmation from Computer Engineering** — it's a real behavior change, not a relabeling.
- **Parallel processing is now required, not elective-only.** CIS 200 and CIS 300 both weave in parallel/concurrent content as required core material (2026-07-13). If CompE's own curriculum currently sources parallel-computing exposure from elsewhere (or didn't require it), this is new, positive overlap worth flagging to them directly.
- **ECE 241 is inside our map, not outside it.** The prior analysis didn't discuss ECE 241 at all, since it predates the current degree-map structure. It now sits in Y1S2 as a required core course, confirmed to stay there for CompE-alignment reasons (2026-07-14).

## The credit-volume question, updated but not resolved

Minimal direct mapping (CIS 116 + CIS 200 + CIS 300 = 8 credits) plus CIS 115's CS0-adjacent content is closer to CompE's historical 12-credit consumption than the old 1-credit-block mapping was (previously ~8-9 credits spread across many pieces), but it's not an exact match, and the same three explanations from the prior analysis still apply:

1. The new core's courses may simply be denser per credit than the old traditional courses were.
2. There may genuinely be less seat-time, which would need to be resolved with Computer Engineering directly.
3. CompE's degree may reasonably draw additional core pieces beyond the minimal four (CIS 260, CIS 225, CIS 251 are all plausible additions given "most of the core" is the stated relationship, not just these four).

**This is not resolved by the redesign and needs the same input the prior analysis asked for and never received**: Computer Engineering's current CS0/CS1/Data-Structures/OOP learning outcomes and ABET contact-hour requirements.

## Where this fits the service-course model

Given "most of the core," Computer Engineering may no longer be best described by the prior analysis's "Traditional-Course Repackaging" pattern at all — it may be closer to a **Shared Foundation** pattern: CompE and CS draw from largely the same required core (not a curated subset, not a repackaged bundle), with ECE 241 as the anchor course that runs in the opposite direction (CS requiring a CompE course, not just CompE requiring CS courses). Whether this is a fourth service pattern distinct from the three the GIST analysis catalogs (Topical Unit, Curated Foundational Path, Traditional-Course Repackaging), or a variant of Curated Foundational Path at much larger scale, is worth resolving explicitly if the CS+CE dual-degree direction gets pursued — a real dual-degree pathway is a different institutional arrangement than any of the three patterns catalogued so far, and would need its own analysis once (if) that direction firms up.

## Open issues

1. **Credit volume, still open.** Needs Computer Engineering's current outcomes and ABET contact-hour requirements — not resolved by this regeneration, same ask as before.
2. **Windows Forms/Visual Studio removal — needs explicit confirmation from Computer Engineering.** If any of their own downstream coursework assumed a desktop-GUI deliverable from CIS 200 or CIS 300, that assumption is now false.
3. **Dual-degree direction.** If CS+CE pursues an actual dual-degree/out-of-department-specialization pathway, this document's framing (service mapping) may need to become a different kind of analysis entirely (shared-curriculum/dual-degree design) rather than a service-course crosswalk. Not decided; flagged for whoever picks this up next.
4. **CS0/CS1 boundary.** Both CIS 115 and CIS 116 now cover ground the old CS0/CS1 split addressed — confirm where Computer Engineering's own boundary falls, same open question as the prior analysis, now against the new course pair.

## What we need from Computer Engineering

- Their current CS0, CS1, Data Structures, and OOP **learning outcomes** (to confirm the mappings above and resolve the CS0/CS1 boundary).
- Their **ABET contact-hour requirements** for these courses (to resolve the credit-volume question).
- Confirmation that the loss of Windows Forms/Visual Studio from CIS 200/300 doesn't break any of their downstream assumptions.
- Their read on the dual-degree direction, if that's being pursued seriously enough to warrant a real proposal.
