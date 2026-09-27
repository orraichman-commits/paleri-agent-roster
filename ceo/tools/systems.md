# Tool — Systems (CEO Executive Control Center)

What is actually there. Do not treat a missing system as wired.

There is **no GOD Runtime** and **no database**. Bots read their folders in this repo on every wake. Coordination is the three chat groups, a DM to you (`paleri os ceo`), and the PALERI task board in Notion. That board is written only by the Notion memory bot, which is the Knowledge Agent. Canon stays in the repo. The Training Room living layer (lessons, video approval log) is in Notion.

`schedules/` is not a cron. You wake Thursday's review, the daily read, and the Loop Closer by naming them. Do not invent a scheduler.

---

## Chat groups — in use

- **Company** — every agent. Handoffs and deliverables.
- **Management** — you, `supervisor`, `board-ops`, `finance-controller`, `marketing`.
- **Board** — you, `board-ops`, `supervisor`, `finance-controller`, `ai-cost-manager`, `knowledge`.

Membership is also in `knowledge/memory/funnels.md`.

## Your chat with Or — in use

The only channel to Or after other agents finish SETUP. Owner commands arrive here. Gate 1, Gate 2, and the video approve/reject are requested here. The daily note and Thursday's review go out here. Or publishes by hand. There is no Board Meeting inbox and no Approval Inbox.

## Notion — in use, split by who writes

- **PALERI task board** — the Notion memory bot writes. You read.
- **Training Room living layer** — the same bot writes lessons and the video approval log. You read.
- **Canon** — `knowledge/memory/` in the repo. A change is a proposal. You ask Or. The file changes only after he accepts. The Knowledge Agent does not commit it.

## Products table — in use

Live rows: Or's Google Sheet. You read and write. Finance reads and does not write. The schema is `memory/products-table.md`. Prices without VAT. Or is עוסק פטור.

## LIO — external, not ours

You send product name and a screenshot after research finishes. LIO asks the supplier, checks every 15 minutes, updates you, and stops. You do not change LIO.

## Specialist connectors — theirs, not yours

Shopify admin (drafts only), Meta Ads (read), Shopify analytics (read), Perplexity, Foreplay, Meta Ads Library, Higgsfield (`HIGGSFIELD_API_KEY`). Each pack's **Setup connections** list is the source of truth. You do not open those accounts. A missing connector is a coverage gap in their report.

## Loop Closer — a skill, not a system

`performance-analyst` posts the pack. `knowledge` writes lessons into the Notion living layer and hands you the summary. You wake it weekly and at the end of a test. No SQL workflow. Canonical Training Room changes still need Or, and you request them.

## Supervisor and Board Ops — bots, not database rows

They read the groups and the task board. Board Ops is not seated in a Finance Office table. It reports to you. You send Thursday's message to Or. `schedules/` does not fire it.

## Not available yet

GOD Runtime, workflow engine, `workflow_instances`, `tasks`, `ceo_package`, `world_events`, `ledger_events`, `content_assets`, `budget_events`, Supabase, Decision Queue, Approval Inbox, Board Meeting as a separate app, and a token-cost ledger (the AI Cost Manager must say when the figure is missing).

Do not emit `<action>{"type":"create_task"...}</action>`. Name the agent in the company group.
