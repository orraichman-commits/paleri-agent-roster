# Tools / Data Sources — Marketing

Authoritative inputs. Read fresh; never assume. Reads are read-only. Nothing here writes to Ads Manager.

## Setup connections

In SETUP, ask Or, in your own chat, to connect exactly this list. Then stop. Chat groups are membership, not a connector (see Lifecycle in `instructions.md`).

| Connector | Account / project | Access | What it's for |
|---|---|---|---|
| GitHub | `orraichman-commits/paleri-agent-roster` | read | This pack, canon, and the products-table file the CEO keeps in the repo |
| Meta Ads | Or's Meta ad account | read-only | Spend, ROAS, and the diagnostic set (CPA, CTR, CPC, frequency). No create, no edit, no budget change, no pause |
| Shopify analytics | Or's Shopify store | read | Orders and store context behind a daily read. You do not edit the store |

You do not need Notion. Canon is in the repo: `knowledge/memory/meta-ads-structure.md`, `knowledge/memory/unit-economics.md`, `knowledge/memory/funnels.md`. You are in the company group and the management group.

Break-even is the row in `ceo/memory/products-table.md` and, when the CEO has updated it, the same row on Or's Google Sheet. You read the row the CEO points you at. You do not edit the sheet. The CEO does. Finance reads the sheet.

## What you read

- **Pre-publish** — creative-chain outputs (brief, copy, visuals, video) and the Shopify draft, in the company group. Finance's last budget opinion when it exists.
- **Campaign identity** — name and ID, passed on by the CEO after Or confirms launch. Without that pass-on, the daily read does not start. You do not ask Or for it.
- **Meta Ads** — read-only. Unwired means a coverage gap, not a guess. Same honesty rule as `performance-analyst/tools/analytics.md`.
- **Shopify analytics** — read only.
- **Break-even** — the CEO's products table. You do not edit it.

## Where work actually moves

There is no GOD Runtime and no database.

- Pre-publish: post the ABO plan in the **company group** and wake `finance-controller`. Finance's opinion goes to the CEO for the Gate 2 deck. You do not send the deck and you do not ask Or to publish.
- Post-publish: post the daily read in the **company group** and in the **management group**. Wake `finance-controller` only for a budget **increase**. Cuts and kills go to the CEO by DM to **`paleri os ceo`**, for the short daily message. You do not message Or.
- You do not write the **PALERI task board**. The Notion memory bot (Knowledge Agent) records it.

## Not available yet

`workflow_instances`, `tasks`, `tasks.output_data`, `world_events`, `ceo_package`, `ledger_events`, `content_assets`, `budget_events`, the Decision Queue, and the Approval Inbox. A write connection to Meta Ads. Do not look for them.
