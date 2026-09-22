# CEO Skills

This folder holds the CEO's on-demand know-how, loaded by the **Brain Loader**
(`src/lib/ceo/prompt.ts` → `loadCeoBrain`). Composition is deterministic:

- **always loaded:** `../instructions.md`, `../memory/owner-preferences.md`,
  `../memory/kpis.md`, `../outputs/schema.md`
- **per call context:** board_meeting → decision-framework, operating-procedure, delegation;
  package_review → decision-framework, package-review
- **keyword-triggered:** any other skill whose `trigger_keywords` frontmatter matches the
  owner's message (e.g. unit-economics on pricing/margin talk)

`agents/instructions/ceo-agent.md` remains only as the **fallback brain** if the modular
tree fails to load.

## Frontmatter convention (every skill file)

```yaml
---
layer: thinking | operating | executive | business
trigger_keywords: comma, separated, terms (empty = context-selected only)
source: provenance when adapted from an external repo (name + license) — omit for original skills
wired_mirror: where (if anywhere) a compressed copy lives
---
```

Keyword rules: the loader substring-matches lowercased keywords against the owner's message —
keywords must not contain `:` and must be checked against common-word collisions in **both**
languages before shipping (e.g. bare `סדר` matches `בסדר`, bare `test` matches `latest`,
bare `ספק` means both "supplier" and "doubt").

## Current skills

| Skill | Layer | Loaded |
|---|---|---|
| `decision-framework.md` | thinking | both contexts (always-selected) |
| `operating-procedure.md` | operating | board_meeting (includes operating rhythm + executive communication) |
| `package-review.md` | operating | package_review |
| `delegation.md` | executive | board_meeting |
| `unit-economics.md` | business | keyword-triggered (pricing/margin/ROAS/CPA terms) |
| `prioritization.md` | executive | keyword-triggered (priorities/sequencing/focus terms) |
| `strategic-review.md` | business | keyword-triggered (strategy/quarterly/direction terms) |
| `decision-quality.md` | thinking | keyword-triggered (risk/irreversible/pre-mortem terms) |
| `experimentation.md` | business | keyword-triggered (experiment/pilot/validate terms) |
| `negotiation.md` | business | keyword-triggered (negotiation/supplier/terms terms) |

External adaptations (each rewritten for PALERI, never copied verbatim; provenance in the
file's `source:` frontmatter): `prioritization.md` and `strategic-review.md` from a CEO
advisor skeleton; `decision-quality.md` from tjboudreaux/cc-thinking-skills (MIT);
`experimentation.md` from rampstackco/claude-skills (MIT); `negotiation.md` from
wondelai/skills (MIT). Corporate material (fundraising, boards, M&A, HR, culture programs,
live-conversation scripts) was deliberately not adapted.

## Division of labor between overlapping skills
- `decision-framework.md` rates decisions (five factors); `decision-quality.md` stress-tests
  the consequential ones (doors, second-order, pre-mortem) — it references, never repeats,
  the factors.
- `strategic-review.md` keeps the standing risk register for a *direction*;
  `decision-quality.md` pre-mortems a *single decision*.
- `experimentation.md` designs the small test that `decision-framework.md`'s "prefer
  reversible" bias keeps recommending.

## Reserved — future skills (content not written; do not invent)
- `capital-allocation.md` — where to invest budget/effort (blocked until real spend data exists).
- `product-launch.md` — the launch decision playbook (blocked until connectors are live).
