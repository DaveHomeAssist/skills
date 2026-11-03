---
name: Status Naming
category: Operating Convention
purpose: Stable session identity with established project emoji categories
---

# Session naming

Canonical rule, updated at Dave's direction on 2026-11-03. Repository adapters,
logging skills and communications instructions defer here. Direct current user
instructions and deliberate manual titles take precedence. This replaces earlier
status-light, creation-date, clock-time and status-change rename schemes.

## Format

`<project emoji> | <Title> | <Phase> | <MM-DD>`

- `🧪 | Desktop Freeze and Quick Prompts | Audit | 10-27`
- `🔫 | BUS073 Work | Build | 10-17`
- `🎤 | Stage Controls | Review | 10-18`
- `👾 | Tool Routing | Fix | 10-18`

The project heading supplies the project name; do not repeat it as a separate
field in the chat title. Keep exactly four fields, separated by ` | `. Use a
concise, recognizable title and preserve useful identifiers such as BUS073.
Phases use title case: Research, Plan, Design, Build, Fix, Audit, Review, Verify,
Release, Ops and Scheduled. Select the phase from actual work, not a completion
claim. This format supersedes project-name-first, phase-before-title and mandatory
parent/subproject-pair formats, including older literals in repository adapters.

## Date and stability

MM-DD is the verified latest meaningful conversation activity date in
America/New_York when an authorized title is generated or updated. Use actual
conversation evidence; a rename, metadata cleanup or status poll is not meaningful
activity. Do not substitute the creation date or today's date for unavailable
activity evidence. Leave an existing title unchanged when that evidence is uncertain.
For a new conversation, the current substantive request supplies the activity date.
The date stays stable between authorized naming events: no daily rollover, periodic
refresh or status-change rename. Put exact timestamps and verification status in
the report body, never in the title.

## Emoji categories

Use the project's established emoji consistently across its chats. Read the
current project heading and verified project identity before selecting it.
Decorative repeated symbols, cloud markers and host badges in a heading are not
additional title fields. The Workspace and Systems headings provide examples:
System Workflows uses ⚙️, Network + Homelab uses 🌐, Notion Agent uses 🧩 and
Stream Deck uses 🎛️. Preserve those headings themselves.

Use one project emoji in a newly generated title. Existing parent/subproject
pairs remain historical identities, not a requirement to repeat both symbols.
An established substantial subproject may retain its established category emoji;
do not create a category for each bug, phase, tool, machine or one-off task.
Only branch into a new emoji category when distinct, substantial ongoing work
justifies it. Record the durable scope and reason in this registry before using
the new category consistently. A phase or status change never justifies a new
emoji. Where identity is uncertain, preserve the existing title rather than guess.

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
