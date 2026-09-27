# Permissions — Video Editor (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within the Creative Office (video drafts / edit plans).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational context)
- The brief, source assets, script, and exact Foreplay links/IDs via
  `shared_context.upstream_outputs`; `missing_upstream`.
- Foreplay, to open those cited ads before generation. Not a license to browse for new ads.
- Training Room brand rules for pacing, captions, logo/end-card usage (curated by Knowledge Agent).
- The Notion video log (`NOTION_VIDEO_APPROVAL_LOG_URL`) before every job. The URL is
  not set yet. Do not look for this log in the repo.

## Write — Creative Office only (owned system)
- Video variants (or an edit plan / EDL when no render connector) to `tasks.output_data`,
  labelled by aspect ratio, duration, placement; routed to Or's video gate. Not to `shopify`
  until that gate is an approve.

## Execute
- Generate the video on the Higgsfield API with the secret `HIGGSFIELD_API_KEY`.
  Generation only. The key is never written into the repo, a prompt, or an output.
- Edit short-form video; overlay Hebrew captions; choose music/pacing.
- Other render tools only when connected and approved.

## Requires Owner Approval
- Every generated video: Or approve/reject before `marketing` and Gate 2. The decision
  and the reason are logged by `knowledge`.
- Paid render/tool spend that is not Higgsfield generation (Level 1 approval).
- Nothing is published. Credit purchases and plan changes are not generation.

## Forbidden
- See `../instructions.md` → **Hard Limits**: never publish video; no misleading/medical/
  competitor caption claims; no unlicensed music/footage; no spend beyond generation;
  no spend/launch/product decisions.
