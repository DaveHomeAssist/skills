---
name: Knowledge Graph
category: Notion-Specific
purpose: Map entities and their relationships
---

# Knowledge Graph

**Category:** Notion-Specific
**Purpose:** Map entities and their relationships

## Description

Extract entities and link them to build a second-brain knowledge graph. Identifies people, projects, tools, decisions, and concepts, then maps how they connect.

## Input

- Source text (notes, transcripts, documents, or multiple sources)
- Optional: entity types to focus on (people, projects, tools, decisions)
- Optional: existing graph (to merge into rather than start fresh)
- Optional: output format (JSON, markdown table, mermaid diagram)

## Output Contract

- Entity list: name, type, first-seen source
- Relationship list: entity A, relationship verb, entity B
- No duplicate entities (normalize names: "Dave" and "Dave RambleOn" = same entity)
- Relationships are directional and labeled (owns, depends-on, blocks, uses)
- Orphan entities flagged (mentioned but not connected to anything)

## Prompt

```
Extract a knowledge graph from the following content.

{{#if entity_types}}Focus on: {{entity_types}}{{/if}}
Output format: {{format | default: "JSON"}}

For each entity: { name, type, source }
For each relationship: { from, verb, to }

Rules:
- Normalize names (same person/project = one entity)
- Relationships must be directional and labeled
- Flag orphan entities that aren't connected to anything
- Do not invent relationships not stated in the source

Input:
{{input}}
```

## Examples

**Input:** Project notes mentioning Dave, PromptLab, Lemon Squeezy, D-001, hash routing

**Output:** Entities: Dave (person), PromptLab (project), Lemon Squeezy (tool), D-001 (decision). Relations: Dave owns PromptLab, D-001 blocks PromptLab Phase 2, PromptLab uses Lemon Squeezy.
