---
name: Transform
category: Core
purpose: Convert input to a different useful format
---

# Transform

**Category:** Core
**Purpose:** Convert input to a different useful format

## Description

Turn notes into blog posts, meetings into task lists, raw data into structured output. The input and output are genuinely different artifacts — not just reformatted, but different in purpose and structure.

## Input

- Source content (any format)
- Target format (blog post, task list, email draft, database rows, changelog entry, Slack message)
- Optional: tone/voice (professional, casual, technical)
- Optional: constraints (word count, required sections)

## Output Contract

- Output is a complete, usable artifact in the target format
- All source facts preserved unless the target format doesn't support them
- Format conventions of the target followed (blog posts have intros, task lists have assignees)
- No hallucinated details — gaps flagged with [TBD] markers

## Prompt

```
Transform the following content into: {{target_format}}

Rules:
- Produce a complete, usable artifact in the target format
- Preserve all facts and decisions from the source
- Follow conventions of the target format
- Mark any gaps or missing info with [TBD]
- Tone: {{tone | default: "match the source"}}

{{#if constraints}}Constraints: {{constraints}}{{/if}}

Source:
{{input}}
```

## Examples

**Input:** Meeting notes about a product launch

**Target:** Slack announcement

**Output:** A ready-to-paste message with key dates, owners, and call to action — not reformatted notes, but an actual announcement.
