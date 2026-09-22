---
layer: business
trigger_keywords: experiment, a/b, split test, test small, small test, pilot, validate, hypothesis, ניסוי, טסט, פיילוט, השערה
source: adapted from rampstackco/claude-skills experiment-design (MIT), resized to small-store traffic
wired_mirror: none — loaded on demand by the Brain Loader (keyword-triggered)
---

# Skill: Experimentation — CEO (test-small discipline)

The Owner Preference is lean and reversible; this skill is how a "small test" becomes a real
decision instead of a vibe. The CEO **designs** the test — the Owner runs and funds it (Hard
Limits: no real spend without approval), and with connectors not yet live, real market
evidence only enters through the Owner or commissioned research.

## The hypothesis (four parts, or it is not a test)
"If we [change X], [metric Y] moves by [~Z], because [mechanism]."
Missing magnitude → success is undefined. Missing mechanism → a failure teaches nothing.
Write it down before anything launches.

## Metrics
Exactly **one primary metric**. Two or three guardrails — for PALERI usually contribution
per order, refund rate, CPA (see `unit-economics.md`). A positive primary metric never
overrides a broken guardrail: lifting conversion while refunds double is a loss, not a win.

## Decide the ending before the start
Written before launch: the **scale threshold**, the **kill threshold**, and the **time-box**
(or order/spend budget). Then:
- Judge at the pre-set point — no stopping early on good news (peeking manufactures false
  winners). A kill threshold hit early *is* acted on early; that is what it is for.
- **Inconclusive is a real outcome.** "We learned a lot" without a scale/kill/iterate
  decision is a failed test. Name what the next, sharper test would be.

## Small-store honesty
PALERI's traffic is small; classical A/B significance is mostly out of reach. Therefore:
- Prefer **sequential probes** (one change at a time, before/after with guardrails) over
  split tests that will never reach power.
- Only test changes expected to move the metric a **lot** — small-effect tests are noise at
  this volume.
- Climb the cheapest-probe ladder first: existing evidence (competitor ads, reviews,
  commissioned research) → landing/product-page change → small ad-budget probe → inventory
  or supplier commitment. Never buy an expensive answer a cheap probe could give.
- Never claim statistical rigor a 30-order sample cannot support — say "directional" and
  size the follow-up bet accordingly.

## What NOT to test
Bugs and broken flows (just fix them), legal/VAT compliance, Hard Limits, and anything a
simulation would "answer" — simulated agent output is never presented as test evidence.
