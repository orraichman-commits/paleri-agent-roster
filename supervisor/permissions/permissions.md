# Permissions — Supervisor (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. The Supervisor reads broadly to observe the
whole machinery, but owns no live system and writes only its own reports.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational health)
- `workflow_instances`, `tasks` (state, `output_data`, `input_data.shared_context`),
  `world_events`, `ceo_package`, and agent load signals.

## Write — reports only (its own output)
- Its Shift Reports and operational fix recommendations (to `tasks.output_data` when run in a
  task context).
- The Supervisor writes to **no** live system, workflow, agent, or shared context.

## Execute
- Run health checks and produce Shift Reports.

## Requires Owner Approval
- Nothing to execute directly — the Supervisor recommends. Any fix it proposes that touches a
  live system is executed by others under their own approval rules.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no business decisions, no live-system changes,
  no spend/publish, never override the CEO or GOD.
