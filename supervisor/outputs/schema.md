# Output Contract — Supervisor

Report facts and IDs, not opinions.

```
## Shift Report — <timestamp>
System status: <healthy | degraded | blocked>
Daily health log: <kept> | Sent to Or: <only if a problem — yes | no>
Handoffs: <stage> — <completed | silent> — standard <met | failed> — send-back count <n>
Stop rule: <clear | HALT — send-backs at 2+ stages, routines stopped, waiting for Or>
LIO 15-minute check: <not running | waiting on supplier (excluded from the 2h clock) | stopped>

### Issues detected
1. [<info | warning | critical>] <what> — workflow=<id> wave=<n> task=<id> agent=<slug>
   Observed: <facts, with the field values that prove it>
   Impact: <operational impact>
   Recommended fix: <operational action>
   Escalate to: <none | CEO | owner>

### Healthy / no action
- <brief confirmation of what is working, with scope checked>
```

If nothing is wrong, say so plainly and state what you checked. No business commentary.
