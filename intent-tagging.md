---
name: Intent Tagging
category: Advanced
purpose: Decompose user intent into atomic units
---

# Intent Tagging

**Category:** Advanced
**Purpose:** Decompose user intent into atomic units

## Description

Identify intent units, assign priority and ambiguity level. Takes a complex or vague user message and breaks it into the distinct things the user actually wants. Powers smart routing, task decomposition, and clarification prompts.

## Input

- User message or request (any complexity)
- Optional: available actions (what the system can do — helps map intents to capabilities)
- Optional: conversation history (for context-dependent intents)

## Output Contract

- Array of intent units, each with: intent label, extracted parameters, priority (primary / secondary / implied), ambiguity (clear / needs-clarification / vague)
- Primary intent listed first
- Implied intents (things the user probably wants but didn't say) marked as such
- Ambiguous intents include a clarification question

## Prompt

```
Decompose this user message into atomic intent units.

{{#if actions}}Available actions: {{actions}}{{/if}}

For each intent:
- label: what the user wants (verb + object)
- parameters: extracted values (names, dates, targets)
- priority: primary, secondary, or implied
- ambiguity: clear, needs-clarification, or vague
- clarification: (if ambiguous) question to ask

Message:
{{input}}
```

## Examples

**Input:** "Fix the LinkedIn URL on the video engineer page and also check if the Trailkeeper errors are still broken"

**Output:**
1. `{ label: "fix-url", parameters: { file: "video-engineer.html", target: "LinkedIn" }, priority: "primary", ambiguity: "clear" }`
2. `{ label: "verify-bug-status", parameters: { project: "Trailkeeper", bug: "error differentiation" }, priority: "secondary", ambiguity: "needs-clarification", clarification: "Which specific errors — timeout vs network, or all error handling?" }`
