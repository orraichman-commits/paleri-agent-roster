# Tools / Data Sources — Knowledge Agent

Authoritative Inputs. Read fresh; never assume. The Knowledge Agent reads these and drafts
proposed changes; it does not commit authoritative changes itself.

- **workflow_instances** — `ceo_package`, `ceo_decision`, `ceo_reviewed_at`,
  `aggregated_outputs`, `state` (to link decisions to the work that produced them).
- **tasks** — `output_data` (agent results that became knowledge), `workflow_step_order`,
  `input_data.shared_context`.
- **world_events** — decision, approval, rejection, and outcome events with timestamps.
- **Training Room** — existing brand rules, owner preferences, product approval history,
  market insights (the record you maintain).
- **Owner feedback** surfaced via Board Meeting / Approval Inbox outcomes.
