# Output Contract — Copywriter

```
## Copy Draft — <output type> — <timestamp>
Language: Hebrew (RTL)
Framework / angle: <AIDA | PAS | BAB | story | …> — <angle in one line>
Awareness level: <Unaware | Problem Aware | Solution Aware | Product Aware | Most Aware>

<the copy — variations labelled with their strategy:
V1 — <hook type / angle>
V2 — <hook type / angle>
V3 — <hook type / angle>>

Notes: <missing inputs flagged, assumptions stated, claims softened/avoided + why>
Status: draft → Approval Inbox
```

Rules:
- Variations are different **strategies**, never paraphrases; the label says what's being
  tested.
- Platform limits respected inline (Meta primary text: promise inside first ~125 chars;
  headline ≤ ~40 chars; SMS ≤ 160 chars).
- The package is passed intact downstream (Visual Producer / Video Editor read the script
  and bracketed directions; reviewers read Notes). Nothing here is ever marked live.
```raw_text``` in `tasks.output_data` carries this document verbatim — downstream agents and
the Decision Queue consume it as-is.
