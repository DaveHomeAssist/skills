---
name: Workflow Automation
category: Notion-Specific
purpose: Define automated triggers and actions
---

# Workflow Automation

**Category:** Notion-Specific
**Purpose:** Define automated triggers and actions

## Description

Specify triggers, actions, tools, and output formats for automation. Designs the "when X happens, do Y" logic for Notion automations, GitHub Actions, cron jobs, and agent pipelines.

## Input

- Goal (what should happen automatically)
- Trigger (what event starts the workflow)
- Optional: tools available (Notion API, GitHub Actions, cron, webhooks, agents)
- Optional: constraints (frequency limits, cost, permissions)

## Output Contract

- Trigger specification (event, condition, schedule)
- Action sequence (ordered steps with inputs/outputs)
- Error handling (what happens when a step fails)
- Tool mapping (which tool executes each step)
- YAML/JSON config if target platform supports it (e.g., GitHub Actions workflow)

## Prompt

```
Design an automation workflow.

Goal: {{goal}}
Trigger: {{trigger}}
{{#if tools}}Available tools: {{tools}}{{/if}}
{{#if constraints}}Constraints: {{constraints}}{{/if}}

Provide:
1. **Trigger** — event, condition, or schedule
2. **Steps** — ordered actions with inputs and outputs
3. **Error handling** — what happens when each step fails
4. **Tool mapping** — which tool runs each step
5. **Config** — YAML or JSON if applicable
```

## Examples

**Input:** "Automatically publish the Daily Prophet site every morning at 6am ET from Notion content"

**Output:** GitHub Actions workflow with cron trigger, Notion API query step, PowerShell build step, Pages deploy step, with error handling and diagnostic artifact upload.
