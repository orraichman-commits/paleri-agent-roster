# Tools / Data Sources — Marketing

Authoritative Inputs. Read fresh; never assume. Reads are read-only. Nothing here
writes to Ads Manager.

- **tasks.input_data** — the task: pre-publish structure, or a daily read.
- **tasks.input_data.shared_context.upstream_outputs** — creative chain outputs
  (brief, copy, visuals, video), the Shopify draft, Finance's last budget opinion,
  and the CEO products-table row for this product. **missing_upstream** for anything
  not delivered.
- **Campaign identity** — name and ID from Or, after he confirms launch. Without it
  the daily read does not start.
- **Meta Ads** — read-only metrics when a connector exists: spend, ROAS, and the
  diagnostic set (CPA, CTR, CPC, frequency). Unwired means a coverage gap, not a
  guess. Same honesty rule as `performance-analyst/tools/analytics.md`.
- **Training Room canon** — `knowledge/memory/meta-ads-structure.md`,
  `knowledge/memory/unit-economics.md`, `knowledge/memory/funnels.md`.
- **Break-even** — `ceo/memory/products-table.md`. You read the row. You do not
  edit the table. The CEO does.

Output (an ABO plan or a daily read) is written to **tasks.output_data**.
