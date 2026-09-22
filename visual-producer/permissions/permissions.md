# Permissions — Visual Producer (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within the Creative Office (visual asset drafts / specs).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational context)
- The creative brief via `shared_context.upstream_outputs`; `missing_upstream`.
- Training Room brand visual rules, palette, logo usage (curated by the Knowledge Agent).
- Product imagery / source assets referenced by the brief.

## Write — Creative Office only (owned system)
- Visual asset drafts (or generation specs when no connector) to `tasks.output_data`,
  labelled by format/placement; routed to Level 1 approval.

## Execute
- Generate/prepare assets and format variants per the brief; use image tools only when
  connected and approved.

## Requires Owner Approval
- Paid generation-tool spend / external API calls (Level 1 approval); nothing published.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never publish assets; no policy-violating,
  misleading, brand-breaking, or unlicensed visuals; no spend/launch/product decisions.
