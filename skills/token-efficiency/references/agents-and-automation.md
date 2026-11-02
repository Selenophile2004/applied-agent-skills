# Agents and automation

Use for building agent applications and automated workflows. Building an agent does not itself authorize dispatching worker agents during this task.

- Define the agent's objective, inputs, outputs, tool boundaries, state and success criteria. Choose the simplest architecture that meets them; add retrieval, memory, orchestration or multiple agents only for an actual requirement.
- Keep stable shared instructions concise. Retrieve task-specific evidence and tool definitions on demand using supported mechanisms; retain complete authoritative material where the decision requires it. Avoid repeatedly embedding full documents, conversation history or duplicate tool output.
- Return selected fields, summaries and recoverable handles from tools; perform deterministic filtering and transformation in code. Preserve errors, continuation/pagination information, provenance and the data needed for the next decision.
- Cache only when inputs, permissions and freshness make reuse valid; define invalidation. Keep durable task state outside repeated prompts when the platform supports it. Do not add keep-alive calls merely to preserve a cache.
- Design bounded retries, explicit completion/failure states and loop recovery. Runtime limits should expose incomplete work and preserve progress, not silently truncate it or mark it successful.
- Record available input/output/cache usage, tool calls, latency and retries. Include child-agent cost when relevant. Evaluate quality before trading model capability, context or verification for lower cost; do not silently downgrade models.
- Verify representative success and failure paths, tool contracts and relevant permissions. Scope evaluation to the requested functionality and authorized resources; preserve approval boundaries for actual external actions.
