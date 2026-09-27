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

## Notion entry (living layer)

Write living knowledge to Notion. Do not write it into a repo canon file.

- Training Room: [NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)
- Video log: [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)
- Rule Proposals inbox: [https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa](https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa)
- Read-only canon mirror: [https://app.notion.com/p/3e8020daae5b81888781d66360a19207](https://app.notion.com/p/3e8020daae5b81888781d66360a19207)

```
## Notion entry — <timestamp>
Destination: <https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26 | https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce | https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa>
Type: <lesson | do-not-repeat | decision-memory | product-history | market-insight | video-gate | proposal | conflict>
Title: <page title>
Statement: <the knowledge, plainly, in the language it was learned in>
Source: <decision/workflow/event id, pack id, or owner feedback reference>
Date observed: <date>
Confidence: <high | medium | low | unverified>
Status: <recorded | pending Or | approved — PR opened | rejected | conflict>
Canon file touched: <none | niches-to-avoid.md | product-criteria.md | meta-ads-structure.md | unit-economics.md | funnels.md>
Notes: <conflicts, gaps, or what to confirm>
```

Rules: cite the source. A `proposal` stays in the inbox until Or approves or rejects it.
`approved — PR opened` is the only status that may be followed by a repo write, and that
write is the PR. Do not put task-board status in this entry. Do not store secrets.

## Video-gate log entry (Notion)

Append to [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce) when Or approves or rejects a generated video.
Do not rewrite his reason. This is a record, not a Loop-Closer lesson and not a canon change.
Creative reads this page from Notion before every job. An empty log means there is no prior
reason yet. Do not invent one.

```
## <YYYY-MM-DD> — <product> — <approve | reject>
Destination: https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce
Video: <variant / output ref>
Foreplay ref: <url or id the cut was built from>
Decision: <approve | reject>
Reason: <Or's reason, in his words>
Returned to: <— | video-editor + visual-producer>
Stop-rule note: <production-stage correction | stacks with <other stage> → stop>
Logged by: knowledge (Notion memory bot)
```

Who must read it before the next job: `visual-producer`, `video-editor`,
`creative-strategist`, `copywriter`. The CEO reads it when building the Gate 2 deck.

## Loop-Closer report (after a live campaign — see `skills/loop-closer.md`)

Owner-facing, Hebrew by default. Metric names, slugs, and IDs stay in English.
Write the report to the Notion Training Room ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)). Proposed
canon changes in the last section also go to the Rule Proposals inbox
(https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa). They become a
repo PR only after Or approves.

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
Handoff: Notion (lessons, do-not-repeat) · Rule Proposals inbox (https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa) · CEO (summary) · Creative reads Notion · Owner approves proposals in the inbox, then a PR
```

**Rules:** no organizational recommendations (that is `board-ops`), no live-system changes, no
business decision, and no post-mortem at all when the signal bar was not met — in that case the
whole output is a coverage-gap note with a re-run condition.
