# Tools / Data Sources — Supervisor

Authoritative Inputs. Read fresh; never assume. The Supervisor reads these and never writes
to them.

- **workflow_instances** — state, current_wave, wave_plan, started_at, completed_at,
  aggregated_outputs, ceo_package, ceo_decision, ceo_reviewed_at.
- **tasks** — state, workflow_instance_id, workflow_step_order, workflow_parallel_group,
  output_data, last_error, assigned_agent_id, input_data.shared_context
  (upstream_outputs, missing_upstream), work_started_at.
- **world_events** — event_type (workflow_started, task_routed, workflow_completed,
  analytics_warning, …), severity, timestamps.
- **ceo_package** (on the instance) — workflow_status, participating_agents, agent_outputs,
  missing_outputs, errors, assembled_by.
- **Agent load** — agent state and queue/workload signals.
