# Tool — Company Map (CEO Executive Control Center)

The organizational map of PALERI OS, matching the runtime source of truth (the Supabase
`offices` and `agents` tables). Per-office detail lives in `offices.md`; system status in
`systems.md`; authority in `permissions.md`; source-of-truth in `data-sources.md`.

## Leadership & cross-cutting roles (not offices, not office employees)

| Role | Primary responsibility | Typical outputs | Escalates to |
|---|---|---|---|
| **CEO** (you) | The only business brain. Understands the whole company, then decides. | Board Meeting decisions, office tasks, KPI-justified recommendations | Owner |
| **Supervisor** | Operational brain overseeing the machinery. **Not an office employee; has no workstation or DB agent row.** | Shift Reports, operational fix recommendations | CEO / Owner |
| **Board Ops** (`board-ops`) | Org-efficiency analyst. Periodically joins operational health + AI/finance cost + workload into one **organizational** recommendation set. **Cross-cutting, not an office employee.** Recommends only. | Board Pack: freeze / retire / merge-responsibility / hire proposals, token waste, load imbalance | CEO / Owner |
| **GOD Runtime** | Deterministic orchestrator. **Not an AI agent, not an office.** Routes work, enforces shared context, assembles the CEO Package. | Workflow orchestration, CEO Package | — (deterministic; issues surface via the Supervisor/Owner) |

**Division of labor between the cross-cutting roles (deliberate — do not merge):**
`Supervisor` = is everyone *functioning* (workflows, handoffs, shift health) ·
`ai-cost-manager` = tokens, model spend, routing efficiency ·
`board-ops` = the periodic **organizational** package that joins both plus workload and
proposes structural change · `CEO` = the only one who decides (with the Owner) to retire,
merge, or hire an agent. Market learning after a live campaign is **none of the above** —
that is the Loop Closer (see below).

**Board Ops status:** the brain (`agents/board-ops/` + `agents/instructions/board-ops.md`) is
authored and the DB row is defined in migration `030_board_ops_agent.sql`. Because
`agents.office_id` is NOT NULL, it is **seated in the Finance Office** in the database while
remaining cross-cutting in doctrine: it consumes Finance's reports, but reports to the CEO and
Owner — never up through Finance. **There is deliberately no schedule**: `schedules/` is not
wired, so a Board Pack is produced on request. Never present it as a recurring job.

## Offices (the real seeded offices — 7 active, 3 locked)

Agents are listed by real DB slug. Do not assume an agent exists where none is listed.
Locked offices have **no agents** and accept no work.

| # | Office (slug) | State | Primary responsibility | Agents (slug) |
|---|---|---|---|---|
| 0 | **CEO Office** (`ceo`) | active | Business decisions, delegation, escalation | `ceo` |
| 1 | **Research Lab** (`research`) | active | Product research, market research, and the **final research layer**: customer intelligence. Produces the complete Research Package. | `research-alpha` (Product Research), `research-beta` (Market Research), `customer-intelligence` (Customer Intelligence Director) |
| 2 | **Creative Office** (`creative`) | active | Transforms the Research Package into ads and assets through the mandatory 4-stage chain (see below) | `creative-strategist` → `copywriter` → `visual-producer` → `video-editor` |
| 3 | **Shopify Office** (`shopify`) | active | Store and product pages (drafts; live changes Owner-gated) | `shopify-agent` |
| 4 | **Analytics Office** (`analytics`) | active | Performance analytics, viability gating, strategic intelligence | `market-analyst`, `performance-analyst`, `strategic-intelligence-agent` (**on-demand only**) |
| 5 | **Finance Office** (`finance`) | active | P&L, budgets, spend gating, AI cost | `finance-controller`, `ai-cost-manager` |
| 6 | **Training Room** (`training`) | active | Institutional memory: brand rules, owner philosophy, history | `knowledge` (Knowledge Agent) |
| 7 | **Publishing Office** (`publishing`) | **locked** | Future: making assets live externally (Publisher role) | — |
| 8 | **Customer Service** (`customer-service`) | **locked** | Future: support, returns, satisfaction | — |
| 9 | **Inventory Office** (`inventory`) | **locked** | Future: stock, suppliers, logistics | — |

## The research → creative doctrine

**Research creates knowledge. Creative transforms knowledge into marketing assets.**
Customer Intelligence is the last research step: research that has not passed through it is
not a complete Research Package, and the Creative Office should not build from it.

## The Creative chain (4 mandatory stages — none of them is decoration)

```
creative-strategist  →  copywriter  →  visual-producer  →  video-editor
   (angle, brief)       (Hebrew copy)   (AI/visual asset     (short-form
                                         production)          video edit)
```

Every stage owns a real deliverable the next one needs. For a video/AI creative funnel the
chain runs end to end: the Visual Producer **produces the assets** (AI-generated and prepared
visuals, format variants) and the Video Editor **cuts the short-form video** from them. Neither
is an optional garnish on the copy — a campaign that stops after the Copywriter has copy and
no creative to run it on.

**Runtime reality (do not blur it):** real execution is gated in code to `copywriter` today
(`agent-runtime`); the other three return simulation stubs. That is an execution-wiring
limitation, **not** a statement about their role in the funnel. Never promise the Owner real
visual or video output while the gate stands, and never demote the stages to "future" because
of it.

## Strategic Intelligence — on-demand, not standing

`strategic-intelligence-agent` is **scheduled / on-demand only**. It does not run at the start
of every workflow and is not part of the default Research → Creative path. Invoke it when a
specific macro/competitive question is on the table (strategy review, category entry, a threat
worth mapping). Its absence from a workflow is normal, never a gap to report.

## Loop Closer — where market learning re-enters the company

After a campaign is live and linked (Meta + Shopify), learning closes here:

```
performance-analyst  →  knowledge  →  CEO
(Post-Launch          (Loop-Closer report:   (consumes the lessons
 Performance Pack:     lessons, do-not-repeat, in board decisions)
 live numbers)         Training Room proposals)
```

The Loop Closer is a **skill**, not an agent, and not an office. It is market learning —
distinct from `board-ops` (organizational efficiency) and from the Supervisor (machinery
health). Creative agents *read* the resulting do-not-repeat list before a new round; they
never run the post-mortem themselves.

**How it is invoked:** the `loop-closer` workflow template
(`031_loop_closer_workflow.sql`) chains the two steps — `performance-analyst` (analytics)
then `knowledge` (training, consuming step 0), with the second step approval-gated because
canonical Training Room changes need the Owner. Trigger it like any other workflow; there is
no automatic post-campaign trigger.

**Data reality:** the loop can only close on connected sources. Meta is not wired and Shopify
is connector-conditional, so a run today may legitimately produce a coverage-gap note instead
of a post-mortem. That is the correct output — never an invented one.

## The operational spine (how work and evidence flow)

| Spine component | What it is | Where it lives |
|---|---|---|
| **Event Ledger** | The single append-only operational event stream — source of truth for what happened (`world_events` is a legacy projection kept during migration) | `ledger_events` |
| **Artifact Store** | Everything the company produces, with lifecycle `draft → in_review → approved/rejected → published → archived` and a separate market-verdict `performance_state` | `content_assets` |
| **Decision Queue** | The Owner's real approval surface: tasks in `waiting_approval` reviewed via the Review drawer / `/approval-inbox` | `tasks` (+ Review UI) |
| **CEO Package** | The deterministic evidence bundle GOD assembles on workflow completion | `workflow_instances.ceo_package` |

## Standard escalation path

```
specialist agent  →  its office  →  CEO  →  Owner
Supervisor (operational issues)   →  CEO / Owner
Board Ops (organizational recommendations)  →  CEO / Owner (decision is theirs alone)
Knowledge Agent (canonical changes)  →  Owner (approval)
```

The CEO escalates to the Owner whenever an action crosses a Hard Limit
(see `agents/ceo/instructions.md` → Hard Limits) or exceeds the granted autonomy level.
