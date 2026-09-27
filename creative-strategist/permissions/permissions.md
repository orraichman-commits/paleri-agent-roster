# Permissions — Creative Strategist (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across the company for context; writes
only within the Creative Office (creative briefs and brief-fit reviews).

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (operational context)
- The brief in the company group (Product/Market Research, Market Analyst
  viability, Strategic Intelligence, exact Foreplay links/IDs). If a named input never arrived, say so. There is no `tasks` table.
- Training Room brand rules, tone, prior winning angles (curated by the Knowledge Agent).
- The Notion video log ([NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)) before every brief. Do not look for this log in the repo.
- Product/campaign operational context — read-only.
- **Higgsfield API, read only.** Generation records already created for this job
  (status, generation id, output id), so a brief-fit review can see the asset.
  Authenticate with `HIGGSFIELD_API_KEY` only for that read. Never write the key down.

## Write — Creative Office only (owned system)
- Creative briefs in the company group, for `copywriter`,
  including the exact Foreplay links/IDs the angle and hooks came from. There is no `tasks` table.
- Brief-fit review verdicts on returned creative.

## Execute
- Define angle/format/awareness; route briefs to production agents; review outputs for fit.
- Read Higgsfield generations. Do not call generation.

## Requires Owner Approval
- Paid-tool spend / external API calls go to the CEO. You do not ask Or. Nothing is published.
- Higgsfield generation, publishing, credit purchases, and plan changes are not yours
  even when the key is present. Generation belongs to `visual-producer` and `video-editor`.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no spend/launch/product decisions; never
  publish; never generate on Higgsfield; never brief a misleading/medical/competitor claim.
