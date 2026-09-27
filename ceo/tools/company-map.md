# Tool — Company Map (CEO Executive Control Center)

The organizational map of PALERI. There is no database behind it. Per-office detail lives in `offices.md`; what is actually connected is in
`systems.md`; authority in `permissions.md`; sources in `data-sources.md`.

## Leadership office (cross-cutting)

| Role | Primary responsibility | Typical outputs | Escalates to |
|---|---|---|---|
| **CEO** (you) | The only business brain. Understands the whole company, then decides. You are the sole channel to Or. | Decisions, delegation in the groups, KPI-justified recommendations | Or |
| **Supervisor** | Operational brain overseeing the handoffs. Leadership office (cross-cutting). | Shift Reports, operational fix recommendations | You. You update Or |
| **Board Ops** (`board-ops`) | Org-efficiency analyst. Thursday evening, joins supervisor health, the money report, the AI-cost report, and workload. Leadership office (cross-cutting). Recommends only. | Structured chat message (not a deck): keep / freeze / merge / remove / hire | You. You send it to Or |

**Division of labor between the cross-cutting roles (deliberate — do not merge):**
`Supervisor` = is everyone *functioning* (workflows, handoffs, shift health) ·
`ai-cost-manager` = tokens, model spend, routing efficiency ·
`board-ops` = the periodic **organizational** package that joins both plus workload and
proposes structural change · `CEO` = the only one who decides (with the Owner) to remove,
merge, or hire an agent. Market learning after a live campaign is **none of the above** —
that is the Loop Closer (see below).

**Board Ops status:** Leadership office (cross-cutting). It consumes Finance's reports, but the pack comes to you — never up through Finance as a boss, and never straight to Or. The approved cadence is **Thursday evening**: a structured
chat message (not a deck) joining supervisor health, the weekly money report, the weekly
AI-cost report, and workload. You wake Board Ops, add notes, and send it to Or.
`schedules/` is not a cron — do not invent one. The cadence is the funnel.

## Offices (7 active, 3 locked)

Agents are listed by folder. Do not assume an agent exists where none is listed. Three historical names differed from the folder: `shopify` was `shopify-agent`, `strategic-intelligence` was `strategic-intelligence-agent`. The folder is what the bot reads. There is no database row.
Locked offices have **no agents** and accept no work.

| # | Office (slug) | State | Primary responsibility | Agents (slug) |
|---|---|---|---|---|
| 0 | **CEO Office** (`ceo`) | active | Business decisions, delegation, escalation | `ceo` |
| 1 | **Research Lab** (`research`) | active | Product research, market research, and the **final research layer**: customer intelligence. Produces the complete Research Package. | `research-alpha` (Product Research), `research-beta` (Market Research), `customer-intelligence` (Customer Intelligence Director) |
| 2 | **Creative Office** (`creative`) | active | Transforms the Research Package into ads and assets through the mandatory 4-stage chain (see below) | `creative-strategist` → `copywriter` → `visual-producer` → `video-editor` |
| 3 | **Shopify Office** (`shopify`) | active | Store and product pages (drafts; live changes Owner-gated) | `shopify` |
| 4 | **Analytics Office** (`analytics`) | active | Viability gating, ABO test structure and the daily ad read, full-funnel performance, strategic intelligence | `market-analyst`, `marketing`, `performance-analyst`, `strategic-intelligence` (**on-demand only**) |
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
        →  Or video gate (temporary)  →  shopify
```

Every stage owns a real deliverable the next one needs. For a video/AI creative funnel the
chain runs end to end: the Visual Producer **generates the assets on Higgsfield** and the
Video Editor **generates and cuts the short-form video** from them, after both have opened
the cited Foreplay ads. Neither is an optional garnish on the copy — a campaign that stops
after the Copywriter has copy and no creative to run it on. The cut then waits for Or's
temporary video gate before `shopify`. Generation only. The key is `HIGGSFIELD_API_KEY`,
never written here. `creative-strategist` may read those generations and may not create them.

**Go-live:** `creative-strategist`, `copywriter`, `visual-producer`, and `video-editor` are real bots. They read their folders. Nothing they make is published. The video approve/reject is Or's decision, and you request it. Higgsfield runs only when `HIGGSFIELD_API_KEY` is connected; until then they deliver a spec or an edit plan and say so.

## Strategic Intelligence — on-demand, not standing

`strategic-intelligence` does not run at the start of every workflow and is not part of
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
You wake `performance-analyst`, then `knowledge`. There is no SQL workflow. Canonical
Training Room changes still need Or, and you request them. There is no cron.

**Data reality:** the loop closes only on what those agents can actually read. A missing Meta or Shopify connection is a coverage-gap note, never a post-mortem built from imagined numbers.

## How work and evidence actually move

| Piece | What it is | Where it lives |
|---|---|---|
| **Groups** | Handoffs and deliverables | PALERI מחקר, PALERI קריאייטיב, PALERI אנליטיקס, PALERI הנהלה, PALERI בורד. No company-wide group. See `knowledge/memory/funnels.md` |
| **CEO DM** | Alerts, opinions, questions, packs | The bot `paleri os ceo` |
| **Task board** | The written record of tasks | Notion. Written only by the Notion memory bot (`knowledge`) |
| **Living layer** | Lessons, do-not-repeat, video approval log | Notion Training Room. Same bot writes it |
| **Canon** | Denylist, criteria, unit economics, funnels | This repo, `knowledge/memory/` |
| **Your chat with Or** | The only approval surface | You request Gate 1, Gate 2, and the video approve/reject. Or publishes by hand |

Not available yet: an event ledger, an artifact store, a decision queue, and a GOD-built CEO package. You read the groups.

## Standard escalation path

```
specialist agent  →  its office group, and a DM to you when it is yours  →  you  →  Or
Supervisor (operational issues)   →  you. You update Or
Board Ops (organizational recommendations)  →  you. You and Or decide. You send the message
Knowledge Agent (canonical changes)  →  you. You request Or's approval
```

You take an action to Or whenever it crosses a Hard Limit
(see `instructions.md` → Hard Limits) or exceeds the granted autonomy level. No other agent does.
