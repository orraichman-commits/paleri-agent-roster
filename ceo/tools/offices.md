# Tool — Offices (CEO Executive Control Center)

Per-office detail for the **real seeded offices** (Supabase `offices` table — the runtime
source of truth). The overview map is in `company-map.md`. Agents are named by real DB slug.
Locked offices have no agents and accept no work — do not route anything there.

---

## CEO Office (`ceo`) — active
- **Mission:** Business judgment for the whole company.
- **Agents:** `ceo` (you — the only business brain).
- **Note:** GOD and the Supervisor are NOT here; they are cross-cutting runtime roles, not office employees.

## Research Lab (`research`) — active
- **Mission:** Produce the complete Research Package: what to sell, the market it lives in, and who buys it.
- **Responsibilities:** Product sourcing/evaluation (`research-alpha`), market & competitor-ad research (`research-beta`), and the **final research layer** — customer avatars, pains, desired outcomes, objections, awareness levels, buying motivations (`customer-intelligence`).
- **Expected outputs:** Product research reports, market research, Customer Intelligence Briefs → together the Research Package.
- **Doctrine:** research that has not passed through Customer Intelligence is not a complete package; Creative should not build from it. CI runs in parallel with the finders. There is no supplier search — after research finishes, the CEO hands the product name and a screenshot to external LIO.
- **CEO involves it when:** evaluating what to sell, validating a product idea, or preparing the research a launch will be built on.
- **Escalates to CEO when:** a qualified product needs a go/no-go, or research quality is too low to score.

## Creative Office (`creative`) — active
- **Mission:** Transform the Research Package into high-converting creative for Israeli Meta campaigns.
- **Agents (the mandatory 4-stage chain, in order):**
  1. `creative-strategist` — angle, positioning, format mix; writes the brief.
  2. `copywriter` — the Hebrew copy (hooks, primary text, headlines, CTAs).
  3. `visual-producer` — **produces the AI/visual assets**: ad creatives, product mockups,
     lifestyle visuals, format variants (9:16 / 1:1 / 4:5).
  4. `video-editor` — **cuts the short-form video** from those assets: hook, pacing, Hebrew
     captions, format/duration variants.
- **Chain doctrine:** for a video/AI creative funnel all four stages run. Visual and video are
  deliverables the campaign cannot launch without — not decoration on top of the copy. The
  Copywriter remains the linchpin of the message; it is simply not the whole creative.
- **Expected outputs:** Creative briefs, Hebrew copy, visual assets, short-form video — all approval-gated drafts that land in the Artifact Store.
- **Execution reality:** real execution is gated in code to `copywriter` today; the other three
  return simulation stubs (`tools/systems.md` → Agent Runtime). Report that honestly when
  promising output; it does not change their place in the chain.
- **Before a new creative round:** `creative-strategist` and `copywriter` read the current
  **do-not-repeat** list from the Knowledge Agent's latest Loop-Closer report, when one exists.
- **CEO involves it when:** a completed Research Package needs creative for launch or testing.
- **Escalates to CEO when:** an angle needs a business call, or a brief would require a prohibited claim.

## Shopify Office (`shopify`) — active
- **Mission:** Run the store layer as drafts; live changes are Owner-gated.
- **Agents:** `shopify-agent`.
- **Expected outputs:** Hebrew product page drafts (approval-gated); store optimization proposals.
- **Escalates to CEO/Owner when:** any live store change (publish, live price, theme) needs Level 4 approval.

## Analytics Office (`analytics`) — active
- **Mission:** Turn data into decision-ready insight, gate viability, and organize the Meta test.
- **Agents:**
  - `market-analyst` — viability scoring/gate (**standing**: part of funnel A).
  - `marketing` — ABO test structure before publish, and the every-24h ad-set read after
    Or confirms launch. Recommendations only. Never publishes, never changes a budget.
  - `performance-analyst` — weekly and end-of-test full-funnel read (Shopify included) and
    the **Post-Launch Performance Pack** that feeds the Loop Closer. Not the daily read.
  - `strategic-intelligence-agent` — macro/competitive intelligence, **on-demand only**.
    The CEO triggers it without asking Or: new niche, a string of failures in one niche,
    a notable competitor move, or Or asked. Short enter / wait / avoid.
- **Distinct on purpose:** `market-analyst` gates *whether to go*; `marketing` structures
  the test and reads it daily; `performance-analyst` measures the full funnel weekly and
  at the end of a test. Do not merge them. There is **no Marketing Office**.
- **Expected outputs:** Viability analyses, ABO plans, daily reads, performance summaries, Post-Launch Performance Packs, on-demand intelligence briefs.
- **CEO involves it when:** assessing performance, opportunities, threats, product viability, or the shape of a test.
- **Escalates to CEO when:** a KPI deteriorates materially, a kill or a raise is recommended, or intelligence implies a strategic decision.

## Finance Office (`finance`) — active
- **Mission:** Protect PALERI's money and keep spend efficient.
- **Agents:** `finance-controller`, `ai-cost-manager`.
- **Expected outputs:** Financial summaries, spend decisions, AI cost-efficiency reports.
- **Escalates to CEO/Owner when:** spend is at/above threshold, or on overruns/spikes.

## Training Room (`training`) — active
- **Mission:** Be the institutional memory of the company.
- **Agents:** `knowledge` (Knowledge Agent).
- **Expected outputs:** Curated, sourced, confidence-rated knowledge; proposed canonical updates (Owner-approved); **Loop-Closer reports** after a live campaign (lessons + do-not-repeat).
- **CEO involves it when:** it needs prior context, owner preferences, or decision history before deciding — or weekly / at the end of a test, when the Loop Closer should close.

---

## Cross-cutting roles (not offices, no office employees)

## Board Ops (`board-ops`) — cross-cutting
- **Mission:** Periodically join operational health, AI/finance cost, and workload into one
  organizational recommendation set for the Owner and CEO.
- **Inputs:** Supervisor Shift Reports, AI Cost Manager reports, Finance Controller summaries,
  office/agent workload status.
- **Expected outputs:** A Thursday-evening chat message — keep / freeze / merge / remove / hire,
  token waste, load imbalance — **recommendations only**. Not a deck.
- **Hard boundary:** never changes live config, never removes an agent, never approves spend.
  The CEO and Owner decide; Board Ops only assembles the case.
- **DB seat:** `agents.office_id` is NOT NULL, so the row lives in the **Finance Office**
  (migration `030_board_ops_agent.sql`) while the role stays cross-cutting: it consumes
  Finance's reports but reports to the CEO and Owner, never up through Finance. A workflow
  step declaring `board-ops` must therefore name `office_slug: finance`.
- **Thursday evening — the approved cadence.** A structured chat message, not a deck. The
  CEO wakes Board Ops, adds notes, and sends the message to Or. `schedules/` is not a wired
  cron; do not invent one, and do not describe the review as optional.

---

## Locked offices (seeded, no agents, accept no work)

## Publishing Office (`publishing`) — locked
- **Future mission:** The only place assets go live externally (Publisher role — never the creating specialist). Until unlocked, nothing publishes automatically; publishing decisions are CEO→Owner calls executed manually.
- **Planned shape when it opens (not now):** once the store is live externally, this office gets
  **one single Publishing agent** — not a full office of specialists. Approved direction only;
  no brain, no slug, no DB row exists yet. Do not create it before the Owner opens the office.

## Customer Service (`customer-service`) — locked
- **Future mission:** Support, returns, satisfaction. No agent exists; customer-facing messaging is Owner-gated and manual today.
- **No future agent is approved.** Unlike Publishing, nothing is planned here yet — do not scope one.

## Inventory Office (`inventory`) — locked
- **Future mission:** Stock, suppliers, logistics. No agent exists today.
- **No future agent is approved.** Nothing is planned here yet — do not scope one.

---

## What does NOT exist (do not route work to these)

There is **no Marketing Office**. `marketing` is an Analytics agent: it builds the ABO test
and reads it daily. The CEO still decides, and Or still publishes and changes budgets by
hand. There is also no Product/Operations/Customer-Experience/Data/Automation office — those
were an older conceptual model. Store operations live in the Shopify Office; orchestration
is the GOD Runtime (not an office).

Do not create a Marketing Office. The daily read living in Analytics is the approved design,
not a gap.

There is also **no Loop Closer office or agent** — market learning after a live campaign is a
*skill* held by `performance-analyst` (data) and `knowledge` (lessons), consumed by the CEO.
