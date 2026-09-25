# Tools / Data Sources — Customer Intelligence Agent

Authoritative Inputs. Read fresh; never assume.

- **tasks.input_data** — the product/campaign scope and the question being asked.
- **tasks.input_data.shared_context.upstream_outputs** — the evidence base:
  - `research-alpha` (Product Research) — product facts, review signals, provisional AliExpress cost. Not a supplier.
  - `research-beta` (Market Research) — demand, competition, pricing landscape.
  - `market-analyst` — viability scoring and recommended angle candidates.
  - `strategic-intelligence-agent` — competitive/macro context.
  - `performance-analyst` — live campaign signals (when a campaign already ran:
    which angles/audiences actually converted — the strongest evidence there is).
  - **missing_upstream** — declared inputs that produced nothing; these become the
    brief's named blind spots.
- **Training Room** (via Knowledge Agent) — prior avatars, past angle performance,
  owner's product criteria, accumulated Israeli-market knowledge. Canon for this gate:
  `knowledge/memory/niches-to-avoid.md`, `knowledge/memory/product-criteria.md`.
- **memory/israeli-consumer.md** — durable Israeli consumer-psychology reference
  (agent-local view; the Training Room remains canonical).
- **External research connectors** (reviews platforms, audience tools) — only when
  connected and Level 1 approved. Not available today; never assume access.

Output (a Customer Intelligence Brief) is written to **tasks.output_data**. It completes
the Research Package and becomes `upstream_outputs` for the Creative Office (Creative
Strategist, Copywriter, Visual Producer, Video Editor) and part of the CEO package.
