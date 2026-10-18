---
name: Status Naming
category: Operating Convention
purpose: Stable session identity with a canonical project and parent/subproject emoji map
---

# Session naming

Canonical rule, updated at Dave's direction on 2026-10-18. Repository adapters,
logging skills and communications instructions defer here. Direct current user
instructions and deliberate manual titles take precedence. This replaces earlier
status-light, creation-date, clock-time and status-change rename schemes.

## Format

`<emoji(s)> <Project> | <PHASE> | <Title> <MM-DD>`

- `🕹️🔫 BlockBiz | BUILD | BUS073 Work 10-17`
- `🕹️🎤 Front of House | REVIEW | Stage Controls 10-18`
- `👾 DaveLLM | FIX | Tool Routing 10-18`
- `🧪 PromptLab | REVIEW | Create Slice 2A 10-18`

Preserve normal project spelling and capitalization and useful identifiers such
as BUS073. Use a concise, recognizable scope. Standard phases are RESEARCH,
PLAN, DESIGN, BUILD, FIX, AUDIT, REVIEW, VERIFY, RELEASE, OPS and SCHEDULED.
Select the phase from actual work, not from a completion claim.

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

## Emoji map

A standalone project uses one emoji. A project family with subprojects uses two:
parent first, subproject second, with no space between them. Family-wide work uses
the explicitly mapped overview/catalog symbol as its second emoji. Never add a
third status, clock, cloud or workflow symbol to a newly generated standard title.
These mappings establish the naming registry; they do not change product ownership.

| Parent / standalone | Scope / project label | Prefix |
| --- | --- | --- |
| MixMash | MixMash (family-wide work) | 🕹️🗂️ |
| MixMash | MixMash Catalog | 🕹️🗂️ |
| MixMash | BlockBiz | 🕹️🔫 |
| MixMash | Front of House | 🕹️🎤 |
| MixMash | EMPIRES | 🕹️🏰 |
| MixMash | Horseshoes | 🕹️🐴 |
| MixMash | Curling Simulator | 🕹️🥌 |
| MixMash | Zelda2MarioCoop | 🕹️🍄 |
| FMP | FMP (family-wide work) | 🏟️🗂️ |
| FMP | FMP Displays | 🏟️📺 |
| FMP | FMP Cameras | 🏟️🎥 |
| FMP | FMP Switcher Ops | 🏟️🎛️ |
| DaveLLM (explicit primary-name exception) | DaveLLM | 👾 |
| DaveLLM | DaveHarness | 👾🧰 |
| Standalone | PromptLab | 🧪 |
| System by Dave | System by Dave (family-wide work) | ⚙️🗂️ |
| System by Dave | AVbyDave | ⚙️🎥 |
| Standalone | CueForge | 🎬 |
| Standalone | NoteForge | 📝 |
| Standalone | Garden OS | 🪴 |
| Standalone | CurlPlan | 🥌 |
| Standalone | Syrum | 🌊 |
| Standalone | Workspace | 🗂️ |

Dave explicitly specified `👾 DaveLLM |`; that primary title keeps one emoji even
though its named DaveHarness subproject uses the parent/subproject pair. Independent
products remain independent even when another project hosts a release or links to them.

The Catalog/overview symbol 🗂️ is now a defined mapping, replacing its previous
provisional cleanup assignment. For an unlisted project, preserve its verified
existing symbol and label; do not invent parentage or borrow a similar project's
identity. Record a new mapping here when the project relationship is established.

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
- A requested status report retains evidence-based Green/Yellow/Red/Grey or traffic
  lights in its body. Verification requirements remain intact. A title proves no
  completion, merge, deployment or physical acceptance.
- An independently authorized new log or Notion record may use the session title;
  its schema, status fields, routing and write/readback rules still govern it.

## Propagation and validation

Adapters link here instead of copying the map or date rules. Remove superseded
local title schemas, automatic RENAME directives and status-triggered Notion writes.
A deliberate local exception must identify its scope and purpose and stay within
higher authority. A report-only audit checks format and mapping only for eligible,
agent-generated titles; it reports protected and uncertain titles without mutation.
Changing this policy does not authorize a bulk rename or wake existing sessions.
