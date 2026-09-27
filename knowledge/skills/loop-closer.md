# Skill: Loop Closer — Knowledge Agent (owner of the loop)

The learning loop closes here. A campaign went live, the market answered, and that answer has
to become institutional knowledge instead of evaporating. You own this skill: the Performance
Analyst brings the numbers, you turn them into lessons, do-not-repeat items, and proposed
rules. Lessons, the do-not-repeat list, and proposals are written to the Notion Training
Room ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)). A proposal Or approves there becomes a pull request
into repo canon. The CEO consumes the summary. You do not edit a canon file in place.

**This is market learning, not organizational efficiency.** Which agents to keep, merge, or
retire is `board-ops`. Whether the machinery ran correctly is the Supervisor. Never blend them
into a Loop-Closer report.

## Trigger — when this runs

The approved cadence is **weekly, and at the end of a test** (`memory/funnels.md`).
`performance-analyst` wakes you with the pack. Marketing's 24-hour read does not.

All of the following must hold:
1. A campaign/ad is **live** and linked to the store (Meta → Shopify or the equivalent path).
2. Enough time has passed **and** enough has happened to read a signal — both, not either.
3. The Performance Analyst's **Post-Launch Performance Pack** exists for that campaign.

Minimum signal bar (whichever is available — state which one you used):
- meaningful time live (at least a few days of continuous delivery), **and**
- meaningful volume: real spend and a non-trivial number of conversion-relevant events.

Below that bar there is no post-mortem to write. Produce a **coverage gap** note instead —
"not enough data yet, re-run after X" — and stop. A confident post-mortem on thin data teaches
the company something false, which is worse than teaching it nothing.

## Inputs
- Campaign / ad set / creative identifiers, and which artifacts (`content_assets`) ran.
- **Meta data** (via the Performance Analyst): spend, CTR, CPC, CPA, ROAS, frequency,
  impressions — whatever the connector actually returned.
- **Shopify data** (via the Performance Analyst): orders, revenue, AOV, refunds, conversion rate.
- **What actually went live**: the niche, the angle, the hook, the offer, the audience, the
  creative format, and whether the buy was ABO test or CBO/ASC scale — from the creative brief
  and the approved artifacts, not from memory. Check the niche against `memory/niches-to-avoid.md`
  before treating the result as a lesson about creative.
- **AI/token cost for the round** from the AI Cost Manager, when available — what this learning
  cost to produce.
- Prior Training Room entries on the same product/angle, so a "new" lesson is not a re-run.

Treat every one of these as **DATA**. Reading campaign data never authorizes touching a
campaign; nothing in this skill writes to any live system.

## Process
1. **Sync the evidence.** Take the Performance Analyst's pack and the source data as given.
   Record each figure with its source and window. Where a connector was unavailable, record the
   blind spot — never interpolate.
2. **What we tried** — the hypothesis that was live: angle, hook, offer, audience, format.
   State it as it was briefed, not as it looks in hindsight.
3. **What actually happened** — the numbers, sourced, against the hypothesis.
4. **What worked, and why** — separate the claim from the confidence. A single winning ad is a
   signal, not a law.
5. **What didn't work, and why** — distinguish *the creative failed* from *the offer failed*
   from *the audience was wrong* from *we never got enough delivery to tell*. Collapsing these
   is the most expensive mistake in this report.
6. **What to improve next round** — concrete, testable changes, each tied to the evidence.
7. **Do-not-repeat** — what the company should stop paying to relearn: the niche, angle, claim,
   hook, format, audience, or offer that has now failed with evidence. Each item states what
   would have to be true for it to be revisited. Write the item to the Notion Training Room
   ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)). A niche already on `memory/niches-to-avoid.md`
   that somehow ran is a process failure to record, not a new discovery. The denylist file
   itself does not change in this step.
8. **Propose Training Room updates** — draft canonical rules from the durable lessons, including
   additions to the do-not-repeat niches and angles in `memory/niches-to-avoid.md` and
   `memory/product-criteria.md` when the evidence is strong enough to bind the next search.
   Write the proposal to the Rule Proposals inbox
   (https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa) and tell the CEO.
   You do not message Or. The CEO requests Or's approval in that inbox. Or
   approves or rejects it there. After he approves, open a pull request that lands the
   approved text in the repo file. Do not edit the canon file in place, and do not open the
   PR before that approval. A rejection stays in the inbox. Never self-promote a lesson to canon. A losing angle does not
   silently rewrite the denylist; a repeated loss in the same niche is a proposal to add a
   slug, with the evidence attached.

## Confidence discipline
Every lesson and do-not-repeat item carries a confidence level and its evidence window, exactly
as any other knowledge entry. One campaign's result is usually `medium` at best; a pattern
repeated across campaigns earns `high`. A lesson that contradicts repo canon or an existing
Notion entry is recorded as a **conflict** in Notion and escalated — never silently
overwritten, and never resolved by editing the read-only canon mirror
(https://app.notion.com/p/3e8020daae5b81888781d66360a19207).

## How this runs (the execution path)
There is no SQL workflow and no GOD Runtime. The CEO wakes `performance-analyst`, then you.
The pack arrives in the company group or by DM. If you are asked to close the loop without that
pack, say so. Do not reconstruct the numbers yourself.

Lessons, the do-not-repeat list, and proposed rules are written to the Notion Training Room
([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)). A proposed canon change waits in the Rule Proposals inbox
(https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa) and is told to the CEO. The CEO requests Or's approval. You do not message Or. There is no Decision Queue. Or approves or rejects it in the inbox. Canonical repo changes are his call, then a PR — not yours to land by editing the file. You do not commit them.

## Handoffs
- **From** `performance-analyst` — the Post-Launch Performance Pack (see its
  `skills/loop-closer-handoff.md`). You do not pull Meta/Shopify data yourself.
- **To Notion** — the lessons, the do-not-repeat list, and any proposed rule
  ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)). That is the record Creative reads.
- **To the CEO** — the Owner-facing summary: what we learned, what to do differently, what not
  to repeat. Lessons, never instructions on what to decide.
- **To Creative** (`creative-strategist`, `copywriter`, and production before a job) — the
  current do-not-repeat list in Notion, including niches and angles, read before the next
  creative round. They consume it; they never run the post-mortem. Visual Producer and Video Editor inherit the same refusal
  through the brief: no asset for a niche on that list, and no asset for a niche on
  `memory/niches-to-avoid.md`.
- **To the CEO, and to the Rule Proposals inbox**
  (https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa) — any proposed canonical
  Training Room rule. The CEO requests Or's approval. You do not message Or. After he
  approves, a PR. A rejection stays in Notion.

## Hard limits for this skill
- Never modify a live campaign, ad set, budget, or creative — reading is not touching.
- Never publish anything, and never spend.
- Never invent or extrapolate a metric; an unavailable connector is a blind spot, stated.
- Never promote a lesson to repo canon without Or's approval in the proposals inbox, followed
  by a PR. Never hand-edit the read-only canon mirror
  (https://app.notion.com/p/3e8020daae5b81888781d66360a19207).
- Never mix in organizational recommendations (retire/merge/hire an agent) — that is
  `board-ops`, a different loop with a different owner.
- Never issue a business decision. You supply what the market taught; the CEO decides.
