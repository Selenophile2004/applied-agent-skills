# Agent Reliability and Regression Evaluation

## Inputs

Baseline/candidate versions, representative cases, observable criteria, fixtures and available telemetry.

## Deliverables

Per-case comparisons, grading methods, evidence handles, regressions, unrun cases and actual cost/latency.

## Applied request

~~~text
Compare a retrieval-agent change on grounded-answer, missing-evidence, conflict and malicious-document cases with mocked tools.
~~~

## Acceptance criteria

Same conditions; executable and model-judged checks distinguished; repaired attempts not counted as first-attempt successes; unknown metrics remain unknown.

## Use this skill

Claude Code: /eval-harness. Codex: $eval-harness. Claude chat: enable the uploaded individual skill and describe the task.

Read [SKILL.md](SKILL.md) for the workflow and conditional references. Tools, model access and source inputs come from your environment.

[Install for your platform](../../docs/installation.md) | [Catalog](../../README.md)
