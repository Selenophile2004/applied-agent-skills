# Install a selected skill

## Claude Code
Copy skills/<name>/ into ~/.claude/skills/<name>/ (Windows: %USERPROFILE%\.claude\skills\). Keep SKILL.md directly in that folder. Invoke /skill-name or describe a matching task.

Merge examples/claude-code-defaults.md into the active CLAUDE.md for economical defaults, preserving existing instructions and adjusting the installed path.

## Claude chat and Cowork
Upload one individual skill ZIP using the platform's custom-skills controls, then enable it. Each ZIP contains one skill folder with SKILL.md and references. Do not upload the multi-skill repository as one skill. Capabilities and administrator settings may affect execution.

See [official instructions](https://support.claude.com/en/articles/12512180-use-skills-in-claude). Hosted chat should not assume a local CLI path or CLAUDE.md.

## Codex
Copy skills/<name>/ into ~/.agents/skills/<name>/ (Windows: %USERPROFILE%\.agents\skills\). Mention $skill-name or use matching. Optional agents/openai.yaml provides Codex metadata.

Merge examples/codex-defaults.md into the active instructions, normally ~/.codex/AGENTS.md. Respect CODEX_HOME or an active AGENTS.override.md. Preserve existing instructions.

## Verify
Ask the host which skill is available and run a small relevant task. Discovery alone does not prove output quality. Restart if a local skill update is not detected.

[Compatibility and verification limits](compatibility.md)
