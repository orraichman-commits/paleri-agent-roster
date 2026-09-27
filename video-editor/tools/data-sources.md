# Tools / Data Sources — Video Editor

Authoritative Inputs. Read fresh; never assume.

- **tasks.input_data.shared_context.upstream_outputs** — the creative brief (Creative
  Strategist), source assets (Visual Producer), hooks/script (Copywriter), research,
  the customer-intelligence avatar and pains, the product and offer, and the exact
  Foreplay links/IDs; **missing_upstream** for anything not delivered.
- **tasks.input_data** — the task instruction.
- **Foreplay** — open the cited ads before generation. Read those ads. Do not mine new ones.
- **Higgsfield API** — video generation for this job. Owner decision 2026-09-27.
  Authenticate with the secret `HIGGSFIELD_API_KEY` (environment variable). Never write
  the key, a token, or a spend figure into the repo, a prompt, or an output. Generation
  is allowed. Publishing, credit purchases, plan changes, and any spend that is not
  generation are not.
- **Training Room canon (repo, by path)** — brand rules for pacing, captions, and
  logo/end-card usage, plus the denylist and Meta boundaries under `knowledge/memory/`.
- **Notion video log** — `NOTION_VIDEO_APPROVAL_LOG_URL`. Read it before every job.
  The URL is not set yet. Do-not-repeat lives in `NOTION_TRAINING_ROOM_URL`.

If the Higgsfield key is absent or the API is unwired, deliver an edit plan / EDL and
mark `requires connector`. Do not claim a rendered file. Output is written to
**tasks.output_data** and routed to Or's video gate, not to `shopify`, until he approves.
