+++
title = "Cybersecurity"
weight = 20
ordinal = "5.2"
+++

> *Working draft for faculty review.*

## Premise

The B.S. in Cybersecurity shares its first two years in full with the B.S. in Computer Science — the same core, course for course. The upper division is where the two degrees diverge: Cybersecurity adds a security-specific sequence (network programming, information security, cryptography, a security elective, a criminology/society course, and a specialized capstone) in place of the general CS electives.

Because a Cybersecurity student completes essentially the entire Computer Science core plus a full security specialization, this degree map is built to independently satisfy **both** ABET's Computer Science criteria and its Cybersecurity criteria — a graduate of this program should be eligible to have both accreditations recognized, not just the one named on the diploma.

The degree includes two capstone experiences with distinct purposes: **CIS 400**, taken at the midpoint of the program, is a substantial team-based systems project that validates the two-year core before a student moves into specialization coursework. **CIS 599 (Cybersecurity Project)**, taken in the final semester, is the specialization's own capstone. Together they satisfy the major-project requirement in both degrees' ABET criteria.

## Degree Map

| Course | Title | Credits |
|---|---|---|
| **Year 1, Semester 1** | | **14** |
| CIS 115 | Introduction to Computing Science | 2 |
| CIS 116 | Introduction to Programming | 2 |
| DEN 161 | Engineering Problem Solving | 1 |
| CIS 120 | Web Foundations | 1 |
| MATH XXX | Discrete Math: Logic and Sets | 1 |
| MATH XXX | Discrete Math: Counting Finite Configurations | 1 |
| ENGL 100 | Expository Writing I (KSC-1) | 3 |
| — | Core Communication Requirement (KSC-2) | 3 |
| **Year 1, Semester 2** | | **17** |
| CIS 260 | Foundations of Relational Databases | 1 |
| CIS 220 | Platform Programming (Web section) | 1 |
| CIS 200 | Programming Fundamentals | 3 |
| ECE 241 | Introduction to Electrical and Computer Engineering | 3 |
| MATH 220 | Analytic Geometry and Calculus I (KSC-3) | 4 |
| MATH XXX | Discrete Math: Recursive and Modular Computation | 1 |
| MATH XXX | Discrete Math: Graphs, Trees, and Maps | 1 |
| ENGL 200 | Expository Writing II | 3 |
| **Year 2, Semester 1** | | **15** |
| CIS 300 | Data and Program Structures | 3 |
| CIS 320 | User Experience Development (Web section) | 1 |
| CIS 301 | Logical Foundations of Programming | 2 |
| MATH 515 or 551 | Linear Algebra or Applied Matrix Theory | 3 |
| CIS 225 | Foundations of Computer Networks | 1 |
| CIS 251 | Foundations of Cybersecurity | 1 |
| — | Natural & Physical Sciences, with Lab (KSC-4) | 4 |
| **Year 2, Semester 2** | | **15** |
| CIS 141 | AI/Data Science | 1 |
| CIS 308 | C Language Laboratory | 1 |
| CIS 400 | Software Systems Capstone | 3 |
| — | Arts & Humanities (KSC-6) | 3 |
| STAT 410 | Statistics for Computing | 4 |
| SOCIO 211 | Introduction to Sociology (KSC-5) | 3 |
| **Year 3, Semester 1** | | **15** |
| CIS 450 | Computer Architecture and Operations | 3 |
| CIS 501 | Software Architecture and Design | 3 |
| CIS 505 | Introduction to Programming Languages | 3 |
| ENGL 415 or 516 | Technical Writing | 3 |
| — | Social & Behavioral Sciences (KSC-5) | 3 |
| **Year 3, Semester 2** | | **15** |
| CIS 560 | Database System Concepts | 3 |
| CIS 575 | Introduction to Algorithm Analysis | 3 |
| CIS 415 | Ethics and Conduct for Computing Professionals | 3 |
| CIS 655 or 755 | Cybersecurity Elective | 3 |
| — | Free Elective (KSC-7) | 3 |
| **Year 4, Semester 1** | | **15** |
| CIS 525 | Introduction to Network Programming | 3 |
| CIS 551 | Fundamentals of Computer and Information Security | 3 |
| CIS 553 | Fundamentals of Cryptography | 3 |
| — | Arts & Humanities (KSC-6) | 3 |
| CRIM 550 | Cybercrime, Security, and Society | 3 |
| **Year 4, Semester 2** | | **15** |
| — | Required Technical Elective | 3 |
| CIS 599 | Cybersecurity Project (Capstone) | 3 |
| — | Upper Division Elective | 3 |
| — | Upper Division Elective | 3 |
| — | Upper Division Elective | 3 |
| **Total** | | **121** |

**Math elective note**: choosing MATH 515 or 551 for the Year 2 math slot satisfies both the shared core's linear-algebra requirement and Cybersecurity's own math-elective requirement with a single course.

## ABET Cybersecurity Requirement Fulfillment

ABET's Cybersecurity criteria require at least 45 semester credit hours of computing and cybersecurity coursework, applying six crosscutting concepts across eight fundamental knowledge areas, plus at least 6 semester credit hours of mathematics covering discrete math and statistics.

**Re-checked against CIS 251's real, drafted learning objectives, 2026-08-04.** Every CIS 251 citation below was checked against its actual 7 SLOs and 8-week schedule (`content/course-designs/cis-251.md`) — see `specialization-model.md`'s "seed → deep spiral" section for the same check. CIS 251 is a broad, intro-level survey course — CIA triad, common threats/attackers, defensive best practices, risk/incident response, ethics/privacy/law, emerging tech/careers — not a course with explicit threat-modeling methodology, named least-privilege/trust-boundary concepts, or applied cryptography tied to the core's modular-arithmetic content. That changes which rows below it genuinely supports.

**Crosscutting concepts**

| Concept | Where it's applied |
|---|---|
| Confidentiality, Integrity, Availability | CIS 251 (SLO 2, the CIA triad by name), CIS 260 (access control), CIS 551 |
| Risk | CIS 251 (SLO 4, Week 6 risk management), CIS 551 |
| Adversarial thinking | CIS 251 (SLO 3, Week 4 threats/attackers — survey-level, not formal adversarial modeling), CIS 551, CIS 553 |
| Systems thinking | Woven throughout the core's data-structures, networking, and systems coursework (CIS 300, 225, 400, 450) |

**Eight fundamental areas**

| Area | Coverage |
|---|---|
| Data Security | CIS 260, CIS 251 (Week 2 authn/authz, Week 5 encryption/backups — generic, intro-level), CIS 553 |
| Software Security | CIS 400, CIS 551. **CIS 251 removed 2026-08-04** — its real content has no software-security material (no secure coding, no vulnerability classes like injection/buffer overflow); the earlier citation overclaimed |
| Component Security | CIS 300 (interfaces, contracts), CIS 501 — see faculty concerns below |
| Connection Security | CIS 225, CIS 525. (CIS 251's Week 3 — IP addresses, DNS, packets — touches this lightly, but CIS 225 already owns the depth here.) |
| System Security | CIS 400, CIS 450, CIS 551 |
| Human Security | CRIM 550, **CIS 251** (Week 4 — phishing, social engineering, insider threats is a direct, well-supported match; strengthened from "see faculty concerns below," this is one of CIS 251's strongest fits, not a thin one) |
| Organizational Security | CRIM 550, **CIS 251** (Week 6 — risk assessment and incident-response planning is org-level activity; a light but real contribution) — still the thinnest area even with this, see faculty concerns below |
| Societal Security | CRIM 550, SOCIO 211, CIS 415, **CIS 251** (Week 7 — ethics, privacy, regulations, responsible behavior is a strong, direct match; added 2026-08-04, previously missing from this row despite being one of CIS 251's clearest fits) |

**Advanced depth**: CIS 551, CIS 553, CIS 525, and the CIS 655/755 elective provide advanced cybersecurity coursework building on the crosscutting concepts and fundamentals above.

**Computing and cybersecurity credit hours**: the CIS-prefixed coursework in this map (shared core plus specialization) totals well over 50 semester credit hours, clearing the 45-hour floor with room to spare.

**Mathematics**: the discrete-math sequence (4 credits) and statistics course (4 credits) total 8 semester credit hours, clearing the 6-hour floor.

## ABET Computer Science Requirement Fulfillment

ABET's Computer Science criteria require at least 30 semester credit hours of computing coursework (including techniques and tools for computing practice, security and privacy principles, and the societal impacts of computing), of which at least 40 semester credit hours must be CS-specific — covering algorithms and complexity, computer science theory, programming language concepts, and software development in substantial depth; substantial depth in at least one general-purpose language; exposure to computer architecture, information management, networking, operating systems, and parallel and distributed computing; the study of computing systems at varying levels of abstraction; and a major project. Separately, at least 15 semester credit hours of mathematics and statistics are required, including discrete mathematics, probability, and statistics, at a rigor at least equivalent to introductory calculus.

**Algorithms, theory, languages, and software development**: CIS 300 and CIS 575 (algorithms and complexity); CIS 115, CIS 301, CIS 505, and CIS 220/225 (computer science theory — computability, formal languages, automata); CIS 505 (programming language concepts); CIS 400, CIS 501, and CIS 300's server-layer and concurrency work (software development).

**General-purpose language**: CIS 116 and CIS 200/300 provide sustained, substantial work in a single general-purpose language across three courses.

**Exposure areas**: computer architecture (CIS 115); information management (CIS 260, CIS 560); networking (CIS 225, CIS 525); operating systems and parallel/distributed computing — **corrected 2026-08-04**: CIS 220 gives a light, genuine OS-exposure touch ("browser as mini-OS"), but the deeper formalization this row used to attribute to CIS 220/CIS 300 core content was never actually built there (see `resources/reference/spiral-threads.md`'s correction note). Coverage instead rests on **CIS 525** in this map's required Year 4 sequence — but see the concern flagged below: unlike the AI Systems map, this degree hard-codes CIS 525 alone rather than the general Systems Elective choice (CIS 520/525/625), so it may not independently clear the OS-exposure half of this requirement the way CIS 520 or CIS 625 would.

**Abstraction across scales**: the core's progression from representation (CIS 115) through data structures (CIS 300) to systems and architecture (CIS 450, CIS 501) demonstrates computing systems at multiple levels of abstraction.

**Major project**: satisfied jointly by CIS 400 (core-level systems project) and CIS 599 (specialization capstone).

**Mathematics**: MATH 220 (calculus), the discrete-math sequence, STAT 410, and the Year 2 math elective (MATH 515 or 551) together total 15 semester credit hours, meeting the floor exactly.

**Security, privacy, and societal impact** (general-criteria requirement, not CS-specific): CIS 251, CIS 415, and CRIM 550.

## Concerns for Faculty

1. **MATH 221 (Calculus II) is not included in this map.** It appears in the currently-published Cybersecurity requirements, but neither ABET criteria requires it specifically, and no course in this map depends on it as a prerequisite. Removing it is a substantive change from the published curriculum and should be confirmed explicitly, not treated as incidental.
2. **The CS mathematics floor (15 SCH) is met exactly, with no margin.** Any future adjustment to the math sequence, the statistics course, or the Year 2 math elective should be checked against this floor before being made.
3. **Component Security and Organizational Security are the genuinely thin areas of the eight ABET Cybersecurity fundamental areas — Human Security is not.** CIS 251's Week 4 (phishing, social engineering, insider threats) is a direct, well-supported match for Human Security. Component Security has no CIS 251 support at all (that course has no component/architecture-level content) and still leans entirely on CIS 300/CIS 501's general contract/interface framing. Organizational Security gets a light, real boost from CIS 251's Week 6 (incident-response planning) but is still the thinnest of the eight — coverage still leans mostly on CRIM 550. Likely candidates for explicit attention remain CIS 551 (component/system security) and CIS 599 (organizational context, if the capstone project is scoped to include it).
4. **The dual-purpose capstone structure (CIS 400 + CIS 599) should be confirmed as satisfying both degrees' major-project requirements**, since CIS 400's scope is general systems work, not security-specific — the CS major-project requirement is clearly met, and the Cybersecurity major-project requirement rests on CIS 599 alone carrying that weight for the specialization.
5. **Total program length is 121 credit hours**, one hour above the currently-published 120-hour total. This matches the Computer Science degree's own total under this design and is not specific to Cybersecurity, but both should be reconciled together if 120 is a hard institutional ceiling.
6. **ABET operating-systems exposure for this specific degree map needs a direct check.** This map requires CIS 525 (Network Programming) alone in Year 4, rather than the general Systems Elective choice (CIS 520 Operating Systems I / CIS 525 / CIS 625 Concurrent Software Systems) the AI Systems map uses. The core content this exposure claim used to rest on (deep OS/concurrency formalization) was found to have no confirmed home anywhere in the core (`resources/reference/spiral-threads.md`, 2026-08-04). Confirm whether CIS 525 alone still clears the ABET OS-exposure bar for Cybersecurity, or whether this map needs a second required course from the Systems Elective list.
7. **New, 2026-08-04 — CIS 251's real content is narrower than earlier framing assumed, and this ripples beyond this table.** `specialization-model.md`'s "seed → deep spiral" section claims cyber upper-division courses (CIS 551, 553) can assume threat modeling, least privilege, trust boundaries, and applied cryptography with a modular-arithmetic tie-in from CIS 251 — none of which are in its real 7 SLOs or 8-week schedule (which covers CIA triad, threat/attacker survey, defensive best practices, risk/incident response, and ethics/privacy/law, at an intro-survey level throughout). That page has been corrected with a caveat; whether CIS 251 should be *redesigned* to actually carry that deeper content (matching the original design intent), or whether CIS 551/553 need to assume less and teach more themselves, is a real open decision for course-designer/faculty — not resolved by this correction.
