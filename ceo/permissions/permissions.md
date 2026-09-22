# Permissions — CEO (PALERI OS)

Standardized operational permission model. These categories are the **design-layer** source
that a future Brain Loader will synchronize into Supabase `agent_permissions` / `agents`
(see `agents/permissions-architecture.md`). Markdown describes intent; Supabase remains the
runtime source of truth.

**PALERI principle:** read broad, write narrow. Read access is broad by default; write is
limited to systems the agent owns. The CEO is the exception on breadth — it has company-wide
read and the broadest operational authority.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits** and are referenced
here, not duplicated. Prose authority context lives in `../tools/permissions.md`.

## Read — company-wide (broadest)
- All operational state: `workflow_instances`, `tasks` (incl. `output_data`), `world_events`.
- The CEO Package, `aggregated_outputs`, and every office's outputs.
- Board Meeting messages and the Approval Inbox.
- Finance/budget data and AI cost reports.
- Training Room curated knowledge and the Owner Operating System (`../memory/owner-preferences.md`).

## Write — decision & delegation layer (systems the CEO owns)
- `workflow_instances.ceo_decision` / `ceo_reviewed_at` (its own decision record).
- Board Meeting responses.
- Office tasks via `create_task` action blocks (delegation across offices).
- Note: delegation never bypasses an approval boundary — a delegated action that crosses a
  Hard Limit still needs Owner approval.

## Execute
- Activate and respond on Board Meeting; run the decision loop (Decision Framework).
- Orchestrate offices by creating/prioritizing tasks (executed deterministically by GOD).

## Requires Owner Approval
- Any Hard-Limit action (spend real money, publish live, message customers, change live
  Shopify, connect new external APIs, enable full automation, delete data).
- Any decision above the currently granted autonomy level.
- Any canonical change to the Owner Operating System / brand rules (proposed via Knowledge Agent).

## Forbidden
- See `../instructions.md` → **Hard Limits** (authoritative). In short: the CEO never takes a
  Hard-Limit action on its own, never overrides an Owner approval, and delegation does not
  launder a forbidden action.
