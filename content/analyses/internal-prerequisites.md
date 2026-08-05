+++
title = "Internal Prerequisite Analysis"
weight = 60
ordinal = "6.6"
+++

> *Working draft for faculty review. This analysis looks **inside** the two-year core — not the upper-division chains — at what the course sequence's interconnection means when reality intrudes: a student fails a course, drops mid-term, or enters off-sequence. CIS/MATH/STAT numbers are actual K-State courses (or, for the MATH/STAT modules, confirmed course slots in `resources/reference/degree-maps/cs.md`).*

{{< mermaid align="center" zoom="true" >}}
flowchart TB
  %% Internal prerequisites of the two-year core (arrow = 'is required by'). Solid/thick = hard prerequisite. Dotted = soft/spiral-continuity, not registrar-enforced.
  subgraph Y1F["Year 1, Semester 1"]
    direction LR
    CIS115["CIS 115<br/>Intro to Computing Sci"]
    CIS116["CIS 116<br/>Intro to Programming"]
    CIS120["CIS 120<br/>Web Foundations"]
    MLOGIC["MATH<br/>Logic and Sets"]
    MCOUNT["MATH<br/>Counting Finite Config."]
  end
  subgraph Y1S["Year 1, Semester 2"]
    direction LR
    CIS260["CIS 260<br/>Rel. Databases"]
    CIS220["CIS 220<br/>Platform Programming"]
    CIS200["CIS 200<br/>Programming Fundamentals"]
    MCALC["MATH 220<br/>Calculus I"]
    MRECMOD["MATH<br/>Recursive/Modular"]
    MGRAPHS["MATH<br/>Graphs/Trees/Maps"]
  end
  subgraph Y2F["Year 2, Semester 1"]
    direction LR
    CIS300["CIS 300<br/>Data & Program Structures"]
    CIS320["CIS 320<br/>User Experience Dev"]
    CIS301["CIS 301<br/>Logical Foundations"]
    CIS225["CIS 225<br/>Computer Networks"]
    CIS251["CIS 251<br/>Foundations of Cybersecurity"]
  end
  subgraph Y2S["Year 2, Semester 2"]
    direction LR
    CIS141["CIS 141<br/>AI/Data Science"]
    CIS308["CIS 308<br/>C Language Lab"]
    CIS400["CIS 400<br/>Capstone of the Core"]
    STAT410["STAT 410<br/>Statistics for Computing"]
  end
  CIS115 <-.-> CIS116
  CIS116 ==> CIS200
  MCALC ==> CIS200
  CIS120 ==> CIS220
  CIS200 ==> CIS300
  MGRAPHS -.->|"either suffices"| CIS300
  MCALC -.->|"either suffices"| CIS300
  CIS200 ==> CIS301
  CIS120 ==> CIS320
  CIS200 ==> CIS320
  CIS220 ==> CIS320
  CIS300 ==> CIS400
  CIS120 ==> CIS400
  CIS260 ==> CIS400
  MLOGIC -.-> MCOUNT
  MRECMOD -.-> MGRAPHS
  CIS116 -.-> CIS260
  CIS120 -.-> CIS300
  CIS220 -.-> CIS300
  CIS301 -.-> CIS400
  MRECMOD -.-> CIS251
  CIS115 -.-> CIS141
  CIS116 -.-> CIS141
  CIS260 -.-> CIS141
  classDef wall fill:#7c2d12,stroke:#fff,stroke-width:2px,color:#fff;
  classDef mid fill:#9a3412,stroke:#fff,color:#fff;
  classDef ext fill:#1e3a5f,stroke:#fff,color:#fff;
  classDef term fill:#14532d,stroke:#fff,color:#fff;
  class CIS116 wall;
  class CIS200,CIS120 mid;
  class MLOGIC,MCOUNT,MCALC,MRECMOD,MGRAPHS,STAT410 ext;
  class CIS115,CIS220,CIS260,CIS300,CIS301,CIS320,CIS400,CIS225,CIS251,CIS141,CIS308 term;
{{< /mermaid >}}

## The central tension

The tight interconnection that makes the spiral coherent is also a structural risk: early courses can carry outsized downstream weight if a student fails or delays them. In practice, that risk is narrow: **CIS 116 and CIS 200, both taken in the first year, are the only courses whose failure has any real multi-course cascade risk** — everything else in the two-year core either blocks nothing, or blocks at most one downstream course.

This is still worth planning for — a student can fail a course, drop mid-term, or transfer in off-sequence, and those scenarios matter regardless of how narrow the risk is. But the severity to plan for is real and bounded, not sweeping.

## The dependency facts

The core contains **13 hard internal prerequisite edges** among real CIS/MATH courses, plus one corequisite pairing (CIS 115 ⇄ CIS 116) and a handful of soft spiral-continuity links that aren't registrar-enforced.

| Semester gap | Edges | Nature |
|---|---|---|
| 0 (same semester) | 1 | MATH 220 (Calculus I) → CIS 200, both Y1 Spring — a concurrent-enrollment-allowed prerequisite, not a hard sequential gate |
| 1 | 7 | Adjacent-semester dependencies — CIS 116→CIS 200, CIS 120→CIS 220, CIS 200→{CIS 300, CIS 301, CIS 320}, CIS 220→CIS 320, MATH (Graphs/Trees/Maps or Calc I)→CIS 300 |
| 2 | 3 | CIS 120→CIS 400, CIS 300→CIS 400, CIS 260→CIS 400 (all landing at the Y2 Spring capstone) |
| 3+ | 0 | Nothing in the sequence reaches across more than two semesters as a hard prerequisite |

Five courses have **no stated prerequisite at all**: CIS 260, CIS 225, CIS 251, CIS 141, and (unconfirmed either way) CIS 308. Three of those — CIS 225, CIS 251, CIS 308 — explicitly require instructor permission instead of a course prerequisite, a real gatekeeping mechanism in its own right.

## Blast radius — the load-bearing courses

The decisive measure is **blast radius**: if a course is failed or skipped, how many later courses are hard-blocked (transitively)?

| Course | Downstream courses blocked |
|---|---|
| CIS 116 — Introduction to Programming | **5** (CIS 200, CIS 300, CIS 301, CIS 320, CIS 400) |
| CIS 200 — Programming Fundamentals | 4 (CIS 300, CIS 301, CIS 320, CIS 400) |
| CIS 120 — Web Foundations | 3 (CIS 220, CIS 320, CIS 400) |
| CIS 220 — Platform Programming | 1 (CIS 320) |
| CIS 260 — Foundations of Relational Databases | 1 (CIS 400) |
| CIS 300 — Data and Program Structures | 1 (CIS 400) |

**CIS 116 is the single worst case, blocking 5 of the remaining 13 core courses** — real, worth protecting, but a bounded risk, not a cascade across most of the program. **CIS 115, CIS 301, CIS 320, CIS 400, CIS 225, CIS 251, CIS 141, CIS 308, and every MATH/STAT course carry zero downstream hard-block risk** — more than half the core.

Two structural reasons the risk stays this contained:
1. **The core has relatively few courses** — 14 CIS courses plus the MATH/STAT sequence — so there are simply fewer links in any given dependency chain.
2. **Several courses stand outside the hard-prerequisite graph entirely** — CIS 260, CIS 225, CIS 251, and CIS 141 have no stated prerequisite at all, either by design (broad-access intro-style courses) or because their prerequisite structure hasn't been finalized yet (see the open items below).

## Two open items surfaced while building this analysis, not resolved here

Checking every course's real `Course Prerequisites` section against what its content actually presupposes surfaced two cases where content and stated prerequisites don't quite line up. Both were checked with the user rather than assumed:

1. **CIS 301 → CIS 400.** CIS 400's confirmed testing/verification content thematically builds on CIS 301's "verification formalized" pass (`thread-correctness-verification.md`), but CIS 400's own prerequisites (CIS 300, CIS 120, CIS 260) don't include CIS 301. **User's call: keep this as a soft/spiral-continuity link only** (shown dotted in the diagram above), not a hard prerequisite — matches what `cis-400.md` actually states.
2. **MATH Recursive and Modular Computation → CIS 251.** `cs.md`'s own CIS 251 entry says its applied-cryptography content builds on this course's modular arithmetic, "correctly sequenced before this course" — but CIS 251's own page lists no prerequisite at all. **User's call: don't add it as a hard prerequisite in this diagram, but log it as a proposed addition** — done, see the "Proposed Changes" section in `cis-251.md`.

CIS 141 was also checked (it has no stated prerequisites despite thematic dependence on CIS 116/200/260's AI-practice progression and CIS 115's processor-architecture seed) — **user's call: leave it prerequisite-free**, matching its current drafted state exactly; shown with soft links only in the diagram.

## The messy scenarios

### 1. A student fails a high-radius course (CIS 116 or CIS 200)

This is the scenario that decides whether the structure is humane. CIS 116's failure blocks 5 downstream courses; CIS 200's blocks 4. The severity depends on **re-offering cadence** — if these Y1-Fall/Y1-Spring courses run only annually, a failed attempt still costs most of a year on a 5-course chain.

The competency model is the structural escape hatch: because competencies belong to the program rather than the course, a student who fails CIS 116 or CIS 200 but can demonstrate the relevant competency could clear the downstream prerequisite without a full re-sit — but only if the (still under-specified, per the assessment chapter's own open items) re-demonstration mechanics are built.

### 2. A student drops mid-term (illness in week 4)

`cs.md` notes the degree map is "reported in 16-week semesters, not 8-week blocks." But several individual 1-credit courses still run as **8-week half-semester modules within that 16-week frame**: confirmed for CIS 251 (its own drafted schedule is explicitly 8 weeks) and the MATH sequence (each pair of modules is explicitly "first 8 weeks" / "second 8 weeks" of its semester). Whether CIS 220, CIS 225, CIS 260, CIS 320, CIS 141, and CIS 308 follow the same pattern isn't confirmed — their schedules are mostly still TBD. So the core risk this scenario describes — a short illness costing a disproportionate share of an 8-week course's contact time — is **real for at least some courses**, though not uniform across the whole program.

The 1-credit granularity helps: the student loses one credit, not a multi-credit course. Course-level (not term-level) incompletes are the right mitigation.

### 3. Off-sequence entry (spring transfer, or a major change after year 1)

CIS 116 → CIS 200 → {CIS 300, CIS 301, CIS 320} → CIS 400 is a real, drafted four-semester chain a spring entrant would need to navigate. Mitigations: a spring-start cohort, summer offerings, or competency placement — each with its own cost (section count, faculty load, and assessment-system readiness, respectively).

### 4. The CIS 115 ⇄ CIS 116 corequisite

The one real coupling risk in the current design: CIS 115 lists CIS 116 as a corequisite. If the two are taught by different instructors without coordination, the coupling could break — a single, specific, identifiable pairing to watch, not a program-wide pattern.

## Recommendations

1. **Protect CIS 116 and CIS 200** (the only two real load-bearing courses): offer them most frequently, prioritize tutoring/support, and make them the first courses for which competency re-demonstration is available.
2. **Resolve the re-offering cadence** for CIS 116 and CIS 200 before launch — a scheduling/staffing decision.
3. **Specify competency re-demonstration** in the assessment chapter — the structural escape hatch for course failure, still flagged as needing definition.
4. **Confirm which 1-credit courses actually run as 8-week half-semester modules** (beyond the two confirmed cases, CIS 251 and the MATH pairs) before finalizing incomplete/withdrawal policy — this determines how real Scenario 2's risk is on a course-by-course basis.
5. **Plan an off-sequence entry path** — spring cohort, summer offerings, or placement.
6. **Coordinate the CIS 115/CIS 116 corequisite** explicitly if taught by different instructors.
7. **Resolve the two open prerequisite items above** — decide whether to formalize MATH Recursive and Modular Computation as a CIS 251 prerequisite (already logged as a proposed change in `cis-251.md`), and keep watching whether CIS 301's thematic role in CIS 400 stays informal as content gets drafted further.

## Bottom line

The internal prerequisite structure is genuinely resilient: 13 hard edges, a maximum blast radius of 5, and only two courses (CIS 116, CIS 200) carrying any real multi-course cascade risk. More than half the core — CIS 260, CIS 225, CIS 251, and CIS 141 among them — has no stated prerequisite at all, producing a shallow, resilient dependency graph rather than a tightly-coupled one. The mitigations this document recommends — re-offering cadence for the two real load-bearing courses, competency re-demonstration, confirming which courses actually run as 8-week modules, and an off-sequence entry path — are the unglamorous machinery that catches a student who stumbles, sized to the risk that's actually there.
