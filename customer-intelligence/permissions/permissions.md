# Permissions — Customer Intelligence Agent (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a
future Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Reads across research, analytics, and
performance data to understand the customer; writes only its own intelligence briefs.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (evidence synthesis)
- Its task and `shared_context.upstream_outputs` (Product Research, Market Research,
  Market Analyst, Strategic Intelligence, Performance Analyst outputs); `missing_upstream`.
- Training Room customer/market knowledge and prior avatar/angle history (curated by the
  Knowledge Agent).
- External research connectors (reviews/audience tools) — read-only, only when connected
  and Level 1 approved.

## Write — Research Office only (owned output)
- Customer Intelligence Briefs (avatars, segments, chains, awareness, angles, positioning,
  offer angles) to `tasks.output_data`; consumed downstream after review.
- Avatar-update recommendations flagged to the Knowledge Agent (Training Room writes are
  the Knowledge Agent's, not yours).

## Execute
- Synthesize customer avatars, segmentation, pain/outcome/objection chains, awareness
  classification, motivation analysis, angle/positioning/offer-angle recommendations.

## Requires Owner Approval
- Paid research tools / external APIs (Level 1 approval).
- Any data-collection method touching real customers (surveys, review scraping) —
  and even then, never direct customer contact.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no copy/creative/brief production; no
  business decisions (go/no-go, pricing, launch, spend); no customer/competitor contact;
  no publishing; no invented customer "facts".

## Suggested `agent_permissions` rows (runtime model, migration-time)
| action | level | approval_level | notes |
|---|---|---|---|
| execute_task | allowed | 0 | Core work capability |
| call_external_api | requires_approval | 1 | Audience/review research data sources |
| spend_budget | forbidden | 0 | No budget authority |
| contact_customers | forbidden | 0 | Analysis only — never outreach |
