# Contributing

## Propose a skill

Open a skill request issue describing the recurring problem, intended users, expected outcome, constraints, and evidence. A proposed skill should normally live at `skills/<skill-name>/SKILL.md`.

## Required structure

Each skill must define:

- Purpose
- Intended use
- Constraints
- Success criteria

Add tool-routing rules and validation or stopping conditions when they are relevant. Do not force irrelevant sections into a skill.

## Standards

- Use kebab-case directory names.
- Keep one skill in one `SKILL.md` unless a future format explicitly requires otherwise.
- Prefer direct, scannable Markdown and precise terminology.
- Preserve factual claims and examples; do not invent capabilities, guarantees, benchmarks, or official policies.
- Cite authoritative sources for time-sensitive, technical, or otherwise consequential claims. Distinguish sourced facts from inference.

## Pull requests

Keep changes focused. Explain the purpose, scope, and validation performed. Update the README skill index when adding or renaming a skill. Do not include secrets, credentials, private information, generated clutter, or unrelated formatting churn.

## Review checklist

- [ ] The skill has a clear purpose and intended use.
- [ ] Constraints and success criteria are explicit.
- [ ] Tool routing and stopping conditions are included when relevant.
- [ ] Claims are supported and no capabilities are fabricated.
- [ ] Markdown headings, links, and fences are consistent.
- [ ] README index and version metadata are accurate.
- [ ] Validation was performed and described.
