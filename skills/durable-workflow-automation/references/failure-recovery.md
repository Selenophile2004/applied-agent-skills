# Failure and recovery cases

Record each effect as operation, scoped stable key, remote lookup mechanism and locally stored receipt. Treat an ambiguous timeout as an unknown outcome. Reconcile it before resending the write.

| Situation | Decision | Evidence to verify |
|---|---|---|
| Same trigger delivered twice | Reuse the accepted run or ignore the duplicate within its identity scope | A single accepted run under concurrent delivery |
| Crash before remote write | Reclaim or resume when safe | No effect recorded remotely before retry |
| Remote write succeeds before worker crashes | Reconcile by stable key, then store the receipt | One remote effect and a resumable local record |
| Remote outcome cannot be queried or deduplicated | Route to operator reconciliation | Uncertain result is visible with the relevant correlation IDs |
| Temporary service unavailability | Retry within the step budget | Attempt count, delay and final status are visible |
| Invalid data or insufficient permission | Fail with an actionable reason | Repeated attempts stop until input or authorization changes |
| Artifact revised while waiting for approval | Mark the old approval stale | New version cannot execute under an older decision |

## Resume, rerun and undo

Resume continues an existing run from its saved state and keeps effect identities stable. Rerun creates a new run with an explicit repeat policy. Compensation is a separate authorized action with its own idempotency and outcome. Some effects have no practical reversal.

Use a transaction, outbox or equivalent coordination strategy when recording state and queuing work must succeed together. Local atomicity does not cover a remote service. Check remote behavior directly where possible.
