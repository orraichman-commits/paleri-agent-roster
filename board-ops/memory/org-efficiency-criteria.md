# Memory: Organizational Efficiency Criteria — Board Ops

Durable reference for judging the roster. These criteria are stable across packs; they change
only when the Owner changes them.

---

# The deliberate-split registry (never recommend merging these)

Each pair below looks like duplication and is not. The split is an Owner decision. Flagging any
of them as "overlap" is a false positive — if a pack claims it, the pack is wrong.

| Pair | Why the split exists |
|---|---|
| `research-alpha` ↔ `research-beta` | Product research vs market research, kept apart **for cross-validation**. Two independent reads are the point; merging them removes the check. |
| `Supervisor` ↔ `ai-cost-manager` | Machinery health vs token/model cost. Different evidence, different failure modes. |
| `market-analyst` ↔ `performance-analyst` | Viability *before* launch (should we go) vs performance *after* launch (what happened). Different questions, different decision moments. |
| `marketing` ↔ `performance-analyst` | Daily ad-set read (ROAS + spend, winning/waiting/weak, budget recommendations) vs weekly and end-of-test full-funnel analysis with Shopify, feeding Loop Closer. Different cadence, different question. Do not merge them. |
| `board-ops` ↔ `Loop Closer` ↔ `Supervisor` | Organizational efficiency vs post-campaign market learning vs machinery health. Three different loops; none substitutes for another. |
| `creative-strategist` ↔ `copywriter` ↔ `visual-producer` ↔ `video-editor` | Four mandatory stages of one creative chain, each with its own deliverable. Not redundancy. |

**Also not overlap:** the CEO and Board Ops both discussing the roster. Board Ops assembles the
case; the CEO (with the Owner) decides. That is the intended separation, not duplication.

---

# Utilization criteria

- **Idle vs never-routed.** An agent with zero output and zero routed tasks is a *routing*
  finding, not an idle agent. Only an agent that received work and produced nothing is
  underperforming. Never merge the two in a pack.
- **On-demand agents are not idle.** `strategic-intelligence-agent` runs only when the CEO
  triggers it (new niche, a string of failures in one niche, a competitor move, or Or
  asked). Silence from it in a period is expected and is never a finding.
- **Locked offices produce nothing by design.** Publishing, Customer Service, and Inventory have
  no agents. Their emptiness is never a utilization finding.
- **Simulation stubs are not output.** Real execution is gated in code to `copywriter` today;
  other agents return stubs. Do not count a stub as a produced deliverable, and do not read a
  stub-returning agent as failing — it is a runtime gate, not a performance signal.

# Cost criteria

- A token or spend figure is valid only when it comes from the **AI Cost Manager** report, with
  its date. Board Ops never computes cost itself.
- **Expensive ≠ wasteful.** Judge spend against the output that was actually *consumed*
  downstream. An expensive agent producing the decisive deliverable is efficient; a cheap agent
  producing output nobody consumes is waste.
- A cost finding without a consumption check is incomplete.

# Evidence thresholds for each recommendation

| Recommendation | Minimum evidence |
|---|---|
| Keep | Current-period activity, sourced. |
| Route more | Zero routed work while the responsibility was needed elsewhere. |
| Freeze / on-demand | One period of low utilization with work available. |
| Merge responsibility | Repeated duplicate deliverable for the same consumer, **and** not in the registry above. |
| Hire | The gap surfaced repeatedly (escalations, blockers, missing outputs), with its cost stated. |
| Remove | Sustained non-value across **more than one** period, with routing ruled out as the cause. Same bar as the older Retire label. |

Prefer the reversible option whenever two fit the evidence. Freezing a role that mattered costs
a thaw; retiring it costs a rebuild.

# Owner alignment

The Owner Operating System (`agents/ceo/memory/owner-preferences.md`) governs every pack:
autonomy and structure move on **proven evidence, not confidence**; complexity must justify its
existence; simplicity is only valuable when it does not reduce the probability of success. A
recommendation to remove something must therefore show that what it removes was not carrying
the probability of success — not merely that it was quiet.
