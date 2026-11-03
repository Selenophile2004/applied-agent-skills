---
name: agent-workflow-design
description: "Design and implement AI agent workflows that combine model decisions, deterministic steps, tools and observable completion."
---

# Agent Workflow Design

1. Define user goal, inputs, permitted actions, output schema and observable success. Compare a deterministic workflow, a single agent and delegated agents against the actual requirement. Add delegation when evidence shows a distinct need and authorization permits it.
2. Draw the path from request to verified result. For each step specify model judgment, deterministic transformation, tool operation or human decision. Specify state owner, handoff payload, termination conditions and recovery.
3. Design narrow tools and structured outputs with validation. Keep authorization at execution boundaries. Separate trusted instructions from retrieved content. For risky writes specify the approval requirement already applicable to the operation.
4. Build the smallest representative slice. Trace selected tool calls, step status, latency and usage when available. Keep sensitive payloads out of routine traces. Set bounded attempts and surface unresolved work.
5. Evaluate success, missing evidence, bad tool input, a transient failure and an unauthorized action with representative fixtures. Use eval-harness when comparative evaluation is useful. Deliver architecture, contracts, implemented slice if requested and measured results.

## Implementation contract

Record each step's typed input, output, state owner, authorization decision, success signal and failure transition. Distinguish a draft artifact from verified completion. Include terminal states for success, partial result, denied action, exhausted budget and recovery needed.

Use versioned state and carry artifact handles across steps. Validate model-produced arguments before executing tools. Separate the model's proposed action from the server's policy decision. Handle ambiguous write outcomes through reconciliation or idempotency before retry. Reuse the platform's run and recovery machinery when available.

For concrete state transitions and checks, read [a bounded agent workflow](references/applied-workflow.md).
