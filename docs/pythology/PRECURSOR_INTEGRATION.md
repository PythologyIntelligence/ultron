# Pythology Precursor Collective Intelligence — Integration Contract

Status: DEVELOPMENT / NOT DEPLOYED. This integration does not modify Prometheus or any laboratory yet.

## Objective
Use Ultron Memory, Skill and Harness Hubs as a controlled knowledge layer for Prometheus environmental precursor research across EnviroArc, Atlas (New Zealand focus), Weather, and Subterranean.

## Research namespaces
- `enviroarc`: cross-domain environmental context, cascading hazards and impacts.
- `atlas`: New Zealand-focused observations and regional baselines.
- `weather`: meteorological precursor and extreme-weather investigations.
- `subterranean`: seismicity, geology, fault mechanics and earthquake-precursor hypotheses.

## Required memory record
Each proposed record MUST include:
- `record_id`, `namespace`, `created_at_utc`, `source_id`, `source_uri` (where applicable)
- `observation_window`, `region`, `sensor_or_dataset`, `method_version`
- `claim`, `evidence_refs`, `limitations`, `provenance`
- `evidence_status`: `observed` | `published` | `hypothesis` | `simulated` | `validated` | `refuted`
- `review_status`: `proposed` | `reviewed` | `approved` | `rejected`
- `confidence_basis` (not an unsupported numeric certainty)
- `visibility`: `domain` | `cross_domain`

## Rules
1. No direct production ingestion until namespace isolation, authorization and provenance are implemented and tested. Current Ultron endpoints must be security-reviewed.
2. Never convert correlation into causation or a prediction without out-of-sample validation.
3. Never turn an unreviewed memory into an executable skill or deploy an evolved skill automatically.
4. Share only approved, sanitized, provenance-bearing records across domains. Default to domain-only visibility.
5. Preserve competing explanations, null results, monitoring gaps, instrumentation changes and regional baseline differences.
6. Subterranean comparisons must stratify by fault type, depth, geology, geography and monitoring coverage; compare global, fault-class and region-specific baselines.
7. Atlas retains a New Zealand baseline while permitting explicitly labelled global comparisons.
8. Maintain audit trails for all imports, updates, review decisions, skill revisions and agent access.
9. Do not upload credentials, personal data, raw private logs or proprietary source material to public Ultron endpoints.
10. Keep Prometheus and live research services unchanged until explicit deployment approval.

## First acceptance tests
- Reject a record missing source provenance.
- Reject unsupported evidence_status values.
- Deny cross-domain retrieval of unapproved records.
- Retrieve an approved cross-domain record without losing its evidence label.
- Prevent automatic skill activation from hypotheses.
- Demonstrate that contradictory and negative findings are retained.
- Demonstrate rollback and export before production connection.

## Next implementation phase
Build an isolated adapter with schema validation, namespace authorization, review queue and retrieval filters; unit-test with synthetic records. Then trial against non-sensitive, read-only exports from the four labs. Only after a successful security and science review should Prometheus receive a production connector.
