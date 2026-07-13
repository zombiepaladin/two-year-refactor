+++
title = "Block 5 — Store"
weight = 50
ordinal = "1.1.5"
+++

**Year 2, Fall · Weeks 1–8 · 8-week block · 3 credits**

> *Working draft for faculty review. Course codes are placeholders. This block is one of eight; it is best read alongside the two-year arc below.*

**Two-year arc:** Read (B1) → Modify (B2) → Model (B3) → Structure (B4) → **➤ Store (B5)** → Build responsibly (B6) → Judge (B7) → Operate (B8)

---

## Purpose

**Cognitive frame:** INFORMATION AT REST: shared, persistent, queryable structure — the Year-2 escalation from Year 1's data-in-motion.

**Essential question:** *How do we store, share, query, and describe information that outlives the program?*

INFORMATION AT REST: shared, persistent, queryable structure — the Year 2 escalation from Year 1's data-in-motion. Persistence motivator (why files aren't enough) opens SQL Fundamentals; Database Design carries schema-as-contract (Boundaries), data minimization + access control (Security), transactions/concurrency (Computational Models), and anchors the Data Investigation assessment. STAT-101 descriptive statistics pairs here (describe the data you now store). Relational Databases offered as a 2-credit service unit, followed by a partner department's domain-application course (the service-course model).

## Structure

Computer science courses (2):

| Code | Course | Cr | Focus |
|---|---|---|---|
| CS-201 | **SQL Fundamentals** | 1 | Opens with the persistence motivator (why files are not enough — durability, concurrent access, querying, integrity), then SELECT/INSERT/UPDATE/DELETE/JOIN. Query-optimization seed (indexes, query plans). SQL named explicitly as DECLARATIVE querying (state what data; the planner finds how) — the same declarative idea as HTML, now for data (Computational Models pass). First half of the Relational Databases service unit. |
| CS-202 | **Database Design** | 1 | Schema design, normalization, relational modeling. Schema-as-contract (Boundaries); data minimization + access control (Security); transactions/concurrency (Computational Models); schema-decision documentation. Anchors the Data Investigation signature assessment. Solo Git branching + AI design-discussion embedded. Second half of the Relational Databases service unit. |
| CS-203 | **Non-Relational Databases** | 1 | The three major non-relational storage models as a complete landscape alongside the relational model from CS-201/202: document databases (JSON-document model, schema flexibility, MongoDB-style querying), key-value stores (conceptual; O(1) lookup, cache layers), and graph databases (Neo4j/Cypher; pattern-matching queries). Storage-model choice as a design decision — what does the data's natural shape suggest? Graph spiral: graph databases as the persist pass (model B3 → represent B4 → persist here → algorithms B7). Completes the full storage landscape for B7 integration work. |

Co-designed external courses (1):

| Code | Course | Cr | Notes |
|---|---|---|---|
| STAT-101 | **Descriptive Statistics & Data Summarization** | 1 | (External/co-designed, stats dept. Describe data the student is now storing; feeds the data-visualization throughline. First of the statistics-for-ML sequence.) |

**Block load:** 4 concurrent courses (3 CS + 1 external), 3 credits.

## Threads passing through this block

Competencies are program-level and developed across many blocks; this block is one context in which they are demonstrated. The threads with a pass here:

- **Data Structures & Representation** — Relational data as a formal, queryable model; non-relational models (document, key-value, graph) as the design-space alternatives — the full storage landscape (pass 4).
- **Boundaries & Contracts** — Schema as a contract about data shape; transaction as an all-or-nothing contract (pass 3).
- **Computational Models** — Concurrent data access, transactions, rollback — a third error-handling model (pass 4).
- **Trustworthy Computing (lens)** — Data minimization in schema design; access control as a schema dimension (who can see what).
- **Optimization (lens)** — Query optimization — indexes, query plans.
- **Professional Practices — documentation (lens)** — Document schema decisions (ties to the data-minimization justification).
- **Human-Centered Computing** — Visualize query results as a tool for Data Investigation, not just presentation (pass 3).
- **Professional Practices — version control (lens)** — Solo feature branching — try a schema alternative safely (pass 3).
- **AI-Assisted Development (bounded)** — AI as a design-alternatives/tradeoff discussion partner; student justifies the final choice (medium stakes).

## Open questions for faculty review

1. Service-course model: SQL Fundamentals + Database Design form a 2-credit "Relational Databases" service unit, intended to be followed by a partner department's domain-application course (e.g. business data applications) — together a one-semester progression for a visiting student. This is the general service-course model: we own the domain-neutral foundation, the partner owns the application.
2. This reverses an earlier idea (round 7) of pushing Database Design into Block 6 to make a full-semester service course; keeping both in Block 5 protects Block 6 from further density.
3. External pacing now runs as math B1–B4 (consecutive) and statistics B5–B8 (consecutive). B5 now carries STAT-101 Descriptive Statistics. Load is regular across the curriculum (six blocks of 4 courses, two of 3).
4. Probability ownership is unresolved: the discrete-math draft's Course 2 already covers finite/counting-based probability through Bayes, while the statistics sequence wants continuous probability + distributions. Likely split (discrete owns finite, stats owns continuous) but this is for the cross-department co-design meeting.

---

*Spine position: **Store**. Builds on Block 4. Leads into Block 6.*
