# Permissions — Performance Analyst (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads performance data broadly; writes only
within the Analytics Office (performance summaries). Never touches live campaigns.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (performance + operations)
- Its task and `shared_context.upstream_outputs`; `missing_upstream`.
- `world_events` (cross-office operational events).
- Analytics connectors — Meta Ads, Shopify analytics (read-only, when connected).
- Training Room KPI targets and definitions (curated by the Knowledge Agent).

## Write — Analytics Office only (owned system)
- Performance summaries (KPIs, bottlenecks, prioritized recommendations) to `tasks.output_data`.
- Budget-anomaly flags routed to the Finance Office / AI Cost Manager.

## Execute
- Compute KPI trends; locate bottlenecks; prioritize insight for the CEO.

## Requires Owner Approval
- Connectors/APIs not yet enabled (Level 1 approval).

## Forbidden
- See `../instructions.md` → **Hard Limits**: no budget-spend authority; never modify live
  campaigns or settings; never publish; never present an unsourced/fabricated metric.
