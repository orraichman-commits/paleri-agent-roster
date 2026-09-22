# Tools / Data Sources — Finance Controller

Authoritative Inputs. Read fresh; never assume. The Finance Controller reads these and never
executes payments or changes billing.

- **budget_events** — spend records across cost categories (including `ad_spend` and
  `ai_token`).
- **tasks.input_data** — the task / spend request.
- **tasks.input_data.shared_context.upstream_outputs** — Performance Analyst efficiency data,
  AI Cost Manager token reports; **missing_upstream** for gaps.
- **Training Room** — budget thresholds and the owner's spend preferences (via Knowledge Agent).

Output (a financial summary / spend decision) is written to **tasks.output_data**.
