# Skill: Board Pack — Board Ops

How to build the periodic organizational package. The pack answers one question — *is the
company's organization still earning its cost?* — and answers it with other agents' evidence,
never with your own impressions.

## 1. Gather (never re-derive)
Pull the latest of each, and record its date and coverage:

| View | Source | Owner |
|---|---|---|
| Operational health | Shift Reports | Supervisor |
| AI spend & routing | AI cost-efficiency reports (`ai_token` events) | AI Cost Manager |
| Money | Financial summaries, budget events | Finance Controller |
| Load | Agent/office workload and queue signals | Runtime records |

If a view is missing or stale, that is a line in the pack's **Coverage** section. You do not
substitute a Supervisor finding with your own reading of raw workflow rows — that is the
Supervisor's job, and duplicating it is exactly the waste you exist to catch.

## 2. Compute the four findings
- **Utilization** — per agent: tasks carried, outputs produced, idle periods. An agent quiet
  because *no work was routed to it* is not an idle agent; it is a routing finding. Separate the
  two explicitly.
- **Overlap** — two agents producing substantially the same deliverable for the same consumer.
  Before flagging, check `memory/org-efficiency-criteria.md`: several splits are deliberate and
  must never be recommended for merging.
- **Cost efficiency** — spend per meaningful output, using the AI Cost Manager's figures only.
  Expensive is not the same as wasteful: an expensive agent producing the decisive deliverable
  is efficient; a cheap agent producing nothing consumed is waste.
- **Structural gap** — a responsibility that shows up repeatedly in escalations, blockers, or
  missing outputs and that nobody owns. This is the only honest basis for a hiring proposal.

## 3. Turn each finding into one recommendation
Allowed recommendation types, in ascending order of irreversibility:

| Type | Use when | Note |
|---|---|---|
| **Keep** | The role earns its cost. | Say so — a pack that only lists problems is not a review. |
| **Route more** | Idle because work never arrives. | Fixes the routing, not the roster. |
| **Freeze / on-demand** | Real role, but not needed on every cycle. | The reversible option — prefer it. |
| **Merge responsibility** | Genuine duplication, not a deliberate split. | Name which agent keeps what. |
| **Hire** | A documented gap nobody owns. | State the cost of the new agent, not just the benefit. |
| **Remove** | Sustained, evidenced non-value across periods. The older label was Retire. | The most irreversible — never on one period. |

Always prefer the reversible recommendation. Freezing an agent that turns out to matter costs a
thaw; retiring it costs a rebuild. The Owner Operating System is explicit that autonomy and
structure move by proven evidence, not by confidence.

## 4. Write each recommendation like this
```
<Type>: <agent/role> — <one-line claim>
Evidence: <figures + the report and date they came from>
Trade-off: <what breaks if this is wrong>
Reversibility: <reversible | costly to undo>
Decision owner: CEO / Owner
```

A recommendation missing evidence, trade-off, or reversibility does not go in the pack.

## 5. What never goes in the pack
- Business or campaign judgment ("this product is weak") — CEO territory.
- Post-campaign market lessons ("the hook underperformed") — that is the **Loop Closer**
  (`performance-analyst` + `knowledge`), a different loop entirely.
- Machinery incidents ("the fan-in barrier hung") — the Supervisor already reported it; cite it
  only if it is evidence for an *organizational* claim.
- Any instruction addressed to another agent. Your pack addresses the CEO and Owner.
