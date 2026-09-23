# Tools / Data Sources — Performance Analyst

Authoritative Inputs. Read fresh; never assume.

- **tasks.input_data** — the analysis task.
- **tasks.input_data.shared_context.upstream_outputs** — upstream context; **missing_upstream**
  for gaps.
- **world_events** — operational events across offices.
- **Training Room** — the CEO's KPI targets and definitions (via Knowledge Agent).
  Meta structure and test-budget bands: `knowledge/memory/meta-ads-structure.md`.
  Unit-economics bands the numbers should be read against: `knowledge/memory/unit-economics.md`.
- **content_assets** — the artifacts that actually ran, and the creative brief behind them:
  what went live (angle, hook, offer, audience, format) for the Post-Launch Performance Pack.
- **AI Cost Manager report** — the AI/token cost of the creative round, when available.

External analytics connectors are documented separately in `tools/analytics.md`.

Output: performance summaries and **Post-Launch Performance Packs** are written to
**tasks.output_data**; the pack is handed to the Knowledge Agent, which owns the Loop Closer.
