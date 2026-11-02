---
name: security-review
description: Review application and agent security when requested or when changing authentication, permissions, secrets, sensitive data, payments or exposed tool/API boundaries.
metadata:
  source: https://github.com/WorldFlowAI/everything-claude-code
  source-commit: 432485ba6b92c14fb357276a98957f348bcff9ee
  adaptation: Agent Skills; English; task-scoped; 2026-11-02
---

# Security review

Use for requested security reviews or substantive changes to authentication, authorization, secrets, sensitive data, payments, exposed APIs or agent tool boundaries. Focus on the changed attack surface and relevant dependencies. This complements general code review; it does not require a full security audit for every edit.

## Review

- Establish assets, entry points, trust boundaries and allowed actions. Trace untrusted input through validation, authorization and the consequential operation.
- Check object-level and tenant-level authorization on the server; authentication or a UI restriction alone does not establish permission. Inspect session/token validation, expiry and revocation where relevant.
- Validate inputs with actual runtime schemas and appropriate limits. Use parameterized database operations and contextual output encoding. Check CSRF for cookie-authenticated state changes, SSRF/redirect boundaries, injection and unsafe deserialization as applicable.
- Inspect file uploads and filesystem/process operations for path traversal, size/decompression limits, spoofed content types and shell injection. Treat supplied MIME types and extensions as insufficient on their own.
- Keep secrets and sensitive data out of prompts, logs, errors and client bundles. Check repository/configuration exposure without printing secret values. Follow the application's approved secret-management mechanism.
- For agents, keep instructions separate from retrieved/tool content; validate tool arguments and enforce permissions independently of model text. Check prompt-injection paths, credential exposure, cross-user retrieval and side-effect boundaries.
- Review payment/webhook authenticity, replay protection, idempotency, rate limiting, dependencies and deployment settings only where relevant to the application.

## Evidence and fixes

Report concrete findings with severity, location, trigger, impact and a practical fix. Distinguish confirmed issues from hypotheses and coverage gaps; never promise that a checklist proves security.

Use safe local tests or authorized environments. Active exploitation of unrelated systems, credential rotation, dependency upgrades, deployment and other external mutations require their existing authorization; review scope does not grant it.

When implementing fixes, preserve intended behavior and check the affected boundary. Do not run automatic audit fixes, add approval ceremonies or impose arbitrary test percentages.

For topic-specific historical examples, consult [upstream reference](https://github.com/WorldFlowAI/everything-claude-code/blob/432485ba6b92c14fb357276a98957f348bcff9ee/skills/security-review/SKILL.md). Verify framework/version semantics before adapting any snippet; its examples are not complete production security implementations.

## Specialized cases and output contract

For substantive relevant work, read [the applied workflow](references/trust-boundary-cases.md). Keep unrelated references unloaded.

## Task contract

Inputs: Changed routes/tools, data flow, caller identity, authorization policy and authorized fixtures.

Deliver: Findings with severity, location, trigger, evidence, impact and fix; hypotheses and untested surfaces labeled.

Acceptance: Object/tenant policy enforced server-side; tool privileges independent of model assertions; redacted secrets; explicit coverage gaps.
