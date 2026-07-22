# Real-World Assets Index

Real institutional projects available as curricular assets. Each has its own roadmap doc tracking curricular capability requests against actual project state. Prefer a real asset over an invented example wherever one plausibly fits — check this index before proposing a hypothetical for any networking, concurrency, or embedding-systems pairing.

| asset | status | primary track relevance | primary norm(s)/scope | roadmap doc |
|---|---|---|---|---|
| Classroom plant-sensor API (Raspberry Pi sensors in instrumented classrooms) | co-developed (requested/confirmed cycle, led by Nathan) | Foundations (all tracks) | networking (live JSON API), embedding-systems | `plant-sensor-api-roadmap.md` |
| "Where Did They Go?" visualization (Vue + JS + D3.js, KSDS project, partnership with the Chapman Center for Rural Studies, History dept.) | active development, external repo (github.com/ksu-cs/development-project-ksds); **being built for eventual multi-state reuse, not Kansas-only** (2026-07-15) | Data Science flagship (1 of 2); cross-disciplinary embedding-systems for all tracks | networking (batch/generated static JSON + GeoJSON), embedding-systems, human-interaction | `ks-population-trends-roadmap.md` |
| Historical archive (replacement for a commercial tool currently used by the Chapman Center) | green-field / planned, not yet built | Data Science + ethics/embedding-systems anchor for all tracks | concurrency (collaborative editing/versioning, later spiral revisit), embedding-systems, human-interaction | `ks-population-trends-roadmap.md` (shared doc, own section) |
| Kansas Mesonet (climate sensor network, mesonet.k-state.edu) | established, live, external ownership; API-expansion collaboration in progress; classroom-use authorization pending (expected favorable) | Data Science flagship (2 of 2) | networking (live CSV API — format contrast to the JSON-based assets above), embedding-systems (real usage-policy/authorization constraints) | `kansas-mesonet-roadmap.md` |

## Notes on using this index

- **"Where Did They Go?" and the historical archive are a cross-disciplinary asset.** Real stakeholders outside CS (Chapman Center historians, community members) depend on or contribute to this pipeline. Embedding-systems teaching here should surface multi-stakeholder dependency ("what if CS changes the static-file format and History's workflow silently breaks"), not just infrastructure failure modes.
- **The historical archive doesn't exist yet.** Treat any capability request against it as design input to a genuinely green-field build, not a request against something already built.
- **Kansas Mesonet's CSV format is a deliberate contrast point** to the JSON convention used by the plant-sensor and KSDS assets — a useful moment for teaching that "the network boundary" doesn't imply a single data format, not something to smooth over by converting to JSON before students see it.
- **Kansas Mesonet's classroom-use authorization is pending, not confirmed.** See `kansas-mesonet-roadmap.md` for status tracking.