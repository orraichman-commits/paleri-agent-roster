# Output Contract — Customer Intelligence Agent

The Customer Intelligence Brief. **Priority-ordered by design**: downstream context is
byte-capped (see `_shared/contextAssembly.ts` — 4000 bytes per upstream output), so the
sections are ordered most-load-bearing first. If truncation cuts the tail, the head must
still be executable.

```
## Customer Intelligence Brief — <product/campaign> — <timestamp>

### CORE (self-sufficient if the rest is truncated)
Primary avatar: <one dense paragraph — who, life context, identity pain, desired
  after-state, dominant motivation>
Awareness level: <level> → <messaging implication in one line>
Primary angle: <#1 ranked angle — segment × driver × why it should win>
Top objection: <the kill-power #1 objection> → <neutralizer or "no neutralizer — flag">
Voice of customer: "<verbatim Hebrew phrase for the pain>" / "<phrase for the wish>"

### SEGMENTS
  - <segment name>: <distinguishing trait> | awareness: <level> | represented by: <avatar>
    (only segments that change the message)

### PAIN → OUTCOME → OBJECTION (per segment)
  - Pain: <ranked, surface vs identity> → Outcome: <functional + emotional, customer words>
    → Objections: <ranked by kill-power, each with neutralizer or gap-flag>

### MOTIVATIONS & PSYCHOLOGY
Dominant drivers: <top 2–3, ranked> | Decision mode: <impulse | considered> → <implication>

### MESSAGING ANGLES (ranked, 3–5)
  - Angle <n>: <hypothesis> | segment: <s> | awareness: <level> | driver: <d>
    | evidence: <source> | falsified by: <signal to watch>

### POSITIONING
For <segment>, <product> is the <frame> that <differentiated outcome>,
unlike <current alternative>. Survives strongest competitor claim: <yes | no — detail>

### OFFER ANGLES (options with trade-offs — framing only, pricing is CEO/owner)
  - <option>: <psychology fit> | trade-off: <cost/risk>

### EVIDENCE & CONFIDENCE
Sources: <upstream steps / Training Room items used>
Assumptions: <each labelled, with confidence>
Blind spots: <missing_upstream, unavailable connectors, unanswered questions>
Confidence: <high | medium | low>

Handoff: completes the Research Package → Creative Office
  (Creative Strategist for angle selection → Copywriter / Visual Producer / Video Editor)
Status: draft → review → downstream consumption
```

Rules:
- The CORE section is mandatory and complete on its own.
- No copy, no hooks, no headlines, no creative direction — angles are hypotheses.
- Hebrew voice-of-customer phrases verbatim.
- Every claim: source or labelled assumption.
