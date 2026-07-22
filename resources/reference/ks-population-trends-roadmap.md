# KS Population Trends — Curriculum Capability Roadmap

Partnership: K-State CS + the Chapman Center for Rural Studies (History department). Two coupled systems, used by both CS students and Chapman Center historians/history students — a genuinely cross-disciplinary asset, not CS-internal.

**status** values (same discipline as the plant-sensor roadmap): `requested` / `confirmed` / `deferred`.

## 1. "Where Did They Go?" visualization

Repo: `github.com/ksu-cs/development-project-ksds` (Vue + JavaScript + D3.js frontend, Node.js backend, static JSON/GeoJSON data, MIT license). Active development, 12+ releases as of mid-2026. Visualizes rural population migration in Kansas — county borders, rail/interstate infrastructure, Army Corps of Engineers lakes, town populations, hospitals, schools — with playback over time.

| capability | status | first curricular need | sequence point | notes |
|---|---|---|---|---|
| static GeoJSON/JSON consumption | requested | Data Science track, TBD | batch/generated-data pattern (networking norm — contrast to the live-API pattern used elsewhere) | |

## 2. Historical archive (replacement for a commercial tool — green-field)

Not yet built. Replaces a commercial service the Chapman Center needs to move away from. A prior student-built prototype exists (from a past web development course) but was too closely modeled on the commercial platform's design — a cleaner rebuild is intended, not a port. **This is the one asset where curricular requirements can shape initial design rather than retrofitting onto something already built** — flag any capability request here explicitly as design input to a real, not-yet-started build, not a request against existing functionality.

Purpose: community members and historians upload/correct/share historical records and media tied to Kansas communities (dates, missing data, archival media), with full search. Also generates the static files "Where Did They Go?" consumes.

| capability | status | first curricular need | sequence point | notes |
|---|---|---|---|---|
| community correction/versioning workflow | requested (design input to green-field build) | later concurrency revisit, TBD | recursion-not-repetition revisit of the CS-101 shared-state pairing (Doll, §7) | conflict resolution, audit trails, provenance at collaborative-editing scale. See competency-architect's gap-check on whether `competencies.md` already covers this. |
| public search over historical media | requested | Data Science / IR teaching example, TBD | | |

## Deferred/candidate

- Data provenance / correction-policy / "whose history gets preserved" as an ethics or professional-practice unit anchor — ties directly to the rural-STEM-camp outreach work already underway (NCES locale codes, ~69 partner districts). Not a coincidence — worth treating as one continuous thread of civic-facing CS work rather than two separate projects.ß