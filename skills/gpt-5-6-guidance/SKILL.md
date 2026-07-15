---
name: gpt-5-6-guidance
description: Guidance for writing and refining prompts, tool descriptions, and agent instructions for GPT-5.6 workflows.
version: 1.0.0
status: draft
---

# GPT-5.6 Guidance

Use these rules when writing or refining prompts, tool descriptions, and agent instructions for GPT-5.6 Sol.

## Core rule

Define the outcome, constraints, required evidence, and success criteria. Stop there. Let the model choose the path.

## Simplify

Start with a working prompt and tool set. Remove one category at a time and test.

Remove:

- Repeated rules
- Style or process instructions the model already follows
- Examples that do not change behavior
- Tools unrelated to the task

Keep:

- User-visible outcome
- Success criteria and stopping conditions
- Safety, policy, evidence, and permission constraints
- Context-dependent tool-routing rules
- Required output format and validation rules

Check the remaining instructions for contradictions.

## Outcome first and stopping conditions

State what success looks like. Do not prescribe every step.

```text
Resolve the request end to end.

Success means:
- Make the decision using available evidence
- Complete allowed actions before responding
- Return completed_actions, customer_message, and blockers
- Ask for the smallest missing field when evidence is insufficient
```

Use decision rules for judgment calls such as when to search, ask, or iterate. Reserve `ALWAYS`, `NEVER`, `must`, and `only` for true invariants.

Add explicit stopping conditions:

```text
Resolve the request in the fewest useful tool loops without sacrificing correctness, required evidence, calculations, or citations.

After each result, check whether the core request can now be answered. If yes, answer. If evidence is still missing, name the smallest missing piece and use the smallest useful fallback.
```

## Length and tone

Use `text.verbosity` in the API to set default detail level. Add task-specific length rules only when needed.

When shorter output is required, tell the model exactly what to preserve and what to remove:

```text
Lead with the conclusion. Include only the evidence, caveats, and next action required. Omit introductions, repetition, and secondary detail.
```

For editing and rewriting tasks:

```text
Preserve the requested artifact, length, structure, genre, and factual claims. Improve clarity and correctness without adding new claims or changing tone.
```

Describe tone through specific behaviors rather than labels:

```text
State the answer directly. Acknowledge the specific problem before giving the next step. Use reassurance only when relevant. Omit generic praise and sign-offs.
```

## Autonomy and approval

Define authorization levels clearly.

Default policy:

- Answer, explain, review, diagnose, or plan → inspect and report. Do not make changes unless requested.
- Change, build, or fix → make the requested in-scope changes and run non-destructive validation without asking first.
- External writes, destructive actions, purchases, or scope expansion → require confirmation first.

Name safe local actions explicitly. Keep the policy in one place. State each rule once.

For long-running work, define the current layer: research, design, implementation, review, or external coordination.

## Tool use

Expose only relevant tools. Describe what each tool does, when to use it, key return fields, and error behavior.

When prerequisites matter:

```text
Before taking an action, complete required discovery, retrieval, and validation. Do not skip steps because the final state appears obvious.
```

Parallelize independent reads. Keep dependent work sequential. After parallel results, synthesize before acting.

If a tool returns empty or narrow results, try one or two meaningful fallbacks before concluding no result exists.

## Programmatic tool calling

Use Programmatic Tool Calling only for bounded reduction stages such as filtering, joining, aggregation, deduplication, or compact schema output.

State explicitly:

- The exact stage
- Which tools are allowed
- Output schema
- Retry limit
- When to hand back to direct tool calls

Test both the `program_output` and the final message.

## Grounding and retrieval

For ordinary questions, start with one broad search using precise keywords. Answer from the top results if they contain sufficient support.

Make additional retrieval calls only when:

- A required fact, source, ID, or date is missing
- Exhaustive coverage or comparison is requested
- A specific artifact must be read

Do not retrieve again to improve phrasing or support non-essential detail.

For research:

- Cite only retrieved sources
- Attach citations to the claims they support
- Label inference separately
- Report conflicts and missing evidence instead of guessing

For drafting, distinguish sourced facts from invented content. Do not fabricate names, metrics, dates, or capabilities.

## Long-running workflows

Before the first tool call in a multi-step task, send a short user-visible update stating the first step.

Send updates only at major phase changes. Each update states one concrete outcome and the next step.

Preserve original phase values when replaying history. Compact after major milestones. Treat compacted items as opaque state.

Use current-turn reasoning when earlier reasoning is no longer relevant.

## Reasoning effort

Start with the current reasoning effort setting.

Test one level lower on representative tasks before increasing.

Use higher effort only when it produces a measurable improvement on evaluations. Do not increase effort to compensate for missing success criteria or verification rules.

## Visual and frontend tasks

For incremental UI changes:

- Inspect and preserve existing design tokens, components, and patterns
- Do not add unrequested features or decoration
- Render and inspect before finalizing

For vision or spatial tasks, choose image detail level intentionally. Use higher detail only when coordinate precision or dense content justifies the cost.

## Validation before finishing

Give the model tools to validate its output and state what validation is required.

For coding:

```text
After changes, run the most relevant validation:
- Targeted tests for changed behavior
- Type or lint checks
- Build checks for affected packages
- Minimal smoke test if full validation is expensive

If validation cannot run, explain why and describe the next best check.
```

For visual artifacts, render the artifact. Inspect layout, spacing, clipping, missing content, and consistency. Revise until it matches requirements.

## Prompt structure

Use this structure for complex prompts. Keep every section short.

```text
Role: [function and context]
Personality: [specific tone behaviors]
Goal: [user-visible outcome]
Success criteria: [what must be true]
Constraints: [policy, safety, evidence, limits]
Tools: [allowed tools and routing rules]
Output: [format and length rules]
Stop rules: [when to stop, fallback, or ask]
```

## Migration process

When moving an existing prompt stack to GPT-5.6:

1. Switch the model while keeping the current reasoning effort.
2. Run evaluations before changing the prompt.
3. Remove repeated instructions and irrelevant tools.
4. Add the smallest change that fixes a measured failure.
5. Re-run evaluations after each edit.

Debug regressions with real traces. Make targeted edits. Never rewrite a working stack at once.
