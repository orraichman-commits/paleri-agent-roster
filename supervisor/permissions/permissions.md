# Permissions — Supervisor (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. The Supervisor reads broadly to observe the
whole machinery, but owns no live system and writes only its own reports.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational health)
- The company, management, and board groups, and the PALERI task board (read only).
- Not available yet: `workflow_instances`, `tasks`, `world_events`, `ceo_package`. Do not look for them.

## Write — reports only (its own output)
- Shift Reports and operational fix recommendations, posted to the CEO and, when it is Thursday's input, the board group.
- The Supervisor writes to **no** live system, the task board, or another agent's work. Do not message Or.

## Execute
- Run health checks and produce Shift Reports.

## Requires Owner Approval
- Nothing to execute directly — the Supervisor recommends. Any fix it proposes that touches a
  live system is executed by others under their own approval rules.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no business decisions, no live-system changes,
  no spend/publish, never override the CEO. There is no GOD Runtime.
