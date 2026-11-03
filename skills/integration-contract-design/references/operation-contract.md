# Operation contract and fixtures

## Template

| Field | Detail |
|---|---|
| Operation | One business action and its version |
| Caller | Authenticated context and required grants |
| Input | Schema, units, bounds, date rules and unknown-field handling |
| Output | Stable IDs, status, evidence handles and cursor when applicable |
| Effects | State changed, effect key scope, repeat and reconciliation behavior |
| Failure | Stable outcome code, user action and retry classification |
| Resources | Request limits, timeouts and meaningful observability |

## Example

A reporting tool returns a bounded page of approved metrics for a period. Inputs include metric ID, period, optional dimensions and cursor. Caller scope comes from trusted context. Output includes rows, units, source identifiers and a next cursor. The cursor is tied to the original filters and scope. Empty results remain distinct from forbidden access and provider failures.

For a write tool, an example idempotency scope is tenant plus operation plus key. An accepted repeat with an equivalent payload returns the existing result. A conflicting reuse receives an explicit error. If the provider cannot determine an earlier write's outcome, expose a reconciliation state with a correlation handle.

## Fixtures

- Valid scoped input returns only authorized records with consistent units.
- Out-of-range period or malformed cursor is rejected before downstream work.
- A cursor from another scope or changed filters is rejected.
- Empty data returns a valid empty response.
- Transient provider failure is distinguishable from permanent failure.
- For writes, equivalent replay yields one effect and conflicting replay yields an actionable error.

Keep examples small. Record actual protocol and service behavior where it differs from the proposed contract.
