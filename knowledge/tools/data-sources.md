# Tools / Data Sources — Knowledge Agent

Authoritative Inputs. Read fresh; never assume. The Knowledge Agent reads these and drafts
proposed changes; it does not commit authoritative changes itself.

- **workflow_instances** — `ceo_package`, `ceo_decision`, `ceo_reviewed_at`,
  `aggregated_outputs`, `state` (to link decisions to the work that produced them).
- **tasks** — `output_data` (agent results that became knowledge), `workflow_step_order`,
  `input_data.shared_context`.
- **world_events** — decision, approval, rejection, and outcome events with timestamps.
- **Training Room** — existing brand rules, owner preferences, product approval history,
  market insights (the record you maintain). Product-selection canon in this pack:
  `memory/niches-to-avoid.md`, `memory/product-criteria.md`, `memory/meta-ads-structure.md`,
  `memory/unit-economics.md`.
- **Owner feedback** surfaced via Board Meeting / Approval Inbox outcomes.
- **Post-Launch Performance Pack** (Performance Analyst) — the live campaign evidence the Loop
  Closer runs on: Meta/Shopify figures, what went live, attribution linkage, blind spots. You
  consume this pack; you never query Meta or Shopify yourself.
- **AI Cost Manager report** — the AI/token cost of a creative round, when available, so a
  lesson can carry what it cost to learn.
- **content_assets** — the artifacts that actually ran (what was live is a fact about the
  artifacts, not a memory).
