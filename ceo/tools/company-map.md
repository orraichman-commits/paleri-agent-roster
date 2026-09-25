# Tool — Company Map (CEO Executive Control Center)

The organizational map of PALERI OS, matching the runtime source of truth (the Supabase
`offices` and `agents` tables). Per-office detail lives in `offices.md`; system status in
`systems.md`; authority in `permissions.md`; source-of-truth in `data-sources.md`.

## Leadership & cross-cutting roles (not offices, not office employees)

| Role | Primary responsibility | Typical outputs | Escalates to |
|---|---|---|---|
| **CEO** (you) | The only business brain. Understands the whole company, then decides. | Board Meeting decisions, office tasks, KPI-justified recommendations | Owner |
| **Supervisor** | Operational brain overseeing the machinery. **Not an office employee; has no workstation or DB agent row.** | Shift Reports, operational fix recommendations | CEO / Owner |
| **Board Ops** (`board-ops`) | Org-efficiency analyst. Thursday evening, joins supervisor health, the money report, the AI-cost report, and workload. **Cross-cutting, not an office employee.** Recommends only. | Structured chat message (not a deck): keep / freeze / merge / remove / hire | CEO / Owner |
| **GOD Runtime** | Deterministic orchestrator. **Not an AI agent, not an office.** Routes work, enforces shared context, assembles the CEO Package. | Workflow orchestration, CEO Package | — (deterministic; issues surface via the Supervisor/Owner) |

**Division of labor between the cross-cutting roles (deliberate — do not merge):**
`Supervisor` = is everyone *functioning* (workflows, handoffs, shift health) ·
`ai-cost-manager` = tokens, model spend, routing efficiency ·
`board-ops` = the periodic **organizational** package that joins both plus workload and
proposes structural change · `CEO` = the only one who decides (with the Owner) to remove,
merge, or hire an agent. Market learning after a live campaign is **none of the above** —
that is the Loop Closer (see below).

**Board Ops status:** the brain (`agents/board-ops/` + `agents/instructions/board-ops.md`) is
authored and the DB row is defined in migration `030_board_ops_agent.sql`. Because
`agents.office_id` is NOT NULL, it is **seated in the Finance Office** in the database while
remaining cross-cutting in doctrine: it consumes Finance's reports, but reports to the CEO and
Owner — never up through Finance. The approved cadence is **Thursday evening**: a structured
chat message (not a deck) joining supervisor health, the weekly money report, the weekly
AI-cost report, and workload. The CEO wakes Board Ops, adds notes, and sends it to Or.
`schedules/` is still not a wired cron — do not invent one. The cadence is the funnel.

## Offices (the real seeded offices — 7 active, 3 locked)

Agents are listed by real DB slug. Do not assume an agent exists where none is listed.
Locked offices have **no agents** and accept no work.

| # | Office (slug) | State | Primary responsibility | Agents (slug) |
|---|---|---|---|---|
| 0 | **CEO Office** (`ceo`) | active | Business decisions, delegation, escalation | `ceo` |
| 1 | **Research Lab** (`research`) | active | Product research, market research, and the **final research layer**: customer intelligence. Produces the complete Research Package. | `research-alpha` (Product Research), `research-beta` (Market Research), `customer-intelligence` (Customer Intelligence Director) |
| 2 | **Creative Office** (`creative`) | active | Transforms the Research Package into ads and assets through the mandatory 4-stage chain (see below) | `creative-strategist` → `copywriter` → `visual-producer` → `video-editor` |
| 3 | **Shopify Office** (`shopify`) | active | Store and product pages (drafts; live changes Owner-gated) | `shopify-agent` |
| 4 | **Analytics Office** (`analytics`) | active | Viability gating, ABO test structure and the daily ad read, full-funnel performance, strategic intelligence | `market-analyst`, `marketing`, `performance-analyst`, `strategic-intelligence-agent` (**on-demand only**) |
| 5 | **Finance Office** (`finance`) | active | P&L, budgets, spend gating, AI cost | `finance-controller`, `ai-cost-manager` |
| 6 | **Training Room** (`training`) | active | Institutional memory: brand rules, owner philosophy, history | `knowledge` (Knowledge Agent) |
| 7 | **Publishing Office** (`publishing`) | **locked** | Future: making assets live externally (Publisher role) | — |
| 8 | **Customer Service** (`customer-service`) | **locked** | Future: support, returns, satisfaction | — |
| 9 | **Inventory Office** (`inventory`) | **locked** | Future: stock, suppliers, logistics | — |

## The research → creative doctrine

**Research creates knowledge. Creative transforms knowledge into marketing assets.**
Customer Intelligence completes the Research Package: research that has not passed through
it is not complete, and the Creative Office should not build from it. CI works **in parallel**
with the product and market finders and hands the brief to the CEO. It does not wait for the
supplier quote.

**No supplier search.** Or has his own supplier. After research finishes, the CEO sends the
product name and a screenshot to **LIO**, Or's external agent (not in this roster). LIO asks
the main supplier, checks every 15 minutes, updates the CEO, and stops. The approved flow
is `knowledge/memory/funnels.md`.

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

`strategic-intelligence-agent` does not run at the start of every workflow and is not part of
funnel A. The CEO triggers it **without asking Or** before entering a new niche, when several
products in the same niche fail in a row, on a notable competitor move, or when Or asks.
Output is a short enter / wait / avoid. Its absence from an ordinary product run is normal,
never a gap to report.

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

**How it is invoked:** weekly, and at the end of a test — not on Marketing's 24-hour read.
The `loop-closer` workflow template (`031_loop_closer_workflow.sql`) chains
`performance-analyst` (analytics) then `knowledge` (training, consuming step 0). Canonical
Training Room changes still need the Owner. There is no claim of a wired cron; the CEO
wakes the loop on that cadence.

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
