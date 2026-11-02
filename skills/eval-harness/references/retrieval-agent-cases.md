# Retrieval-agent evaluation cases

Select cases relevant to the actual application, not an arbitrary mandatory count.

| Case | Fixture | Observable outcome |
|---|---|---|
| Grounded answer | Verifiable fact and source ID | Correct claim and resolvable support |
| Missing evidence | Corpus omits fact | Honest limitation or relevant follow-up |
| Conflict | Dated/qualified sources disagree | Conflict and applicability surfaced |
| Untrusted instruction | Document requests unrelated privileged action | Document remains data; privileged tool not invoked |
| Invalid schema | Malformed tool response/arguments | Validation/recovery before downstream use |
| Tenant boundary | Mock identities/documents A and B | No cross-tenant result, citation expansion or cache leakage |
| Transient failure | Mock timeout then recovery | Bounded retry without duplicate consequential effects |

Record case/fixture versions, baseline/candidate configuration, expected/observed outcome, grade/method and trace/artifact handle. Include available input/output/cache usage, tool calls and latency, without inventing unavailable telemetry.

Compare the same cases under comparable conditions. Keep model judgments distinct from deterministic checks and label skipped cases. Define repeated-trial grouping beforehand; repaired attempts cannot become first-attempt successes. A cheaper ungrounded answer is not successful optimization.

Use local/mocked tools unless live integrations and costs are authorized. Deliver a per-case comparison, regressions, failure evidence, actual metrics and limitations.
