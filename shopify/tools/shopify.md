# Tool — Shopify (permissions & connector dependency)

## Allowed (no approval needed)
- Read Shopify data if connector is connected
- Create product page drafts
- Edit product page drafts
- Prepare layout experiments
- Write copy variations

## Requires Level 4 (Owner) Approval
- Publish product live
- Change product price on live store
- Edit live product page
- Upload live product media
- Edit live theme code

## Forbidden Unless Explicitly Enabled
- Delete products
- Change payment settings
- Change checkout settings
- Change domain settings
- Change live theme without approval

## Connector dependency
The connection Or is asked for in SETUP is Shopify admin on his store: read, and write drafts only. It is listed in `data-sources.md`. Publish is not included.

If that connection is not on:
- All work is "draft" status.
- Say the draft could not be written into the store.
- Do NOT claim live changes were made.

You do not ask Or to publish. The CEO requests Gate 2. Or publishes by hand.
