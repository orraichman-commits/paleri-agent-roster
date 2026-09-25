# Permissions — Product Research Agent (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within its office (research reports).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational + research context)
- Its task and `shared_context.upstream_outputs` (Market Research trends, Strategic
  Intelligence); `missing_upstream`.
- Training Room product criteria and prior product verdicts (curated by the Knowledge Agent).
- External research connectors (read-only, when connected and approved). No supplier lookup.

## Write — Research Lab only (owned system)
- Structured product research reports to `tasks.output_data` for handoff to the Market Analyst.

## Execute
- Run product research; record AliExpress unit cost; score candidates against criteria;
  qualify/reject with evidence. Do not search for a supplier.

## Requires Owner Approval
- Paid research tools / external APIs not yet enabled (Level 1 approval).

## Forbidden
- See `../instructions.md` → **Hard Limits**: no go/no-go/spend/launch decisions; never
  contact suppliers/customers; never publish; never present fabricated data as fact.
