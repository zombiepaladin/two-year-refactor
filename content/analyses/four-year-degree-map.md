+++
title = "Four-Year Degree Map: Merging the Core with the Existing Proposal"
weight = 60
ordinal = "6.6"
+++

> *Working draft for faculty review. Merges `resources/reference/degree-maps/cs.md` — an earlier semester-by-semester sketch that uses real K-State course numbers — with the fully-designed two-year, 8-block core (`CS-101`–`CS-212`, placeholders) and the specialization model. Where the two sources disagreed, this document records the decision made and who made it, rather than silently picking one. Course codes for the new core are placeholders; CIS/MATH/STAT/ECE/DEN numbers are real K-State courses.*

## Why this document exists

Three things existed before this pass, developed somewhat independently:

1. **The two-year core**, designed block-by-block (`content/course-designs/block-1..8/`) with full weekly maps, competencies, and spiral links — reported in 8-week blocks.
2. **`resources/reference/degree-maps/cs.md`**, an earlier attempt to sketch the whole four-year degree in ordinary 16-week semesters, using real course numbers for most of it (some already replaced by the core, some genuinely new, some untouched upper-division).
3. **The design-log resolutions** (Rounds 38–44) and their published expressions — `kstate-replacement.md`, `curriculum-transition.md`, `specialization-model.md` — which settled *what the core replaces* but hadn't yet been checked against the semester-by-semester map in (2).

These three didn't fully agree with each other. This document reconciles them into one proposed four-year map, with every place they conflicted resolved explicitly (either by a decision below, or flagged as still open).

## Decisions made this session

| # | Question | Decision | Rationale / source |
|---|---|---|---|
| 1 | CIS 116 (Intro to Programming) and CIS 308 (C Lab) — replaced by the core, or standalone? | **CIS 116 is not a pre-block on-ramp.** It runs *in parallel* with Blocks 1 & 2, not before them, and **may eventually merge with CS-101** — treated as a live, unresolved merge candidate, not yet executed. **CIS 308 is kept as a default leaning** (not resolved) — see the open fork below; its survival depends on whether upper-division systems/OS content stays C-based or moves to Rust. | User, this session — overrides `curriculum-transition.md`'s "CIS 116 is a pre-core on-ramp" framing and treats `kstate-replacement.md`'s "certificate replaces 308" framing as one branch of a still-open fork, not a settled fact. |
| 2 | Calculus and Linear Algebra timing — Year 3 (Round 40's "locked" constraint) or Years 1–2 (`degree-maps/cs.md`'s draft)? | **Years 1–2**, per `degree-maps/cs.md`: Calculus in Year 1 Semester 2, Linear Algebra in Year 2 Semester 1. **This reverses Round 40.** | User, this session. |
| 3 | Statistics — a 4×1cr sequence spread across Blocks 5–8, or a single traditional course? | **A single 4-credit course**, delivered in one semester — but designed internally as **two 2-credit-equivalent movements** (a spiral-consistent internal structure) rather than one undifferentiated block. Because Calculus now precedes it in the sequence (decision #2), **the course may assume Calc I** — the Round 40 non-calculus constraint is lifted. | User, this session. |
| 4 | Years 3–4 shape — redraw around the specialization model, or keep `degree-maps/cs.md`'s upper division? | **Keep the existing upper-division course shell** (CIS 450/501/505/560/575/415, systems elective, tech electives, capstone) — it does **not** get the full spiral treatment applied to Years 1–2. Instead, **learning objectives shift** within existing course numbers where the core has absorbed foundational content, and the **elective slots are chosen deliberately to build toward each specialization** rather than left as generic "any 500-level CIS." Treated as genuinely fluid — this document makes concrete suggestions, not final decisions. | User, this session. |

## Corrections found while merging (factual, not decisions)

While lining up `degree-maps/cs.md` against the now-fully-built core, a few things in the older sketch turned out to be incomplete or misaligned with the more recently developed material. These aren't judgment calls — they're places the older document was drafted before the core's block sequence existed in final form.

- **Block-to-semester placement.** `degree-maps/cs.md` placed "Foundations of Relational Databases" (→ `CS-201` SQL, Block 5) in **Year 1 Semester 2**, and "Foundations of Computer Networks" (→ `CS-209` OSI Networking, Block 7) in **Year 2 Semester 1**. But `block-inventory.md`'s own arithmetic ("two blocks per semester") places B5/B6 in Year 2 Semester 1 and B7/B8 in Year 2 Semester 2 — a full semester later than the older sketch guessed for networking, and a full **year** later for databases. This document uses the block-inventory placement as authoritative, since it's the more recently and thoroughly developed artifact. **Flag:** if databases are genuinely wanted a year earlier than the core currently sequences them, that's a block-reordering question for whoever owns the block sequence next — not something resolved here.
- **Year 3's missing Semester 2 — now fixed directly in `degree-maps/cs.md`.** The source document originally listed nine 3-credit items under a single Year 3 "Semester 1" heading with no "Semester 2." This has since been corrected in the source itself: Semester 1 now holds CIS 450, CIS 501, CIS 505, Technical Writing, and a second Social & Behavioral Sciences Requirement; Semester 2 holds CIS 560, CIS 575, CIS 415, an Unrestricted Elective, and a Free Elective (KSC 070). The table below matches this split exactly, which differs from the split this document originally proposed (it had guessed CIS 560 into Semester 1 and CIS 450 into Semester 2) — the source file's own split is now authoritative.
- **Year 4 Semester 2 — fixed, but overshot.** The original listed only three items (9 credits) against Semester 1's five (15 credits); this document flagged it as under-full and recommended one additional elective slot. The source has since had **two** "Upper Division Elective" entries added (not one), bringing Semester 2 to five items / 15 credits. See "Credit total reconciliation" below — this fix overshoots the 120-credit target rather than landing on it.
- **`block-inventory.md`'s blank external-course column for Blocks 5–8 is now understood to be correct, not a gap.** Round 40 had planned a `STAT-101..104` sequence one-per-block there; decision #3 above replaces that with a single standalone statistics course that isn't block-paired at all. Nothing needs to be added to `block-inventory.md`'s B5–B8 external column under the resolution adopted here.
- **Linear algebra course choice.** `degree-maps/cs.md` lists three options (MATH 350, MATH 515, MATH 551) without a preference. Both the Data Science and A.I. Systems specialization documents independently prefer **MATH 551 (Applied Matrix Theory)** over MATH 515, specifically because 551 needs only Calc I while 515 needs Calc III — which matters a great deal now that Linear Algebra is sequenced in Year 2 Semester 1, directly after a single semester of Calculus. This document adopts that preference as the recommended default, not a hard requirement.

---

## Proposed four-year map

### Year 1

**Semester 1 (Fall)**

| Item | Cr | Notes |
|---|---|---|
| Block 1 (Weeks 1–8): CS-101, CS-102, CS-103 | 3 | Core |
| Block 1 external: MATH-101 Discrete Math — Logic & Sets | 1 | Core |
| Block 2 (Weeks 9–16): CS-104, CS-105, CS-106 | 3 | Core |
| Block 2 external: MATH-102 Discrete Math — Counting Finite Configurations | 1 | Core |
| CIS 116 Introduction to Programming | 1–2 | Parallel to Blocks 1–2, not a prerequisite to them. **Live merge candidate with CS-101** — not yet executed; see open items. |
| DEN 161 Engineering Problem Solving | 1 | College of Engineering–controlled. **Not addressed anywhere in the core design work** — carried over from the original sketch unexamined; needs explicit confirmation it's still wanted. |
| ENGL 100 Expository Writing I | 3 | K-State Core |
| Core Communication Requirement | 3 | K-State Core |
| Social & Behavioral Sciences Requirement | 3 | K-State Core |
| **Semester total** | **19–20** | **Flag: this is a heavy semester** — see "Year 1 Semester 1 credit load" below. |

**Semester 2 (Spring)**

| Item | Cr | Notes |
|---|---|---|
| Block 3 (Weeks 1–8): CS-107, CS-108, CS-109 | 3 | Core |
| Block 3 external: MATH-103 Discrete Math — Recursive & Modular Computation | 1 | Core |
| Block 4 (Weeks 9–16): CS-110, CS-111, CS-112 | 3 | Core |
| Block 4 external: MATH-104 Discrete Math — Graphs, Trees & Networks | 1 | Core |
| Calculus (Calc I, or Calc II/III by placement) | 4 | Placed here per decision #2 |
| ECE 241 Introduction to Electrical and Computer Engineering | 3 | **Unresolved fork** — see below |
| ENGL 200 Expository Writing II | 3 | K-State Core |
| **Semester total** | **18** | |

### Year 2

**Semester 1 (Fall)**

| Item | Cr | Notes |
|---|---|---|
| Block 5 (Weeks 1–8): CS-201, CS-202, CS-203 | 3 | Core — corrected placement, see "Corrections" above |
| Block 6 (Weeks 9–16): CS-204, CS-205, CS-206 | 3 | Core |
| Linear Algebra — **MATH 551 recommended** (see rationale above) | 3 | Placed here per decision #2 |
| Natural & Physical Sciences Requirement (with lab) | 4 | K-State Core |
| CIS 308 C Language Laboratory | 1 | **Kept as default leaning** — see open fork below |
| **Semester total** | **14** | |

**Semester 2 (Spring)**

| Item | Cr | Notes |
|---|---|---|
| Block 7 (Weeks 1–8): CS-207, CS-208, CS-209 | 3 | Core — corrected placement, see "Corrections" above |
| Block 8 (Weeks 9–16): CS-210, CS-211, CS-212 | 3 | Core |
| Statistics (single course, internally two 2cr movements — see below) | 4 | May assume Calc I, per decision #3 |
| Arts & Humanities Requirement | 3 | K-State Core |
| Communication Elective | 3 | As in the original draft (COMM 323/326, MANGT 220, THTRE 171/265) |
| **Semester total** | **16** | |

**The statistics course, internally.** Delivered as one 4-credit, one-semester course, but organized as two movements so the spiral/competency framing survives the administrative reality of a single course shell:

- **Movement 1 (~2cr equivalent):** descriptive statistics, probability (now assuming Calc I — continuous distributions can be taught with actual integration rather than conceptually), and an introduction to sampling.
- **Movement 2 (~2cr equivalent):** distributions, inference basics, and regression (least squares, now reachable with more rigor given the calculus prerequisite).

This is lighter-weight than the Statistics department's own calculus-based sequence (STAT 510/511, 610/611) — deliberately so, since this course is the *foundation-level* statistics requirement, not the specialization-level depth that Data Science and A.I. draw on separately (see below).

### Year 3

*Not spiral-designed — existing upper-division course shells, kept largely intact, with objectives shifted where the core now covers what these courses used to teach first. Split into two semesters (the original draft only had one) to keep credit loads reasonable.*

**Semester 1** *(matches `degree-maps/cs.md`'s own split, corrected from this document's earlier guess)*

| Item | Cr | Notes |
|---|---|---|
| CIS 450 Computer Architecture and Operations | 3 | **Objectives shifted** — see below |
| CIS 501 Software Architecture and Design | 3 | |
| CIS 505 Introduction to Programming Languages | 3 | |
| Technical Writing Requirement | 3 | K-State Core |
| Social and Behavioral Sciences Requirement (KSC 050) | 3 | **Second instance of this requirement** — also appears Year 1 Semester 1. See "Possible duplicate requirement" below. |
| **Semester total** | **15** | |

**Semester 2**

| Item | Cr | Notes |
|---|---|---|
| CIS 560 Database System Concepts | 3 | Per Round 41, this "narrows to elective depth" for students who don't need it — see specialization guidance below for who should still take it as required. |
| CIS 575 Introduction to Algorithm Analysis | 3 | Per Round 41, narrows to elective depth — see specialization guidance |
| CIS 415 Ethics and Conduct for Computing Professionals | 3 | **Objectives shifted** — see below |
| Unrestricted Elective | 3 | |
| Free Elective (KSC 070) | 3 | |
| **Semester total** | **15** | |

**CIS 450, objectives shifted.** The core (`CS-103` + `CS-210`) now covers programmer-facing architecture — stack/heap, the process model, cache misses, memory hierarchy — the content CIS 450 used to introduce first. Re-teaching that would be redundant. `curriculum-transition.md` already identified the residual content the core deliberately does *not* cover: "register transfer abstraction, addressing modes, assembly language, compiler output, and hardware interrupts... the new curriculum draws its boundary above the ISA." **Recommendation: shift CIS 450's objectives to exactly that residual** — ISA-level architecture, assembly, interrupts, low-level I/O — so it becomes the course that goes *below* the core's deliberate abstraction line, rather than repeating what's above it. This also makes it a cleaner prerequisite for the Systems Elective (CIS 520/525/625) in Year 4.

**CIS 415, objectives shifted.** The core's embedded ethics (Trustworthy Computing lens + Block 6) carries the *foundational* ethics load. `curriculum-transition.md` separately proposed a new "CIS 3xx Ethics" course for professional codes of conduct, IP/licensing, and software-development ethics as professional practice — content that's genuinely standalone and doesn't map cleanly onto any single core course. **Recommendation: don't create a new course number — shift CIS 415's own objectives to exactly that content.** It's cheaper administratively (no new course to get approved) and keeps a recognizable, already-accredited course number intact for ABET's professional-responsibility outcome, while letting the embedded core content carry the introductory ethics work.

### Year 4

**Semester 1**

| Item | Cr | Notes |
|---|---|---|
| Systems Elective — choose one: CIS 520 Operating Systems I, CIS 525 Intro to Network Programming, CIS 625 Concurrent Software Systems | 3 | |
| Required Technical Elective (specialization-shaped — see below) | 3 | |
| Required Technical Elective (specialization-shaped — see below) | 3 | |
| Arts & Humanities Requirement | 3 | K-State Core |
| Unrestricted Elective | 3 | |
| **Semester total** | **15** | |

**Semester 2** *(now updated in the source — two additional Upper Division Elective slots added)*

| Item | Cr | Notes |
|---|---|---|
| Required Technical Elective (specialization-shaped — see below) | 3 | |
| Capstone — choose one: CIS 598 Computer Science Project, CIS 643 Software Engineering Project II, DEN 591 Interdisciplinary Engineering Capstone II, **or a specialization capstone** (see below) | 3 | |
| Upper Division Elective | 3 | |
| Upper Division Elective | 3 | **New** |
| Upper Division Elective | 3 | **New** |
| **Semester total** | **15** | Up from 9 — see "Credit total reconciliation" below; this now *overshoots* the balanced 15/semester pattern rather than falling short of it. |

---

## Credit total reconciliation

The goal was 120 total credit hours. Tallying the map above, semester by semester:

| Semester | Credits |
|---|---|
| Y1 S1 | 17 |
| Y1 S2 | 17 |
| Y2 S1 | 14 |
| Y2 S2 | 15 |
| Y3 S1 | 15 |
| Y3 S2 | 15 |
| Y4 S1 | 15 |
| Y4 S2 | 15 |
| **Total** | **123** (using CIS 115 = 2cr and CIS 200 = 4cr, the un-reduced values the source document leaves open) |

**This overshoots 120 by 3 credits** (121–123 depending on how the two still-open variable-credit questions resolve — see below), not by coincidence: the Year 4 Semester 2 fix added **two** Upper Division Elective slots (+6 credits) where the prior gap from 117 was only **one** slot (+3 credits) short. The fix over-corrected.

**Two things affect the exact number, both already flagged and still unresolved in the source document:**
- **CIS 115**: "1 or 2 credits, to be refactored" — a 1-credit swing.
- **CIS 200**: "4 credits, may reduce to 3" — another 1-credit swing.

Depending on how those resolve, the current total is **121, 122, or 123** — never exactly 120.

**Cleanest single fix to land on exactly 120:** drop one of the three Upper Division Elective slots in Year 4 Semester 2 back out (returning it to two, 12 credits, still up from the original 9), which — combined with the un-reduced CIS 115/CIS 200 values — lands the grand total at exactly 120. Resolving the CIS 115/CIS 200 ambiguity alone doesn't close the gap on its own (best case, both reduced, still lands at 121); the Year 4 Semester 2 trim is the piece that actually closes it.

**Possible duplicate requirement, still worth confirming.** "Social and Behavioral Sciences Requirement" now appears twice — Year 1 Semester 1 and Year 3 Semester 1 — both tagged KSC 050. If K-State's gen-ed structure genuinely requires two social/behavioral courses under that code, this is correct as-is and not part of the overshoot. If it's a duplication introduced while filling in Year 3's missing semester, removing the second instance would *also* help close the gap (120 − 3 = 117, which would then need the Year 4 Semester 2 trim on top to still reach exactly 120 — the two issues are independent and both need a decision, not just one).

## Shaping the electives toward the specializations

The user's instruction this session: Years 3–4 electives should be **selected to produce the specialization degrees**, not left generic. Below are concrete suggestions per specialization, pulled directly from the specialization recommendation documents already drafted (`content/specializations/`) — these are proposals for which of the "Required Technical Elective" and capstone slots above to fill with what, not new analysis.

### Cybersecurity (the strongest-fit specialization — an existing K-State degree)

| Slot | Suggested course |
|---|---|
| Required Technical Elective ×3 | CIS 525 Network Programming, CIS 551 Fundamentals of Computer & Information Security, CIS 553 Fundamentals of Cryptography |
| Restricted elective | CIS 655 or CIS 755 (Systems Security) |
| Capstone | CIS 599 Cybersecurity Project |
| Context (likely additional/replacing an Unrestricted Elective) | CRIM 550 Cybercrime, Security & Society; SOCIO 211 |
| Math dependency to plan | CIS 553 needs more number theory than the core's MATH-103 modular arithmetic provides — MATH 506 Number Theory is the natural Year 3/4 feeder; not yet slotted above. |

### Data Science (CS-flavored — partners with, doesn't duplicate, the Statistics B.S. in Data Science)

| Slot | Suggested course |
|---|---|
| CIS 560 (Year 3 Sem 2) | **Required, not elective**, for this track — data management depth is load-bearing |
| Required Technical Elective ×3 | CIS 533 Intro to Data Science Foundations, CIS 531 Intro to Programming Techniques for Data Science, CIS 561 Intro to Data Science in Practice |
| Statistics-partnership depth (additional electives, likely replacing Unrestricted Electives) | STAT 705 Regression & ANOVA, STAT 745 Statistical Graphics, STAT 766 Applied Data Mining/ML — reachable without further calculus; STAT 760 Optimization and 511/610-611 rigor need the calculus this map now provides in Years 1–2, easing the timing concern the Data Science document originally flagged |
| Capstone | CIS 561 is itself capstone-bearing |
| Note | Moving Calculus to Years 1–2 (decision #2) substantially **eases** the "calculus-sequencing tension" the Data Science document flagged as its biggest open issue — the calculus-gated statistics courses no longer have to compress into Years 3–4 alone. |

### A.I. Systems (the most math-dependent specialization)

| Slot | Suggested course |
|---|---|
| Required Technical Elective ×3 | CIS 530 Intro to Artificial Intelligence, CIS 532 Intro to Deep Learning, CIS 537 Computer Vision (or another application-area course, e.g. CIS 833 for NLP) |
| Math/stat depth (replacing Unrestricted Electives) | STAT 510/511 (calculus-based probability), STAT 760 Optimization for Data Science |
| Capstone | An A.I.-flavored capstone within CIS 598 — the natural home for the "Agentic A.I." pinnacle the core's AI-Assisted Development thread was designed to lead toward; likely needs authoring, not yet a distinct course |
| Known gap (unaffected by this document) | A.I. system architecture / MLOps has no existing K-State course — flagged in `ai-systems.md`, still open |
| Note | Same easing effect as Data Science: A.I.'s specialization document called calculus timing "the hardest scheduling dependency" under the year-3-calculus plan; decision #2 substantially resolves it. |

### Software Architecture (still a stub — least developed of the four)

| Slot | Suggested course |
|---|---|
| CIS 501, CIS 505 (Year 3 Sem 1) | **Likely required, not elective**, for this track, per the existing stub's own note |
| Required Technical Elective ×3 | Not yet identified — `software-architecture.md` has only on-ramp threads named (Boundaries & Contracts, Sociotechnical Structure, APIs & Networked Systems, Correctness & Verification, Human-Centered Computing), no concrete course list. **This specialization needs the same drafting pass the other three already got before its electives can be filled in here with confidence.** |

---

## Two forks left genuinely open

**CIS 308 (C Language Laboratory).** Kept as the default leaning this session, but its survival is really a question about what upper-division systems courses assume: if Operating Systems (CIS 520), Network Programming (CIS 525), and Concurrent Software Systems (CIS 625) stay C-based, CIS 308 remains a load-bearing prerequisite course and should stay. If those courses move to Rust instead (a live possibility, not addressed here), CIS 308 loses its rationale and the `kstate-replacement.md` certificate-model answer becomes the better fit again. This document does not resolve which — it's presented as a fork contingent on a decision about the Systems Elective courses' language, not on anything in the core itself.

**ECE 241 (Intro to Electrical and Computer Engineering).** `degree-maps/cs.md` keeps it ("potentially removable... politically tricky"). `curriculum-transition.md` drops it entirely ("no longer required for CS students... neither the ISA layer nor electrical engineering is part of the new curriculum's scope"). These two already-committed documents disagree and neither the user nor this session resolved it. This map keeps ECE 241 (Year 1 Semester 2) as a placeholder pending that decision, but flags it prominently rather than treating either position as settled.

## Year 1 Semester 1 credit load

Adding up Blocks 1–2 (8cr), CIS 116 (1–2cr), DEN 161 (1cr), and three K-State Core gen-eds (9cr) totals **19–20 credits** in a single semester — noticeably heavier than `degree-maps/cs.md`'s original Semester 1 (~17–18cr), because the block core delivers six CS courses (`CS-101`–`CS-106`) where the old sketch's CIS 115 + CIS 120 totaled only three credits for a comparable slice of content. This is a direct, mechanical consequence of "two blocks per semester" plus everything else a first-semester student is also expected to carry (gen-ed, DEN 161, CIS 116) — not a new problem this document introduces, but the first time it's been made concrete by actually trying to fit real gen-ed and non-CS requirements around the block schedule. **This needs a decision:** accept a heavy first semester, move one of DEN 161 / CIS 116 / a gen-ed requirement to Semester 2, or reconsider whether Blocks 1 and 2 can genuinely coexist with a full outside load in one semester.

## What this document does not resolve

- **The full ABET credit-floor accounting** (30cr computing-general / 40cr CS-specific / 15cr math-stat, and how CIS 450/415/560/575's disposition affects the CS Requirements total) is `kstate-replacement.md`'s job, not repeated here. That document's credit reconciliation should be revisited in light of decision #2 (calculus back in Years 1–2) and decision #4 (upper-division courses kept rather than narrowed), since both change the math underneath it.
- **Software Architecture's specialization stack** — genuinely not designed yet.
- **The CIS 116 / CS-101 merge** — named as a live possibility, not executed.
- **Whether CIS 560 and CIS 575 are required-for-everyone or elective-for-most-required-for-some** — this document leans toward "required in general, but load-bearing specifically for Data Science (560) — otherwise available as elective depth," but that's a proposal, not a ratified structure.
