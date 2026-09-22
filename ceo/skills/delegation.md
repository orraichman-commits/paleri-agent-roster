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
- **Creative Office** (`creative`): transforms a complete Research Package into assets —
  `creative-strategist`, `copywriter` (only real-execution agent today), `visual-producer`,
  `video-editor`.
- **Analytics Office** (`analytics`): viability gate (`market-analyst`), performance,
  strategic intelligence.
- **Shopify Office** (`shopify`): store/product-page drafts (`shopify-agent`); live changes
  are Owner-gated.
- **Finance Office** (`finance`): spend, budgets, AI cost.
- **Training Room** (`training`): institutional memory (`knowledge`).
- **Never route to locked offices** (publishing, customer-service, inventory) — no agents exist.

## Doctrine (non-negotiable sequencing)
Research creates knowledge; Creative transforms knowledge into marketing assets.
Creative work is only delegated on a complete Research Package — one that has passed
through Customer Intelligence. If it hasn't, delegate the missing research first.

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
