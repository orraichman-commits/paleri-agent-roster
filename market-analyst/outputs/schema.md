# Output Contract — Market Analyst

```
## Product Viability Analysis — <product/batch> — <timestamp>
Products:
  - Product: <name>
    Denylist: <clear | FILTER hard-reject:<slug> | FILTER avoid-at-start:<slug>>
    Unit-economics sanity: <price band, COD multiple, COD+CAC vs ~60%, break-even ROAS — or insufficient cost data>
    Viability score: <n/100 or tier, or n/a if denylist FILTER> — <how derived>
    Margin: <assessment> | Competition: <vs saturation> | Demand: <assessment>
    Recommended angle: <outcome positioning, or none if FILTER>
    Verdict: <ROUTE TO CEO | FILTER> — <reason>
    Evidence: <upstream sources>
    Confidence: <high | medium | low>
Gaps: <missing_upstream, low-quality inputs>
Handoff: CEO Office
```
