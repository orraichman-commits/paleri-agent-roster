# Tool — Systems (CEO Executive Control Center)

The major systems the CEO uses or receives information from, with an honest status for each.
**Status legend:** `WIRED` (connected and in use) · `PARTIAL` (exists but capability
incomplete) · `PLANNED — NOT YET WIRED` (do not assume it exists).

Do not treat a `PLANNED` system as available. Where a system produces authoritative data,
see `data-sources.md` for its trust level.

---

## Workflow Engine — `WIRED`
Orchestrates multi-step work as `workflow_instances` built from workflow templates. Runs in
waves with a race-safe fan-in barrier. Source of workflow state (`state`, `current_wave`,
`wave_plan`, `aggregated_outputs`).

## GOD Runtime — `WIRED`
The **deterministic** orchestration engine. No AI, no reasoning, no business judgment. It
routes tasks, enforces `consumes`-based shared context, and assembles the CEO Package. The
CEO never directs GOD as a brain; GOD only executes deterministic orchestration.

## Agent Runtime — `PARTIAL`
Executes agents against their brains. Real execution is currently gated in code to a single
agent (`copywriter`); other agents are defined but not yet enabled for live execution. Treat
non-copywriter execution as not yet available.

This is an **execution-wiring gate, not an org statement.** `visual-producer` and
`video-editor` are full, mandatory stages of the Creative chain whose runtime is not enabled
yet — not optional or future roles. Plan the whole chain; report honestly which stages can
execute for real today.

## Supervisor — `PARTIAL`
The operational supervisor brain exists and produces Shift Reports, but it is **not yet wired
into the runtime execution loop**. Use its reports as advisory input when available; do not
assume automatic, continuous supervision yet. The Supervisor covers machinery health only — it
does not do business post-mortems (Loop Closer) or organizational recommendations (Board Ops).

## Board Ops — `PARTIAL`
The org-efficiency agent is seeded (migration `030_board_ops_agent.sql`) and can be declared as
a workflow specialist. It sits in the Finance Office in the DB (`agents.office_id` is NOT NULL)
while remaining cross-cutting in doctrine. The approved cadence is **Thursday evening**
(a chat message, not a deck). The CEO wakes it. `schedules/` is not a wired cron — do not
invent one — and never act on a pack as if the Owner already approved it.

## Loop Closer — `PARTIAL` (skill + workflow, not a system)
Post-launch market learning: `performance-analyst` assembles the Post-Launch Performance Pack,
`knowledge` turns it into lessons, do-not-repeat items, and proposed Training Room updates, and
the CEO consumes the summary. The `loop-closer` workflow template
(`031_loop_closer_workflow.sql`) chains the two steps, with the Knowledge step approval-gated —
so the skill has a real execution path rather than being brain text nothing can invoke.

It remains **gated by its data sources**: Meta is not wired and Shopify is
connector-conditional, so today the loop closes only on what is actually connected. With
insufficient live campaign data the correct output is a coverage-gap note with a re-run
condition — never a post-mortem built from imagined numbers.

## Knowledge Agent — `PARTIAL`
The Knowledge Agent brain and its record exist and can answer/curate. The automatic
learning-from-outcomes loop is **not yet implemented**. Curated knowledge is available;
continuous auto-learning is planned.

## Training Room — `PARTIAL`
The reference layer for brand rules, owner philosophy, product/decision history, and market
insights, curated by the Knowledge Agent. The canonical, fully-backed store is still being
built out; treat entries as curated and confidence-rated, not absolute.

## CEO Package — `WIRED`
The deterministic technical package GOD assembles on workflow completion
(`workflow_instances.ceo_package`): participating agents, agent outputs, `missing_outputs`,
errors, `assembled_by`. It is the CEO's primary evidence bundle for a business decision.

## Event Ledger — `WIRED`
The operational spine: one append-only event stream (`ledger_events`, namespaced
`domain.action` types with severity, actor, and subject references). **Source of truth for
what happened.** `world_events` is kept only as a legacy projection during migration —
new reasoning should read the ledger.

## Artifact Store — `WIRED`
Everything the company produces lands in `content_assets`: lifecycle
`draft → in_review → approved/rejected → published → archived`, plus a separate market-verdict
`performance_state`. Real-execution outputs dual-write an artifact alongside
`tasks.output_data`; owner review transitions the artifact and emits `artifact.*` events.
Browsable at `/artifacts`.

## Decision Queue — `WIRED`
The Owner's real approval surface: tasks in `waiting_approval` (plus any legacy
approval_requests), rendered by one shared ReviewQueue in the Review drawer and
`/approval-inbox`. Approve/reject releases the workload slot, transitions the artifact,
and notifies GOD to advance the workflow.

## Supabase — `WIRED`
The database of record underneath the Workflow Engine, tasks, events, and budget data. The
underlying source of truth for most CEO inputs.

## Shopify — `CONDITIONAL` (connector)
Live store data and publishing, available **only when the connector is connected**. When it
is not, all store work is draft. Never assume live Shopify actions occurred without a
connected connector and Owner approval.

## Meta (Ads) — `PLANNED — NOT YET WIRED`
Paid-media platform for campaigns and ad performance. Not connected yet. Do not assume Meta
campaign data or publishing is available.

## Board Meeting — `WIRED`
The CEO's primary intake channel for owner commands, department escalations, and requests,
and the channel the CEO responds on (see `agents/ceo/outputs/schema.md`).

## Approval Inbox — `WIRED`
Where actions that cross a Hard Limit or exceed autonomy wait for Owner approval, and where
prior approvals/rejections are recorded.
