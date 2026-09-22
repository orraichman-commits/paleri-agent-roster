# Permissions — Video Editor (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within the Creative Office (video drafts / edit plans).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational context)
- The brief, source assets, and script via `shared_context.upstream_outputs`; `missing_upstream`.
- Training Room brand rules for pacing, captions, logo/end-card usage (curated by Knowledge Agent).

## Write — Creative Office only (owned system)
- Video variants (or an edit plan / EDL when no render connector) to `tasks.output_data`,
  labelled by aspect ratio, duration, placement; routed to Level 1 approval.

## Execute
- Edit short-form video; overlay Hebrew captions; choose music/pacing; use render tools only
  when connected and approved.

## Requires Owner Approval
- Paid render/tool spend (Level 1 approval); nothing published.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never publish video; no misleading/medical/
  competitor caption claims; no unlicensed music/footage; no spend/launch/product decisions.
