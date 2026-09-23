# Output Contract — Performance Analyst

## Performance summary (standing)

```
## Performance Summary — <scope> — <timestamp>
Window: <date range> | Sources: <Meta Ads / Shopify / internal — connector state>
KPIs:
  - ROAS: <value> (<trend>) | CTR: <value> | CPA: <value> | AOV: <value>
Bottlenecks / underperformers:
  - <area> — <quantified impact> — Recommended action: <op fix> — Owner: <office>
Budget anomalies: <flag → Finance / AI Cost Manager>
Blind spots: <missing_upstream, unavailable connectors>
Priority for CEO: <top 1–3 items>
```

## Post-Launch Performance Pack (the Loop-Closer data leg — see `skills/loop-closer-handoff.md`)

Evidence only. No lessons, no do-not-repeat items, no business interpretation — those are the
Knowledge Agent's.

```
## Post-Launch Performance Pack — <campaign> — <timestamp>
Window: <date range> | Live since: <date>
Signal bar: <time live + volume> — <met | NOT met>
Sources: Meta <connected | NOT wired> · Shopify <connected | not connected> · internal

Identity: campaign=<id> adset=<id> creative=<id> artifacts=<content_assets ids>

What went live (from the brief + approved artifacts):
  Angle: <…> | Hook: <…> | Offer: <…> | Audience: <…> | Format: <…>

Meta (when connected):
  - Spend: <…> | Impressions: <…> | CTR: <…> | CPC: <…> | CPA: <…> | ROAS: <…> | Frequency: <…>

Shopify (when connected):
  - Orders: <…> | Revenue: <…> | AOV: <…> | Refunds: <…> | Conversion rate: <…>

Attribution linkage: <tracked | assumed> — Confidence: <high | medium | low>
AI/token cost for the round: <from AI Cost Manager, when available>
Ambiguities: <e.g. delivery too low to separate creative from audience>
Blind spots: <unavailable connectors, missing windows, missing_upstream>

Handoff: Knowledge Agent (Loop Closer)
```

If the signal bar is **not met**, the pack is replaced by a coverage-gap note: what is missing
and when re-running would be worth it. Never pad a thin pack into a full-looking one.
