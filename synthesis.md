---
name: Synthesis
category: Advanced
purpose: Combine multiple inputs into insights
---

# Synthesis

**Category:** Advanced
**Purpose:** Combine multiple inputs into insights

## Description

Detect patterns, draw conclusions, and make recommendations from multiple sources. Unlike Summarize (which compresses one input), Synthesis combines many inputs and produces something new — a conclusion, a pattern, a recommendation that wasn't in any single source.

## Input

- Multiple sources (2+): documents, data points, observations, conversation logs
- Optional: question to answer (what should the synthesis address?)
- Optional: output format (narrative, recommendations, pattern list, brief)

## Output Contract

- Patterns identified across sources with supporting evidence
- Contradictions between sources flagged explicitly
- Conclusions clearly labeled as inferred (not just restated from sources)
- Recommendations are actionable and tied to specific evidence
- Sources cited for each claim (which input contributed what)

## Prompt

```
Synthesize the following inputs into insights.

{{#if question}}Question to answer: {{question}}{{/if}}
Output format: {{format | default: "narrative with recommendations"}}

Rules:
- Identify patterns that appear across multiple sources
- Flag contradictions between sources
- Label conclusions as inferred vs directly stated
- Cite which source supports each claim
- Provide actionable recommendations tied to evidence

Sources:
{{#each sources}}
### Source {{@index}}
{{this}}
{{/each}}
```

## Examples

**Input:** Three sources — a task tracker export, a git log summary, and a conversation transcript from the same week

**Question:** "What's the actual velocity and where are the bottlenecks?"

**Output:** Pattern: 60% of completed work was bug fixes triggered by the Codex sweep, not planned feature work. Contradiction: task tracker shows 3 items "in progress" but git log shows no commits on those branches in 5 days. Recommendation: close or defer the stale in-progress items and schedule a focused feature sprint.
