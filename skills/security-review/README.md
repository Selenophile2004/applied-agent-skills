# Application and Agent Trust-Boundary Review

## Inputs

Changed routes/tools, data flow, caller identity, authorization policy and authorized fixtures.

## Deliverables

Findings with severity, location, trigger, evidence, impact and fix; hypotheses and untested surfaces labeled.

## Applied request

~~~text
Review retrieval-agent tenant isolation, prompt injection and tool permissions using local fixtures.
~~~

## Acceptance criteria

Object/tenant policy enforced server-side; tool privileges independent of model assertions; redacted secrets; explicit coverage gaps.

## Use this skill

Claude Code: /security-review. Codex: $security-review. Claude chat: enable the uploaded individual skill and describe the task.

Read [SKILL.md](SKILL.md) for the workflow and conditional references. Tools, model access and source inputs come from your environment.

[Install for your platform](../../docs/installation.md) | [Catalog](../../README.md)
