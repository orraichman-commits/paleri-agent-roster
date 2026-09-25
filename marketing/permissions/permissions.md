# Permissions — Marketing (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads ad data and upstream assets; writes only
the ABO plan and the daily read. Never touches the ad account.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (assets + ad data)
- Its task and `shared_context.upstream_outputs` (creative chain, Shopify draft, Finance
  opinion, CEO products-table row); `missing_upstream`.
- Meta Ads metrics, read-only, when a connector exists and Or has given the campaign name
  and ID.
- Training Room canon for structure, unit economics, and funnels.

## Write — Analytics Office only (owned system)
- ABO test plans (structure + proposed budget) to `tasks.output_data`, handed to
  `finance-controller`.
- Daily reads (label, ROAS, spend, recommended move) to `tasks.output_data`, handed to
  the CEO. Budget-increase recommendations are also handed to Finance.

## Execute
- Group assets into an ABO test by angle / avatar / copy / hook.
- Propose a test budget. Recommend +20%, −20%, a kill, a fatigue loop, or a CBO home.

## Requires Owner Approval
- Any live change: publish, budget edit, pause, kill. Or applies these by hand.
  Publishing Office stays locked.
- Connectors/APIs not yet enabled (Level 1 approval).

## Forbidden
- See `../instructions.md` → **Hard Limits**: never publish; never change budgets; never
  spend; never present an unsourced metric; never decide a label from CTR, CPC, CPA, or
  frequency alone.
