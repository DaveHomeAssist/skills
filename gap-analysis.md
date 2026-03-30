---
name: Gap Analysis
category: Cowork
purpose: Find missing components or risks
---

# Gap Analysis

**Category:** Cowork
**Purpose:** Find missing components or risks

## Description

Spot blind spots and suggest additions to plans, prompts, systems, or specs. Answers: "What's missing that should be here?" Different from Critique — Gap Analysis focuses on absence, not quality.

## Input

- Plan, spec, checklist, system design, or prompt to analyze
- Optional: reference standard (what "complete" looks like — e.g., OWASP top 10, a competitor's feature set)
- Optional: scope (security gaps, UX gaps, data gaps, process gaps)

## Output Contract

- Each gap includes: what's missing, why it matters, suggested addition
- Gaps ranked by impact (critical / important / nice-to-have)
- No false positives — only flag genuinely missing things, not style preferences
- If a reference standard is provided, gaps are mapped to specific standard items

## Prompt

```
Analyze the following for gaps and missing components.

{{#if reference}}Reference standard: {{reference}}{{/if}}
{{#if scope}}Focus on: {{scope}}{{/if}}

For each gap, provide:
- **What's missing**: specific component or coverage
- **Why it matters**: risk or consequence of the gap
- **Suggested addition**: how to close the gap
- **Impact**: critical, important, or nice-to-have

Input:
{{input}}
```

## Examples

**Input:** A deployment checklist for a new web app

**Output:** Missing: no rollback plan (critical), no monitoring/alerting setup (critical), no load testing before launch (important), no runbook for on-call (nice-to-have).
