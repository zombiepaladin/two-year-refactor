+++
title = "Five-Year Transition: Old Curriculum Support"
weight = 40
ordinal = "6.4"
+++

> *Working draft for faculty review. Maps the old sub-500 CIS courses and ECE 241 to new core equivalents so that students on the old B.S. in Computer Science curriculum can be supported for five years without running parallel old-course sections.*
>
> **Rewritten 2026-08-05.** The original version of this document assumed the new core would introduce entirely new course numbers (a distinct, more granular course-by-course design), requiring a complex many-to-one substitution mapping for every old course. **That assumption no longer holds.** The real redesign, once course-designer fleshed it out, reused the *same* catalog numbers for nearly every course this document worried about — CIS 115, 116, 200, 300, 301, 308, 400, 415, and 450 are all still those numbers, redesigned underneath. That eliminates most of the substitution problem this document exists to solve. See "The headline finding" below.

## The problem

When the two-year core is adopted, students who enrolled under the old curriculum must still be able to complete their degree. The solution is course substitution: identify which old courses are fully covered by new core courses and establish official equivalencies, so that old-track students take new courses that satisfy their old requirements.

This document answers: *which old courses need to keep running, and which can be retired on day one?*

## The headline finding: there's much less to solve than the substitution-mapping approach implied

Checked every course in scope against the real, current degree map (`resources/reference/degree-maps/cs.md`) and the fleshed-out `content/course-designs/*.md` pages. Result:

| Old course | Real new-core status |
|---|---|
| CIS 115 Introduction to Computing Science | **Same number, survives.** Redesigned content (history + computational-representation seed), credit hedge 1–2 (was 2). |
| CIS 116 Introduction to Programming | **Same number, survives.** Redesigned as a Python course, now 2 credits (was 1) — a real credit-hour increase, not a substitution question. |
| CIS 200 Programming Fundamentals | **Same number, survives.** Now 3 credits (was 4, confirmed intentional reduction — Windows Forms/Visual Studio dropped). |
| CIS 300 Data and Program Structures | **Same number, survives.** Same 3 credits; redesigned practice vehicle (client/server web architecture, not desktop). |
| CIS 301 Logical Foundations of Programming | **Same number, survives.** Now 2 credits (was 3) — the new discrete-math sequence absorbs the introductory logic content CIS 301 used to carry, so CIS 301 itself deepens rather than introduces. |
| CIS 308 C Language Laboratory | **Same number, survives, unchanged** — standalone, still 1 credit. |
| CIS 400 Object-Oriented Design, Implementation and Testing | **Same number, survives.** Same 3 credits; content substantially redesigned (capstone-of-the-core team project, not the old solo point-of-sale app). |
| CIS 415 Ethics and Conduct for Computing Professionals | **Same number, survives** — still in the real degree map (Year 3, Semester 2), credit possibly reducing from 3 to 1 as ethics gets embedded elsewhere in the core, but **not retired**. |
| CIS 450 Computer Architecture and Operations | **Same number, survives** — still in the real degree map (Year 3, Semester 1), same 3 credits, flagged as possibly becoming an elective as some content migrates to CIS 115, but **not retired**. |
| ECE 241 Introduction to Electrical and Computer Engineering | **Survives** — still in the real degree map (Year 1, Semester 2 in the current map, moved earlier than its old placement), 3 credits. **Not dropped**, contrary to what this document originally assumed. |

**What this means for old-track students: for every course above, "already completed the old version" satisfies "requirement met."** A course being redesigned under its own number doesn't require a substitution decision — a student's transcript already shows they passed CIS 300 (or 415, or 450); that the content underneath has changed doesn't retroactively unsatisfy the requirement. **None of these ten courses need the complex multi-course substitution mapping this document originally built.**

## What's actually left to solve

Given the finding above, the real transition questions are narrower than originally scoped:

1. **Credit-hour changes on four courses** (CIS 116: 1→2; CIS 200: 4→3; CIS 301: 3→2; CIS 415: possibly 3→1) don't block individual students' requirement satisfaction, but do affect **total-degree credit-count accounting** for the transition period — worth a registrar/advising check that a mixed old-credits/new-credits transcript still totals correctly, not a substitution mapping.
2. **Content redesign on CIS 300 and CIS 400** is substantial enough that old-track students completing these under the *old* content and new-track students completing them under the *new* content will have learned genuinely different things, even though both satisfy "CIS 300" / "CIS 400" on a transcript. Worth flagging to advisors and to whichever upper-division courses assume specific prerequisite content (e.g., CIS 400's old solo-project skills vs. its new team-project skills) — not a credit or substitution problem, a content-continuity one.
3. **ECE 241 and CIS 415's survival should be confirmed as final**, not assumed temporary. This document's original premise (ECE 241 dropped, CIS 415 replaced by a new standalone ethics course) never actually happened — the real degree map keeps both. If that's the settled answer, this document's original "Remaining action items" #1 and #4 below (author a new ethics course; remove ECE 241 from the catalog) are moot and should be dropped, not just deferred.
4. **Upper-division prerequisite audit is still real** — any 500-level course that lists CIS 450, ECE 241, CIS 300, CIS 301, CIS 400, or CIS 415 as a prerequisite should have its prerequisite statement re-checked against the *redesigned* content of those same-numbered courses, since a student satisfying the prerequisite via the old content vs. the new content may arrive with different preparation. This is a content-currency check, not a substitution-table lookup.

## Remaining action items

1. **Confirm ECE 241 and CIS 415's survival is the final, intended answer** (not a transition-period holdover) — this document's original plan assumed both would eventually be retired/replaced; the real degree map keeps both indefinitely. If that's not actually settled, flag it explicitly rather than let this document's stale assumption stand uncorrected elsewhere.
2. **Upper-division prerequisite audit**, scoped to content-currency (see item 4 above), not course-substitution.
3. **Confirm the credit-hour changes on CIS 116/200/301/415 don't create a total-credit-count problem** for students transitioning mid-degree.
4. **CIS 308 status for new-track students** — it remains standalone and required for old-track students; for new-track students it's now a required Year 2 Spring core course too (per the real degree map), so this is no longer an open question the way it was in the original version of this document.
