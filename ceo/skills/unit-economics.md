---
layer: business
trigger_keywords: margin, profit, price, pricing, cost, roas, mer, cpa, aov, unit economics, break-even, רווח, מחיר, עלות, תמחור, שולי
wired_mirror: none — loaded on demand by the Brain Loader (keyword-triggered)
---

# Skill: Unit Economics — CEO (formula-only)

The arithmetic behind "Profit first." Formulas only — **real numbers live with the Owner**:
target thresholds come from `memory/kpis.md`, and actual costs must be asked for, never
invented. If an input is unknown, say so and ask; a made-up COGS is worse than no analysis.

## Per-order contribution (the core equation)

```
Contribution = AOV
             − COGS (product cost + inbound shipping, per order)
             − Fulfillment (outbound shipping + packaging)
             − Payment fees (processor % × AOV + fixed fee)
             − Refund cost (Refund Rate × AOV, plus non-recoverable costs)
             − CPA (ad spend ÷ new customers, blended if returning customers exist)
```

An order is profitable only if Contribution > 0 **after** CPA. A product is viable only if
Contribution at a *realistic* CPA clears the Owner's margin target (see `memory/kpis.md`).

## VAT (Israeli market) — עוסק פטור
Or is an exempt dealer. Shelf price **is** the price in the model. Do not divide by
1.18, do not strip an 18% VAT portion, and do not force a .90 ending because of VAT.
The products table (`memory/products-table.md`) is the record:

```
clearing         = 0.05 × price
margin           = price − cost − clearing
margin%          = margin / price
Break-even ROAS  = price / margin
Profit at ROAS X = margin% − 1/X
```

Flag markup (`price / cost`) under **2.5×**. AliExpress cost is provisional until LIO's
supplier quote replaces it. There is no turnover-ceiling alert and no monthly Meta
spend ceiling.

## Break-even thresholds (derive, then compare to targets)

```
Variable margin  = AOV − COGS − Fulfillment − Fees − Refund cost   (before ad spend)
Break-even CPA   = Variable margin                                  (spend above ⇒ loss)
Break-even ROAS  = AOV ÷ Variable margin
MER              = Total revenue ÷ Total ad spend  (blended, the honest company-level lens)
```

Rules of thumb for judgment (not substitutes for the math). The Owner-facing statement
of the same ideas is `knowledge/memory/unit-economics.md`; Meta test budgets are
`knowledge/memory/meta-ads-structure.md`. Course bands, not laws:

- COD means **cost of delivery** (COGS + outbound + pick/pack + payment and platform
  fees), not cash on delivery.
- COD + CAC near or under **~60% of revenue** is the healthy band the course uses.
- Gross margin roughly **10–40%**, with ~**30%** a reasonable dropshipping expectation.
- Shelf price ≥ **2.5× COD**, prefer 3–4×. ×3–×4 is a rule of thumb.
- Israeli impulse band **89–399 ₪**, without VAT.
- A *required* (break-even) ROAS under ~2, preferably under ~1.8, means the margin is
  wide enough. Campaign ROAS still has to clear break-even. Wanting a low ROAS is not
  the goal.
- If Break-even ROAS is above what the channel realistically delivers for this niche,
  the product fails viability regardless of how good the creative is.
- Prefer MER over per-campaign ROAS when attribution is murky (it usually is on Meta).
- Cash timing matters in dropshipping: supplier payment now vs. customer money later —
  flag any product where scale would strain cash flow (Owner preference: lean, reversible).

## Worked example (placeholder numbers — never present as real)
Price ₪200 (no VAT). Cost ₪50. Clearing 5% = ₪10. Margin = 200 − 50 − 10 = ₪140.
Margin% = 0.70. Markup = 4.0×. Break-even ROAS = 200 / 140 ≈ 1.43.
Profit at ROAS 2 = 0.70 − 1/2 = 0.20 of price. The contribution stack above is the
full per-order lens; the products-table line is what Marketing kills against and what
Gate 1 flags. Judge both against the Owner's targets, not against zero.

## Output discipline
Every pricing/product recommendation shows its arithmetic inline (the equation with the
numbers used and their source: Owner-provided, measured, or assumed — assumptions flagged).
