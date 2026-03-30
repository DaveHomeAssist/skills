---
name: System Builder
category: Cowork
purpose: Design structured workflows
---

# System Builder

**Category:** Cowork
**Purpose:** Design structured workflows

## Description

Define components, inputs/outputs, dependencies for systems or prompts. Takes a goal and produces an architecture — the boxes, arrows, and contracts between them.

## Input

- Goal or problem statement (what the system should do)
- Optional: existing components (what's already built)
- Optional: constraints (platform, language, budget, team)
- Optional: scale requirements (how many users, how much data)

## Output Contract

- Component list with responsibilities
- Data flow diagram (described in text or mermaid)
- Input/output contract for each component
- Dependency map (what depends on what)
- Integration points clearly marked
- First step to build identified

## Prompt

```
Design a system for: {{goal}}

{{#if existing}}Existing components: {{existing}}{{/if}}
{{#if constraints}}Constraints: {{constraints}}{{/if}}

Provide:
1. **Components** — list each with its single responsibility
2. **Data flow** — how data moves between components
3. **Contracts** — input/output spec for each component
4. **Dependencies** — what depends on what
5. **Integration points** — where components connect
6. **First step** — what to build first and why
```

## Examples

**Input:** "Design a daily newsletter pipeline that crawls MLB data, enriches with AI, and deploys to GitHub Pages"

**Output:** Three-stage pipeline (crawl, enrich, render) with contracts between stages, fallback behavior, and validation checkpoints.
