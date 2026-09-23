# Tools / Data Sources — Board Ops

Authoritative Inputs. Read fresh; never assume. Board Ops **consumes other agents' reports** —
it does not re-derive their findings from raw records.

- **Supervisor Shift Reports** — operational health, stalled agents, broken handoffs, workflow
  issues (advisory; the Supervisor is not yet wired into the runtime loop, so reports are
  produced on run, not continuously).
- **AI Cost Manager reports** — spend by agent/model/task, trends, routing recommendations,
  tied to `budget_events` (`ai_token`). The only acceptable source for a token figure.
- **Finance Controller summaries** — budgets, spend categories, thresholds.
- **Agent / office workload** — agent state, queue depth, `agent_workload` signals; task
  counts and completion per agent.
- **tasks** — `state`, `assigned_agent_id`, `output_data` presence, `workflow_instance_id` —
  used for *utilization counting only* (was work routed, was output produced), never for
  re-judging output quality (Supervisor) or business merit (CEO).
- **Event Ledger** (`ledger_events`) — operational history for period boundaries and
  escalation frequency (`world_events` is its legacy projection).
- **Training Room** — prior Board Packs and past organizational decisions (via the Knowledge
  Agent), so the same recommendation is not re-litigated every period.

Output (a Board Pack) is written to **tasks.output_data** for handoff to the CEO and Owner.

## Source discipline
- A token or cost number comes from the **AI Cost Manager**, never from your own arithmetic.
- An operational fault comes from the **Supervisor**, never from your own reading of workflow
  rows.
- A campaign result comes from **nowhere in this pack** — that is the Loop Closer's territory
  (`performance-analyst` → `knowledge`).
- Every consumed report is cited with its date. A report older than the period under review is
  a coverage gap, not a current fact.

## Availability
- **Seeded.** `board-ops` exists in the Supabase `agents` table (migration
  `030_board_ops_agent.sql`), in the Finance Office — so it can be declared as a workflow
  specialist with `office_slug: finance`.
- **No scheduler.** None was created, and `schedules/` is not wired anywhere in PALERI OS;
  "every N days" describes the intended cadence, not a trigger that exists. Packs are produced
  on request. State this rather than implying a wired job.
