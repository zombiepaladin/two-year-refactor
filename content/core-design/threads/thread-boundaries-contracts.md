+++
title = "Boundaries & Contracts"
weight = 80
ordinal = "1.2.8"
+++

> *Working draft for faculty review. A **spiral** deepens through escalating passes across the two-year core. This is the spiral (meta-thread); one of eight spirals (with three lenses and one bounded practice — twelve threads total, plus two cross-cutting norms).*

**In one line:** A promise about behavior at a boundary, independent of what's hidden behind it — escalating by the kind of boundary the contract spans.

---

## Character

Both a spiral and a meta-thread: it names the common structure beneath ADTs, APIs, schemas, trust boundaries, versioning, and verification. Arguably the strongest expression of the program's systems-thinking ethos — and the thread that absorbed the "boundaries and contracts" idea the now-retired APIs & Networked Systems spiral also carried (confirmed sufficient on its own, 2026-07-15; see `resources/design-log.md`).

## Passes across the two years

| Course | What's new at this pass |
|---|---|
| **CIS 200 / CIS 300** (Y1 Spring / Y2 Fall) | Boundary = an interface within one program: class encapsulation (CIS 200's OOP introduction) and ADT contracts (CIS 300) — names the informal pre/post-condition reasoning seeded earlier. |
| **CIS 220 / CIS 300 / CIS 320** (Y1 Spring / Y2 Fall) | Boundary becomes a process/network boundary: an API contract (request → response), the other side unseen — the CIS 300 (server) / CIS 320 (client) pairing, with CIS 220 carrying the structural-boundary depth. |
| **CIS 260** (Y1 Spring) — Foundations of Relational Databases | Boundary becomes a data/persistence boundary: schema as contract; transaction as all-or-nothing contract. |
| **CIS 251** (Y2 Fall) — Foundations of Cybersecurity | A trust boundary is a contract about what each side may assume — the formalized pass. |
| **CIS 301 / CIS 400** (Y2 Fall / Y2 Spring) | Contracts meet verification and testing: CIS 301 reasons formally about whether a contract holds; CIS 400 checks it empirically (testing, formalized). |
| **CIS 400** (Y2 Spring) — capstone of the core | Defend the boundaries and contracts you designed — the course's live-walkthrough/architecture-defense assessment. Contracts over time: API/semantic versioning as a compatibility contract, closing the loop opened by semver's introduction in CIS 116's professional-practices touch. |

## Connections

- Unifies semantic versioning (Professional Practices), Correctness & Verification (informal-reasoning seed), the networked-computing norm (API contracts), Data Structures (schemas/ADTs), Trustworthy Computing (trust boundaries), and versioning (CIS 400).

## Open questions for faculty review

1. As a meta-thread it adds tracking overhead. Part of the broader thread-legibility question (see Program Overview, Open Questions).

---

*For how this lands in a specific course, see that course's design page under `content/course-designs/`.*
