---
name: token-efficiency
description: Reduce redundant token and tool use in analysis, file creation, software/web development, agents, automation, and other multi-step work while preserving quality.
license: MIT
metadata:
  source: https://github.com/undefdev/token-efficiency
  upstream-blob: cf31795d8e02a3a2dffb7634264e926422eb7777
  customization: General-purpose agent execution; 2026-11-02
---

# Token efficiency

Optimize total effort to a verified result, including context, tool output, retries and any authorized workers. Apply across projects and domains. Preserve requested analytical depth, complete artifacts and necessary checks; impose no arbitrary token cap or reduction in reasoning effort. These instructions are English; use the user's requested language for communication and deliverables.

## Core execution

- Start from the current request and applicable instructions. Locate the relevant sources, state and assets in the task workspace before expanding discovery. Verify current paths; avoid broad drive, repository or account scans for a local question.
- Reuse evidence already in context. Search for files/symbols, then read enough original source and dependencies for the decision. Expand ambiguous or truncated results; they never establish absence. Before editing or making a consequential decision, consult the authoritative original with adequate context. Re-read after relevant changes, failed edit matches, or loss of necessary context.
- Filter before results enter context: use tool parameters, structured queries, selected ranges and format-aware parsers. Compute over the complete relevant input when required; return the schema, aggregates, relevant records and diagnostics. Deliver requested large raw data as an artifact rather than repeating it in chat.
- Reuse persisted results and inspect relevant sections of verbose output while preserving errors and original exit status. Prefer supported native tools and existing runtimes; respect tool-specific rules. Use platform-appropriate commands and literal paths.
- Make focused edits; reuse existing assets, working code and verified content. Script repetitive transformations when more reliable than generating them manually. Full reads, rewrites and rebuilds remain appropriate when scope or dependencies require them.
- Batch independent calls when supported. Prefer completion events to polling. After two identical failed attempts, diagnose before another unchanged retry; changed inputs and necessary verification reruns are different. Delegate only when authorized and the work justifies all workers' context and coordination.
- Keep reusable prompt prefixes stable where practical; cache behavior depends on the provider. Use native context management and retain constraints, decisions, exact errors, failed approaches, recovery handles and next actions. Update an existing checkpoint for substantial resumable work when useful; avoid extra paperwork for simple tasks.
- Complete the requested result and relevant verification. Link artifacts instead of repeating their bodies; keep delivery messages concise unless detailed prose is requested. Do not reduce requested coverage, editability, citations, tests or visual review for token savings. Report uncertainty and unperformed checks honestly.

## Conditional guidance

Read only the reference that changes how to perform the current task. Combine modes for genuinely mixed work, and use relevant installed skills without loading unrelated manuals.

- Analysis, reasoning, research and decision support: [analysis and research](references/analysis-and-research.md).
- Datasets, spreadsheets and BI: [data and BI](references/data-and-bi.md).
- Documents, presentations, PDFs and other file outputs: [files and deliverables](references/files-and-deliverables.md).
- Websites, interfaces and visual assets: [web and design](references/web-and-design.md).
- Agent applications, tool workflows and automations: [agents and automation](references/agents-and-automation.md).
- Other software, debugging, APIs and system tasks: [software and systems](references/software-and-systems.md).

For other work, apply the core without inventing a special process. Do not reload unchanged guidance each turn. For simple questions, use the global defaults without unnecessary file reads. Claim savings only from actual measurements.

## Task contract

Inputs: Current brief, required artifacts, source handles and evidence already in context.

Deliver: Complete artifact and relevant checks; observed waste/usage findings when an audit is requested.

Acceptance: Summaries retain recovery handles; ambiguity expands the read; complete outputs and required checks are preserved; savings are measured or unknown.
