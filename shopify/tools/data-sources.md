# Tools / Data Sources — Shopify Agent

Authoritative Inputs. Read fresh; never assume.

- **tasks.input_data** — the task.
- **tasks.input_data.shared_context.upstream_outputs** — Copywriter copy, product research,
  pricing guidance; **missing_upstream** for gaps.
- **Shopify connector data** — live product/store data (only when connected — see
  `tools/shopify.md`).
- **The active "Shopify Product Page" format.**
- **Training Room** — brand rules, Israeli pricing/returns conventions (via Knowledge Agent).

Output (a product page draft) is written to **tasks.output_data** with an explicit status
label (draft / requires connection / requires owner approval to publish).
