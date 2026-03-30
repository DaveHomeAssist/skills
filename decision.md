---
name: Decision
category: Cowork
purpose: Turn ambiguity into clear choices
---

# Decision

**Category:** Cowork
**Purpose:** Turn ambiguity into clear choices

## Description

List options, trade-offs, recommend a path, and explain why. Used when you're stuck between approaches and need structured thinking to move forward.

## Input

- Decision context (what needs to be decided, why now)
- Options (if known — skill can also generate options)
- Optional: constraints (budget, timeline, team size, technical limitations)
- Optional: decision criteria (what matters most — speed, cost, quality, reversibility)

## Output Contract

- 2-5 options presented with clear labels
- Each option has: description, pros, cons, effort estimate
- One recommended option with explicit rationale
- Trade-off matrix if 3+ options
- Consequences section: what the recommendation unlocks and what it closes off

## Prompt

```
Help me decide: {{context}}

{{#if options}}Options to evaluate: {{options}}{{/if}}
{{#if constraints}}Constraints: {{constraints}}{{/if}}
{{#if criteria}}Optimize for: {{criteria}}{{/if}}

For each option, provide:
- Description (1-2 sentences)
- Pros
- Cons
- Effort estimate

Then recommend one option with rationale and consequences.
```

## Examples

**Input:** "Should PromptLab use hash routing or a state router for navigation?"

**Output:** Two options with pros/cons, recommendation for hash routing based on VS Code webview constraints, consequences section noting what's unblocked.
