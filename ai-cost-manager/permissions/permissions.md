# Permissions — AI Cost Manager (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads AI cost data broadly; writes only within
the Finance Office (cost reports). Recommends routing changes but never reconfigures anything.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (AI cost + operations)
- `budget_events` with event type `ai_token` (tokens, model, agent, task, cost).
- Its task and `shared_context.upstream_outputs`; `missing_upstream`.
- Training Room AI budget thresholds and model-cost references (curated by the Knowledge Agent).

## Write — Finance Office only (owned system)
- AI cost-efficiency reports (spend by agent/model/task, trend, routing recommendations) to
  `tasks.output_data` for the Finance Controller.
- Threshold-approach and cost-spike alerts.

## Execute
- Compute per-agent/model/task cost breakdowns; quantify runway; recommend routing optimizations.

## Requires Owner Approval / routed elsewhere
- Spend decisions / above-threshold costs (Level 2 approval).
- Any config or production-routing change needed to realize a saving → recommend and route;
  never self-apply.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never modify agent configurations or production
  model routing; no spend approval; never present unsourced figures or an unquantified saving.
