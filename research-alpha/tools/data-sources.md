# Tools / Data Sources — Product Research Agent

Authoritative Inputs. Read fresh; never assume.

- **tasks.input_data** — the research task (product/category brief, criteria).
- **tasks.input_data.shared_context.upstream_outputs** — upstream context (e.g. Market
  Research trends, Strategic Intelligence); **missing_upstream** for gaps.
- **External research / supplier-lookup connectors** — used only when connected and approved.
  None of these are a live API in this pack. Name the source you actually used; if you
  could not open it, the trail is a blind spot.
  - **Meta Ads Library** (free, course method) — who is running ads, for how long, in
    which country. A live ad of ~14+ days, not a brand-new 7-day test, and more than a
    handful of ads, is evidence of a selling product. Keyword entry points when you have
    no brand name: משלוח חינם, הנחה לזמן מוגבל, percent-off phrases, or the problem.
  - **AliExpress** (sourcing) — unit cost, shipping, availability. Not IP clearance and
    not permission to sell a branded or licensed product.
  - **Foreplay** (paid creative/ad intelligence; optional here, primary for
    `research-beta`) — saved-ad discovery and days-running. Level 1 before any paid use.
  - **Perplexity** (permissioned research; not named in the course) — problem framing and
    demand context. It does not replace an ad you have seen.
- **Training Room** — `knowledge/memory/niches-to-avoid.md`,
  `knowledge/memory/product-criteria.md`, `knowledge/memory/unit-economics.md`, and prior
  product verdicts (via Knowledge Agent).

Output (a structured research report) is written to **tasks.output_data** for handoff to the
Analytics Office (Market Analyst).
