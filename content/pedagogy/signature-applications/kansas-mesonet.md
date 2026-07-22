+++
title = "Kansas Mesonet"
weight = 60
ordinal = "3.6"
+++

> *Working draft for faculty review. This page describes a real institutional asset, not a hypothetical example — see [Signature Applications](..) for why the program prefers real assets over invented ones.*

## What it is

The [Kansas Mesonet](https://mesonet.k-state.edu) is K-State's established, live, statewide network of weather observation platforms — precipitation, temperature, humidity, wind, solar radiation, soil conditions, and more. Unlike the plant-sensor API, it isn't co-developed for this curriculum; K-State is pursuing a collaboration with the Mesonet team to expand its API, but the platform itself is external, existing infrastructure with its own operational priorities.

**Authorization status: pending, expected favorable.** Classroom use requires written authorization from the Mesonet director, since Mesonet's public usage policy prohibits automated scraping/data-ingestion without consent — exactly what a full class making repeated automated calls would be. Nathan has an existing working relationship with the Mesonet team and expects a favorable response, but design work that depends on this should treat it as pending, not settled, until confirmed.

## What's actually real right now

| Capability | Status | Notes |
|---|---|---|
| Station list (name, county, lat/lon) | confirmed (public documentation) | `http://mesonet.k-state.edu/rest/stationnames/` |
| Station data by date range/variables | confirmed (public documentation); **classroom use pending authorization** | Returns CSV, not JSON — up to 3,000 records per request |
| JSON response option | requested | No committed course/sequence point yet — wherever CSV parsing would otherwise be a distraction from the actual lesson |

## Why the CSV format matters pedagogically

Mesonet's CSV response is a deliberate format contrast to the JSON convention used by the plant-sensor API and the "Where Did They Go?" data-visualization tool. It's a real, unforced example that "the network boundary" doesn't imply a single data format — worth letting students encounter directly rather than smoothing over by converting to JSON before they see it.

## Open questions for faculty review

1. Classroom-use authorization is the load-bearing open item — anything scheduled to actually reach students needs this double-checked against confirmed status close to delivery, not assumed from this page.
2. No course/sequence point is confirmed yet for any Mesonet-dependent content. Given the statewide-data / applied-statistics character of this asset, CIS 141 (AI/Data Science) and STAT 410 (Statistics for Computing) are the most plausible hosts, but that's an inference, not a decision — flag for `course-designer`.

---

*See `resources/reference/ks-mesonet-roadmap.md` for the live capability-tracking table.*
