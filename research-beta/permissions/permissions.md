# Permissions — Market Research Agent (PALERI OS)

Standardized operational permission model. There is no Supabase and no Brain Loader.

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within its office (market-intelligence reports).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational + market context)
- The brief and upstream posts in PALERI מחקר (Product Research candidates; Strategic Intelligence when the CEO has brought it across). If a named input never arrived, say so. There is no `tasks` table and no `shared_context`.
- Training Room prior market insights and seasonal patterns (curated by the Knowledge Agent).
- External research / ad-intelligence connectors (read-only, when connected).

## Write — Research Lab only (owned system)
- Structured market-intelligence reports (incl. cross-validation verdicts), posted in
  PALERI מחקר, for handoff to the Market Analyst.

## Execute
- Run trend/demand/competitor/ad-intelligence research; cross-validate Product Research.

## Requires Owner Approval
- Paid research / ad-intelligence tools not yet enabled. `paleri os ceo` approves, or raises it to Or. You do not ask Or.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no go/no-go/spend/launch decisions; never
  contact competitors/customers; never publish; never present fabricated demand as fact.
