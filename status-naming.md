---
name: Status Naming
category: Operating Convention
purpose: Stable session identity with established project emoji categories
---

# Session naming

Canonical rule, updated at Dave's direction on 2026-11-17. Repository adapters,
logging skills, memories and communications instructions defer here. Direct
current user instructions and deliberate manual titles take precedence. This
replaces the 2026-11-03 `<emoji> | <Title> | <Phase> | <MM-DD>` rule and every
earlier status-light (🚦, "→ state, reason"), project-name-first and
time-in-the-middle scheme.

## Format

`<group emoji> | PHASE | Durable Purpose | MM-DD h:mm AM/PM`

- `❄️ | FIX | Studio P3-P4 Temp Readback (PR 463) | 11-12 1:58 AM`
- `❄️ | PREP | Lamp Change And AV Video Plan | 11-14 10:51 AM`
- `📝 | OPS | Storage Register and Second-Copy Plan | 11-09 4:50 PM`
- `☃️ | ORCHESTRATOR | Frozen Group Command | 11-17 1:06 AM`

Exactly four fields, separated by ` | `.

- **Group emoji:** the emoji of the session's Claude Code sidebar group (for
  example ❄️ Frozen, 🎥 AV By Dave, 🧪 Prompt Lab, 📝 Ops, 💻 Dev Tools,
  🕹️ Games, 🧩 One Offs). Use the registry below when the session has no group
  or the group has no emoji, and 📁 if neither applies. Use one emoji.
- **PHASE:** one uppercase word or short phrase for the kind of work the session
  owns from now on: RESEARCH, PLAN, DESIGN, BUILD, FIX, AUDIT, REVIEW, VERIFY,
  PREP, RELEASE, ACCESS, OPS, FILE CLEANUP, SCHEDULED. ORCHESTRATOR is reserved
  for a group's orchestrator session, which uses its persona emoji (☃️ for
  Frozen) in place of the group emoji and stays pinned.
- **Durable Purpose:** two to six words in Title Case naming why the session
  still exists: the deliverable, owned area or blocker, not whatever it happened
  to do first. Keep useful identifiers such as `(PR 463)` or `BUS073`. Don't
  repeat the PHASE word. Keep a marker Dave added himself, such as KEEP.
- **MM-DD h:mm AM/PM:** the session's creation time (`createdAt`) converted to
  America/New_York. Late-evening UTC times fall on the previous day.

Keep the whole title under about 70 characters.

## Stability

The date and time never change: they identify the session. Rename only when the
session's durable purpose or phase has really changed, or on Dave's request.
Status, verification results, traffic lights and "→ state" clauses belong in
the report body, never in the title. A status change is not a reason to rename.

## Emoji registry

The sidebar group emoji leads. This registry supplies the emoji for ungrouped
sessions and for groups without one. Add a category only for substantial ongoing
work, and record it here first.

| Established project or category | Emoji |
| --- | --- |
| MixMash and its catalog | 🕹️ |
| BlockBiz / Block Business | 🔫 |
| Front of House | 🎤 |
| EMPIRES | 🏰 |
| Horseshoes | 🐴 |
| Curling Simulator / CurlPlan | 🥌 |
| Zelda2MarioCoop | 🍄 |
| FMP | 🏟️ |
| DaveLLM / DaveHarness | 👾 |
| PromptLab | 🧪 |
| System by Dave / System Workflows | ⚙️ |
| AVbyDave | 🎥 |
| CueForge | 🎟️ |
| NoteForge | 📝 |
| Garden OS | 🌿 |
| Syrum | 🌊 |
| Workspace organization | 🗂️ |
| Dave computer workspace | 💻 |
| Network + Homelab | 🌐 |
| Notion Agent | 🧩 |
| Stream Deck | 🎛️ |

The registry preserves established categories and does not change ownership or
merge projects that share an emoji. Current deliberate project headings take
precedence over an older registry symbol. For an unlisted project, preserve its
verified existing emoji; add a new category only under the ongoing-work rule above.

## Purposeful exceptions and boundaries

- Preserve any title Dave sets manually, even if nonconforming. Only an explicit
  request to rename that particular title overrides it.
- Bulk cleanup excludes active, pinned, reference, owner, automation and uncertain
  sessions. Their existing names remain protected. An explicit scoped request may
  name a specific exception; this policy itself does not authorize touching them.
- Existing project/sidebar labels (including repeated emojis), cloud/clock workflow
  labels and durable owner labels are separate surfaces. Preserve them until their
  purpose and specific change authority are known.
- Historical logs, Notion records, filenames, routing tokens, database IDs, product
  labels and scheduled-job identifiers retain their own contracts. Do not retrofit
  them or synchronize them automatically with a chat title.
- A communications entry records the existing manual title, or a canonical proposed
  title if needed. Writing the entry does not rename the chat.
- A requested status report follows the active workspace reporting contract and
  its approved status vocabulary. This naming rule defines no separate status
  system. Verification requirements remain intact. A title proves no completion,
  merge, deployment or physical acceptance.
- An independently authorized new log or Notion record may use the session title;
  its schema, status fields, routing and write/readback rules still govern it.

## Propagation and validation

Adapters link here instead of copying the map or date rules. Remove superseded
local title schemas, automatic RENAME directives and status-triggered Notion writes.
A deliberate local exception must identify its scope and purpose and stay within
higher authority. A report-only audit checks format and mapping only for eligible,
agent-generated titles; it reports protected and uncertain titles without mutation.
Changing this policy does not authorize a bulk rename or wake existing sessions.
