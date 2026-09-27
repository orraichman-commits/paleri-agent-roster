# Skill: System Monitoring — Supervisor

Detailed detection criteria for each responsibility.

## 1. Workflow health
There is no workflow table. Watch the company group and the task board (read only).
- A handoff that was announced and then went quiet past the time the funnel allows.
- Work that was started in the group and never closed with an output or an explicit stop.
- Parallel work (research-alpha, research-beta, customer-intelligence) where one voice never came back.
- The same stage failing and being sent back again.

## 2. Agent coordination
- Every handoff: did it complete, did the output meet the receiving contract, how many
  stages have sent work back for a standard failure.
- A stage with no output for **2 hours**: one nudge, then an alert to the CEO (who
  updates Or). LIO waiting on the supplier is excluded from this clock.
- Stop rule: standard-failure send-backs at **2 or more stages** → halt all routines,
  confirm temporary routines have stopped (LIO's 15-minute supplier check), tell the CEO. Do not message Or.
- Agents dispatched but never started, or that never reported back.
- Agents idle while work is queued, or one agent overloaded while others sit idle.
- Handoffs between waves that did not actually transfer the expected work.

## 3. Shared-context correctness
- An agent who says a named upstream input never arrived.
- Output that ignores the upstream post it was given (disconnected work).
- A handoff that names an input the previous agent did not actually post.

## 4. Output integrity
- An agent who claims to be done and posts nothing.
- Output unrelated to the task or the upstream inputs.
- Off-topic or generic filler — flag operational relevance only, never business merit.
- An agent who said they started and then went silent. Evidence is the message and the time, not a row.

## 5. What the CEO received
- When a stage that reports to the CEO finishes, check that `paleri os ceo` was actually given the output in the group or by DM.
- A CEO asked to decide without that output is a critical incident. There is no `ceo_package`.
