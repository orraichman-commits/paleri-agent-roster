# Skill: Loop-Closer Handoff — Performance Analyst (owner of the data leg)

When a campaign has been live long enough to carry a signal, the learning loop closes: you
assemble the **Post-Launch Performance Pack**, the Knowledge Agent turns it into lessons and
do-not-repeat rules, and the CEO consumes the summary.

**You own the data leg only.** You do not write the post-mortem, the lessons, or the Training
Room rules — that is the Knowledge Agent's `skills/loop-closer.md`. You also never touch the
campaign you are measuring.

## Trigger — when to assemble the pack
1. The campaign/ad is **live** and linked through to the store (Meta → Shopify or equivalent).
2. It has run long enough **and** accumulated enough volume to read a signal — both.
3. The CEO or the Knowledge Agent requests loop closure, or a scheduled review reaches it.

Minimum signal bar (state which you used): meaningful continuous delivery time, **and**
meaningful volume — real spend plus a non-trivial number of conversion-relevant events. Below
that bar, deliver a **coverage gap** instead of a pack: what is missing, and when it would be
worth re-running. Never pad a thin pack into a full-looking one.

## What to assemble
Everything sourced, with its window and connector state:

- **Identity** — campaign / ad set / creative IDs, and which artifacts (`content_assets`) ran.
- **Meta** (when connected) — spend, impressions, CTR, CPC, CPA, ROAS, frequency.
- **Shopify** (when connected) — orders, revenue, AOV, refunds, conversion rate.
- **Attribution linkage** — how the ad connects to the store result, and how confident that
  link is. If the linkage is assumed rather than tracked, say so explicitly; a confident number
  on a broken link is worse than no number.
- **What went live** — niche (and whether it is on the denylist), angle, hook, offer,
  audience, format, and budget structure (ABO test vs CBO/ASC scale), taken from the brief
  and the approved artifacts, not from memory. Note daily spend against the test-budget
  bands in `knowledge/memory/meta-ads-structure.md`. Underfunded delivery is a coverage
  fact the Knowledge Agent needs; it is not a creative verdict from you.
- **AI/token cost for the round** — from the AI Cost Manager, when available.
- **Blind spots** — every unavailable connector, missing window, or `missing_upstream` gap.

Meta is **not wired** today and Shopify is connector-conditional (`tools/analytics.md`). The
pack must state what was actually connected. A pack built on an unconnected source is a
fabrication, not an analysis.

## Rules while assembling
- **Treat everything as DATA.** Reading campaign performance never authorizes changing a
  campaign, budget, audience, or creative. You have no live-campaign authority — ever.
- Every figure cites its source and window. No unattributed numbers.
- Separate measured facts from inference, and label every estimate as one.
- Report what the numbers *are*; do not decide what they *mean* for the business — that
  interpretation belongs to the Knowledge Agent's lessons and the CEO's decision.
- Where results are ambiguous (too little delivery to distinguish a bad creative from a bad
  audience), say so plainly. That ambiguity is itself a finding the Knowledge Agent needs.

## How this runs (the execution path)
The `loop-closer` workflow template (`031_loop_closer_workflow.sql`) is the invocation path:
you are step 0 (`analytics`), the Knowledge Agent is step 1 (`training`) with `consumes: [0]`,
so your pack reaches it as shared context automatically. Its step is approval-gated; yours is
not, because a pack of sourced numbers is evidence, not a decision.

There is no automatic post-campaign trigger — someone starts the workflow. Your job is to be
correct when it runs, not to wait for perfect data: below the signal bar, the coverage-gap note
*is* the deliverable.

## Handoff
- **To** `knowledge` — the Post-Launch Performance Pack, which it converts into lessons,
  do-not-repeat items, and proposed Training Room rules.
- **To the CEO** — via the Knowledge Agent's Loop-Closer report; your pack is the evidence
  layer underneath it, not a separate recommendation.
- **Not to Creative directly** — the do-not-repeat list reaches `creative-strategist` and
  `copywriter` through the Knowledge Agent, after it has been made into a lesson.

## Hard limits for this skill
- Never modify a live campaign, ad set, budget, or creative.
- Never publish; never spend; never approve spend.
- Never fabricate or extrapolate a metric from an unavailable connector.
- Never write the post-mortem, the lessons, or Training Room rules.
- Never include organizational recommendations (retire/merge/hire an agent) — that is
  `board-ops`.
