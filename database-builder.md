---
name: Database Builder
category: Notion-Specific
purpose: Create Notion DB schema
---

# Database Builder

**Category:** Notion-Specific
**Purpose:** Create Notion DB schema

## Description

Define properties, types, and example rows for Notion databases. Produces a ready-to-create schema with property names, types, options, and relationships.

## Input

- What the database tracks (leads, tasks, content, inventory)
- Key fields / columns needed
- Optional: relationships to other databases
- Optional: views needed (table, board, calendar, gallery)
- Optional: example data (3-5 rows)

## Output Contract

- Schema table: property name, type, options (if select/multi-select), description
- SQL-style CREATE TABLE for Notion MCP tool compatibility
- Suggested views with grouping/filtering/sorting
- 3 example rows that exercise all property types
- Relations include both sides (source and target DB)

## Prompt

```
Design a Notion database for: {{purpose}}

{{#if fields}}Required fields: {{fields}}{{/if}}
{{#if relations}}Related databases: {{relations}}{{/if}}
{{#if views}}Views needed: {{views}}{{/if}}

Provide:
1. **Schema table** — property name, type, options, description
2. **CREATE TABLE** — SQL DDL compatible with Notion MCP
3. **Views** — name, type, group-by, sort, filter for each
4. **Example rows** — 3-5 rows exercising all property types
```

## Examples

**Input:** "Track LLM conversation notes with entry type, topic tags, confidence, and source agent"

**Output:** Schema with Title (title), Entry Type (select), Topic Tags (multi-select), Confidence (select), Status (status), Date (date), Source LLM (select), Note (rich text). Board view grouped by Entry Type, table view sorted by date.
