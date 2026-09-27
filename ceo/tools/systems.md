# Tool — Systems (CEO Executive Control Center)

What is actually there. Do not treat a missing system as wired.

There is **no GOD Runtime** and **no database**. Bots read their folders in this repo on every wake. Coordination is five chat groups, a DM to you (`paleri os ceo`), and the PALERI task board in Notion. A group holds at most 6 members, so there is no company-wide group. You sit in every group and bridge between them. That board is written only by the Notion memory bot, which is the Knowledge Agent. Canon stays in the repo. The Training Room living layer (lessons, video approval log) is in Notion.

`schedules/` is not a cron. You wake Thursday's review, the daily read, and the Loop Closer by naming them. Do not invent a scheduler.

---

## Chat groups — in use

- **PALERI מחקר** — you, `research-alpha`, `research-beta`, `customer-intelligence`, `market-analyst`, LIO.
- **PALERI קריאייטיב** — you, `creative-strategist`, `copywriter`, `visual-producer`, `video-editor`, `shopify`.
- **PALERI אנליטיקס** — you, `marketing`, `performance-analyst`, `strategic-intelligence`, `finance-controller`, `ai-cost-manager`.
- **PALERI הנהלה** (management) — you, `supervisor`, `board-ops`, `finance-controller`, `marketing`.
- **PALERI בורד** (board) — you, `board-ops`, `supervisor`, `finance-controller`, `ai-cost-manager`, `knowledge`.

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

They sit in the Leadership office (cross-cutting). They do not watch an office group. They follow handoffs on the task board (`knowledge` is the only writer) and in your status posts in PALERI הנהלה and PALERI בורד. Board Ops is not seated in a Finance Office table. It reports to you. You send Thursday's message to Or. `schedules/` does not fire it.

## Not available yet

GOD Runtime, workflow engine, `workflow_instances`, `tasks`, `ceo_package`, `world_events`, `ledger_events`, `content_assets`, `budget_events`, Supabase, Decision Queue, Approval Inbox, Board Meeting as a separate app, and a token-cost ledger (the AI Cost Manager must say when the figure is missing).

Do not emit `<action>{"type":"create_task"...}</action>`. Name the agent in their office group, or DM them. A handoff that crosses offices goes by DM, or through you.
