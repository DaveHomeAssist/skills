---
name: Status Naming
category: Operating Convention
purpose: Give every piece of work one name that carries its status light
---

# Status Naming

**Category:** Operating Convention
**Purpose:** Give every piece of work one name that carries its status light

This is the canonical source. Repositories carry a short copy of the format in
their `AGENTS.md` or `CLAUDE.md`; when the two disagree, this file wins.

## Format

```
Project | 🚦 | Phase | Title → state, reason | MM-DD
```

The same string is used everywhere the work is named:

- the status title in chat (the first line of a status report),
- the session title (the rename line),
- the `Human Name` of the row in Notion **DB | Status Check Runs**.

## Fields

| Field | Rule |
|---|---|
| **Project** | The product or workstream, as named in DB \| Projects & Software (for example `System by Dave`, `Garden OS`). |
| **🚦** | The light, then an optional modifier. |
| **Phase** | One of `Research`, `Design`, `Build`, `Audit`, `Scheduled`. |
| **Title → state, reason** | A short title for the work, an arrow, a state word, and the reason in a few words. |
| **MM-DD** | The date of the latest light change. |

### Lights

| Light | Meaning |
|---|---|
| 🟢 | Complete and verified |
| 🟡 | Partial or unconfirmed |
| 🔴 | Not started, blocked or failed |
| ⚪ | Unverifiable: no source of truth, or the query failed |

### Modifiers

Append to 🟡, 🔴 or ⚪, never to 🟢. A modifier never raises the light.

| Modifier | Meaning |
|---|---|
| ⏳ | Scheduled: parked by design, clears on a known date (needs a Resolve By date) |
| 🙋 | Awaiting Dave: needs a decision from Dave (needs a one-line ask) |
| 🚧 | Blocked: external dependency (name the blocker) |
| *(none)* | Active: actionable now, agent owned |

## Rules

1. **Every light change produces a new name.** Give it in chat as a `RENAME:` line
   and write it to the Notion row's `Human Name` in the same step.
2. **One light per name.** If parts differ, use the lowest light and say which part
   lags in the reason.
3. **The title light and the table light match**, modifier included.
4. **Verify before naming.** A light comes from a checked source (record, commit,
   deploy, live page), never from the conversation alone. If nothing can be checked,
   the light is ⚪.

## Examples

```
System by Dave | 🔴🙋 | Build | fmp-suite preview → back online, Branch needs None | 09-25
System by Dave | 🟡 | Build | AV + three.js fixes → 3 merged, rig readback pending | 09-25
System by Dave | 🟢 | Build | AV + three.js fixes → rig, Throwline, switcher guide live | 09-25
Garden OS | 🟡⏳ | Scheduled | Frost alerts → built, activation parked to 10-15 | 09-25
Tech | ⚪ | Research | Canon ELPH 340 HS teardown → no source record yet | 08-18
```

## Repository copy

Paste this into a repository's `AGENTS.md` (or `CLAUDE.md` when that is the file
agents read first):

```markdown
## Status naming

Name work with one string everywhere (chat status title, session title, Notion
Status Check Runs "Human Name"):

`Project | 🚦 | Phase | Title → state, reason | MM-DD`

- 🚦: 🟢 complete and verified · 🟡 partial · 🔴 not started, blocked or failed · ⚪ unverifiable.
  Add ⏳ scheduled, 🙋 awaiting Dave or 🚧 blocked to 🟡/🔴/⚪, never to 🟢.
- Phase: Research, Design, Build, Audit or Scheduled. MM-DD: date of the latest light change.
- Every light change gets a new name: a `RENAME:` line in chat and the Notion row updated.
- Canonical source: https://github.com/DaveHomeAssist/skills/blob/master/status-naming.md
```
