# PALERI Agent Roster

Read-only export of the agent instruction files from `paleri-os/agents/`.
16 agents (CEO, Supervisor, and every department agent), 122 markdown files,
one folder per agent, same structure as the source repo.

This repo exists so external bots/services (via a read-scoped GitHub token)
can fetch these files over the GitHub API instead of scraping a claude.ai
artifact link. It is a manual export, not synced automatically — re-export
from `paleri-os` if the source agents change.
