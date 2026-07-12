# Block Inventory

The structural unit is the **1-credit, 8-week course**. Courses are deliberately small and short so that prerequisite chains stay short and parallel — a topic that would traditionally be one large course (e.g. databases) is split across several 1-credit courses that can be sequenced flexibly. Eight 8-week blocks span two years (two blocks per semester).

The math department is co-designing a sequence of discrete math courses landing in the first year, following the same 8-week format, emphasizing cross-curriculuar connections, supporting the competency assessment platform, and integrating the spiral curriculum considerations.

Additionally, students will take a series of traditional math and statistics courses: in the second semester, a 4-credit caclulus course, in the third semester a 3-credit linear algebra course, and in the fourth semester a four-credit statistics course. These courses will likely not be integrated into the competency platform. However, the stats course will be co-desgined to a degree - we can specify desired topical coverage and depth.

| Block | CS courses | External (co-designed) |
|---|---|---|
| B1 | CS-101 Imperative Programming; CS-102 Functional Programming; CS-103 Computational Representation | MATH-101 Discrete Math: Logic and Sets |
| B2 | CS-104 Data Transformation & Manipulation; CS-105 Code Reading & Repair; CS-106 Web Foundations & Data-Driven Rendering | MATH-102 Discrete Math: Counting Finite Configurations |
| B3 | CS-107 Software Modeling and Design; CS-108 Computational Abstractions; CS-109 Abstract Data Types | MATH-103 Discrete Math: Recursive and Modular Computation |
| B4 | CS-110 Trees, Hashing & Hierarchies; CS-111 Systems & APIs; CS-112 Algorithmic Design Patterns | MATH-104 Discrete Math: Graphs, Trees, and Networks |
| B5 | CS-201 SQL Fundamentals; CS-202 Database Design; CS-203 Non-Relational Databases | |
| B6 | CS-204 Software Testing & Validation; CS-205 Security Fundamentals; CS-206 Collaborative Development | |
| B7 | CS-207 Graphs & Network Algorithms; CS-208 Data Integration & Application-Database Interfaces; CS-209 OSI Networking Fundamentals | |
| B8 | CS-210 Deployment & Operations; CS-211 Human-Centered Design & Validation; CS-212 Data Analysis & Responsible AI | |

## Course-level status

The table above tracks blocks; this table tracks individual course scoping status as block files are completed. **Only rows listed here have been scoped to block-file completeness** — absence from this table means the course is still at "working description" stub level (see `content/course-designs/`), not that it's been deprioritized.

| Block | Code | Title | Status | Prerequisites | Competencies covered |
|---|---|---|---|---|---|
| B1 | CS-101 | Imperative Programming | draft | none (program entry point) | SD.2, CR.1, CR.2, PP.1, PP.2, HCP.4 |
| B1 | CS-102 | Functional Programming | draft | none (co-scheduled with CS-101/CS-103/MATH-101) | SD.2, CR.2, CR.1, PP.1, PP.2, HCP.4 |
| B1 | CS-103 | Computational Representation | draft | none (co-scheduled with CS-101/CS-102/MATH-101) | CR.3, SI.1, PP.1, DI.1, CR.1, HCP.3 |

All three B1 CS courses are now built to full block-file completeness (see `content/course-designs/block-1/`). Status remains **draft**, not **stable**, for all three — each file's own open questions flag unpiloted density risk, and CS-103 in particular is flagged as needing a pilot pass before being trusted as a stable design. MATH-101 remains stub-only (external, co-designed by the math department — not this role's file to complete) but now has a concrete week-pairing ask from CS-103 (see below).

**Flags from the 2026-07-09 CS-101 pass (historical — see `resources/design-log.md` for full rationale):**
- ~~CS-101's HTML/CSS-reading-substrate framing had no logged rationale~~ — **RESOLVED (2026-07-09, follow-on revision):** confirmed by direct user instruction to be a misplaced duplication; removed, already lived fully in CS-106.
- ~~CS-101's concurrency seed likely affects CS-102's scope (companion pass)~~ — **RESOLVED (2026-07-12):** CS-102 is now built with this as firmly-adopted content at its own Week 7, not a recommendation.
- ~~CS-101's mutable-variable-assignment topic (Week 2) is a pairing point for CS-102~~ — **RESOLVED (2026-07-12):** CS-102's Week 2 is built to match exactly.
- ~~CS-101's Week 7 cross-references CS-103's OS-process seed~~ — **RESOLVED (2026-07-12):** CS-103 is now built with its own Week 6 process-execution seed explicitly cross-referencing CS-101's Week 7.
- ~~CS-101's stack/heap widget proposes a concrete/formative (CS-101) vs. formal/graded (CS-103) split, needing CS-103's confirmation~~ — **RESOLVED (2026-07-12):** CS-103 is built adopting exactly this split, at its own Week 6, and extends the same tool to register-level tracing.
- Density: CS-101's own open questions still flag Weeks 3 and 6 as having little slack — unresolved, unchanged this session.

**New flags from the 2026-07-12 block-scale build (CS-102 + CS-103 completed; see `resources/design-log.md` for full rationale):**
- **New same-block content, not previously flagged:** CS-101's Week 7 now also includes a bounded, surface-level glimpse of the shared-memory hazard itself (a hand-traced lost-update example), and CS-102's Week 7 sharpens it (immutability avoids the hazard by construction). This revises the previously-logged B1→B8 concurrency spacing judgment — see both files' "Concurrency seed"/"Concurrency companion pass" sections and `content/core-design/threads/thread-computational-models.md`'s updated B1/B8 rows. **Recommend confirming CS-210 (B8) is scoped to explicitly recall and resolve this puzzle**, not just introduce synchronization cold.
- **Recursion is now explicit connective tissue, not two unrelated topics:** CS-101 Week 6 and CS-102 Week 6 use the *same* worked recursive function, from two angles (memory-trace vs. elegance/composition). **The specific function has not been chosen** — flagged as a shared open item in both files' "Recursion: one function, two angles" sections; whoever authors the actual widget/exercise content should pick one function and update both files together.
- **CS-103's register-transfer model (new content) has no identified forward spiral link** — unlike every other new topic this session, I could not find a natural later-block reinforcement point. Flagged in CS-103's own open questions; may be fine as a single-pass foundational topic, but noted since every other thread in this program has an explicit spiral trace and this one currently doesn't.
- **CS-103's VS Code register-view tool bridge is unconfirmed** — may require switching from Python (used everywhere else) to a small C debugging target (GDB/LLDB register views), a bigger ask than CS-101's same-language tool bridge. Needs confirmation from whoever holds the actual plugin.
- **CS-103's 8-bit float layout (1 sign + 4 exponent, bias 7 + 3 mantissa)** is a specific design proposal made this session, not a confirmed decision — flagged for faculty confirmation in CS-103's own file.
- **MATH-101 cross-tie now has a concrete week proposal:** CS-103 proposes its own Week 2 (Boolean logic/bitwise) as the pairing point with MATH-101's truth-tables/predicate-logic/sets content. `content/course-designs/block-1/math-101.md` was **not edited** (external, math-department-owned) — this is a confirmation ask for MATH-101's co-designers, not a settled fact.
- **CS-103 is the densest of the three B1 courses** — its own open questions give an honest, non-forced density read and recommend piloting before treating it as stable, more so than CS-101 or CS-102.
- **No missing competency IDs were found this session.** Per instruction, competency-ID gaps are to be flagged to the competency-architect agent rather than resolved here — none were needed; all new content (recursion, shared-memory glimpse, Babbage, binary/float representation, registers) mapped cleanly onto existing IDs in `resources/reference/competency-framework.md`.
