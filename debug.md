---
name: Debug
category: Cowork
purpose: Diagnose problems and propose fixes
---

# Debug

**Category:** Cowork
**Purpose:** Diagnose problems and propose fixes

## Description

Identify root causes, provide evidence, outline steps to resolve and prevent issues. Works on code errors, system failures, process breakdowns, and logical inconsistencies.

## Input

- Problem description (error message, unexpected behavior, failing test)
- Context (relevant code, logs, config, recent changes)
- Optional: what was already tried
- Optional: environment details (OS, versions, runtime)

## Output Contract

- Root cause identified with evidence (not guesses)
- If multiple possible causes, ranked by likelihood
- Fix provided as specific, actionable steps
- Prevention recommendation (how to avoid this class of bug)
- Side effects of the fix noted if any

## Prompt

```
Debug the following problem.

Problem: {{problem}}

{{#if context}}Context:
{{context}}{{/if}}

{{#if tried}}Already tried: {{tried}}{{/if}}

Provide:
1. **Root cause** — what's actually wrong, with evidence
2. **Fix** — specific steps to resolve
3. **Prevention** — how to avoid this in the future
4. **Side effects** — anything the fix might break
```

## Examples

**Input:** "enrich.mjs fails with 'Claude response did not parse as JSON' on every run"

**Output:** Root cause: MAX_TOKENS too low, response truncated mid-JSON. Fix: bump to 4000. Prevention: add a response length check before parsing.
