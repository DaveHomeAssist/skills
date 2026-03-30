---
name: Critique
category: Cowork
purpose: Evaluate quality and identify weaknesses
---

# Critique

**Category:** Cowork
**Purpose:** Evaluate quality and identify weaknesses

## Description

Highlight strengths, weaknesses, and missing elements with improvement suggestions. Works on code, writing, designs, plans, prompts — anything that can be evaluated against a standard.

## Input

- Artifact to critique (code, document, plan, prompt, design spec)
- Optional: evaluation criteria (clarity, correctness, completeness, tone, performance)
- Optional: severity threshold (only flag medium+ issues, or include nits)

## Output Contract

- Structured as: Strengths, Weaknesses, Missing, Suggestions
- Each weakness includes severity (high / medium / low) and a specific fix
- Strengths are called out — not just a list of problems
- Suggestions are actionable, not vague ("add error handling to fetchJson" not "improve error handling")
- No rewriting the artifact — critique only

## Prompt

```
Critique the following artifact.

{{#if criteria}}Evaluate on: {{criteria}}{{/if}}
Severity threshold: {{threshold | default: "all"}}

Structure your response as:
1. **Strengths** — what works well
2. **Weaknesses** — specific issues with severity and fix
3. **Missing** — what should be there but isn't
4. **Suggestions** — actionable improvements

Be direct. Be specific. Do not rewrite the artifact.

Artifact:
{{input}}
```

## Examples

**Input:** A draft README for an open-source project

**Output:** Strengths (clear install instructions), Weaknesses (no license section — high, add MIT/Apache), Missing (contributing guide, changelog), Suggestions (add badges for build status and npm version).
