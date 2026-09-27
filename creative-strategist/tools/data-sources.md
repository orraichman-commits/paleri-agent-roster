# Tools / Data Sources — Creative Strategist

Authoritative Inputs. Read fresh; never assume.

- **tasks.input_data** — the task brief.
- **tasks.input_data.shared_context.upstream_outputs** — upstream research (Product/Market
  Research, Market Analyst viability, Strategic Intelligence); **missing_upstream** for gaps.
- **Training Room** — PALERI brand rules, tone, prior winning angles, the do-not-repeat
  list, and `knowledge/memory/video-approval-log.md` (via Knowledge Agent). Read the log
  before every brief. Canon: `knowledge/memory/niches-to-avoid.md`,
  `knowledge/memory/product-criteria.md`, `knowledge/memory/meta-ads-structure.md`.
- **Product data** feeding the campaign.
- **Higgsfield API (read only)** — generations already produced for this job, for
  brief-fit review. Secret: `HIGGSFIELD_API_KEY`. Do not generate, publish, or spend.
  Never write the key into the repo or an output.

The brief is written to **tasks.output_data** and becomes the downstream production agents'
`upstream_outputs`.
