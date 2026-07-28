# Data Notice

## Purpose

This repository is a technical sample for the [Europe Truck Dispatch Guard Actor](https://apify.com/kamerozkan/europe-truck-dispatch-guard). It demonstrates three current-schema input recipes and privacy-minimized projections of documented live results.

It is not legal advice, a permit to drive, a live traffic service, a route planner, or a complete temporary-order monitor.

## Audit snapshot

The following state was verified from public Apify API and Store surfaces on 2026-07-28:

| Item | Verified value |
|---|---|
| Actor | `kamerozkan/europe-truck-dispatch-guard` |
| Actor ID | `SiIev8cPVajLV9yqW` |
| Public | `true` |
| Latest build | `0.6.7`, build ID `Ov9M3jptgujNU4KNe`, status `SUCCEEDED` |
| Actor totals | 7 builds, 5 runs |
| Last run start exposed by Store API | `2026-07-28T21:22:15.447Z` |
| Saved tasks | 0 |
| Public Store Examples collection | 0 examples |
| Live result timestamps documented by the Actor | `2026-07-28T13:47:48.897Z` and `2026-07-28T21:22:18.361Z` |

The signed-in owner console showed zero Saved tasks, and the public Store Examples page returned an empty collection during the audit. Therefore none of the three inputs in this repository is presented as a public Apify Example Task.

The Actor build changed after the inspected runs. The current input and dataset schemas were read from successful build `0.6.7`. The latest inspected successful run was `U8FHhQEAhguqWir0o`, used build `0.6.4`, produced one result, and wrote dataset `fmV2nDvMiEFI3PVh2`. Earlier successful run `tLyQjqqumeAmok3tq` used build `0.6.3`, produced two results, and wrote dataset `LC9VxsaySscTkO1Fo`. This repository does not claim runtime validation of build `0.6.7`.

## Input provenance

- [`01_cross_border_public_schema_input.json`](01_cross_border_public_schema_input.json) is the exact default input exposed by the successful `0.6.7` build input schema.
- [`02_cross_border_conditional_replay_input.json`](02_cross_border_conditional_replay_input.json) is the exact input from successful run `U8FHhQEAhguqWir0o`.
- [`03_verified_germany_batch_input.json`](03_verified_germany_batch_input.json) is the exact two-query input from successful run `tLyQjqqumeAmok3tq`.

Input 01 is a current-schema example and was not run during this repository audit. Inputs 02 and 03 are historical run configurations with fixed 2026 dates.

## Output provenance

The Actor README states that two records are unedited output from live runs on 2026-07-28:

- [`01_live_cross_border_prohibited_output.json`](01_live_cross_border_prohibited_output.json) is a field-level projection of the documented `PROHIBITED` row evaluated at `2026-07-28T13:47:48.897Z`.
- [`02_live_cross_border_conditional_output.json`](02_live_cross_border_conditional_output.json) is a field-level projection of the `CONDITIONAL` row from run `U8FHhQEAhguqWir0o`, evaluated at `2026-07-28T21:22:18.361Z`.
- [`03_live_summer_a8_prohibited_output.json`](03_live_summer_a8_prohibited_output.json) is a field-level projection of the `summer-a8-segment` row from run `tLyQjqqumeAmok3tq`, evaluated at `2026-07-26T17:59:21.709Z`.

The public Store README shortened nested route, conflict, country-assessment, and border-visit objects in its display. Those shortened placeholder strings were omitted instead of being published as if they were Actor data. No omitted value was inferred.

The original summer-source title used a Unicode dash. Repository copy normalizes it to an ASCII hyphen; the legal meaning and source URL are unchanged.

## Privacy and secret minimization

The files preserve route coordinates, query IDs, rule identifiers, public official-source links, time windows, decision fields, warnings, and rule-set versions needed to explain the output contract.

The repository excludes:

- Apify API tokens
- signed dataset URLs
- cookies and session material
- proxy credentials and proxy session identifiers
- IP addresses and user-agent strings
- request headers and raw request logs
- account or customer data
- person-level contact data

## Interpretation limits

- `PROHIBITED`, `CONDITIONAL`, `ALLOWED`, and `ERROR` are Actor output states, not legal determinations.
- `CONDITIONAL` means that one or more route facts, temporary orders, exemptions, permits, or documents still require verification.
- `ALLOWED` must not be interpreted as a permit, safety guarantee, or proof that no temporary restriction exists.
- The Actor does not calculate routes, fetch live traffic, verify permits, calculate driver working or rest periods, or fetch temporary orders by itself.
- Geometry and boundary data can differ near borders. Timing quality depends on caller-supplied route data.
- The documented rule sets are versioned for 2026 and do not establish coverage for another year.
- Repeated runs are polling, not continuous real-time monitoring.
- No uptime, freshness, legal completeness, route safety, accuracy, or coverage guarantee is provided.
- This independent Actor is not affiliated with or endorsed by German, Swiss, French, EU, road, police, customs, or transport authorities.

Before dispatch, verify current official rules, route geometry, road spans, temporary orders, vehicle and cargo classification, exemptions, permits, and supporting documents with the responsible authority or a qualified professional.
