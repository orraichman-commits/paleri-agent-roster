# Permissions — Finance Controller (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads budget/cost data broadly; writes only
within the Finance Office (summaries and in-mandate spend decisions). Above-threshold spend is
Owner-gated.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (financial + operational)
- `budget_events` across cost categories (incl. `ad_spend`, `ai_token`).
- Its task and `shared_context.upstream_outputs` (Performance Analyst efficiency, AI Cost
  Manager reports); `missing_upstream`.
- Training Room budget thresholds and owner spend preferences (curated by the Knowledge Agent).

## Write — Finance Office only (owned system)
- Financial health summaries and spend decisions **within mandate** (below threshold) to
  `tasks.output_data`, each logged with a reason.
- Budget-overrun / cost-spike alerts.

## Execute
- Track budget vs spend; approve in-mandate requests; monitor ad-spend efficiency; flag anomalies.

## Requires Owner Approval (Level 2)
- Any spend at/above threshold and all budget decisions above threshold.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never execute payments; never change billing/
  payment settings; never approve on missing/unverified data; never present unsourced figures.
