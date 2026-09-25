# Skill: Product Research — Product Research Agent

Qualify products for the Israeli dropshipping pipeline. The denylist is a gate, not a
score. Read `knowledge/memory/niches-to-avoid.md` and `knowledge/memory/product-criteria.md`
before any QUALIFY. Those files are the criteria; this skill is how you apply them.

## 1. Denylist first
Map the candidate to a slug. `hard-reject` (skin, ingestibles, emergency, zero-value
gimmick, licensed IP, counterfeit) is an immediate **REJECT** — no sourcing deep-dive
required beyond enough evidence to name the slug. `avoid-at-start` (apparel, jewelry,
footwear, expensive electronics, heavy goods, trend/situational) is also a **REJECT**
for a starting test unless the task quotes an explicit Owner override. AliExpress
availability does not clear IP and is not a supplier to pursue. Or has his own supplier.
Do not search for one.

If the niche is denied, stop. Do not hand a "qualified with caveats" product downstream.

## 2. Six criteria
For anything still alive, score each slug and show the evidence:

`lf8-real-need`, `not-commodity`, `perceived-value`, `margin-room`, `not-saturated`,
`wow-factor`.

A meaningful miss on need, commodity status, or saturation is a REJECT named by slug.
Clearing "most" of the six does not save a gimmick. State which LF8 drive the outcome
pulls, and whether we are selling a solved problem or an emotion — outcome, not feature.

Also check:

- Israeli price band **89–399 ₪** (`price-band-il`). Outside it, say so; do not quietly
  QUALIFY a $5 item or a $500 item.
- Market price versus AliExpress unit cost: **≥ ×2.5** or it does not QUALIFY. Unknown
  AliExpress cost is an unknown, not a ×4 fantasy. COD floor (≥ ×2.5, prefer ×3–×4) in
  `unit-economics.md` is the same idea once delivery cost is known. Prices are without VAT.
- We understand the niche well enough to talk like the buyer. If not, REJECT.
- Audience is not tiny.
- The product is evergreen, not a news cycle.

## 3. What to document when you QUALIFY or REJECT
- **AliExpress cost** — the unit cost you observed, labelled provisional. Not a supplier,
  not a lead time, not a vendor recommendation. Legal clearance is still not AliExpress.
- **Margin** — range and the basis (cost, shipping, implied shelf price).
- **Competition** — level with evidence. Competition that is already selling is a
  positive signal if the offer or the ad can be better. Saturation (the market already
  owns it) is a failed `not-saturated`.
- **Israeli-market fit** — price band, delivery expectation, whether the outcome
  translates.
- **Search trail** — which source showed the product already selling (Ads Library,
  Foreplay if approved, or neither). A candidate nobody is advertising is higher risk;
  label it. Do not invent an ad you did not see.

Cross-check with `research-beta` when their intelligence is in `upstream_outputs`.
Conflicts are recorded, not smoothed over.

## Verdict
**QUALIFY** or **REJECT**, with the slug that decided it and the sources. Structure the
output so the Market Analyst can score it without re-doing the search
(`outputs/schema.md`).
