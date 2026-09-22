# Tools / Data Sources — AI Cost Manager

Authoritative Inputs. Read fresh; never assume.

- **budget_events** — records with event type `ai_token` (tokens, model, agent, task, cost).
- **tasks.input_data** — the task.
- **tasks.input_data.shared_context.upstream_outputs** — upstream context; **missing_upstream**
  for gaps.
- **Training Room** — AI budget thresholds and model-cost references (via Knowledge Agent).

Output (an AI cost-efficiency report) is written to **tasks.output_data** for handoff to the
Finance Controller.
