# Memory: Potential Products Table — CEO

The CEO keeps this table. It is the unit-economics record per product. When Or asks
about a product's money, answer from this table. Do not re-derive a second model in
the reply and call it the table.

Or is an Israeli **עוסק פטור** (VAT-exempt dealer). Every price here is **without VAT**.
Do not add VAT, do not strip VAT, and do not force a .90 ending because of VAT.
Canon: `knowledge/memory/unit-economics.md`. Flow: `knowledge/memory/funnels.md`.

## Row

| Field | Rule |
|---|---|
| Product | Name used in the Gate 1 deck |
| AliExpress cost | Provisional. Research records it for the ≥ 2.5× market-price screen. Not a supplier. |
| Cost | Real supplier cost once LIO returns the quote. **Replaces** the AliExpress cost in the formulas below. Until then, mark the row provisional. |
| Price | Final shelf price, without VAT. Same number as the Shopify draft. |
| Clearing | **5% of price** |
| Margin | `price − cost − clearing` |
| Margin % | `margin / price` |
| Markup | `price / cost`. **Flag if under 2.5×.** |
| Break-even ROAS | `price / margin` |
| Profit at ROAS X | `margin% − 1/X` (share of price) |

Worked shape (placeholder — never present as a live product): price 200 ₪, cost 50 ₪,
clearing 10 ₪, margin 140 ₪, margin% 0.70, markup 4.0×, break-even ROAS 200/140 ≈ 1.43.
Profit at ROAS 2 = 0.70 − 0.50 = 0.20.

## Who writes, who reads

- **CEO** writes and replaces cost when LIO updates the quote. A markup under 2.5× is
  flagged in the Gate 1 deck (or in an update to Or if the deck already went).
- **finance-controller** recalculates markup and break-even from the row. It does not
  invent a second cost.
- **marketing** reads break-even ROAS for labels and kills. It does not edit the row.
- **shopify** prices the draft without VAT, at the price on this row once the row exists.

There is no turnover-ceiling column and no monthly Meta-spend ceiling. Approval stays
per campaign.

## Empty on purpose

No product rows are seeded here. A row is added when research routes a candidate. An
empty table is the honest starting state, not a gap to fill with examples.
