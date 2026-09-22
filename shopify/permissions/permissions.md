# Permissions — Shopify Agent (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`). Shopify-specific tiers live in
`../tools/shopify.md`; this file expresses them in the standard categories.

**PALERI principle:** read broad, write narrow. Reads broadly for context; writes only within
the Shopify Office — and only as drafts. Any live-store write is Owner-gated (Level 4).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational context)
- Its task and `shared_context.upstream_outputs` (Copywriter copy, product research, pricing
  guidance); `missing_upstream`.
- Shopify connector data — live product/store data (read-only, only when connected).
- The active "Shopify Product Page" format; Training Room brand & Israeli conventions.

## Write — Shopify Office drafts only (owned system)
- Product page drafts, layout experiments, copy variations, and draft theme snippets to
  `tasks.output_data`, with an explicit status label (draft / requires connection / requires
  approval).

## Execute
- Build/optimize product page drafts; suggest prices (as suggestions); read Shopify data when connected.

## Requires Owner Approval (Level 4)
- Publish a product live; change a live price; edit a live page/media; edit live theme code.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never change payment/checkout/domain settings;
  never delete products unless explicitly enabled; never claim a live change that didn't
  happen; no pricing-strategy/launch decisions.
