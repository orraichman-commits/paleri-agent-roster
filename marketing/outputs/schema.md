# Output Contract — Marketing

## ABO test plan (pre-publish)

```
## ABO Test Plan — <product> — <timestamp>
Price (ex-VAT): <₪ from Shopify draft and products table — or CONFLICT>
Break-even ROAS: <from products table, or provisional / missing>
Campaign type: Sales | Budget level: ABO (ad set)

Ad sets:
  - Name: <angle / avatar>
    Testing: <angle | avatar | copy | hook>
    Ads (max 3 near 50–60 ₪/day, else max 5–6): <hook + format; image and video not mixed>
    Proposed daily budget: <20–35 ₪ | 60–100 ₪> — <why this floor>

Total daily test budget: <₪>
  vs 0.5× price: <meets | short by ₪>
  vs ideal 100–200%: <inside | below | above>
Layers in conflict: <yes — both numbers shown | no>

Handoff: finance-controller (budget review). Not a spend approval.
```

## Daily read (post-publish)

```
## Daily Read — <campaign name> — <campaign id> — <timestamp>
Window: <24h ending …> | Source: <Meta connected | NOT wired>
Product break-even ROAS: <value> | Cost basis: <supplier quote | AliExpress provisional>

Ad sets:
  - <name>: Label <winning | waiting | weak>
    ROAS: <…> | Spend: <₪> | Hours in this state: <…>
    Diagnosis only: CPA <…> | CTR <…> | CPC <…> | Frequency <…>
    Move: <+20% (another 48h winning) | −20% (weak) | kill (48–72h below break-even) | none>
    Finance: <wake — increase only | not woken>

Fatigue: <none | creative-strategist, then Gate 2 again>
CBO-ready: <none | ad set names — test stays ABO, scale is CBO>
Blind spots: <no campaign ID, unwired connector, missing products-table row>
Handoff: CEO (short daily message to Or). Deck only at end of test.
```

A read without a campaign ID is a blocker note, not a labelled grid.
