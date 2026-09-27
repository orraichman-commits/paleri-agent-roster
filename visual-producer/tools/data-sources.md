# Tools / Data Sources — Visual Producer

Authoritative inputs. Read fresh; never assume.

## Setup connections

In SETUP, ask Or, in your own chat, to connect exactly this list. Then stop. Chat groups are membership, not a connector (see Lifecycle in `instructions.md`).

| Connector | Account / project | Access | What it's for |
|---|---|---|---|
| GitHub | `orraichman-commits/paleri-agent-roster` | read | This pack, and Training Room canon under `knowledge/memory/` |
| Foreplay | Or's Foreplay account | read | Open the cited ads before generation. You do not mine new ones, and you do not publish |
| Higgsfield | API secret `HIGGSFIELD_API_KEY` | generate | Image and visual generation for the brief. Not a publish right, and not a live ad. Never write the key into the repo, a prompt, or an output |
| Notion | Video approval log — [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce) | read | Read before every job. You do not write this log |
| Notion | Training Room living layer — [NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26) | read | Do-not-repeat, lessons, brand visual rules. Canon stays in the repo |

If the Higgsfield key is absent or the API is unwired, deliver specs and mark `requires connector`. Do not claim a file exists.

## What you read

- **The upstream package** in the company group — the creative brief (`creative-strategist`), the copy (`copywriter`), research, the customer-intelligence avatar and pains, the product and offer, and the exact Foreplay links/IDs. If a named input never arrived, say so. Do not invent the ad.
- **Foreplay** — open the cited ads before generation. Read those ads. Do not mine new ones.
- **Higgsfield API** — image generation for this job (and a source clip the brief needs as an asset). Authenticate with the secret `HIGGSFIELD_API_KEY` (environment variable). Generation is allowed. Publishing, credit purchases, plan changes, and any spend that is not generation are not.
- **Canon in the repo** — brand visual rules, palette, logo usage, denylist, and Meta boundaries under `knowledge/memory/`.
- **Notion video log** — [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce). Read it before every job.
- **Notion Training Room** — [NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26). Do-not-repeat and brand visual rules.
- **Product imagery** the brief points at.

## Where work actually moves

There is no GOD Runtime and no database.

- Post the assets (or the spec, if Higgsfield is not connected) in the **company group** and wake `video-editor`, with the same Foreplay link or ID.
- You do not wake `shopify` or `marketing`. Nothing you make is published. You do not ask Or to approve an image. You do not message Or after SETUP.
- You do not write the **PALERI task board** or the video approval log. The Notion memory bot (Knowledge Agent) records them.

## Not available yet

`workflow_instances`, `tasks`, `tasks.output_data`, `world_events`, `ceo_package`, `ledger_events`, `content_assets`, `budget_events`, the Decision Queue, and the Approval Inbox. Do not look for them.
