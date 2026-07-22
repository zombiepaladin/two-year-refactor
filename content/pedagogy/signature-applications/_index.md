+++
title = "Signature Applications"
weight = 40
ordinal = "3.4"
+++

> *Working draft for faculty review. The signature-application concept — teaching against real, institutionally-grounded systems rather than invented examples — is a pedagogical design decision, not yet fully ratified. This page describes the concept; the companion pages describe each real asset.*

## The concept

Wherever a course needs a networked, data-bearing, or embedding-systems example, the program prefers a real institutional asset over a hypothetical one. A live sensor, a real state agency's data feed, a real community's archive make the underlying idea — a network boundary, a data format, a stakeholder who depends on this system continuing to work — concrete rather than assumed.

This is a deliberate discipline, not a stylistic preference: every asset referenced in course design is tracked in `resources/reference/real-world-assets-index.md` against its own capability roadmap, with each capability marked `requested` (curriculum wants it, not yet safe to depend on), `confirmed` (verified and stable — safe to build course content against), or `deferred` (a future possibility, not currently needed). Only the asset's own owner marks a capability `confirmed`. **Course content should never depend on a capability that isn't `confirmed`.**

## The four real assets

| Asset | Domain | Status |
|---|---|---|
| [Classroom Plant-Sensor API](./plant-sensor-api) | Environmental sensing, co-developed for this program | One capability requested; live but minimal |
| [Kansas Mesonet](./kansas-mesonet) | Statewide environmental monitoring, external/established | Live and public; classroom-use authorization pending |
| [Data-Visualization Tool ("Where Did They Go?")](./data-visualization) | Kansas rural population history, external/active development | Context and consumption source, not a build target |
| [Historical Archive](./historical-archive) | Kansas community history archive, green-field | Not yet built — CIS 400's confirmed capstone domain |

A fifth project, **Chrysalis** (a competency-tracking and messaging platform), is real infrastructure actually being built for the program, but its role as an *instructional* asset — something students read or build against, rather than simply use as a tool — is not yet confirmed. It isn't covered here as a signature application until that's decided.

## Why real assets over invented ones

1. **Stakes.** Each asset is used by real people — Kansas historians, K-State's own environmental-monitoring mission, students' own classroom. The work is not hypothetical.
2. **Land-grant relevance.** K-State's land-grant mission — serving Kansas through education, research, and outreach — is structural in these choices, not ornamental. The Mesonet and the historical archive both connect directly to that mission.
3. **Honest constraints.** Real assets come with real constraints — an external project's release cadence, an agency's authorization process, a not-yet-built system's actual scope. Those constraints are themselves a teaching point (embedding-systems reasoning), not friction to design around.

## Open questions for faculty review

1. **Course-by-course integration is not yet designed.** Each asset page tracks what's real; which course uses which capability at which pass is `course-designer`'s work once `content/course-designs/` is built out, not something asserted here.
2. **Chrysalis's instructional role.** Confirm whether Chrysalis should ever become a signature application in this sense, or remain program infrastructure only.
3. **Asset stability during assessment windows.** External or live assets (Mesonet, "Where Did They Go?") can change independently of the curriculum's schedule — a policy for insulating graded assignments from upstream changes may be needed once specific course integrations are designed.

---

*See `resources/reference/real-world-assets-index.md` for the authoritative asset list and each asset's roadmap doc.*
