# Compatibility and verification

The shared workflows use standard SKILL.md name/description frontmatter and relative references. They do not require Codex tool names, a specific model provider or hard-coded filesystem paths.

| Environment | Use | Requirements |
|---|---|---|
| Claude Code | Local skill folder; /skill-name or implicit matching | Relevant tools and project inputs |
| Claude chat / Cowork | Individual uploaded skill ZIP | Custom skills enabled; required capabilities available |
| Codex | Local skill folder; $skill-name or matching | Relevant tools; optional agents/openai.yaml metadata |
| Other Agent Skills hosts | Follow the host's discovery mechanism | Verify host capabilities |

agents/openai.yaml is optional host metadata, not a shared runtime dependency. No Claude-specific hooks, model-routing config or dynamic shell injection is required.

Manifests, relative links and package structure are validated. Guidance follows official documentation. Live end-to-end execution in every Claude surface has not been performed; universal runtime testing is not claimed.

PowerPoint production needs an authorized supplied template and suitable authoring/rendering tools. Evaluation needs actual cases/fixtures and available telemetry. Skills do not create missing tools, model access or permissions.

- [Claude Code skills](https://code.claude.com/docs/en/skills)
- [Claude custom skills](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- [Agent Skills format](https://agentskills.io/specification)
- [Codex skills](https://learn.chatgpt.com/docs/build-skills)
