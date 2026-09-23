# Output Contract — Knowledge Agent

## Knowledge entry / query response

```
## Knowledge Entry / Response — <timestamp>
Type: <fact | preference | decision-outcome | product-history | market-insight | conflict>
Statement: <the knowledge, plainly>
Source: <decision/workflow/event id or owner feedback reference>
Date observed: <date>
Confidence: <high | medium | low | unverified>
Status: <canonical | pending owner approval | flagged>
Notes: <conflicts, gaps, or what to confirm>
```

## Loop-Closer report (after a live campaign — see `skills/loop-closer.md`)

Owner-facing, Hebrew by default. Metric names, slugs, and IDs stay in English.

```
## Loop-Closer Report — <campaign> — <timestamp>
Window: <date range> | Sources: <Meta / Shopify connector state, via Performance Analyst>
Signal bar: <time live + volume used to justify running this> | Coverage gaps: <blind spots>

### מה ניסינו (hypothesis)
Angle / hook / offer / audience / format: <as briefed, with artifact ids>

### מה קרה בפועל
  - <metric>: <value> — <source + window>

### מה עבד — ולמה
  - <claim> — Evidence: <figures> — Confidence: <high | medium | low>

### מה לא עבד — ולמה
  - <claim> — Cause: <creative | offer | audience | insufficient delivery to tell>
    Evidence: <figures> — Confidence: <high | medium | low>

### מה לשפר בסבב הבא
  - <concrete, testable change> — tied to: <the evidence above>

### לא לחזור על זה (do-not-repeat)
  - <niche slug / angle / claim / hook / format / audience / offer> — Evidence: <why> —
    Revisit only if: <what would have to be true>
  - Denylist check: <clear | ran a hard-reject / avoid-at-start slug — process failure>

### הצעות לעדכון Training Room (pending Owner approval)
  - <proposed canonical rule, including a niches-to-avoid or product-criteria addition> —
    Confidence: <…> — Conflicts with: <existing entry, if any>

### המלצות להמשך
  - CEO: <what the market taught, for the next decision — never what to decide>
  - Creative (`creative-strategist` / `copywriter`): <do-not-repeat to read before next round>
  - Research: <what to re-check or validate>

AI/token cost for the round: <from AI Cost Manager, when available>
Handoff: CEO (summary) · Creative (do-not-repeat) · Owner (canonical proposals)
```

**Rules:** no organizational recommendations (that is `board-ops`), no live-system changes, no
business decision, and no post-mortem at all when the signal bar was not met — in that case the
whole output is a coverage-gap note with a re-run condition.
