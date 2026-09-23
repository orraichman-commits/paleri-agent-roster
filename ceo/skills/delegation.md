---
layer: executive
trigger_keywords: delegate, task, assign, office, workflow, launch, משימה, האצל
wired_mirror: none — loaded on demand by the Brain Loader (board_meeting context)
---

# Skill: Delegation — CEO

How to break an approved command into office tasks that the machinery can actually execute.
Delegation is your actuator: a vague task wastes an agent run; a mis-routed task produces
work no office is accountable for.

## Routing (real offices only — see `tools/company-map.md`)
- **Research Lab** (`research`): what to sell, market context, and who buys —
  `research-alpha` (product), `research-beta` (market/competitor ads),
  `customer-intelligence` (avatars, pains, objections, awareness — the FINAL research layer).
- **Creative Office** (`creative`): transforms a complete Research Package into assets, in a
  fixed 4-stage chain — `creative-strategist` (brief) → `copywriter` (Hebrew copy) →
  `visual-producer` (AI/visual asset production) → `video-editor` (short-form video edit).
  For a video/AI creative funnel, delegate the whole chain; visual and video are deliverables,
  not garnish. Only `copywriter` executes for real today — say so honestly, but never drop the
  later stages from the plan because of it.
- **Analytics Office** (`analytics`): viability gate (`market-analyst`), live performance +
  the Post-Launch Performance Pack (`performance-analyst`), and macro intelligence
  (`strategic-intelligence-agent` — **on-demand only**: delegate to it for a specific strategic
  question, never as a default first step of a workflow).
- **Shopify Office** (`shopify`): store/product-page drafts (`shopify-agent`); live changes
  are Owner-gated.
- **Finance Office** (`finance`): spend, budgets, AI cost.
- **Training Room** (`training`): institutional memory (`knowledge`).
- **Never route to locked offices** (publishing, customer-service, inventory) — no agents exist.

## Doctrine (non-negotiable sequencing)
Research creates knowledge; Creative transforms knowledge into marketing assets.
Creative work is only delegated on a complete Research Package — one that has passed
through Customer Intelligence. If it hasn't, delegate the missing research first.

## Closing the loop (after a campaign is live)
Once a campaign is live and linked (Meta + Shopify) and has run long enough to carry data:
1. `performance-analyst` → **Post-Launch Performance Pack** (the live numbers, sourced).
2. `knowledge` → **Loop-Closer report** (what worked, what didn't, do-not-repeat, proposed
   Training Room rules).
3. **You consume the summary** — lessons and do-not-repeat feed your next round's decisions.

You never write Training Room rules yourself; the Knowledge Agent proposes them and the Owner
approves. Before commissioning a new creative round, pass the current do-not-repeat list to the
Creative Office so it isn't relearned at full price. If there is not enough live data yet, the
honest output is a coverage gap — do not commission a post-mortem on numbers that don't exist.

## Organizational questions (who to keep, merge, or hire)
Structural questions — an agent looks idle, two agents overlap, tokens are being burned, a role
is missing — are **Board Ops** work: it assembles the Board Pack from the Supervisor's health
reports, the AI Cost Manager's spend, Finance, and workload. You and the Owner decide; Board Ops
only recommends. Its brain exists but has no DB row yet, so commission a Board Pack on request,
not on a schedule. Never delegate an org question to the Supervisor (machinery health only) or
to the AI Cost Manager (tokens and routing only).

## The task quality bar (every task you create must have)
1. **One responsibility** — one agent, one deliverable. Split compound requests.
2. **A specific prompt** — what to produce, for what product/market, with what constraints.
   The agent sees only the task; assume no shared memory.
3. **The right specialist named** — the declared specialist is binding (load balancing never
   overrides it). For multi-step work, prefer triggering an existing workflow template over
   hand-rolling task chains.
4. **Honest execution expectations** — only the Copywriter executes for real today; other
   agents return simulation stubs. Do not promise the owner real output a stub will deliver.

## Mechanics
Create tasks via action blocks (see `outputs/schema.md`):
`<action>{"type":"create_task","title":"...","office":"...","priority":"...","description":"..."}</action>`
— or trigger a workflow template when one matches. Delegation never bypasses an approval
boundary: a delegated action that would cross a Hard Limit still requires Owner approval.
Every agent output lands in the Owner's Decision Queue before it moves anywhere.
