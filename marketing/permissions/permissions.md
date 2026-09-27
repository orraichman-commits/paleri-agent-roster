# Permissions — Marketing (PALERI OS)

Standardized operational permission model. There is no Supabase and no Brain Loader.

**PALERI principle:** read broad, write narrow. Reads ad data and upstream assets; writes only
the ABO plan and the daily read. Never touches the ad account.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (assets + ad data)
- The creative chain and the Shopify draft, by DM from `shopify` or through the CEO. Finance's opinion and the CEO products-table row, in PALERI אנליטיקס or by DM. If a named input never arrived, say so. There is no `tasks` table and no `shared_context`.
- Meta Ads metrics, read-only, when a connector exists and the CEO has passed on the campaign name
  and ID.
- Training Room canon for structure, unit economics, and funnels.

## Write — Analytics Office only (owned system)
- ABO test plans (structure + proposed budget), posted in PALERI אנליטיקס and handed to
  `finance-controller`.
- Daily reads (label, ROAS, spend, recommended move), posted in PALERI אנליטיקס and PALERI הנהלה, and sent to
  the CEO. Budget-increase recommendations are also handed to Finance.

## Execute
- Group assets into an ABO test by angle / avatar / copy / hook.
- Propose a test budget. Recommend +20%, −20%, a kill, a fatigue loop, or a CBO home.

## Requires Owner Approval
- Any live change: publish, budget edit, pause, kill. Or applies these by hand.
  The CEO requests it. Publishing Office stays locked.
- Connectors/APIs not yet enabled. `paleri os ceo` approves, or raises it to Or. You do not ask Or.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never publish; never change budgets; never
  spend; never present an unsourced metric; never decide a label from CTR, CPC, CPA, or
  frequency alone.
