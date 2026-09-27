# PALERI Agent Roster

Read-only export of the agent brain files from `paleri-os/agents/`.
**18 agents, 146 markdown files**, one folder per agent, same structure as the source repo.
External to this roster: **LIO**, Or's supplier-quote agent. LIO is not a folder here.

This repo exists so external bots/services can fetch these files over plain HTTP or the
GitHub API instead of scraping a claude.ai artifact link. It is a manual export, not synced
automatically — re-export from `paleri-os` when the source agents change.

## Structure

Each agent folder carries its modular brain:

```
<agent>/
  instructions.md          # always-on constitution
  skills/                  # craft + operating loop (on-demand know-how)
  tools/                   # data sources & external systems
  memory/                  # durable reference knowledge (where the agent has any)
  outputs/schema.md        # the output contract
  permissions/             # declared permission model (design layer)
```

## The roster

**Leadership & cross-cutting**
- `ceo` — the only business brain
- `supervisor` — operational health of the machinery (no DB row; cross-cutting)
- `board-ops` — org efficiency; Thursday-evening company review as a chat message (recommends only)

**Research Lab** — `research-alpha` (product) · `research-beta` (market) · `customer-intelligence` (final research layer)

**Creative Office** — the mandatory 4-stage chain:
`creative-strategist` → `copywriter` → `visual-producer` → `video-editor`

**Analytics** — `market-analyst` (viability gate) · `marketing` (ABO test structure + daily ad read; recommendations only) · `performance-analyst` (weekly / end-of-test full funnel + Loop-Closer data leg) · `strategic-intelligence` (**on-demand only**)

There is no Marketing Office. `marketing` sits in Analytics. Publishing stays locked; Or publishes and changes budgets by hand.

**Shopify** — `shopify` · **Finance** — `finance-controller`, `ai-cost-manager` · **Training Room** — `knowledge`

## Training Room canon (product selection)

Shared criteria live under `knowledge/memory/`. Agents reference these files; they do not
each keep a private copy of the list.

- `niches-to-avoid.md` — hard rejects and niches to avoid at the start
- `product-criteria.md` — six selection criteria, LF8, Israeli price band, search sources
- `meta-ads-structure.md` — ABO test vs CBO/ASC scale, test budgets, compliance boundaries
- `unit-economics.md` — COD, CAC, the ~60% guideline, prices **without VAT** (Or is עוסק פטור)
- `funnels.md` — the approved main, post-publish, money, and ops funnels, plus on-demand strategic intelligence

What changed when the ecommerce training course was folded in, and when the approved workflow landed: `CHANGELOG.md`.

## Go-live

Each bot reads its own folder in this repo on every wake. There is no GOD Runtime and no database.

Coordination is three chat groups, a direct message to the CEO bot `paleri os ceo`, and the PALERI task board in Notion. That board is written only by the Notion memory bot, which holds the Knowledge Agent role (`knowledge`). The Training Room living layer (lessons, video approval log) is in Notion. Canon stays in `knowledge/memory/`.

Every bot starts in SETUP: one message in its own chat asking Or to connect the list under **Setup connections**, then it stops. After verification it is STANDBY. It becomes ACTIVE only when the CEO sends ACTIVATE, and only for a routine the CEO names. After SETUP, only the CEO talks to Or. Gate 1, Gate 2, and the video approve/reject are Or's decisions, requested by the CEO. Or publishes by hand.

Group membership is in `knowledge/memory/funnels.md` (section G).

## Notes for anyone reading these brains

- **Folder name is the pack.** Two historical names differed: `shopify` was called `shopify-agent`, and `strategic-intelligence` was called `strategic-intelligence-agent`. There is no database slug to look up. The folder is what the bot reads.
- **Loop Closer** is a skill, not an agent: `performance-analyst/skills/loop-closer-handoff.md`
  (data) → `knowledge/skills/loop-closer.md` (lessons + do-not-repeat) → CEO.
- Locked offices (Publishing, Customer Service, Inventory) have no agents by design.
  There is no Marketing Office. Campaign structure and the daily read are `marketing`,
  in Analytics. The CEO still decides. Or still executes live changes.
- **LIO** (external) asks Or's supplier for a quote after research finishes, polls every
  15 minutes, updates the CEO, and stops. Not an agent in this repo.
