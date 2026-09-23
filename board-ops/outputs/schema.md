# Output Contract — Board Ops

Owner-facing, Hebrew by default. Slugs, table names, and metric names stay in English.

```
## Board Pack — <period> — <timestamp>
Cadence: <on request | board trigger>   (there is no scheduler — never claim one)
Coverage: <which reports were available, with their dates> | Gaps: <missing / stale sources>

### מצב ארגוני
Headline: <one line — is the organization earning its cost this period>

### ניצולת (utilization)
  - <agent slug>: <tasks routed> / <outputs produced> — <working | idle | saturated>
    Idle because: <no work routed | work routed, nothing produced>   (never merge the two)

### חפיפות (overlap)
  - <agent A> ↔ <agent B>: <the duplicated deliverable> — <genuine | deliberate split, preserved>

### יעילות עלות (cost efficiency)
  - <agent slug>: <spend, from the AI Cost Manager report + date> — <output consumed?> — <verdict>

### פערים מבניים (structural gaps)
  - <responsibility nobody owns> — <where it kept surfacing>

### המלצות
  1. <Keep | Route more | Freeze/on-demand | Merge responsibility | Hire | Retire>: <agent/role>
     Claim: <one line>
     Evidence: <figures + source report + date>
     Trade-off: <what breaks if this is wrong>
     Reversibility: <reversible | costly to undo>
     Decision owner: CEO / Owner

### מה עובד (do not omit)
  - <what is functioning and should be left alone>

Handoff: CEO + Owner — recommendations only; no change is applied by Board Ops.
```

## Rules for this contract
- A recommendation missing evidence, trade-off, or reversibility is dropped, not softened.
- `Retire` requires evidence across more than one period; a single quiet period supports
  `Freeze` at most.
- No business or campaign judgment, no post-mortem of a live campaign (that is the Loop
  Closer), no instruction addressed to another agent.
- If the only honest answer is "not enough data this period", say exactly that and list the
  gaps — an empty pack beats an invented one.
