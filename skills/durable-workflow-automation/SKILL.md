---
name: durable-workflow-automation
description: "Design or implement recoverable automations with persisted state, idempotent effects, bounded retries, human approvals and operator recovery."
---

# Durable Workflow Automation

Use when work can outlive a process, be delivered more than once, wait for a decision or fail partway. Reuse the project's orchestration and storage when they support the required guarantees.

## Design and implement

1. Specify the trigger, event identity, validated inputs and observable completion. Map each step to its inputs, durable outputs, dependencies and externally visible effects.
2. Persist acceptance and use a scoped deduplication key. Protect concurrent delivery with a unique constraint, atomic claim or equivalent mechanism. Identify every write that can be accepted remotely before its local completion is recorded. Choose a stable effect key and a way to check the remote outcome.
3. Store workflow version, run and step status, attempt, result handle and effect identity. Resume from saved outcomes and preserve successful effects. Distinguish retryable failures, permanent errors and unknown outcomes. Define a time budget, attempt limit, backoff and recovery path for each retry policy.
4. Persist required approvals with artifact version, actor, decision and expiry. Enforce them at execution time. Define what cancellation stops, which effects are already committed, and whether compensation is available.
5. Make run ID, failed step, outcome status and the next safe action available to operators. Distinguish resume, rerun and compensation in both UI and run history.
6. Verify duplicate delivery, concurrent claim, failure before and after a remote write, and safe resumption as applicable. Use authorized fixtures. Report evidence from executed checks and identify unresolved outcomes.

## Deliverable

Provide a step graph or state table, persistence and recovery rules, effect and approval contracts, and actual verification results. For design-only work, provide acceptance scenarios. For implementation, include the runnable workflow and environment assumptions.

Read [Failure and recovery cases](references/failure-recovery.md) when a workflow performs external writes or offers manual recovery.
