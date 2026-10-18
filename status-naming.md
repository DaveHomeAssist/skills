---
name: Status Naming
category: Operating Convention
purpose: Give work a recognizable project, phase, title and date while preserving manual names
---

# Status Naming

Updated by Dave on 2026-10-18. This is the canonical source; repository copies
inherit it. It supersedes status-light titles and date-plus-time naming formats.

## Format

`<emoji> <Project> | <PHASE> | <Title> <MM-DD>`

Examples:

- `🕹️🔫 BlockBiz | BUILD | BUS073 Work 10-17`
- `🧪 PromptLab | REVIEW | Create Slice 2A 10-18`
- `🏰 EMPIRES | BUILD | Sprite Rendering 10-18`

## Rules

- Lead with the established project emoji (one or more symbols) and preserve the project's normal spelling and capitalization.
- Use an uppercase phase: RESEARCH, PLAN, DESIGN, BUILD, FIX, AUDIT, REVIEW, VERIFY, RELEASE, OPS or SCHEDULED.
- Keep the title concise and recognizable; preserve identifiers such as BUS073 and filenames.
- End with the task's creation date in America/New_York as MM-DD; retain it across status changes. Use the current Eastern date when first applying the format to an undated task.
- Do not include a status light, progress badge, reason, clock time or automatic date rollover. Put status, evidence and blockers in the body.
- Preserve a title Dave sets manually, even if it differs from this format. Naming rules never authorize overwriting his title; rename it only when he explicitly asks.
- For agent-generated titles, update only when the work's material scope changes or Dave asks; unchanged checks and status changes do not trigger a rename.
- Existing historical logs and Notion rows retain their names; do not bulk rename tasks or write to Notion solely to enforce this format.

## Status reporting

Status remains evidence based and belongs in the report body. The familiar
Green/Yellow/Red/Grey or traffic-light indicators may still describe verification
there; they are not title fields. A stable task title never proves completion.
Use the same user-approved title when an authorized status record needs a name;
creating or renaming that record requires the normal task scope and readback.

## Repository copy

Repository instructions should link to this document, reproduce the format and
manual-title preservation rule, and remove contradictory local naming formats.
