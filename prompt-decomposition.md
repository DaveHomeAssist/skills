---
name: Prompt Decomposition
category: Advanced
purpose: Split complex tasks into steps
---

# Prompt Decomposition

**Category:** Advanced
**Purpose:** Split complex tasks into steps

## Description

Create step-by-step execution plans with sub-prompts. Takes a complex task and breaks it into a sequence of simpler prompts that can be chained, parallelized, or routed to different agents.

## Input

- Complex task description
- Optional: available agents/models (what can execute each step)
- Optional: constraints (must be sequential, can parallelize, budget limits)
- Optional: output format (execution plan, prompt chain, agent routing table)

## Output Contract

- Ordered list of steps, each with: step name, input, prompt, expected output, agent/model
- Dependencies between steps marked (sequential vs parallel)
- Aggregation step if parallel branches need merging
- Estimated token cost per step if models are specified
- Failure handling: what to do if a step fails

## Prompt

```
Decompose this complex task into a chain of simpler sub-prompts.

Task: {{task}}

{{#if agents}}Available agents: {{agents}}{{/if}}
{{#if constraints}}Constraints: {{constraints}}{{/if}}

For each step:
1. **Name** — short label
2. **Depends on** — which prior steps (or "none")
3. **Input** — what this step receives
4. **Prompt** — the actual sub-prompt to execute
5. **Expected output** — what this step produces
6. **Agent** — who executes it
7. **On failure** — fallback behavior
```

## Examples

**Input:** "Audit all 8 repos for high-priority bugs, verify which are fixed, mark done in Notion, and surface remaining issues in the Daily Prophet"

**Output:** 4-step chain: (1) Codex scans repos in parallel, (2) Claude Code verifies fixes on disk, (3) Jerri updates Notion task tracker, (4) Daily Prophet surfaces remaining blockers. Steps 1-2 sequential, step 3-4 parallel after 2 completes.
