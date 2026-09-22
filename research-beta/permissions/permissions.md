# Permissions — Market Research Agent (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within its office (market-intelligence reports).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational + market context)
- Its task and `shared_context.upstream_outputs` (Product Research candidates, Strategic
  Intelligence); `missing_upstream`.
- Training Room prior market insights and seasonal patterns (curated by the Knowledge Agent).
- External research / ad-intelligence connectors (read-only, when connected and approved).

## Write — Research Lab only (owned system)
- Structured market-intelligence reports (incl. cross-validation verdicts) to
  `tasks.output_data` for handoff to the Market Analyst.

## Execute
- Run trend/demand/competitor/ad-intelligence research; cross-validate Product Research.

## Requires Owner Approval
- Paid research / ad-intelligence tools not yet enabled (Level 1 approval).

## Forbidden
- See `../instructions.md` → **Hard Limits**: no go/no-go/spend/launch decisions; never
  contact competitors/customers; never publish; never present fabricated demand as fact.
