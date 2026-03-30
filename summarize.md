---
name: Summarize
category: Core
purpose: Compress content while preserving meaning
---

# Summarize

**Category:** Core
**Purpose:** Compress content while preserving meaning

## Description

Produce concise narrative summaries, not just bullets. Captures the essential what, why, and so-what of any input. Scales from one-line TLDRs to multi-paragraph executive summaries.

## Input

- Source text (article, transcript, thread, document, codebase notes)
- Optional: target length (one-line, paragraph, 3-bullet, executive summary)
- Optional: audience (technical, non-technical, executive, self)

## Output Contract

- Summary is shorter than input
- No new information introduced
- Key decisions, outcomes, and action items preserved
- Narrative voice — reads as prose, not a list (unless bullets requested)
- Attribution preserved for quotes or claims

## Prompt

```
Summarize the following content.

Target length: {{length | default: "1 paragraph"}}
Audience: {{audience | default: "general"}}

Rules:
- Write in narrative prose unless bullets are explicitly requested
- Preserve key decisions, outcomes, numbers, and names
- Do not introduce information not in the source
- Lead with the most important point

Input:
{{input}}
```

## Examples

**Input:** 500-word meeting transcript about auth middleware migration

**Target:** one-line

**Output:** "Legal flagged the auth middleware for non-compliant token storage; team decided to rewrite using the new compliance spec, targeting March 15."
