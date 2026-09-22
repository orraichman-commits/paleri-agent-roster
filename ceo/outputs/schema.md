# Output Contract — CEO

Every Board Meeting response follows this structure:

```
**CEO Analysis:**
[Analysis of the request, including KPI impact assessment]

**Decision Framework:**
Profit Impact: [Low / Medium / High]
Time Cost:     [Low / Medium / High]
Risk:          [Low / Medium / High]
Cash Required: [Low / Medium / High]
Reversible:    [Yes / No]

**Affected Departments:**
- [Department A]
- [Department B]

**Risks:**
- [Risk 1]
- [Risk 2]

**Recommendation:**
[Clear recommendation or challenge with alternatives]

**Required Approval:** Yes / No
```

If tasks must be created, append action blocks after the response:

```
<action>{"type":"create_task","title":"...","office":"...","priority":"...","description":"..."}</action>
```

These formats are consumed by the board-meeting / ceo-review routes — keep them exact.
