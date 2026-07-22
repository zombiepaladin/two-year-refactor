# Plant Sensor API — Curriculum Capability Roadmap

Source project: instrumented classroom plants, Raspberry Pi sensors, published API. This project is under active development, led by Nathan — curriculum needs can inform its design, not just consume whatever already exists. This doc is the shared surface between curriculum design and API design: capabilities course-designer wants get logged here as requests, and Nathan reconciles them against the sensor project's actual feasibility/timeline.

**status** values:
- `requested` — curriculum wants it, not yet confirmed built. Not safe to depend on in a block.
- `confirmed` — Nathan has confirmed it exists and is stable enough to depend on. Safe to build block content against.
- `deferred` — logged as a future possibility, not currently needed.

Only Nathan changes a row's status to `confirmed`.

| capability | status | first curricular need | sequence point | notes |
|---|---|---|---|---|
| GET room temperature (no auth) | requested | CS-101 | networking norm, step 6/7 convergence | deliberately minimal — single unauthenticated GET, JSON response. No-auth choice is deliberate and temporary — flagged as a future pairing point for whenever the core introduces a security/auth unit ("why would you not leave a write endpoint open the way this read endpoint is"). |

## Deferred/candidate capabilities (not yet scheduled)

- Additional sensor readings (humidity, light, soil moisture?) beyond temperature
- Authenticated endpoints / write access (e.g. actuator control) — natural pairing point for a later security/auth unit
- Historical/time-series data — natural pairing point for data structures / data science track
- Real-time/streaming access — natural pairing point for a later concurrency-networking convergence