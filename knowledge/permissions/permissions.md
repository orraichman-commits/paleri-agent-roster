# Permissions — Knowledge Agent (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. The role is held by Notion memory bot.
Living-layer writes go to Notion. Repo canon changes only by a pull request after Or
approves the proposal. The task board is a separate role and is not this permission set.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (decisions, outcomes, history)
- `workflow_instances` (`ceo_decision`, `ceo_reviewed_at`, `aggregated_outputs`, `state`),
  `tasks.output_data`, `world_events`, repo canon under `memory/`, and the Notion Training
  Room ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)), including [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce).
- Owner feedback via Board Meeting / Approval Inbox outcomes.
- The Performance Analyst's Post-Launch Performance Pack, `content_assets` (what ran), and the
  AI Cost Manager's round cost — the Loop Closer's evidence base. **Read via their reports**:
  the Knowledge Agent holds no Meta/Shopify connector access of its own.

## Write — Notion living layer, and repo canon only by PR
- Living-layer entries in the Notion Training Room ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)): lessons,
  do-not-repeat items, decision memory, product and campaign history, conflicts, and flags
  for stale or low-confidence knowledge. Each entry carries source, date, and confidence.
- Loop-Closer output goes to that Notion space. A proposed canon rule goes to the Rule
  Proposals inbox (https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa), not into a repo file.
- Append Or's video-gate decision and reason to [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce) as given.
  That append is a record. It is not a brand-rule change.
- Repo canon (`memory/niches-to-avoid.md`, `memory/product-criteria.md`,
  `memory/meta-ads-structure.md`, `memory/unit-economics.md`, `memory/funnels.md`, and the
  instruction packs) changes only by a pull request opened after Or approves the proposal
  in the inbox. No direct edit. The Notion canon mirror is regenerated from the repo after
  merge and is never hand-edited
  (https://app.notion.com/p/3e8020daae5b81888781d66360a19207). A pattern noticed in the video log becomes canon only
  that way.
- The task board is not a write target for knowledge, and knowledge is not a write target
  for task-board updates.

## Execute
- Answer knowledge queries with sourced facts; run knowledge-hygiene passes.
- Run the Loop Closer on a campaign that has met the signal bar (`skills/loop-closer.md`).

## Requires Owner Approval
- Promoting any proposed change to **canonical** owner preferences or brand rules.
- Resolving a source conflict into a single canonical truth.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no business decisions, never fabricate facts,
  never overwrite canonical knowledge without approval, no spend/publish/live-system changes.
