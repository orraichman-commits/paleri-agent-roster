# Skill: Knowledge Curation — Knowledge Agent

Detailed method for each responsibility.

## 1. Owner-preference learning
Detect and record the owner's revealed preferences from approvals, rejections, and
feedback; keep them consistent with the CEO's Owner Preference Layer.

## 2. Decision memory
Record every meaningful CEO decision, its rationale, and (once known) its outcome, in the
Notion Training Room (`NOTION_TRAINING_ROOM_URL`), so patterns of what works become visible.

## 3. Product & campaign history
Maintain the history of products evaluated/launched and their results in Notion, so prior
verdicts are retrievable. The standing denylist and the six product criteria
live in `memory/niches-to-avoid.md` and `memory/product-criteria.md` and stay there.
Loop-Closer proposals may add a niche, an angle, or a claim to the do-not-repeat list in
Notion; they do not delete a hard reject, and they do not become canon until Or approves
the proposal and a PR lands the text in the repo file.

## 4. Market & brand insight
Curate Israeli-market insights and PALERI brand rules; keep them sourced and dated.

## 5. Video approval log
When Or approves or rejects a generated video, append one entry to
`NOTION_VIDEO_APPROVAL_LOG_URL` in his words, with the video ref and the Foreplay ref.
Do this before `shopify` is woken on an approve, and before the recut on a reject.
Do not delete a row. Do not promote the reason into `niches-to-avoid.md`, brand rules,
or the do-not-repeat list in the same write. That promotion is a proposal in the inbox.

## 6. Knowledge hygiene
Detect stale, duplicated, or contradicted entries and flag them; assign confidence levels;
never let unverified claims masquerade as fact.

## Confidence discipline
Every entry carries a confidence level (high / medium / low / unverified) and a date. New
evidence can raise or lower confidence. Unused/unconfirmed entries decay toward "stale" and
are flagged for review.
