# Kansas Mesonet — Curriculum Capability Roadmap

Established, live platform (`mesonet.k-state.edu`) — not co-developed the way the plant-sensor project is, but K-State is pursuing a collaboration with the Mesonet team to revise/expand their API. Two distinct kinds of entries belong here: capabilities that already exist (confirmed, per public documentation), and capabilities the curriculum would like to request as part of the API-expansion collaboration (following the same requested/confirmed/deferred discipline as the plant-sensor roadmap, but confirmation depends on Nathan's actual collaboration with the Mesonet team, not on curriculum design alone).

## Authorization status: pending (expected favorable)

Nathan has contacted the Mesonet director to confirm written authorization for classroom use. Not yet confirmed, but a favorable response is expected given an existing working relationship and Mesonet's general support for educational use. Design work may proceed on this assumption; anything scheduled to actually deliver to students should have its Mesonet-dependent pieces double-checked against `status = confirmed` closer to delivery, not assumed settled from this note alone.

Mesonet's public usage policy explicitly prohibits automated scraping/data-ingestion without written consent ("to prevent unauthorized use and dependencies") — this is exactly the scenario a full class making repeated automated calls represents, which is why explicit authorization matters here in a way it doesn't for most public APIs.

## Existing capabilities (per public REST documentation; format: CSV, not JSON)

| capability | status | notes |
|---|---|---|
| station list (name, county, lat/lon) | confirmed (public doc) | `http://mesonet.k-state.edu/rest/stationnames/` |
| station data by date range/variables | confirmed (public doc); **classroom-use pending authorization** | returns CSV — a deliberate format contrast to the plant-sensor and KSDS assets' JSON convention; up to 3000 records per request |

## Requested (curriculum-driven API-expansion asks)

| capability | status | first curricular need | notes |
|---|---|---|---|
| JSON response option | requested | TBD — wherever CSV parsing would be a distraction rather than the point | would remove an accidental-complexity tax when the lesson isn't specifically about CSV parsing |