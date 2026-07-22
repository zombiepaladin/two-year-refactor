+++
title = "Historical Archive"
weight = 80
ordinal = "3.8"
+++

> *Working draft for faculty review. This page describes a real institutional asset, not a hypothetical example — see [Signature Applications](..) for why the program prefers real assets over invented ones.*

## What it is

A green-field replacement for a commercial tool the Chapman Center for Rural Studies (History department) currently uses and needs to move away from. **Not yet built** — a prior student-built prototype exists from a past web development course, but it was too closely modeled on the commercial platform it was replacing, and a cleaner rebuild is intended rather than a port.

Purpose: community members and historians upload, correct, and share historical records and media tied to Kansas communities (dates, missing data, archival media), with full search. It also generates the static files the [data-visualization tool](./data-visualization) ("Where Did They Go?") consumes — the two are coupled but distinct systems.

**This is the one asset where curricular requirements can genuinely shape initial design**, rather than retrofitting course content onto something already built. Any capability request here is design input to a real, not-yet-started build.

## What's actually real right now

| Capability | Status | First curricular need |
|---|---|---|
| Community correction/versioning workflow | requested (design input to the green-field build) | A later concurrency revisit — a recursion-not-repetition return to the shared-state pairing seeded early in the core, now at collaborative-editing scale (conflict resolution, audit trails, provenance) |
| Public search over historical media | requested | Data Science / information-retrieval teaching example, sequence point TBD |

## The confirmed connection to CIS 400

This is the real-world domain behind CIS 400's redesign as a capstone-of-the-core: a substantial, deliberately ambiguous-requirements team project (small teams, rotating scope by cohort) building toward this system, not toward "Where Did They Go?" or any other asset. See `resources/reference/degree-maps/cs.md`'s CIS 400 entry for the full rationale — the short version is that a well-defined-spec solo project let AI complete milestones without the student demonstrating understanding, and an ambiguous, authentic, rotating-scope team project closes that gap. CIS 400 also needs real contributor accounts for this system — distinguishing historian/community-contributor edit rights from public anonymous viewing is a genuine, substantial application of CIS 251's authentication/authorization content, at integration scale.

## Deferred, worth tracking

Data provenance, correction policy, and "whose history gets preserved" as an ethics or professional-practice anchor — this ties directly to K-State's rural-STEM-camp outreach work already underway (NCES locale codes, ~69 partner districts), worth treating as one continuous thread of civic-facing CS work rather than two separate projects.

## Open questions for faculty review

1. Full curriculum integration beyond CIS 400 itself (which other courses touch this asset, and how) is not yet designed — flagged for `course-designer`.
2. The community-correction/versioning workflow's "later concurrency revisit" sequence point is directional, not scheduled against a specific course yet.

---

*See `resources/reference/ks-population-trends-roadmap.md` for the live capability-tracking table (shared with the data-visualization tool).*
