# Tool — Company Map (CEO Executive Control Center)

The organizational map of PALERI OS, matching the runtime source of truth (the Supabase
`offices` and `agents` tables). Per-office detail lives in `offices.md`; system status in
`systems.md`; authority in `permissions.md`; source-of-truth in `data-sources.md`.

## Leadership & cross-cutting roles (not offices, not office employees)

| Role | Primary responsibility | Typical outputs | Escalates to |
|---|---|---|---|
| **CEO** (you) | The only business brain. Understands the whole company, then decides. | Board Meeting decisions, office tasks, KPI-justified recommendations | Owner |
| **Supervisor** | Operational brain overseeing the machinery. **Not an office employee; has no workstation or DB agent row.** | Shift Reports, operational fix recommendations | CEO / Owner |
| **GOD Runtime** | Deterministic orchestrator. **Not an AI agent, not an office.** Routes work, enforces shared context, assembles the CEO Package. | Workflow orchestration, CEO Package | — (deterministic; issues surface via the Supervisor/Owner) |

## Offices (the real seeded offices — 7 active, 3 locked)

Agents are listed by real DB slug. Do not assume an agent exists where none is listed.
Locked offices have **no agents** and accept no work.

| # | Office (slug) | State | Primary responsibility | Agents (slug) |
|---|---|---|---|---|
| 0 | **CEO Office** (`ceo`) | active | Business decisions, delegation, escalation | `ceo` |
| 1 | **Research Lab** (`research`) | active | Product research, market research, and the **final research layer**: customer intelligence. Produces the complete Research Package. | `research-alpha` (Product Research), `research-beta` (Market Research), `customer-intelligence` (Customer Intelligence Director) |
| 2 | **Creative Office** (`creative`) | active | Transforms the Research Package into ads and assets: strategy, copy, visuals, video | `creative-strategist`, `copywriter`, `visual-producer`, `video-editor` |
| 3 | **Shopify Office** (`shopify`) | active | Store and product pages (drafts; live changes Owner-gated) | `shopify-agent` |
| 4 | **Analytics Office** (`analytics`) | active | Performance analytics, viability gating, strategic intelligence | `market-analyst`, `performance-analyst`, `strategic-intelligence-agent` |
| 5 | **Finance Office** (`finance`) | active | P&L, budgets, spend gating, AI cost | `finance-controller`, `ai-cost-manager` |
| 6 | **Training Room** (`training`) | active | Institutional memory: brand rules, owner philosophy, history | `knowledge` (Knowledge Agent) |
| 7 | **Publishing Office** (`publishing`) | **locked** | Future: making assets live externally (Publisher role) | — |
| 8 | **Customer Service** (`customer-service`) | **locked** | Future: support, returns, satisfaction | — |
| 9 | **Inventory Office** (`inventory`) | **locked** | Future: stock, suppliers, logistics | — |

## The research → creative doctrine

**Research creates knowledge. Creative transforms knowledge into marketing assets.**
Customer Intelligence is the last research step: research that has not passed through it is
not a complete Research Package, and the Creative Office should not build from it.

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
Knowledge Agent (canonical changes)  →  Owner (approval)
```

The CEO escalates to the Owner whenever an action crosses a Hard Limit
(see `agents/ceo/instructions.md` → Hard Limits) or exceeds the granted autonomy level.
