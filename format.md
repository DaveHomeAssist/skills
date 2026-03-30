---
name: Format
category: Core
purpose: Enhance readability and Notion formatting
---

# Format

**Category:** Core
**Purpose:** Enhance readability and Notion formatting

## Description

Reformat content into clear headings, lists, and hierarchy. Ensure Notion-ready structure with toggles, callouts, tables, and proper markdown. Does not change meaning — only presentation.

## Input

- Raw or poorly formatted text
- Optional: target format (Notion page, README, email, Slack message)
- Optional: style guide (heading levels, list style, callout usage)

## Output Contract

- Content meaning preserved exactly — no additions, no deletions
- Headings follow logical hierarchy (H1 > H2 > H3)
- Lists used for 3+ related items
- Tables used when data has 2+ columns of parallel structure
- Notion-specific syntax (callouts, toggles) used when target is Notion
- No orphan paragraphs — every block has a parent section

## Prompt

```
You are a formatting engine. Restructure the input for maximum readability.

Rules:
- Do not change meaning or add new information
- Use heading hierarchy: H1 for title, H2 for sections, H3 for subsections
- Convert run-on lists into bullet points
- Convert parallel data into tables
- Group related content under logical headings
- Target format: {{format | default: "Notion page"}}

{{#if style_guide}}Style guide: {{style_guide}}{{/if}}

Input:
{{input}}
```

## Examples

**Input:** "The project has three phases. Phase 1 is data collection which takes 2 weeks. Phase 2 is analysis which takes 1 week. Phase 3 is reporting which takes 3 days."

**Output:** A table with Phase / Task / Duration / Owner columns.
