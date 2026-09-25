# Skill: System Monitoring — Supervisor

Detailed detection criteria for each responsibility.

## 1. Workflow health
- Instances stuck in `running` past expected duration (stale `started_at`, no recent events).
- Instances that never reached `completed` / `failed` (orphaned or hung).
- A wave that fanned out but never fanned in: `current_wave` not advancing while the wave's
  tasks are already terminal (fan-in barrier not releasing).
- Repeated failures/retries on the same step or workflow.

## 2. Agent coordination
- Every handoff: did it complete, did the output meet the receiving contract, how many
  stages have sent work back for a standard failure.
- A stage with no output for **2 hours**: one nudge, then an alert to the CEO (who
  updates Or). LIO waiting on the supplier is excluded from this clock.
- Stop rule: standard-failure send-backs at **2 or more stages** → halt all routines,
  confirm temporary routines have stopped (LIO's 15-minute supplier check), wait for Or.
- Agents dispatched but never started, or that never reported back.
- Agents idle while work is queued, or one agent overloaded while others sit idle.
- Handoffs between waves that did not actually transfer the expected work.

## 3. Shared-context correctness
- Steps that declared `consumes` but received nothing (unexpected `missing_upstream`).
- Unused context: an agent given upstream outputs whose result ignores them (disconnected
  work — output that does not build on what it consumed).
- Context that arrived empty when the `wave_plan` implies it should have been populated.

## 4. Output integrity
- Missing outputs: tasks marked `completed` with empty/absent `output_data`, or a non-empty
  `ceo_package.missing_outputs`.
- Disconnected work: output unrelated to its task or its declared upstream inputs.
- Low-quality / irrelevant outputs: off-topic, generic filler, or clearly non-responsive
  output — flagged on operational relevance/coherence only, never business merit.
- Stalled agents: tasks in `in_progress` with an old `work_started_at` and no progress.

## 5. CEO package delivery
- On workflow completion, verify the CEO actually received the technical package:
  `state = 'completed'` MUST carry a non-null `ceo_package`.
- Detect a CEO asked to decide without a package, or a package missing required steps'
  outputs (`missing_outputs` populated). A blind business brain is a critical incident.
