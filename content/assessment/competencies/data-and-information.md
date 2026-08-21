---
title: "Data and Information"
pre: "3. "
weight: 30
---

*Re-checked against real course-design pages, 2026-08-04 — see `resources/design-log.md`. This is the domain most affected by unplaced/unconfirmed content: a data-integration scenario and a responsible-AI/data-analysis capstone from earlier design drafts both anchor several rows below, and neither has a confirmed new-course home except the AI-code-critique slice (→ CIS 141). One genuine resolution: the honest-visualization pass under Communicate Data Insights turns out not to depend on that unplaced content after all — it's confirmed CIS 320 content instead. STAT 410 (replacing the old four-course statistics sequence) has no drafted content yet, so its rows are flagged rather than verified.*

### Represent Information

**I can select and apply appropriate representations for information within computational systems.**

I organize and model information in ways that support effective storage, communication, analysis, and processing.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 115 (Y1 Fall) | Primary home for first pass — bits, booleans, number systems, bitwise operations; the most primitive representation layer. **The stack/heap memory-model half of this pass is unconfirmed** — `cs.md`'s CIS 115 entry explicitly lists it as not moved there, same finding as elsewhere in this pass. |
| CIS 200 (Y1 Spring) | CSV/JSON as format choices — file formats as representation decisions. |
| CIS 300 (Y2 Fall) | Linear structures, stacks, queues, trees as representation choices; ADT contract abstracts over representation. Confirmed. |
| CIS 300 (Y2 Fall) | Trees, hashing, hierarchies. **Spatial indexing (quadtrees, R-trees, geohashing) is proposed, not built** — see `cis-300.md`'s "Proposed Changes," already flagged in the lens pass. | 
| CIS 260 (Y1 Spring) | Relational model as formal queryable representation; schema design as domain-to-model translation. |
| CIS 300 (Y2 Fall) / CIS 400 (Y2 Spring) | Graphs as a general relationship representation (CIS 300); choosing between representations, defended (CIS 400, Design Review re-homing). **"Document" as a representation option is not actually in the core** — non-relational/NoSQL coverage was confirmed dropped from the core entirely (only in the CIS 560 elective), so a relational-vs-document comparison isn't available within the two-year core the way this row implies; relational-vs-graph is. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Algorithm Evaluation Task (constrained) — compare two provided representations for a given problem and justify the choice |
| Independence | Design Brief (open-ended) — given a domain, select and design an appropriate representation without a template |
| Adaptation | CIS 400's team-project representation work — represent a complex multi-faceted domain where no single representation suffices, within the core's own scope. (The old "System Integration Project" ceiling is now at the Year 3–4 capstone.) |
| Leadership | Design Review (CIS 400) — defend representation choices to peers; TA/LA mentoring representation decisions |

**Recurring types:** Algorithm Evaluation Task (comparing representation options) and Design Brief (designing a data model or schema) cover this sub-competency — no dedicated type needed.

---

### Manage Data Resources

**I can acquire, store, transform, and integrate data from multiple sources to support computational goals.**

I work with structured and unstructured data using appropriate technologies, formats, and workflows.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 200 (Y1 Spring) | First pass — parsing, filtering, reshaping, aggregating; CSV/JSON as sources and sinks. **"Data minimization as embedded practice" here is thin** — the confirmed privacy-by-design content sits at CIS 120 instead (see `lens-trustworthy-computing.md`'s narrowed row), not CIS 200. |
| CIS 200 / CIS 300 (Y1 Spring / Y2 Fall) | APIs as data sources — consuming (the "consume" verb). |
| CIS 260 (Y1 Spring) | SQL — querying and transforming relational data. Query optimization specifically is still a proposed, undrafted addition. |
| CIS 260 (Y1 Spring) | Schema design with integrity constraints; Data Investigation signature assessment anchored here (confirmed). Transactions and concurrent access are still a proposed, undrafted addition (`cis-260.md`'s "Proposed Changes"). |
| *unplaced* | Integration pass — combining disparate heterogeneous sources; NoSQL for data that resists relational structure (also unavailable in the core, see Represent Information above); re-identification risk from dataset combination. Same orphaned data-integration content flagged throughout this pass. |
| *unplaced* | Notebook-based pipeline — integrative culmination of acquisition, transformation, and preparation across the full data lifecycle. Depends on unconfirmed data-analysis/responsible-AI content with no current course home. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured data pipeline task — given sources and a specified target output, implement the acquisition and transformation |
| Independence | Open-ended data management — given an investigative question, acquire, clean, and prepare the data needed to answer it |
| Adaptation | Data Investigation (CIS 260) — integrate sources with data quality, privacy, and integrity constraints, within the core's own scope. (The old "System Integration Project" co-anchor is now at the Year 3–4 capstone.) |
| Leadership | TA/LA mentoring data pipeline design; leading data integration retrospectives |

**Recurring type:** Data Pipeline Task — deepens from single-source CSV/JSON transformation (CIS 200) through CIS 260's Data Investigation signature assessment; full-lifecycle notebook pipeline work is unplaced pending a course-designer/faculty decision on where it lands.

---

### Investigate Questions with Data

**I can use computational and statistical methods to investigate questions and evaluate evidence.**

I collect, prepare, analyze, and interpret data to support conclusions and decision-making.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| STAT 410 (Y2 Spring) | First formal pass — descriptive statistics and data summarization; computing and interpreting summary measures and distributions. **STAT 410 has no drafted content yet** — confirmed as the successor to the old four-course non-calculus statistics sequence, now compressed into one 4-credit course, but this and the other STAT 410 rows below can't be checked against real content the way this pass has checked the CIS-numbered rows. |
| CIS 260 (Y1 Spring) | Data Investigation signature assessment — investigate a question using a novel dataset. Confirmed, matches `signature-assessments.md`. |
| STAT 410 (Y2 Spring) | Probability as the foundation for inference — reasoning about uncertainty in evidence. Same STAT 410 caveat. |
| STAT 410 (Y2 Spring) | Random variables, distributions, and sampling — designing sampling strategies, evaluating distributional evidence. Same STAT 410 caveat. |
| *unplaced* | Culminating pass — full notebook-based investigation integrating statistics, visualization, and ethical framing. Depends on the same unconfirmed data-analysis/responsible-AI content flagged above. |
| STAT 410 (Y2 Spring) | Correlation and regression — investigating relationships between variables; causal vs. correlational reasoning. Same STAT 410 caveat. |

Note: STAT courses feed Crystalis evidence via LTI — statistical investigation demonstrated in the statistics sequence counts as competency evidence.

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured investigation — given a dataset and a question, apply specified statistical methods and interpret results |
| Independence | Open-ended investigation — given a domain question, independently design and execute the full investigation |
| Adaptation | Data Investigation (CIS 260 signature) — novel dataset, student-driven question. (A previously-assumed co-anchor — integrative analysis with ethical accountability — remains unconfirmed, not resolved to a specific course.) |
| Leadership | Peer review of analytical methods; TA/LA mentoring investigation design; presenting findings to non-technical audiences |

**Recurring type:** Data Investigation — deepens from guided descriptive statistics (STAT 410, undrafted) through CIS 260's signature event; the full notebook-investigation ceiling once envisioned for this domain is unplaced pending a course-designer/faculty decision.

---

### Communicate Data Insights

**I can create visualizations and explanations that communicate data-driven findings to intended audiences.**

I present results in forms that support understanding, interpretation, and action.

**Primary evidence contexts:**

| Course | Work |
|--------|------|
| CIS 120 (Y1 Fall) | First pass — HTML/CSS visual hierarchy and accessibility; semantic markup as information design; legibility and access as baseline communication goals. Confirmed (CIS 120's real "Web Accessibility" topic). |
| CIS 320 (Y2 Fall) | Binding data to visual marks programmatically; dynamic/interactive rendering, consuming data from the CIS 300 service layer. **Unconfirmed** — proposed, not yet drafted; see `cis-320.md`'s "Proposed Changes." |
| STAT 410 (Y2 Spring) | Statistical visualization — histograms, box plots, scatter plots as communication of distributional properties. STAT 410 has no drafted content yet. |
| CIS 400 (Y2 Spring) | Design Review — communicating data-driven design decisions to critical peers and faculty under scrutiny. Re-homed here per `signature-assessments.md`. |
| CIS 320 (Y2 Fall) | Culminating pass — honest visualization and data ethics; accountability for what a visualization claims and implies. **Resolved, not unplaced**: this is CIS 320's confirmed REPRESENT pass (`thread-human-centered.md`), not the unconfirmed data-analysis content this domain's other rows depend on — the one row here with a confirmed home. Still proposed/undrafted at the course level, but with a confirmed home. |

**Assessment types by level:**

| Level | Assessment type |
|-------|----------------|
| Application | Structured visualization task — given data and an audience, create a specified chart or visual explanation |
| Independence | Open-ended data communication — given data and a communication goal, design and implement an appropriate visualization without a template |
| Adaptation | CIS 320's honest-visualization work — novel domain with ethical documentation, mixed/public audience, within the core's own scope |
| Leadership | TA/LA reviewing visualization choices and teaching visual communication; leading critique sessions on chart design and honest representation |

**Recurring type:** Data Communication Task — deepens from accessibility/legibility focus (CIS 120) through ethical accountability for public-facing visual claims (CIS 320). Audience escalates: any reader (CIS 120) → technical (CIS 320 implementation) → analytical (STAT 410) → public with ethical accountability (CIS 320 culminating pass).
