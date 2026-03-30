---
name: Classify
category: Core
purpose: Assign tags and categories
---

# Classify

**Category:** Core
**Purpose:** Assign tags and categories

## Description

Categorize content by type, priority, intent. Powers database organization, inbox triage, and routing. Works with predefined taxonomies or generates tags from content.

## Input

- Content to classify (single item or batch)
- Optional: taxonomy (predefined list of valid tags)
- Optional: dimensions (priority + topic + intent, or just topic)
- Optional: multi-label (allow multiple tags per item, default: yes)

## Output Contract

- Every input item gets at least one classification per dimension
- Tags come from provided taxonomy when one exists — no invented tags
- When no taxonomy, tags are lowercase-hyphenated and consistent across the batch
- Confidence score (high / medium / low) per classification
- Ambiguous items flagged, not force-classified

## Prompt

```
Classify the following content.

{{#if taxonomy}}Valid tags: {{taxonomy}}{{/if}}
{{#if dimensions}}Classify on: {{dimensions}}{{/if}}
Multi-label: {{multi_label | default: "yes"}}

Rules:
- Use only tags from the provided taxonomy when one exists
- If no taxonomy, generate consistent lowercase-hyphenated tags
- Include confidence (high / medium / low) for each tag
- Flag ambiguous items rather than guessing

Input:
{{input}}
```

## Examples

**Input:** "Fix the login timeout bug affecting mobile users"

**Taxonomy:** `[bug, feature, polish, docs]` + `[high, medium, low]`

**Output:** `{ type: "bug", confidence: "high", priority: "high", priority_confidence: "medium" }`
