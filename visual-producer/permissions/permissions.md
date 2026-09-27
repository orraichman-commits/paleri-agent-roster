# Permissions — Visual Producer (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within the Creative Office (visual asset drafts / specs).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational context)
- The creative brief, copy, research, avatar, and exact Foreplay links/IDs via
  `shared_context.upstream_outputs`; `missing_upstream`.
- Foreplay, to open those cited ads before generation. Not a license to browse for new ads.
- Training Room brand visual rules, palette, logo usage (curated by the Knowledge Agent).
- Product imagery / source assets referenced by the brief.
- The Notion video log (`NOTION_VIDEO_APPROVAL_LOG_URL`) before every job. The URL is
  not set yet. Do not look for this log in the repo.

## Write — Creative Office only (owned system)
- Visual asset drafts (or generation specs when no connector) to `tasks.output_data`,
  labelled by format/placement, with the Foreplay link or ID still attached.
  Routed onward to `video-editor`, not to publishing.

## Execute
- Generate images (and a source clip the brief needs as an asset) on the Higgsfield API
  with the secret `HIGGSFIELD_API_KEY`. Generation only. The key is never written into
  the repo, a prompt, or an output.
- Other image tools only when connected and approved.

## Requires Owner Approval
- Paid generation-tool spend that is not Higgsfield generation, and any external API
  that is not that generation (Level 1 approval).
- Nothing is published. Credit purchases and plan changes are not generation.
- The finished video still waits for Or's video gate. You do not skip that by handing
  assets downstream.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never publish assets; no policy-violating,
  misleading, brand-breaking, or unlicensed visuals; no spend beyond generation;
  no spend/launch/product decisions.
