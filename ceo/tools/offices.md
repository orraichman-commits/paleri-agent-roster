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
- **Doctrine:** research that has not passed through Customer Intelligence is not a complete package; Creative should not build from it.
- **CEO involves it when:** evaluating what to sell, validating a product idea, or preparing the research a launch will be built on.
- **Escalates to CEO when:** a qualified product needs a go/no-go, or research quality is too low to score.

## Creative Office (`creative`) — active
- **Mission:** Transform the Research Package into high-converting creative for Israeli Meta campaigns.
- **Agents:** `creative-strategist` (direction), `copywriter` (the only real-execution agent today), `visual-producer`, `video-editor`.
- **Expected outputs:** Creative briefs, Hebrew copy, visual assets, short-form video — all approval-gated drafts that land in the Artifact Store.
- **CEO involves it when:** a completed Research Package needs creative for launch or testing.
- **Escalates to CEO when:** an angle needs a business call, or a brief would require a prohibited claim.

## Shopify Office (`shopify`) — active
- **Mission:** Run the store layer as drafts; live changes are Owner-gated.
- **Agents:** `shopify-agent`.
- **Expected outputs:** Hebrew product page drafts (approval-gated); store optimization proposals.
- **Escalates to CEO/Owner when:** any live store change (publish, live price, theme) needs Level 4 approval.

## Analytics Office (`analytics`) — active
- **Mission:** Turn data into decision-ready insight and gate viability.
- **Agents:** `market-analyst` (viability scoring/gate), `performance-analyst`, `strategic-intelligence-agent`.
- **Expected outputs:** Viability analyses, performance summaries, intelligence briefs.
- **CEO involves it when:** assessing performance, opportunities, threats, or product viability.
- **Escalates to CEO when:** a KPI deteriorates materially, or intelligence implies a strategic decision.

## Finance Office (`finance`) — active
- **Mission:** Protect PALERI's money and keep spend efficient.
- **Agents:** `finance-controller`, `ai-cost-manager`.
- **Expected outputs:** Financial summaries, spend decisions, AI cost-efficiency reports.
- **Escalates to CEO/Owner when:** spend is at/above threshold, or on overruns/spikes.

## Training Room (`training`) — active
- **Mission:** Be the institutional memory of the company.
- **Agents:** `knowledge` (Knowledge Agent).
- **Expected outputs:** Curated, sourced, confidence-rated knowledge; proposed canonical updates (Owner-approved).
- **CEO involves it when:** it needs prior context, owner preferences, or decision history before deciding.

---

## Locked offices (seeded, no agents, accept no work)

## Publishing Office (`publishing`) — locked
- **Future mission:** The only place assets go live externally (Publisher role — never the creating specialist). Until unlocked, nothing publishes automatically; publishing decisions are CEO→Owner calls executed manually.

## Customer Service (`customer-service`) — locked
- **Future mission:** Support, returns, satisfaction. No agent exists; customer-facing messaging is Owner-gated and manual today.

## Inventory Office (`inventory`) — locked
- **Future mission:** Stock, suppliers, logistics. No agent exists today.

---

## What does NOT exist (do not route work to these)

There is **no Marketing Office** and no Product/Operations/Customer-Experience/Data/Automation
office — those were an older conceptual model. Campaign/audience strategy is currently CEO
work informed by `research-beta` + Analytics; store operations live in the Shopify Office;
orchestration is the GOD Runtime (not an office).
