# Permissions — Market Analyst (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads research broadly; writes only within the
Analytics Office (viability analyses). It gates products but does not decide go/no-go.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (research + criteria)
- Its task and `shared_context.upstream_outputs` (research-alpha product findings,
  research-beta market intelligence, strategic-intelligence briefs); `missing_upstream`.
- Training Room product criteria, scoring rubric, prior verdicts (curated by the Knowledge Agent).

## Write — Analytics Office only (owned system)
- Viability analyses (score + evidence + route decision) to `tasks.output_data`; qualified
  products become the CEO's upstream context.

## Execute
- Score product viability reproducibly; route qualified products to the CEO; filter with reasons.

## Requires Owner Approval
- External APIs/tools not yet enabled (Level 1 approval).

## Forbidden
- See `../instructions.md` → **Hard Limits**: no final go/no-go, no budget spend, no launch;
  never contact suppliers/customers; never issue a score untraceable to criteria/evidence.
