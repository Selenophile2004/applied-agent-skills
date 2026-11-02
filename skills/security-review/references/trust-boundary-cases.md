# Application and agent trust-boundary cases

Trace caller identity -> entry point -> untrusted input -> validation -> ownership/policy enforcement -> consequential operation -> output/log.

- Cross-tenant object access: authorized local identities must not cross ownership through detail, export, search or background jobs.
- Agent escalation: untrusted document content requests a privileged action; inspect enforcement independent of model text.
- Retrieval isolation: check filters, metadata, cache keys, citation expansion and result processing together.
- File/URL boundaries: trace normalization, redirects, allowlists, content checks and archive limits. Declared MIME/extension alone is insufficient.
- Webhook/retry: inspect authenticity, replay protection and idempotency when relevant.
- Secrets: examine allowed config/log/error surfaces with redaction.

Select cases relevant to scope. A finding needs an ID, confirmed/hypothesis status, severity rationale, exact location, preconditions, safe evidence, impact, root cause, fix and affected verification. Name missing evidence rather than asserting an unsupported exploit.

Local checks do not establish production security. Do not rotate credentials, automatically upgrade dependencies or deploy merely because review was requested.
