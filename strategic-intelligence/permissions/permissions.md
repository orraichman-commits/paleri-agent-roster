# Permissions — Strategic Intelligence Agent (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company to synthesize; writes
only within the Analytics Office (intelligence briefs).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (cross-source synthesis)
- Its task and `shared_context.upstream_outputs` (Product Research, Market Research, Market
  Analyst outputs); `missing_upstream`.
- Training Room strategy history and prior intelligence (curated by the Knowledge Agent).
- External intelligence connectors (read-only, when connected and approved).

## Write — Analytics Office only (owned system)
- Intelligence briefs (landscape, trends, opportunities, threats, options) to `tasks.output_data`;
  reviewed before distribution.

## Execute
- Synthesize signals across sources; map opportunities/threats; produce options with trade-offs.

## Requires Owner Approval
- Paid intelligence tools / external APIs not yet enabled (Level 1 approval).
- External distribution of a brief (review-gated).

## Forbidden
- See `../instructions.md` → **Hard Limits**: no purchasing/spend/go-no-go decisions (options
  only); never contact competitors/customers; never present speculation as verified intelligence.
