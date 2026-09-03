# Computational Data Science

Proposed degree map swapping the new two-year core into a B.S. in Computational Data Science, assembled from existing K-State CIS and Statistics courses — no prior official degree to draw from, so this is a first construction. Checked against both `resources/reference/abet/cs.md` (Computer Science criteria) and `resources/reference/abet/ds.md` (Data Science criteria), on the same dual-degree premise as the Cybersecurity and AI maps.

**Positioning note**: K-State's Statistics department already offers a B.S. in Statistics and Data Science (`stats-ds.md`), built on a calculus-first, mathematical-statistics spine. This degree is deliberately **CS-flavored** rather than a duplicate — heavier on programming, data engineering, and systems, drawing on Statistics coursework for inferential depth rather than rebuilding it.

**Course-level constraint, per direct instruction**: undergraduates may take 700-level courses; 800-level and above is excluded. This is a materially different constraint than the AI degree map used (which excluded 700+ entirely) — worth double-checking against the AI map, since some of its proposed-new courses (534/535/536/597) may have had usable 700-level equivalents already sitting in the catalog. Not revisited here; flagged as a separate open item.

## Years 1–2 (= `cs.md`, not reproduced)

Identical to the shared core — see `cs.md` for the full annotated version.

| Semester | Courses | Credits |
|---|---|---|
| Y1S1 | CIS 115, CIS 116, DEN 161, CIS 120, MATH XXX Logic and Sets, MATH XXX Counting Finite Configurations, ENGL 100, Core Communication Requirement (KSC 020) | 14 |
| Y1S2 | CIS 260, CIS 220, CIS 200, ECE 241, Calculus Slot, MATH XXX Recursive and Modular Computation, MATH XXX Graphs/Trees/Maps, ENGL 200 | 17 |
| Y2S1 | CIS 300, CIS 320, CIS 301, Linear Algebra Slot, CIS 225, CIS 251, KSC 040 | 15 |
| Y2S2 | CIS 141, CIS 308, CIS 400, KSC 060, STAT 410, Social & Behavioral Sciences (KSC 050) | 15 |

**Math elective note**: choosing MATH 515 or 551 for the Linear Algebra Slot (Y2S1) covers the linear-algebra spanning concept in the ABET DS criteria directly, and is also a prerequisite for STAT 760 (below).

## The Data Science course pool

Unlike the AI map, **every course in this pool already exists** — no new courses are proposed here.

| Course | Title | Credits | ABET DS topic served |
|---|---|---|---|
| CIS 531 | Intro to Programming Techniques for Data Science and Analytics | 3 | Data preparation and integration |
| CIS 533 | Introduction to Data Science Foundations | 3 | Data preparation, data analysis, data ethics (covers several lifecycle topics in one course) |
| CIS 560 | Database System Concepts | 3 | Data management |
| CIS 561 | Introduction to Data Science in Practice | 3 | Major project (capstone-bearing practicum) |
| STAT 511 | Introductory Probability and Statistics II | 3 | Applied statistical inference |
| STAT 705 | Regression and Analysis of Variance | 3 | Data analysis, model development |
| STAT 745 | Statistical Graphics | 3 | Visualization and communication |
| STAT 760 | Optimization for Data Science | 3 | Optimization |
| STAT 766 | Applied Data Mining / Machine Learning | 3 | Model development and deployment |

## Years 3–4 — Data Science–specific

### Year 3, Semester 1 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| CIS 450 | CIS 450 (Computer Architecture and Operations) | Direct match, satisfies CS ABET |
| CIS 501 | CIS 501 (Software Architecture and Design) | Direct match |
| CIS 505 | CIS 505 (Introduction to Programming Languages) | Direct match |
| Technical Writing Requirement | ENGL 415 or ENGL 516 | Direct match |
| Social & Behavioral Sciences (KSC 050, 2nd of 2) | Stays generic | No DS-specific course identified for this bucket |

### Year 3, Semester 2 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| CIS 560 | CIS 560 (Database System Concepts) | Direct match — required here regardless of `cs.md`'s general elective hedge |
| CIS 575 | CIS 575 (Introduction to Algorithm Analysis) | Direct match |
| CIS 415 | CIS 415 (Ethics and Conduct for Computing) | Contributes to the ABET DS "data ethics" spanning concept alongside CIS 533; see faculty concerns |
| Unrestricted Elective | **STAT 705** (Regression and ANOVA) | Foundational statistics — no calculus prerequisite beyond one prior stats course; positioned first in the STAT sequence |
| Free Elective (KSC 070) | Stays generic | — |

### Year 4, Semester 1 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| Systems Elective | Student choice (CIS 520/525/625) | Not DS-specific; left as genuine student choice |
| Required Technical Elective #1 | **CIS 531** (Programming Techniques for Data Science) | Satisfies the slot's "CIS 500+" rule |
| Required Technical Elective #2 | **CIS 533** (Data Science Foundations) | Same |
| Arts & Humanities (KSC 060, 2nd of 2) | Stays generic | — |
| Unrestricted Elective | **STAT 511** (Introductory Probability and Statistics II) | Sequenced after STAT 705; must precede STAT 760 |

### Year 4, Semester 2 — 15 credits (unchanged from `cs.md`)

| Slot (per `cs.md`) | Filled with | Note |
|---|---|---|
| Required Technical Elective | Stays generic | All DS-specific CIS requirements already placed |
| Capstone | **CIS 561** (Introduction to Data Science in Practice) | Capstone-bearing practicum — also plausibly serves the ABET "application area" requirement if the practicum project is scoped to a specific domain (a natural fit with this curriculum's existing real-world data assets — the historical archive, Kansas Mesonet, or plant-sensor API — rather than an invented example) |
| Upper Division Elective | **STAT 745** (Statistical Graphics) | Needs STAT 705, already satisfied by Y3S2 |
| Upper Division Elective | **STAT 760** (Optimization for Data Science) | Needs STAT 511 and linear algebra, both satisfied by this point |
| Upper Division Elective | **STAT 766** (Applied Data Mining / ML) | Needs STAT 705, already satisfied |

**Years 3–4 subtotal: 60 credits — identical to `cs.md`'s own Year 3–4 total.**

## Credit total

| | Y1S1 | Y1S2 | Y2S1 | Y2S2 | Y3S1 | Y3S2 | Y4S1 | Y4S2 | **Total** |
|---|---|---|---|---|---|---|---|---|---|
| Credits | 14 | 17 | 15 | 15 | 15 | 15 | 15 | 15 | **121** |

Identical to `cs.md`'s, the Cybersecurity map's, and the AI map's own totals.

## ABET Data Science floor check

ABET's DS criteria require **≥45 SCH of data science coursework** — a single combined floor, not separate computing/math floors the way CS, Cybersecurity, and AI each have. The shared core's CIS-prefixed credits (~23 SCH, since "computing including data structures and algorithms" is explicitly one of the DS spanning concepts, the same logic that let general CS coursework count toward Cybersecurity's and AI's floors) plus the nine specialization courses above (27 SCH) total roughly **50 SCH**, clearing the floor without relying on any generic elective slot.

## Open items, not resolved here

1. **The calculus-sequencing tension, carried forward honestly from the prior CS-side analysis, not solved by this map.** The shared core's Calculus Slot only guarantees one of Calc I/II/III (typically Calc I). STAT 511, in particular, and any deeper mathematical-statistics work beyond it, may assume more calculus than that single course provides. This map sequences STAT 511 as late as Year 4 Semester 1 specifically to maximize the chance any calculus prerequisite has been satisfied by then, but that hasn't been verified against STAT 511's actual prerequisite chain.
2. **ABET's "data ethics including legitimate use and algorithmic fairness" and "governance including privacy, security, and stewardship" spanning concepts are covered generally** (CIS 533's societal-aspects content, CIS 415, CIS 560's access-control material) **but not by name.** Whether general coverage is sufficient or whether these need explicit, named treatment somewhere is a faculty judgment call, not resolved here.
3. **"Data acquisition and representativeness"** is covered by CIS 531's data-integration content and general sampling discussion in the statistics sequence, but — like item 2 — not named explicitly anywhere.
4. **The CIS 561 capstone practicum's application-area scoping is not decided.** It plausibly satisfies both the ABET major-project and application-area requirements at once if scoped to a real domain, but which domain (and whether that decision belongs to this document or to whoever builds the course) is open.
5. **Worth revisiting**: since 700-level courses turn out to be usable for undergraduates (800+ is the actual exclusion, not 700+), the AI degree map's proposed new courses (CIS 534/535/536/597) should be checked against whether existing 700-level equivalents could have been used instead, at least for CIS 535 (paired with existing CIS 835) and CIS 536 (paired with the eventual CIS 836). Not revisited in this document.
