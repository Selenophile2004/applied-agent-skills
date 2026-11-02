---
name: backend-patterns
description: Implement backend APIs, data access, caches and jobs for Node.js/TypeScript services; use for substantive server-side changes, with patterns adapted to the existing stack.
metadata:
  source: https://github.com/WorldFlowAI/everything-claude-code
  source-commit: 432485ba6b92c14fb357276a98957f348bcff9ee
  adaptation: Codex; English; task-scoped; 2026-11-02
---

# Backend implementation patterns

Use for implementing or materially changing Node.js/TypeScript services, Express or Next.js API routes, database access, caches and background jobs. Preserve the project's stack and contracts; other stacks can reuse general principles without importing Node-specific APIs.

- Inspect the relevant endpoint, data model, authorization boundary and existing implementation. Choose only the layers the task needs; do not introduce repositories, queues or microservices by default.
- Keep API contracts explicit: runtime input validation, consistent errors, pagination/filtering, status codes and backwards compatibility. Enforce resource/tenant authorization separately from authentication.
- Select needed fields, batch related queries and inspect actual query behavior to avoid N+1 work. Use transactions for genuine atomic invariants, parameterized operations and migrations appropriate to the change.
- Design caches with explicit keys, tenant/permission isolation, freshness and invalidation. Choose shared storage when cross-instance consistency matters; process-local caches and limiters are not distributed guarantees.
- Retry transient failures with bounds, backoff and cancellation where appropriate. Retry writes only with idempotency or equivalent protection. Preserve meaningful errors, timeouts and partial-failure state.
- Use durable queues for jobs that must survive process restarts. Define retries, deduplication, concurrency and failure handling according to requirements; an in-memory example is not a durable job system.
- Keep logs useful and redacted; preserve request correlation without exposing credentials or user data. Validate affected contracts, data integrity and failure paths with existing commands, broadening checks when dependencies require it.
- Make focused changes and reuse existing libraries/runtime. Do not add infrastructure, dependencies or deployments solely to conform to a pattern.

For implementation illustrations, search the relevant API, Database, Caching, Error Handling, Authorization or Background Jobs heading in [upstream reference](https://github.com/WorldFlowAI/everything-claude-code/blob/432485ba6b92c14fb357276a98957f348bcff9ee/skills/backend-patterns/SKILL.md). Read only needed sections. The samples require validation against current library APIs; do not copy them as complete middleware, authorization or durable-queue implementations.
