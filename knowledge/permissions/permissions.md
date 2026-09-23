# Permissions — Knowledge Agent (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. The Knowledge Agent reads history broadly but
owns the Training Room as a **proposal** surface — canonical writes require Owner approval.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (decisions, outcomes, history)
- `workflow_instances` (`ceo_decision`, `ceo_reviewed_at`, `aggregated_outputs`, `state`),
  `tasks.output_data`, `world_events`, and existing Training Room entries.
- Owner feedback via Board Meeting / Approval Inbox outcomes.
- The Performance Analyst's Post-Launch Performance Pack, `content_assets` (what ran), and the
  AI Cost Manager's round cost — the Loop Closer's evidence base. **Read via their reports**:
  the Knowledge Agent holds no Meta/Shopify connector access of its own.

## Write — Training Room drafts (owned system)
- Draft structured knowledge entries and **proposed** Training Room updates (with source, date,
  confidence).
- Flags for stale / contradicted / low-confidence knowledge.
- Loop-Closer reports: lessons, do-not-repeat items, and proposed canonical rules — all as
  drafts/proposals to `tasks.output_data`.
- Canonical entries are **not** written directly — they are proposed.

## Execute
- Answer knowledge queries with sourced facts; run knowledge-hygiene passes.
- Run the Loop Closer on a campaign that has met the signal bar (`skills/loop-closer.md`).

## Requires Owner Approval
- Promoting any proposed change to **canonical** owner preferences or brand rules.
- Resolving a source conflict into a single canonical truth.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no business decisions, never fabricate facts,
  never overwrite canonical knowledge without approval, no spend/publish/live-system changes.
