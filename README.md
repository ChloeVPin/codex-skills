# codex-skills

A curated collection of reusable skills and guidance for building effective Codex and AI-agent workflows.

## Independent project

`codex-skills` is an independent community resource. It is not affiliated with, endorsed by, or maintained by OpenAI unless explicit evidence of such an affiliation is provided.

## What is a skill?

A skill is a focused Markdown instruction set that helps an AI agent perform a recurring task consistently. Skills describe purpose, intended use, constraints, and—where useful—tool routing, success criteria, validation, and stopping conditions.

## Repository structure

```text
skills/<skill-name>/SKILL.md
```

Community and contribution templates live under `.github/`.

## Available skills

| Skill | Description | Status | Version |
| --- | --- | --- | --- |
| [gpt-5-6-guidance](skills/gpt-5-6-guidance/SKILL.md) | Guidance for writing and refining prompts, tool descriptions, and agent instructions for GPT-5.6 workflows. | Draft | 1.0.0 |
| [ui-ux-design](skills/ui-ux-design/SKILL.md) | Design and critique user interfaces through task clarity, hierarchy, interaction states, accessibility, and implementation-aware decisions. | Draft | 1.0.0 |
| [replicate-reference-design](skills/replicate-reference-design/SKILL.md) | Reconstruct interfaces from attached reference images with measured visual fidelity. | Draft | 1.0.0 |
| [design-from-brief](skills/design-from-brief/SKILL.md) | Create distinctive, award-caliber interfaces from written product and design briefs. | Draft | 1.0.0 |

## How to use a skill

Read the relevant `SKILL.md` and provide it to the agent in the instruction context supported by your tooling. Treat each skill as guidance to adapt to the task, available tools, permissions, and current product documentation.

## How to add a skill

Create `skills/<skill-name>/SKILL.md` using kebab-case for `<skill-name>`. Include front matter and proportional guidance covering purpose, intended use, constraints, and success criteria. Update the available-skills table and follow [CONTRIBUTING.md](CONTRIBUTING.md).

## Contributions

Open an issue or pull request using the repository templates. Contributions should be focused, evidence-based, readable, and free of unsupported claims.

## Versioning

Skills use semantic versioning where practical: increment patch versions for editorial corrections, minor versions for backward-compatible guidance, and major versions for substantial behavior or contract changes. Draft skills may change before a stable release.

## License

This repository is available under the [MIT License](LICENSE).
