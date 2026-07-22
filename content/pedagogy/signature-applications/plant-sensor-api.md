+++
title = "Classroom Plant-Sensor API"
weight = 50
ordinal = "3.5"
+++

> *Working draft for faculty review. This page describes a real institutional asset, not a hypothetical example — see [Signature Applications](..) for why the program prefers real assets over invented ones.*

## What it is

An instrumented-classroom project, led by Nathan: Raspberry Pi sensors in classrooms where the program is taught, publishing readings through a live JSON API. It is co-developed alongside the curriculum — capability requests from course design feed back into the project's own roadmap, rather than the curriculum only consuming whatever already happens to exist.

**Status discipline:** every capability is tracked in `resources/reference/plant-sensor-api-roadmap.md` as `requested` (curriculum wants it, not yet safe to depend on), `confirmed` (built and stable — safe to build course content against), or `deferred` (a future possibility, not currently needed). Only the project lead marks a capability `confirmed`.

## What's actually real right now

| Capability | Status | First curricular need |
|---|---|---|
| GET room temperature (no auth) | **requested** | The networking norm's convergence point (shared state + a remote boundary, currently sequenced in CIS 116) |

That's it — a single unauthenticated GET endpoint returning JSON. The no-auth design is deliberate and temporary: it's flagged as a future pairing point for whenever the core's security content lands (CIS 251 now carries that content) — "why would you not leave a write endpoint open the way this read endpoint is" is the intended prompt.

**Deferred, not yet scheduled:** additional sensor readings (humidity, light, soil moisture); authenticated endpoints / write access; historical/time-series data; real-time/streaming access. Each is a plausible future pairing point (security/auth, data structures, concurrency-networking) but none is committed.

## Why a real asset

A live sensor in the student's own classroom makes a network boundary and a JSON response concrete rather than hypothetical from the very first exposure to it, without requiring the curriculum to invent a plausible-sounding fictional API.

## Open questions for faculty review

1. Only one capability is confirmed-requested today. Full course-by-course integration (which course, which assignment, which pass) is `course-designer`'s work once `content/course-designs/` is built out — this page describes the asset, not yet a finished curriculum mapping.
2. The no-auth-endpoint's pairing with CIS 251's security content is a natural fit but not yet a confirmed assignment.

---

*See `resources/reference/plant-sensor-api-roadmap.md` for the live capability-tracking table.*
