---
name: workflow-platform-design
description: "Design multi-user workflow platforms for requests, cases, approvals and automation runs. Produce domain models, state transitions, permissions and operator interfaces."
---

# Workflow Platform Design

Use for a platform that needs to coordinate people, state and automated work. Start with one representative case and the smallest slice that proves the end-to-end behavior. Use the current project, actors and constraints as source material.

## Design workflow

1. Identify who submits, reviews, executes and operates the case. Establish tenant or workspace scope, ownership and authoritative systems. Distinguish business state, such as approved, from execution state, such as job failed. One case can have multiple runs, so a rerun must not erase case history.
2. Model the entities and their identifiers, relationships, versions and retention needs. Assign one authoritative writer per state transition. Decide whether a request can be edited after submission and which changes invalidate approval.
3. Create a transition table with source state, trigger, eligible actor, preconditions, target state, effects and audit event. Define how concurrent updates are rejected or reconciled. Evaluate permissions and state on the server, including each operation exposed through an API or queue.
4. Define operator views for pending work, case history, run details, actionable errors and recovery. UI actions derive from the same authorization and state rules used by the backend. Audit records identify the actor, case version, decision and outcome.
5. Verify one complete case and a relevant denied, stale or failed path. If implementation is requested, deliver the thin vertical slice and evidence from executed checks. For design-only work, label proposed acceptance scenarios separately from observed results.

## Deliverable

Provide the actor and entity model, business and run states, transition table, permission matrix, integration boundaries, operator views and acceptance cases. Scale the detail to the request.

Read [Request-and-approval example](references/request-approval.md) when review, concurrent edits or failed executions complicate the model. For step execution and recovery details use durable-workflow-automation when available.
