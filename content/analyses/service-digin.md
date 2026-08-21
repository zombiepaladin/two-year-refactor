+++
title = "Service: Digital Innovation in Media (DIGIN)"
weight = 70
ordinal = "6.8"
+++

> *Working draft for faculty review. Maps the B.S. in Digital Innovation in Media (DIGIN, A.Q. Miller School of Media and Communication) Computational Core requirement onto the new course-container structure (`resources/reference/degree-maps/cs.md`). Source: `resources/reference/degree-maps/digin.md` (K-State catalog, https://www.k-state.edu/media-communication/academics/bs-digital-innovation-media.html) and `resources/reference/kstate-catalog/cc-*.md`. Course codes for the new core are the working CIS numbers in `cs.md`; several are still placeholders (CIS XXX) pending official assignment.*

## Context

DIGIN is a 120-credit, four-year program that bundles a primary degree with a Minor in Entrepreneurship and Innovation, a Certificate in Digital Engagement, and — the relevant piece here — a **Certificate in Computer Science**, earned by completing DIGIN's 17-credit **Computational Core**:

| CC course | Title | Credits |
|---|---|---|
| CC 110 | Introduction to Computing | 2 |
| CC 111 | Elements of Computer Programming | 1 |
| CC 120 | Web Page Development | 3 |
| CC 210 | Fundamentals Computer Programming Concepts | 4 |
| CC 310 | Data Structures & Algorithms 1 | 3 |
| CC 410 | Advanced Programming | 4 |

This is the same K-State "Computational Core" course-number space used in the GIST service analysis (`service-gist.md`) — CC 110/210/310/410 appear in both — but DIGIN's specific slice differs: it adds **CC 111** and **CC 120** (not required by GIST) and does not require CC 315 or CC 520 (GIST's deeper data-structures and database courses). DIGIN's version is the *lighter, earlier* end of the same shared sequence, consistent with DIGIN being a media/communication degree earning a CS certificate as a secondary credential, not a computing-adjacent science degree like GIST.

**A cross-document note worth resolving:** the GIST analysis describes CC 410 as a 3-credit course; DIGIN's own catalog listing and the CC 410 catalog entry (`kstate-catalog/cc-410.md`) both state **4 credits**. Flagging this discrepancy rather than silently picking one — it should be reconciled (likely the GIST analysis has the stale number) but that's outside this document's scope to fix unilaterally.

## Course-by-course mapping

### CC 110 — Introduction to Computing

**Content** (`kstate-catalog/cc-110.md`): history of computing and computing pioneers; survey of AI, high-performance computing, cryptography, big data, cybersecurity, robotics; binary representation, Boolean logic, data encoding, encryption, error checking; computational thinking; the internet and its history; brief programming exposure.

**Maps to:** **CIS 115** (Introduction to Computing Science, 2 credits — credit count matches CC 110 exactly). As of 2026-07-13, CIS 115 explicitly carries the "how digital computers work" content (binary representation, Boolean logic/bitwise operations, a worked 8-bit float format, the register/register-transfer model — originally scoped as a separate course) run side by side with its history thread. CC 110's own topic list ("basics of binary representation, Boolean logic, data encoding, encryption, and error checking") is close to a word-for-word match for what CIS 115 now covers.

**Fit:** Strong, and the credit counts line up exactly (2 = 2) — the cleanest single-course match in this document. The CS-fields breadth survey (AI, HPC, robotics, cybersecurity) has no dedicated equivalent yet at the level of block-file detail, same open item noted in the GIST analysis.

---

### CC 111 — Elements of Computer Programming

**Content** (`kstate-catalog/cc-111.md`): "Brief experience with computer programming concepts such as variables, data types, functions, conditionals, iteration, and collections." 1 credit.

**Maps to:** **CIS 116** (Introduction to Programming, Python, 2 credits — KBOR CSC1020-equivalent). This is worth stating plainly: CC 111's catalog description is nearly word-for-word identical to CIS 116's own current catalog description ("core concepts such as variables, conditionals, iteration, basic data structures, functions, and classes... Brief experience with computer programming concepts such as variables, data types, functions, conditionals, iteration, and collections"). These aren't just similar courses — they appear to be the same course under different numbering conventions (CC-prefix service course vs. CIS-prefix departmental course).

**Fit:** Excellent, essentially 1:1 in content. Credit mismatch (CC 111 is 1 credit; CIS 116 is proposed at 2) reflects the same intentional credit bump already reasoned through for the redesign generally (CIS 116 needs to keep serving as the KBOR CSC1020 equivalent) — not a DIGIN-specific gap.

---

### CC 120 — Web Page Development

**Content** (`kstate-catalog/cc-120.md`): HTML, CSS, JavaScript as the three core client-side web technologies; HTTP requests/responses; the DOM; web accessibility; web forms; AJAX/Fetch requests to web APIs; web hosting. Explicit student outcomes include using JavaScript to dynamically modify a page and using Fetch to interact with web APIs — real DOM/event-driven depth, not just static markup. 3 credits.

**Maps to:** **CIS 120** (Web Foundations, 1 credit) for the HTML/CSS/JS foundation, plus **CIS 220, Platform Programming (Web section)** (1 credit, new 2026-07-13, reframed 2026-07-15) for the DOM-manipulation/event-driven/Fetch-API depth CC 120's own learning outcomes actually require. CC 120's outcomes list ("dynamically modify the structure and appearance of a webpage," "employ AJAX/Fetch requests") go beyond CIS 120's own scope (explicitly a light seed, not developed deeply there per the 2026-07-13 design note) and land squarely in CIS 220's territory instead.

**Fit:** Good content match across the two courses combined (1+1 = 2 credits) against CC 120's 3 — closer than a single-course mapping would give, and structurally accurate, since CC 120 is genuinely asking for both the foundational and the deeper JS/DOM content our redesign deliberately split across two courses for spacing reasons (see the 2026-07-13 design-log entry on the Y1S2 web-content gap). Web accessibility is covered on both sides (CIS 120's human-centered-design seed; CC 120's own accessibility outcome) — a clean alignment, not a coincidence, since CIS 120's wireframe-then-implement pattern was designed with accessibility as an explicit component.

---

### CC 210 — Fundamental Computer Programming Concepts

**Content** (`kstate-catalog/cc-210.md`): program structure and syntax, primitive types, variables, control flow, iteration, simple algorithms, debugging, good software development practices, **introduction to object-oriented programming**. 4 credits.

**Maps to:** **CIS 200** (Programming Fundamentals, 3 credits — KBOR CSC1030-equivalent). CC 210 is clearly the next step up from CC 111 (which covers "elements": variables/conditionals/iteration/collections) — CC 210 adds control flow depth, simple algorithms, debugging discipline, and the OOP introduction, which is exactly CIS 200's role relative to CIS 116 in the new sequence.

**Fit:** Strong, clean sequential match (CC 111 → CIS 116; CC 210 → CIS 200 is a one-to-one pairing, not a many-to-one collapse). Credit gap (4 vs. 3) is smaller than most other mappings in this document.

---

### CC 310 — Data Structures & Algorithms I

**Content** (`kstate-catalog/cc-310.md`): "Exploration of data structures and related algorithms in computer programming. Basic concepts of complexity analysis. Object-oriented design concepts." 3 credits.

**Maps to:** **CIS 300** (Data and Program Structures, 3 credits — KBOR CSC1040-equivalent).

**Fit:** Excellent, and the credit counts match exactly (3 = 3). Same strong fit already established in the GIST analysis — CIS 300 alone now covers CC 310's full scope as a single, traditionally-sized course.

---

### CC 410 — Advanced Programming

**Content** (`kstate-catalog/cc-410.md` plus the fuller breakdown already established via the GIST analysis's syllabus review): advanced programming techniques and projects; simulation and modeling; **media applications**; secure design; information management; **parallelism**; networking; software development methodologies, processes, and design patterns; practical professional communication and collaboration. 4 credits.

**This is the same structurally complicated mapping the GIST analysis found for its own CC 410, with one DIGIN-specific wrinkle.** The content spreads across several new-core pieces, not one course:

| CC 410 component | New home | Notes |
|---|---|---|
| Secure design | **CIS 251** (Foundations of Cybersecurity) — confirmed 2026-07-14 as the home for authentication, authorization, threat modeling, applied cryptography | Strong, direct |
| Parallelism | **CIS 200 and CIS 300** — parallel processing and concurrent algorithms/thread-safe data structures are now explicitly woven into both (2026-07-13 redesign) | Strong, and freshly confirmed — this is new, required content that didn't exist in the core before this week |
| Networking | **CIS 225** (Foundations of Computer Networks) | Direct |
| Design patterns | **Open** — `cs.md` names CIS 400 or CIS 501 as candidates, not decided | Same unresolved gap the GIST analysis flagged |
| Software development methodologies, professional communication and collaboration | **CIS 400** — redesigned 2026-07-14 into a capstone-of-the-core team project (ambiguous requirements, rotating scope, building toward the historical archive) | Strong on process, but see the structural caveat below |
| Media applications | **No CS-core equivalent, and arguably shouldn't be one** — see note below | DIGIN-specific |
| Simulation and modeling, information management | **Thin** — no clearly confirmed dedicated home in the new map at this level of detail | Open |

**The structural caveat that matters most for DIGIN, more than it did for GIST:** CIS 400 is not a standalone course reachable on its own — it sits at the end of the two-year core, with prerequisites (directly or through sequence) spanning most of what precedes it (CIS 200, 300, 260, 225, 251, 301, 141). A DIGIN student who wants the "professional communication and collaboration" piece of CC 410 cannot pick it up as an isolated add-on the way GIST could add CIS 575 or CIS 560 as bolt-on elective depth. **Getting the CC 410-equivalent collaboration experience now means completing essentially the entire two-year core, not a bounded slice of it.** This is a genuine structural consequence of folding professional-practice/team-collaboration content into a capstone-of-the-core rather than a standalone course (see `resources/reference/spiral-threads.md`'s 2026-07-13 re-homing table and the CIS 400 redesign entry in `design-log.md`) — worth naming as a real cost of that design choice for *any* partner program wanting a lighter-touch taste of collaborative software development, not just DIGIN.

**On "media applications":** DIGIN's own Digital Engagement Core and Foundation Courses already cover media production and strategy directly (MC 265, 370, 365, 445, 565, and the MC 19x media-essentials menu). It's plausible that CC 410's "media applications" framing exists specifically *because* DIGIN students take it — i.e., this may be a DIGIN-specific section or emphasis of CC 410, not a general CS-core expectation. Not confirmed; flagged as a question for the Media and Communication school rather than assumed either way.

**Fit:** Mixed, same pattern as GIST's CC 410 finding — stronger on security, parallelism, and networking than the prior (pre-redesign) analysis would have found, genuinely unresolved on design patterns, and structurally harder to reach in isolation than GIST's equivalent gap, because DIGIN has no analogous "curated add-on" option for the collaboration piece specifically.

---

## Summary table

| DIGIN Computational Core requirement | New core equivalent | Fit |
|---|---|---|
| CC 110 Introduction to Computing | CIS 115 | Strong — credits match exactly |
| CC 111 Elements of Computer Programming | CIS 116 | Excellent — near-identical course descriptions |
| CC 120 Web Page Development | CIS 120 + CIS 220 (Platform Programming, Web section) | Good — combined credit total closer than either alone |
| CC 210 Fundamental Programming Concepts | CIS 200 | Strong — clean one-to-one sequential match |
| CC 310 Data Structures & Algorithms I | CIS 300 | Excellent — credits match exactly |
| CC 410 Advanced Programming | CIS 251 (security) + CIS 200/300 (parallelism) + CIS 225 (networking) + CIS 400 (process/collaboration) + design patterns unresolved | Mixed — strong on several fronts, but the collaboration piece now requires completing nearly the whole core to reach |

## What's genuinely strong here, more than in the other two service analyses

- **CC 111 and CIS 116 look like the same course.** This is the cleanest single mapping across all three service analyses done so far (CompE, GIST, DIGIN).
- **Three of six DIGIN courses (CC 110, CC 310, and effectively CC 111) now match new-core credit counts exactly or near-exactly** — a tighter fit than either the CompE or GIST mappings achieved, likely because DIGIN's slice stops before the deeper, more elective-dependent material (CC 315, CC 520) that caused the larger gaps in the GIST analysis.
- **Parallelism is a newly strong match.** CC 410 explicitly names it, and it became required (not elective) content in CIS 200/300 only this week — DIGIN's own catalog language validates that this was a reasonable thing to make required, independent of DIGIN's request.

## What's weaker or unconfirmed

- **Design patterns has no confirmed home** — same open item as the GIST analysis; this is a redesign-wide gap, not DIGIN-specific.
- **"Simulation and modeling" and "information management" from CC 410 have no clearly confirmed dedicated home** at the current level of detail.
- **The professional-collaboration piece of CC 410 is now only reachable by completing nearly the entire core**, a real structural cost specific to how CIS 400 was redesigned — see the caveat above. This is worth surfacing to whoever owns the CIS 400 design as a general consideration, not just a DIGIN footnote.
- **The CC 410 credit-count discrepancy against the GIST analysis (3 vs. 4)** should be reconciled across both documents.

## Credit comparison

| | Credits |
|---|---|
| DIGIN Computational Core | 17 |
| New core, CC 110/111/120/210/310 equivalent (CIS 115 + 116 + 120 + 220 + 200 + 300) | 12 |
| New core, full CC 410-equivalent reach (adds CIS 225 + 251 + 301 + 141 + 400, i.e. most of the remaining core) | 12 + ~11 = ~23 |

The gap between "12 credits gets you CC 110 through CC 310" and "the CC 410 piece effectively requires ~23 credits of core" is the central finding of this analysis — a much steeper jump than DIGIN's own 12-to-17 progression implies, and steeper than either the CompE or GIST mappings produced.

## The DIGIN service pattern

Doesn't cleanly fit either of the two patterns used in the other analyses. It's not quite **Curated Foundational Path** (GIST's pattern) — that pattern assumes departments can stop wherever their needs are met, but DIGIN's certificate specifically wants the CC 410-level content, which is no longer separable from the full core. It's not **Traditional-Course Repackaging** either (Computer Engineering's closest pattern) — DIGIN doesn't want a specific credit-bundled traditional-course shape, it wants a defined certificate. This may be closest to a **Certificate Completion** pattern in its own right: a partner program defines a fixed credential (here, "Certificate in Computer Science") against a curated subset of the core, but — unlike GIST's curated path — the redesign has made the deepest, most-requested piece of that subset (CC 410's collaboration/process content) effectively require finishing the whole core to reach. Worth naming as its own pattern if more certificate-style service relationships come up, rather than forcing it into the existing two.

## Open questions

1. **Is a lighter-weight version of CIS 400's collaboration content feasible for partner programs**, given it's currently only reachable by completing nearly the whole core? This is the central open question of this analysis, and plausibly relevant beyond DIGIN — any program wanting a "certificate" rather than full core completion runs into the same wall.
2. **Design patterns placement** — unresolved in `cs.md` itself, same as the GIST analysis found.
3. **CC 410 credit count (3 vs. 4)** — reconcile against the GIST analysis.
4. **"Media applications" in CC 410** — confirm with the Media and Communication school whether this is a DIGIN-specific section/emphasis or general CC 410 content, before assuming either way.
5. **Simulation/modeling and information-management content** — no confirmed home yet; may not need one if DIGIN's own program covers this elsewhere (their Digital Engagement Core is a plausible home for at least the media/modeling angle).
6. **CIS 115's own credit hedge** (1 or 2) — same open item as the GIST analysis; matters more here since it happens to already match CC 110's stated 2 credits, which strengthens the case for resolving it toward 2.
