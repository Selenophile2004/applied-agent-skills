# Codex Skill Library

Reusable English-language skills maintained by Selenophile2004 for analysis, translation, consulting proposals, agent evaluation and software development. Instructions are English; outputs follow the user's requested language.

## Skills

| Skill | Purpose |
|---|---|
| token-efficiency | Reduce redundant context and tool usage while preserving complete, verified results |
| deep-translation-comprehension | Faithful translation, concept explanation and reading comprehension |
| issue-tree | Decompose decision questions into actionable investigation trees |
| mece-framework | Audit overlap, coverage and logical levels in structures |
| consulting-proposal-content | Develop modular proposal content, solution phases, execution tables and deep dives |
| consulting-proposal-writing | Turn agreed content into evidence-based proposals and slide storylines |
| persian-landscape-proposals | Produce editable Persian RTL decks using a user-supplied authorized template |
| eval-harness | Evaluate agent/workflow quality, regressions and measured execution cost |
| security-review | Review application and agent security boundaries |
| backend-patterns | Implement APIs, database access, caching and background jobs |
| coding-standards | Maintain TypeScript/JavaScript/React/Node.js code with appropriate checks |

Each folder under skills/ contains a SKILL.md entrypoint. Supporting references load only when needed. These are instructions, not background services, automatically executing agents or bundled model access.

## Install

Copy an individual skills/<name> folder into your user skills directory:

- Windows: %USERPROFILE%\.agents\skills\<name>
- macOS/Linux: ~/.agents/skills/<name>

The installed folder must contain SKILL.md directly. Compare existing same-name skills before replacing them. Codex supports implicit matching by description; you can explicitly mention a skill as $token-efficiency or $security-review. Restart if newly installed skills do not appear.

To use economical defaults across tasks, merge examples/global-instructions.md into the active global instruction file (normally ~/.codex/AGENTS.md). Preserve existing instructions. If CODEX_HOME or an AGENTS.override.md changes the active location, use that active file. Adjust the installed skill path in the example if needed.

## Usage examples

- Use $token-efficiency to build the requested report with complete analysis and only relevant tool output.
- Use $eval-harness to define representative agent cases and compare a candidate against a baseline.
- Use $security-review to review tenant authorization and tool access in this agent application.
- Use $consulting-proposal-content to draft only the requested proposal module.
- Use $persian-landscape-proposals with my authorized template and agreed manifest.

## Requirements and scope

No paid assets, proprietary templates, credentials or client data are bundled. File production requires suitable host tooling and any requested template/assets. Some consulting workflow phases intentionally preserve explicit content-approval gates. Context efficiency does not waive those gates or other authorization requirements.

No percentage of token savings or performance is promised. Quality and actual usage must be evaluated on the intended tasks.

## Licenses

See LICENSE, each skill's LICENSE/NOTICE and THIRD_PARTY_NOTICES.md. Some skills are personal adaptations of existing work; attribution is retained. No affiliation with or endorsement by an organization or platform is implied.
