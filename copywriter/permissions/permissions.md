# Permissions — Copywriter (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`). Markdown describes intent; Supabase
`agent_permissions` remains the runtime source of truth.

**PALERI principle:** read broad, write narrow. The Copywriter can read operational
information across the company, but only writes within its own office (Creative Office) —
copy drafts on its task, routed to approval.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits** and referenced here.

## Read — broad (operational context)
- Its task and brief: `tasks.input_data`, `tasks.input_data.shared_context.upstream_outputs`
  (Creative Strategist angle, research), `missing_upstream`.
- The active Copywriting Format.
- Training Room brand rules, tone, and prior approved copy (curated by the Knowledge Agent).
- Company operational state relevant to its work (product/campaign context) — read-only.

## Write — Creative Office only (owned system)
- Copy drafts to its own `tasks.output_data`, labelled by output type and language.
- Submission of drafts to the Approval Inbox.
- No writes to any other office's systems, no live channels.

## Execute
- Run copywriting tasks; produce variations; recommend a framework/angle.
- Use approved copy tools/connectors only when enabled.

## Requires Owner Approval
- Nothing published or sent by the Copywriter itself — publishing/sending approved copy is a
  downstream, Owner/CEO-gated action.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no generic/AI or misleading/medical/competitor
  claims; never publish; never message real customers; no spend or business decisions.
