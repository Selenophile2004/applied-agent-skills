# Transactional APIs, Tenant Caches and Durable Jobs

## Inputs

Existing stack/contracts, data invariants, tenancy, durability requirements and tests.

## Deliverables

Focused implementation/design, contract/invariant notes and relevant failure-path verification.

## Applied request

~~~text
Design an idempotent create-order endpoint with tenant isolation, atomic inventory checks and durable background processing.
~~~

## Acceptance criteria

No blind write retries; concurrency invariants; tenant-safe cache/invalidation; durable required jobs; justified infrastructure.

## Use this skill

Claude Code: /backend-patterns. Codex: $backend-patterns. Claude chat: enable the uploaded individual skill and describe the task.

Read [SKILL.md](SKILL.md) for the workflow and conditional references. Tools, model access and source inputs come from your environment.

[Install for your platform](../../docs/installation.md) | [Catalog](../../README.md)
