---
name: coding-standards
description: Apply maintainable TypeScript, JavaScript, React and Node.js conventions during substantive implementation or code-quality reviews, following existing project rules.
metadata:
  source: https://github.com/WorldFlowAI/everything-claude-code
  source-commit: 432485ba6b92c14fb357276a98957f348bcff9ee
  adaptation: Codex; English; task-scoped; 2026-11-02
---

# Coding standards

Use when establishing coding conventions, implementing substantial TypeScript/JavaScript/React/Node.js changes, or reviewing code quality in those stacks. Follow the repository's formatter, linter, architecture and public contracts. Adapt principles to other languages without imposing JavaScript-specific rules.

- Prefer clear names, explicit interfaces and the simplest design meeting the current requirement. Reuse established utilities; avoid speculative abstractions, unrelated cleanup and mechanical rewrites.
- Use useful types and runtime validation at external boundaries. Avoid unchecked assertions and broad any types where they conceal actual uncertainty. Static types do not validate network or model output.
- Preserve error context and handle failures at appropriate boundaries. Do not swallow failures or replace actionable causes with generic messages; redact sensitive details at external interfaces.
- Parallelize independent operations only, respecting resource limits and failure semantics. Handle every result when using partial-success APIs and propagate cancellation where appropriate.
- Treat shared state and React props/state as immutable. Local mutation can be appropriate when controlled and safe; do not impose universal copying that harms correctness or performance. Copy before mutating shared arrays with sort or similar APIs.
- Keep React state updates and hook dependencies correct. Preserve accessibility and user-visible behavior. Memoization, lazy loading and new abstractions need a practical reason; do not add them indiscriminately.
- Preserve API response and compatibility conventions. Use parameterized queries and the existing validation mechanism; security-sensitive work may need focused security review.
- Keep functions and modules cohesive. Size and nesting are review signals, not arbitrary universal gates. Comment on non-obvious intent or invariants; avoid restating code.
- Run meaningful affected checks and required project checks. Do not mandate tests for trivial reversible edits, require blanket TDD, or invent a universal 80% coverage gate.

For examples of naming, types, React, APIs and test organization, search the matching heading in [upstream reference](https://github.com/WorldFlowAI/everything-claude-code/blob/432485ba6b92c14fb357276a98957f348bcff9ee/skills/coding-standards/SKILL.md). Read only useful sections. Its absolute style prescriptions and snippets are illustrative; current repository contracts and this entrypoint govern adaptation.
