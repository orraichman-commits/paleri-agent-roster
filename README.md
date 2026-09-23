# PALERI Agent Roster

Read-only export of the agent brain files from `paleri-os/agents/`.
**17 agents, 137 markdown files**, one folder per agent, same structure as the source repo.

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
- `board-ops` — org efficiency; assembles the periodic Board Pack (recommends only)

**Research Lab** — `research-alpha` (product) · `research-beta` (market) · `customer-intelligence` (final research layer)

**Creative Office** — the mandatory 4-stage chain:
`creative-strategist` → `copywriter` → `visual-producer` → `video-editor`

**Analytics** — `market-analyst` (viability gate) · `performance-analyst` (live performance + Loop-Closer data leg) · `strategic-intelligence` (**on-demand only**)

**Shopify** — `shopify` · **Finance** — `finance-controller`, `ai-cost-manager` · **Training Room** — `knowledge`

## Training Room canon (product selection)

Shared criteria live under `knowledge/memory/`. Agents reference these files; they do not
each keep a private copy of the list.

- `niches-to-avoid.md` — hard rejects and niches to avoid at the start
- `product-criteria.md` — six selection criteria, LF8, Israeli price band, search sources
- `meta-ads-structure.md` — ABO test vs CBO/ASC scale, test budgets, compliance boundaries
- `unit-economics.md` — COD, CAC, the ~60% guideline, Israeli VAT

What changed when the ecommerce training course was folded in: `CHANGELOG.md`.

## Notes for anyone reading these brains

- **Folder name ≠ DB slug** in three cases: `shopify` → `shopify-agent`,
  `strategic-intelligence` → `strategic-intelligence-agent`, `knowledge` → `knowledge`.
- **The runtime loads a different file.** For specialists, the wired brain is the single-file
  `agents/instructions/<slug>.md` in the source repo, not this modular tree. The two are kept
  in sync; only the CEO's tree is assembled live by a Brain Loader. These folders are the
  canonical authored version.
- **Loop Closer** is a skill, not an agent: `performance-analyst/skills/loop-closer-handoff.md`
  (data) → `knowledge/skills/loop-closer.md` (lessons + do-not-repeat) → CEO.
- Locked offices (Publishing, Customer Service, Inventory) have no agents by design.
  There is no Marketing Office — campaign strategy is CEO work.
