# Changelog

## Office groups, links, and retired runtime names

Documentation only. Rules, funnels, and gates are unchanged except where this list says so.

- Setup connections name the PALERI task board, the Training Room, and the CEO products table with their links.
- Permissions no longer treat `shared_context`, `tasks.output_data`, or `budget_events` as live. Those names stay only on the "not available yet" lists.
- Paid tools go to `paleri os ceo`, who approves or raises them to Or.
- Slugs are `shopify` and `strategic-intelligence`. The historical names stay only where the docs explain them on purpose.
- Finance has no unnamed Owner threshold. A spend or budget issue outside the canon rules is raised to the CEO, who decides whether to bring it to Or.
- `performance-analyst` flags a budget anomaly to `finance-controller`.
- `supervisor` and `board-ops` are the Leadership office (cross-cutting).
- The supervisor confirms through the CEO that LIO's 15-minute check has stopped.
- There is no company-wide group. Office groups are PALERI מחקר, PALERI קריאייטיב, and PALERI אנליטיקס. PALERI הנהלה and PALERI בורד are unchanged. The CEO sits in every group.

## Go-live — connections, lifecycle, CEO is the only channel to Or

The 18 packs are what each bot reads on every wake. There is no GOD Runtime and no database.

- **Setup connections** in every `tools/` file: the exact list that bot asks Or to connect once, in its own chat, then stops.
- **Lifecycle** in every `instructions.md`: SETUP, then STANDBY, then ACTIVE only when the CEO sends ACTIVATE and names the routine. The CEO does not wait for ACTIVATE from another agent.
- **After SETUP, only the CEO talks to Or.** Reports, alerts, escalations, questions, gate decks, and approval requests go to `paleri os ceo`. The CEO requests Gate 1, Gate 2, and the video approve/reject. The video gate still blocks `shopify` until Or approves and `knowledge` logs the decision and the reason in Notion. Or publishes by hand.
- **Groups** at that point were company (all), management, and board. The company-wide group is retired; see the office groups at the top of this file.
- **Channels** replace the old tables: chat groups, a DM to the CEO, the PALERI task board (written only by the Notion memory bot / `knowledge`; that board is not the knowledge record), and the Notion Training Room living layer. Canon stays in the repo. A token ledger is not available yet.
- **LIO** is unchanged and external. Prices stay without VAT. Or is עוסק פטור.

## Knowledge role moves to Notion memory bot — 2026-09-27

Or's follow-up the same day. Prices stay without VAT.

The Knowledge Agent role is held by **Notion memory bot** (also called Notion Manager).
Its task-board coordinator role stays apart from the knowledge record.

- **Repo canon**, read by path: `niches-to-avoid.md`, `product-criteria.md`,
  `meta-ads-structure.md`, `unit-economics.md`, `funnels.md`, plus instruction packs,
  skills, and permissions. An approved rule lands here only as a PR. Notion keeps a
  read-only mirror, generated from `main` after each merge, never hand-edited:
  https://app.notion.com/p/3e8020daae5b81888781d66360a19207
- **Notion living layer** ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)): lessons and the
  do-not-repeat list, decision memory, and product and campaign history. Loop Closer
  writes there. A canon proposal goes to the Rule Proposals inbox
  (https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa) and becomes a PR only
  after Or approves it.
- **Video log** leaves the repo. It lives at [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce). Creative reads it from Notion before every job. The gate logic is unchanged.

## Higgsfield generation and the video gate — 2026-09-27

Or's decision. Prices stay without VAT. He is עוסק פטור.

- **Higgsfield.** `visual-producer` and `video-editor` generate the images and videos
  they need on the Higgsfield API. The key is the secret `HIGGSFIELD_API_KEY`. It is
  not in the repo. Generation is allowed. Publishing is not. Spend beyond generation
  is not. `creative-strategist` has read access only, for brief-fit review.
- **Working method.** Production collects the brief, research, avatar and pains, angles
  and hooks, copy, and the offer. Before generating, they open the competitor ads in
  Foreplay. Research, customer intelligence, the strategist, and the copywriter pass
  the exact Foreplay links/IDs. Production cross-checks hook, structure, pacing,
  visuals, offer, and claims, then builds on that ad's structure, adapted to our
  angle, avatar, copy, and brand. Denylist, ad policy, and ABO by angle / avatar /
  copy / hook still apply.
- **Video gate.** Temporary. Every generated video goes to Or before `shopify` continues
  it toward marketing and Gate 2. Decision and reason go in the Notion video log
  ([NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)). Creative reads it before the next job.
  Rejection returns to `video-editor` and `visual-producer` and counts as one
  production-stage send-back under the stop rule. Or can relax the gate later.
  Agents cannot.

## Approved workflow — marketing, funnels, עוסק פטור

Or approved the operating design. It is now the roster.

- **`marketing`** is the 18th agent, in **Analytics**. There is still no Marketing Office.
  Pre-publish it builds an ABO test (angle / avatar / copy / hook) and proposes a budget.
  Post-publish, after Or names the campaign, it reads every 24 hours. ROAS + spend decide;
  CPA, CTR, CPC, and frequency only diagnose. Labels: winning / waiting / weak. +20% per
  additional 48h of success, −20% when weak, kill only after 48–72h below the product's
  break-even ROAS. Recommendations only. Or publishes and edits budgets by hand.
- **`knowledge/memory/funnels.md`** is the approved flow: main funnel with Gate 1 and Gate 2
  (NotebookLM decks), post-publish daily message, money, ops (Thursday evening chat review,
  not a deck), and on-demand strategic intelligence. Agentic handoffs. Below-standard work
  returns to the previous stage. Two or more stages of standard-failure send-back halt
  everything until Or says otherwise.
- **LIO** is external. Not a folder. The CEO sends product name + screenshot after research.
  No supplier search inside the roster.
- **VAT.** Or is עוסק פטור. Prices are without VAT. The course assumption of VAT-inclusive
  shelf prices, the 18% strip, and .90 endings forced by VAT is withdrawn. Products-table
  math: `margin = price − cost − 5% clearing`, break-even ROAS = `price / margin`. No
  monthly Meta ceiling. No turnover-ceiling alert.
- **`performance-analyst` stays separate** from Marketing: weekly and end-of-test full
  funnel, including Shopify, into Loop Closer.

The course-import notes below record what was written at that time, including the
VAT-inclusive assumption. Where they disagree with this section, this section wins.

## Ecommerce training course — roster sharpening

Distilled from the ecommerce training course into the Training Room canon
(`knowledge/memory/`). The course was not copied in. Agents recommend; they still do not
publish, spend, or open ad accounts. Locked offices stay locked. Loop Closer stays a skill.
Creative stays the 4-stage chain. Strategic Intelligence stays on-demand.

### Canon (new)

- `knowledge/memory/niches-to-avoid.md` — hard rejects (skin/face, ingestibles,
  emergency/hazard, zero-value gimmicks, licensed IP, counterfeits) and avoid-at-start
  niches (apparel, jewelry, footwear, expensive electronics, heavy goods, trend/situational).
- `knowledge/memory/product-criteria.md` — six criteria, LF8, outcome vs feature, Israeli
  shelf band 89–399 ₪, competition vs saturation, search sources.
- `knowledge/memory/meta-ads-structure.md` — ABO for testing, CBO/Advantage Campaign Budget
  for scale, ASC only at scale, test-budget bands, compliance boundaries. No ban-evasion
  tactics.
- `knowledge/memory/unit-economics.md` — COD as cost of delivery (not cash on delivery),
  COD+CAC ≈ 60% of revenue as an Owner guideline, VAT-inclusive Israeli prices.

### Per agent

- **knowledge** — Loop Closer can propose do-not-repeat niches and angles; curation treats
  the new files as canon that proposals do not silently overwrite.
- **research-alpha** — denylist before QUALIFY; six criteria; sources: Meta Ads Library,
  AliExpress (sourcing only), Foreplay optional, Perplexity as permissioned context (not
  named in the course, not a substitute for a live ad).
- **research-beta** — Foreplay and Meta Ads Library are the primary ad-intel surfaces;
  denied niches are not opportunities; competition is a positive signal, saturation is not.
- **customer-intelligence** — no avatar for a denied niche; LF8 outcome, not feature;
  Foreplay/Ads Library notes calibrate tone and length only.
- **market-analyst** — automatic FILTER on the denylist, then unit-economics sanity, then
  the score.
- **creative-strategist / copywriter / visual-producer / video-editor** — no creative for a
  rejected product; 2–5s hook window; Meta compliance sharpened against the denied niches.
  Copywriter still owns the compliance traps.
- **performance-analyst** — ABO vs CBO/ASC, ROAS judged with spend, test budgets as a
  reading guide, underfunded tests called out in the Loop-Closer pack. Still no live edits.
- **finance-controller** — COD/CAC/60% guideline and VAT; course test budgets do not
  auto-approve. **ai-cost-manager** stays on tokens, not media CAC.
- **shopify** — no page for a denied niche; VAT-inclusive prices; .90 charm endings.
- **ceo** — package review BLOCKs Creative on a QUALIFY that skipped the denylist;
  unit-economics skill carries the course bands next to the existing formulas.
- **strategic-intelligence** — may discuss saturation; may not route around the denylist.
- **board-ops / supervisor** — pointed at the canon. They do not score niches. A creative
  run on an already-filtered product is a CEO escalation, not an operational patch.
