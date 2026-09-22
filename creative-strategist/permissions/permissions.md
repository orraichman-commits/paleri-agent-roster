# Permissions — Creative Strategist (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within the Creative Office (creative briefs and brief-fit reviews).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational context)
- Task brief and `shared_context.upstream_outputs` (Product/Market Research, Market Analyst
  viability, Strategic Intelligence); `missing_upstream`.
- Training Room brand rules, tone, prior winning angles (curated by the Knowledge Agent).
- Product/campaign operational context — read-only.

## Write — Creative Office only (owned system)
- Creative briefs to `tasks.output_data` (become the production agents' upstream context).
- Brief-fit review verdicts on returned creative.

## Execute
- Define angle/format/awareness; route briefs to production agents; review outputs for fit.

## Requires Owner Approval
- Paid-tool spend / external API calls (Level 1 approval); nothing published.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no spend/launch/product decisions; never
  publish; never brief a misleading/medical/competitor claim.
