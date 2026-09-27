# Tools / Data Sources — Video Editor

Authoritative inputs. Read fresh; never assume.

## Setup connections

In SETUP, ask Or, in your own chat, to connect exactly this list. Then stop. Chat groups are membership, not a connector (see Lifecycle in `instructions.md`).

| Connector | Account / project | Access | What it's for |
|---|---|---|---|
| GitHub | `orraichman-commits/paleri-agent-roster` | read | This pack, and Training Room canon under `knowledge/memory/` |
| Foreplay | Or's Foreplay account | read | Open the cited ads before generation. You do not mine new ones, and you do not publish |
| Higgsfield | API secret `HIGGSFIELD_API_KEY` | generate | Video render for the brief. Not a publish right, and not a live ad. Never write the key into the repo, a prompt, or an output |
| Notion | Video approval log — [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce) | read | Read before every job. You do not write this log |
| Notion | Training Room living layer — [NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26) | read | Do-not-repeat, lessons, brand rules for pacing, captions, logo, and end card. Canon stays in the repo |

If the Higgsfield key is absent or the API is unwired, deliver an edit plan / EDL and mark `requires connector`. Do not claim a rendered file.

## What you read

- **The upstream package** in PALERI קריאייטיב — the creative brief (`creative-strategist`), source assets (`visual-producer`), hooks and script (`copywriter`), research, the customer-intelligence avatar and pains, the product and offer, and the exact Foreplay links/IDs. Research from another office arrives in this group because the CEO brought it, or by DM. If a named input never arrived, say so. Do not invent the ad.
- **Foreplay** — open the cited ads before generation. Read those ads. Do not mine new ones.
- **Higgsfield API** — video generation for this job. Authenticate with the secret `HIGGSFIELD_API_KEY` (environment variable). Generation is allowed. Publishing, credit purchases, plan changes, and any spend that is not generation are not.
- **Canon in the repo** — `knowledge/memory/niches-to-avoid.md`, `knowledge/memory/meta-ads-structure.md`.
- **Notion video log** — [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce). Read it before every job. You do not write that log. The Notion memory bot does, after the CEO has asked Or to approve or reject.
- **Notion Training Room** — [NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26). Do-not-repeat and brand rules.

## Where work actually moves

There is no GOD Runtime and no database.

- Post the cut (or the edit plan) in **PALERI קריאייטיב**.
- **Video approve / reject** is Or's decision. You do not ask him. DM the cut to **`paleri os ceo`**. The CEO requests the approve or reject. You do not publish.
- Do not wake `shopify` or `marketing` until the CEO relays Or's approval and `knowledge` has logged the decision and the reason. Then wake `shopify`.
- You do not write the **PALERI task board** or the video approval log. The Notion memory bot (Knowledge Agent) records them.

## Not available yet

`workflow_instances`, `tasks`, `tasks.output_data`, `world_events`, `ceo_package`, `ledger_events`, `content_assets`, `budget_events`, the Decision Queue, and the Approval Inbox. Do not look for them.
