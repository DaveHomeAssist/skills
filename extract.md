---
name: Extract
category: Core
purpose: Systematically pull structure from unstructured content
---

# Extract

**Category:** Core
**Purpose:** Systematically pull structure from unstructured content

## Description

Extract tasks, decisions, facts, ideas, entities, dates from messy notes. Works on meeting transcripts, braindumps, Slack threads, voice memos, and raw intake. Returns typed, structured items ready for a database or task tracker.

## Input

- Raw text (any length, any messiness)
- Optional: extraction targets (e.g., "tasks only", "decisions and dates", "all entities")
- Optional: output format preference (JSON, markdown list, Notion-ready)

## Output Contract

- Every extracted item includes: `type` (task / decision / fact / idea / entity / date), `content`, `confidence` (high / medium / low)
- Tasks include an `assignee` field if one is mentioned, otherwise null
- Dates are normalized to ISO-8601 when possible
- Items appear in document order
- Nothing invented — only what's in the source text

## Prompt

```
You are an extraction engine. Read the input and pull out every structured item.

For each item, return:
- type: one of [task, decision, fact, idea, entity, date]
- content: the extracted item in clear language
- confidence: high, medium, or low
- assignee: (tasks only) who is responsible, or null
- date: ISO-8601 if a date is mentioned, or null

Return as a JSON array. Do not add items that aren't in the source.
Do not summarize. Do not editorialize. Extract only.

{{#if targets}}Focus on: {{targets}}{{/if}}

Input:
{{input}}
```

## Examples

**Input:** "Met with Tom Thursday. He'll send the revised menu by Friday. We decided to go with Lemon Squeezy over Gumroad. Dave needs to set up the Notion integration key before anything else."

**Output:**
```json
[
  { "type": "entity", "content": "Tom", "confidence": "high", "date": null },
  { "type": "date", "content": "Thursday (meeting)", "confidence": "high", "date": "relative" },
  { "type": "task", "content": "Send revised menu", "confidence": "high", "assignee": "Tom", "date": "Friday" },
  { "type": "decision", "content": "Go with Lemon Squeezy over Gumroad", "confidence": "high", "date": null },
  { "type": "task", "content": "Set up Notion integration key", "confidence": "high", "assignee": "Dave", "date": null }
]
```
