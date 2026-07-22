+++
title = "Service: Geographic Information Systems & Technology"
weight = 40
ordinal = "6.4"
+++

> *Working draft for faculty review. Regenerated 2026-07-14 against the new course-container structure (`resources/reference/degree-maps/cs.md`) — the prior version of this analysis was written against the retired 8-week-block structure and is no longer current. Based on syllabi for CC 110, 210, 310, 315, 410, and 520 on file in `resources/syllabai/`; those facts are unchanged by this regeneration. Course codes for the new core are the working CIS numbers in `cs.md`; several are still placeholders (CIS XXX) pending official assignment.*

## Context

The B.S. in Geographic Information Systems & Technology (GIST) requires a **Computational Core (CC)** as its computing foundation — seven courses from K-State's Computational Core sequence, plus a web fundamentals course:

| CC course | Title | Credits |
|---|---|---|
| CC 110 | Introduction to Computing | not stated in syllabus |
| CC 210 | Fundamental Computer Programming Concepts | 4 |
| CC 310 | Data Structures & Algorithms I | 3 |
| CC 315 | Data Structures & Algorithms II | 3 |
| CC 410 | Advanced Programming | 3 |
| CC 520 | Database Essentials | 3 |
| (web fundamentals course) | course not specified | unknown |

**Estimated total:** approximately 17–20 credits, depending on CC 110's credit count and the web course. Unchanged from the prior analysis — GIST's own program facts aren't affected by our redesign.

## Course-by-course mapping

### CC 110 — Introduction to Computing

**Content:** History of computing, binary representation, Boolean logic, data encoding and encryption, computational thinking, internet technology, AI/HCI/cybersecurity/data science breadth survey, basic programming exposure.

**Maps to:** **CIS 115** (Introduction to Computing Science). As of 2026-07-14, CIS 115 explicitly carries what was previously a separate course's content (v1's CS-103 "Computational Representation"): number representation as a design choice, binary representation of integers/characters, Boolean logic and bitwise operations, a worked 8-bit float format, and the register/register-transfer model — run side by side with CIS 115's existing history/overview thread, not as two disconnected topics (the Babbage decimal-vs-binary framing is the explicit bridge between them).

**Fit:** Good, and arguably a cleaner single-course match than before, when this content was split across two separate courses (CS-101's opening weeks + a dedicated CS-103). The breadth survey of CS fields (AI, robotics, HCI) still has no single dedicated equivalent — that content would need to be distributed across later courses' framing as they're built out to block-file detail, which hasn't happened yet for the new map. **Open, unresolved from before:** CIS 115's own credit count is still hedged (1 or 2, trending toward 2 given the added content) — confirm before finalizing this mapping's credit accounting.

---

### CC 210 — Fundamental Computer Programming Concepts

**Content:** Values/types/variables, conditionals/loops, functions, file I/O, collections, programmer-defined objects, Model-View-Controller pattern. Python 3, 4 credits.

**Maps to:** **CIS 116** (Introduction to Programming, Python, 2 credits — KBOR CSC1020-equivalent): variables, conditionals, iteration, functions, collections (lists/dictionaries), and a first touch of classes/objects. Deeper object-oriented structuring continues in **CIS 200** (Programming Fundamentals, 3 credits — KBOR CSC1030-equivalent).

**Fit:** Good for the programming fundamentals. **Not yet confirmed:** whether MVC specifically has a home in the new map. It hasn't been re-decided at the level of detail CC 210's syllabus specifies — this is block-file-level content that doesn't exist yet for the new course containers, unlike the prior analysis's claim that it landed in a specific course. Flagging as open rather than asserting a match.

**Credit note:** CIS 116 (2) + CIS 200 (3) = 5 credits against CC 210's 4 — closer than the prior analysis's comparison (which summed several 1-credit block pieces), since both new courses are now traditionally sized.

---

### CC 310 — Data Structures & Algorithms I

**Content:** Lists, stacks, queues, trees, graphs (basic traversal), searching, sorting, hashing, recursion, complexity analysis. Python, 3 credits.

**Maps to:** **CIS 300** (Data and Program Structures, 3 credits — KBOR CSC1040-equivalent). As of the current redesign, CIS 300 alone covers essentially all of CC 310's list: lists, linked lists, stacks, queues, trees (including BSTs, AVL trees, tries), sets, hash tables, dictionaries, heaps, graphs, standard and advanced sorting/searching algorithms, tree and graph algorithms, and complexity analysis — these are the explicit required outcomes of KBOR CSC1040, which CIS 300 must satisfy.

**Fit:** Excellent, and simpler than before — CC 310's entire content list now maps to *one* traditionally-sized course instead of three distributed 1-credit pieces. **New in this course, not in CC 310 or the prior analysis:** CIS 300 now also explicitly includes concurrent algorithms and thread-safe data structures (2026-07-13 redesign), motivated by its server-layer practice vehicle — a genuine addition beyond CC 310's scope, not a gap.

---

### CC 315 — Data Structures & Algorithms II

**Content:** Advanced trees, graphs (deep pass), heaps; graph searching, shortest path, Minimal Spanning Tree; requirements analysis; application to domain areas. Python, 3 credits. Prerequisite: CC 310.

**Maps to:** Baseline heaps and graphs are already inside **CIS 300** (see above) — **this closes a gap the prior analysis flagged explicitly** (heaps previously had no named home in the new core; they're now an explicit required CSC1040 outcome CIS 300 must cover). Deeper graph algorithms (Dijkstra, MST-style optimization) are the natural territory of **CIS 575** (Introduction to Algorithm Analysis, 3 credits) — but CIS 575 is currently flagged in `cs.md` as **"may become an elective."**

**Fit:** Good for the baseline (stronger than before, since heaps are now confirmed rather than an open question), but the "advanced" and "requirements analysis / domain application" parts of CC 315 depend on GIST selecting CIS 575 specifically, which isn't guaranteed core content for CS majors either — consistent with the existing Curated Foundational Path pattern (GIST selects the pieces it needs), but worth being explicit that this piece is elective, not required, in the new map.

---

### CC 410 — Advanced Programming

**Content:** Software engineering methodologies, design patterns and architectures, computer security, advanced OOP, **GUI programming**, **event-driven programming**, professional communication and collaboration, iterative milestone project serving as a capstone. 3 credits. Prerequisite: CC 315.

**This is the mapping that changed the most, and needs the most faculty attention.** The prior analysis mapped CC 410 largely onto v1's B6 (Collaborative Development, Security Fundamentals, Testing) plus B3's advanced OOP courses. Those don't exist in that form anymore. The new map splits CC 410's content much more widely:

| CC 410 component | New home | Notes |
|---|---|---|
| Advanced OOP | CIS 200 (inheritance now explicitly required, not optional) | Good, direct |
| Design patterns | **Open** — flagged in `cs.md` as a candidate for CIS 400 or CIS 501, not yet decided | Not a confirmed mapping |
| Computer security | **CIS 251** (Foundations of Cybersecurity) — now the confirmed home for authentication, authorization, threat modeling, and applied cryptography (2026-07-14) | Strong, and newly clarified — this was vaguer in the prior analysis |
| GUI programming | The web-platform trajectory: **CIS 120** (HTML/CSS/JS taught) → **CIS 220, Platform Programming, Web section** (deep JS/DOM, new 2026-07-13, reframed 2026-07-15) → **CIS 320, User Experience Development, Web section** (component-based UI library, new 2026-07-13, reframed 2026-07-15) | Strong, and a materially cleaner three-course trajectory than the prior analysis's scattered embedded-content story |
| Event-driven programming | Same trajectory — CIS 220 explicitly carries event-driven programming and the "browser as a mini-OS" event-loop framing | Strong |
| Professional communication and collaboration | **CIS 400** — now redesigned as a capstone-of-the-core team project (2026-07-14), hosting the `professional-practice`/`sociotechnical-collaboration` escalation: collaborative git/PRs, team-facing documentation, code review as interpersonal skill, individually-written retrospectives, estimation | Strong on process — see caveat below |
| Iterative milestone project | **CIS 400** | See caveat below |

**The caveat that matters:** CIS 400 is **no longer a generic OOP/design-patterns/GUI course** — it's a substantial, deliberately ambiguous-requirements team project building toward a specific real-world domain (the historical archive, a green-field replacement for a Chapman Center tool), with scope rotating by cohort. The *process* skills CC 410 wants (professional communication, collaboration, an iterative milestone project) are still a strong match, arguably a better one than before, since the redesign was explicitly built to resist AI-shortcut in a way the old model wasn't. But GIST should not expect CIS 400 to deliver design-patterns or GUI content anymore — those now live elsewhere in the table above, and design patterns specifically has no confirmed home yet.

**Fit:** Mixed — stronger on security and web GUI/event-driven content than the prior analysis, genuinely unresolved on design patterns, and changed in kind (not degraded, but different) on the collaboration/capstone piece. GIST students targeting desktop GIS add-ins (ArcGIS Pro Python toolboxes, QGIS C++ plugins) still need a platform-specific supplement, as before — the web-platform GUI model doesn't cover that ground and was never expected to.

---

### CC 520 — Database Essentials

**Content:** SQL language, NoSQL and its relation to SQL, DBMS design, programming with databases, database system architecture, database efficiency, practical applications. 3 credits.

**Maps to:** **CIS 260** (Foundations of Relational Databases, currently **1 credit**) for SQL fundamentals — single/multi-table queries, joins, subqueries, views, basic database design, data modification. Deeper coverage (relational algebra, NoSQL, database system architecture) is **CIS 560** (Database System Concepts, 3 credits), flagged in `cs.md` as **"may become an elective."**

**Fit:** Weaker than the prior analysis in one specific way worth naming directly: CIS 260 was itself flagged in a 2026-07-13 density review as compressing roughly two courses' worth of v1 content into a single 1-credit course, and its own database-design module was flagged as a likely trim candidate if that density becomes a real problem. Against CC 520's 3 credits and its own stated coverage of NoSQL and DBMS architecture, CIS 260 alone is a real credit and scope gap — closed only if GIST also selects CIS 560, which (like CIS 575 above) is elective, not required, in the new map.

---

### Web fundamentals course

**Content:** Not specified in the GIST program materials provided.

**Maps to:** **CIS 120** (Web Foundations) — HTML, CSS, JavaScript, with a light seed of human-centered design (wireframing into implementation, applied accessibility standards).

**Fit:** Direct, and more explicitly named than before (the prior mapping relied on an embedded-content course; CIS 120 is now a dedicated, purpose-built web foundations course). Same caveat as before: if GIST's actual requirement is a **web-mapping** course (Leaflet, OpenLayers, Mapbox GL) rather than general web technologies, CIS 120 is the foundation and the mapping-specific tool becomes the partner-department's own domain-application layer, not something the core should try to cover.

---

## Summary table

| GIST Computational Core requirement | New core equivalent | Fit |
|---|---|---|
| CC 110 Introduction to Computing | CIS 115 | Good — cleaner single-course match than before |
| CC 210 Programming Fundamentals | CIS 116 + CIS 200 | Good — MVC placement unconfirmed |
| CC 310 Data Structures I | CIS 300 | Excellent — one course, not three distributed pieces |
| CC 315 Data Structures II | CIS 300 (baseline) + CIS 575 (advanced, elective) | Good — heaps gap now closed; advanced content depends on an elective pick |
| CC 410 Advanced Programming | CIS 200 (OOP) + CIS 251 (security) + CIS 120/220/320 (GUI/event-driven) + CIS 400 (process/capstone) | Mixed — stronger on security and GUI, design patterns unresolved, capstone changed in kind |
| CC 520 Database Essentials | CIS 260 (baseline, 1 credit) + CIS 560 (deeper, elective) | Weaker than before — CIS 260's own density flag plus a real credit gap against CC 520's 3 |
| Web fundamentals course | CIS 120 | Direct (if general web; see note above) |

## What's genuinely new or improved, not just relabeled

- **Security has a clean, confirmed home now.** CIS 251 wasn't specifically named as the authn/authz/threat-modeling/crypto anchor in the prior analysis's era — it is now, and it ties directly to modular arithmetic already sequenced earlier (MATH XXX Recursive and Modular Computation).
- **The web/GUI trajectory is more legible.** CIS 120 → CIS 220 (Platform Programming, Web section) → CIS 320 (User Experience Development, Web section) is a purpose-built three-course progression, versus the prior analysis's story of GUI content scattered across the openings of several unrelated courses.
- **Heaps are no longer a gap.** CSC1040's required outcomes explicitly include heaps; CIS 300 must cover them.
- **Concurrent algorithms and thread-safe data structures are new, required content in CIS 300** — not something CC 310/315 asked for, but relevant to GIST students doing any compute-heavy spatial processing.

## What's weaker or unconfirmed, not carried forward from the old analysis without a flag

- **Design patterns has no confirmed home.** `cs.md` names CIS 400 or CIS 501 as candidates, not a decision.
- **CIS 260's density and credit size are a real, already-flagged concern** — it's the weakest link in this mapping against CC 520.
- **Specific content-level claims from the prior analysis (spatial data structures, road-network routing as a named algorithm example, MVC placement) haven't been re-decided at the new course containers' block-file level.** The prior analysis asserted these as settled content; that level of detail doesn't exist yet for the new map, so this regeneration doesn't repeat those claims as fact.

## Credit comparison

| | Credits |
|---|---|
| GIST Computational Core (estimated) | ~17–20 |
| New core, minimal direct mapping (CIS 115 + 116 + 200 + 300 + 260 + 120) | ~12 (CIS 115 at 2) |
| New core, with elective depth added (+ CIS 575, CIS 560, CIS 251) | ~17 |

Closer to GIST's estimated total when the elective-depth pieces are included, though — as before — those pieces are electives for CS majors too, not guaranteed core content, so GIST selecting them is a deliberate curated choice, not automatic overlap.

## The GIST service pattern

Still a clean instance of the **Curated Foundational Path** pattern: GIST selects a domain-matched subset of the new core. What's changed is that several of the pieces GIST needs most for scope and depth (CIS 575, CIS 560) are now explicitly elective rather than embedded core content, which makes the "curated selection" more literal than it was under the old spiral-embedded design — GIST isn't just picking a subset of required core content, it's actively opting into elective-depth courses alongside it.

## Open questions

1. **Design patterns placement** — unresolved in `cs.md` itself, not just in this mapping. Affects whether CC 410's design-patterns content has a clean new-core home at all.
2. **MVC placement** — not yet re-decided at block-file level for CIS 116/200.
3. **CIS 260 vs. CC 520's scope and credit gap** — the weakest mapping in this document; worth flagging to the Geography department directly rather than presenting as resolved.
4. **Desktop GIS add-ins** — unchanged from the prior analysis; the web-platform GUI model doesn't address ArcGIS Pro/QGIS plugin development, and wasn't meant to.
5. **Python specifically** — unchanged from the prior analysis; the new core's CIS 200/300 language is still undecided (object-oriented, C++/Java/C#-family, per the 2026-07-13 CIS 200 shakedown) and CIS 116 uses Python — GIST's own Python-fluency needs (arcpy, geopandas, shapely, rasterio) should be tracked against whichever language CIS 200/300 land on, not assumed.
6. **Statistics** — unchanged from the prior analysis; confirm whether Geography wants the new core's STAT 410 sequence embedded or prefers its own requirement.
7. **Credit count for CC 110 and CIS 115's own hedge** — both still unconfirmed; resolve together when finalizing this mapping's credit accounting.
