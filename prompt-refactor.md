---
name: Prompt Refactor
category: Notion-Specific
purpose: Refine prompts into reusable skills
---

# Prompt Refactor

**Category:** Notion-Specific
**Purpose:** Refine prompts into reusable skills

## Description

Clean up instructions, tighten rules, define output contracts. Takes a working-but-messy prompt and produces a production-grade skill with clear input spec, deterministic output, and edge case handling.

## Input

- Existing prompt (working or draft)
- Optional: failure modes observed (when does it go wrong?)
- Optional: target use case (one-shot, batch, chained)
- Optional: model target (Claude, GPT, local)

## Output Contract

- Refactored prompt with: system message, user template, variables
- Input spec: what's required, what's optional, types
- Output contract: what the prompt guarantees
- Edge cases listed with handling rules
- Before/after comparison showing what changed and why

## Prompt

```
Refactor this prompt into a production-grade reusable skill.

Original prompt:
{{input}}

{{#if failures}}Known failure modes: {{failures}}{{/if}}
{{#if use_case}}Use case: {{use_case}}{{/if}}

Provide:
1. **Refactored prompt** — system message + user template with {{variables}}
2. **Input spec** — required and optional parameters with types
3. **Output contract** — what the prompt guarantees
4. **Edge cases** — known failure modes and how the prompt handles them
5. **Changelog** — what changed from the original and why
```

## Examples

**Input:** A long, rambling prompt that sometimes returns markdown-wrapped JSON

**Output:** Tightened prompt with explicit "Return ONLY valid JSON. No markdown fences." rule, input variables extracted, output contract defined, edge case for empty input handled.
