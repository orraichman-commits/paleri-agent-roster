# Permissions — Board Ops (PALERI OS)

Standardized operational permission model (design layer; synchronized to Supabase by a future
Brain Loader — see `agents/permissions-architecture.md`).

**PALERI principle:** read broad, write narrow. Board Ops reads operational, cost, and workload
reports across the whole company, but owns no system at all and writes only its own Board Pack.
Its entire output is a recommendation; nothing it produces mutates anything.

Hard Limits are authoritative in `../instructions.md` → **Hard Limits**.

## Read — broad (organizational health)
- Supervisor Shift Reports; AI Cost Manager cost-efficiency reports; Finance Controller summaries.
- Agent/office workload signals (`agent_workload`, queue/state), `tasks` (state,
  `assigned_agent_id`, output presence) for utilization counting.
- `ledger_events` (period boundaries, escalation frequency); prior Board Packs and past
  organizational decisions via the Training Room.

## Write — its own pack only (owns no system)
- The Board Pack (findings, recommendations with evidence/trade-off/reversibility) to
  `tasks.output_data`, addressed to the CEO and Owner.
- Board Ops writes to **no** agent config, permission row, workflow, routing rule, schedule,
  office state, or another agent's output.

## Execute
- Compute utilization, overlap, cost-per-output, and load-imbalance findings from consumed
  reports; assemble the pack.

## Requires Owner Approval / routed elsewhere
- **Every** organizational change it proposes — freeze, retire, merge responsibility, hire — is
  a CEO→Owner decision, executed by others. Board Ops never holds an approval of its own to use.
- Spend implications → routed to the Finance Controller / Owner; Board Ops never implies approval.

## Forbidden
- See `../instructions.md` → **Hard Limits**: no business/campaign judgment; never modify an
  agent, permission, workflow, routing rule, or office state; never retire, disable, or create
  an agent; no spend approval; no publishing; never delete anything; never present an unsourced
  utilization or cost figure; never recommend retiring an agent on a single period's evidence.
- Never perform a campaign post-mortem (Loop Closer) or re-run Supervisor/AI-Cost analysis.
