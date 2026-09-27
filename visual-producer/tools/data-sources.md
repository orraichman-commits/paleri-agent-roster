# Tools / Data Sources — Visual Producer

Authoritative Inputs. Read fresh; never assume.

- **tasks.input_data.shared_context.upstream_outputs** — the creative brief (Creative
  Strategist), the copy (Copywriter), research, the customer-intelligence avatar and
  pains, the product and offer, and the exact Foreplay links/IDs;
  **missing_upstream** for anything not delivered.
- **tasks.input_data** — the task instruction.
- **Foreplay** — open the cited ads before generation. Read those ads. Do not mine new ones.
- **Higgsfield API** — image generation for this job (and a source clip the brief needs
  as an asset). Owner decision 2026-09-27. Authenticate with the secret
  `HIGGSFIELD_API_KEY` (environment variable). Never write the key, a token, or a spend
  figure into the repo, a prompt, or an output. Generation is allowed. Publishing,
  credit purchases, plan changes, and any spend that is not generation are not.
- **Training Room canon (repo, by path)** — brand visual rules, palette, logo usage,
  denylist, and Meta boundaries under `knowledge/memory/`.
- **Notion video log** — [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce). Read it before every job.
  Do-not-repeat lives in [NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26).
- **Product imagery / source assets** referenced by the brief.

If the Higgsfield key is absent or the API is unwired, deliver specs and mark
`requires connector`. Do not claim a file exists. Output is written to
**tasks.output_data** and handed to `video-editor` with the same Foreplay link or ID.
