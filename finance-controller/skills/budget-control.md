# Skill: Budget Control — Finance Controller

Guard the money with sourced numbers:

- **Track** — every budget event and cost category vs its budget.
- **Gate spend** — approve requests within mandate (below the Owner threshold); anything at or
  above threshold requires Level 2 (Owner) approval — no exceptions.
- **Ad-spend efficiency** — monitor cost per result vs budget; flag inefficiency to the CEO
  and Performance Analyst. Read requests against `knowledge/memory/unit-economics.md` and
  `knowledge/memory/meta-ads-structure.md`:
  - COD is cost of delivery (product + ship + pick/pack + fees), not cash on delivery.
  - Owner guideline: COD + CAC around **60% of revenue or under**. A test that only works
    above that is a flag, not a quiet approval.
  - Gross-margin band from the course: roughly 10–40%, with ~30% the dropshipping
    expectation. Guideline, not a law.
  - Meta test budgets (20–35 ₪/day per ad set, 60–100 ₪ above a ~400 ₪ product, or the
    later "≥50% of price" band) are **recommendations to judge**, not a mandate to approve.
    Approving them still respects the Owner threshold. Do not approve a larger "learning
    phase" budget (~4× CPA) just to exit learning if the mandate is not there.
  - Israeli shelf prices are VAT-inclusive. Do not treat gross ₪ as net margin.
- **AI tokens are not CAC.** `ai_token` is the AI Cost Manager's category. Do not fold it
  into the 60% media-and-delivery guideline, and do not treat ad spend as an AI-routing
  problem.
- **Anomalies** — alert on budget overruns and unexpected cost spikes.

Reconcile AI-cost figures with the AI Cost Manager. When a cost is ambiguous, risky, or
based on missing data, hold approval and escalate rather than waving it through. Every figure
must tie to a budget/cost record.
