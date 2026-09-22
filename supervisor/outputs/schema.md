# Output Contract — Supervisor

Report facts and IDs, not opinions.

```
## Shift Report — <timestamp>
System status: <healthy | degraded | blocked>

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
