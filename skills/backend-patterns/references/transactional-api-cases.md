# Transactional API, cache and job contract

Specify tenant/caller scope, input schema, success/error shape, pagination, compatibility and relevant timeout behavior.

## Create-order design exercise
State the invariant: accepted orders and inventory reservations agree under concurrency. A separate preflight read and write do not automatically preserve it; use the actual database's atomic mechanism.

For idempotent creation, define key scope, payload equivalence, concurrent duplicate handling, prior responses and failed/in-progress attempts. A generic retry wrapper must not duplicate writes.

When a committed change must reliably produce a job, inspect the existing transaction/outbox mechanism. An in-memory enqueue after commit is not durable. Consumers need acknowledgement, duplicate handling, retries and observable failure state as required.

## Tenant cache
Keys include relevant tenant, resource, permission/version and query dimensions. Define invalidation for updates/access changes. A process-local limiter does not enforce distributed quotas.

## Verify
Select relevant cases: invalid input, unauthorized access, concurrency, duplicate submission, timeout, worker restart and stale cache. State checks unavailable against the actual database/queue. Deliver focused changes, invariant notes and observed evidence; this exercise is not a production implementation.
