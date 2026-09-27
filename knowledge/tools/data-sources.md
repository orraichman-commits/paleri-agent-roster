# Tools / Data Sources — Knowledge Agent

Authoritative Inputs. Read fresh; never assume. The role is held by Notion memory bot
(also called Notion Manager). It reads these and drafts proposed changes. It does not
commit canon itself.

## Repo canon (read by path; write only by PR)

Agents read these files by path. They are the authoritative canon. Notion memory bot
does not edit them in place. After Or approves a proposal in the Notion proposals inbox,
the only repo write is a pull request that carries that approved text. Direct commits to
these files are forbidden.

- `memory/niches-to-avoid.md`
- `memory/product-criteria.md`
- `memory/meta-ads-structure.md`
- `memory/unit-economics.md`
- `memory/funnels.md`
- Instruction packs, `skills/`, and `permissions/` across the roster — same rule. An
  approved change to a pack is a PR. It is not a Notion edit.

## Notion Training Room (living layer — source and destination)

Placeholder `NOTION_TRAINING_ROOM_URL`. The URL is not set yet. This is where living
knowledge is written and where it is read back.

Write here, and read here before answering from memory:

- Loop Closer lessons and the do-not-repeat list
- Decision memory
- Product and campaign history
- The proposals inbox (inside the Training Room), where Or approves or rejects a
  proposed rule. An approval there is what authorizes the canon PR. A rejection stays
  in the inbox. It does not become a repo edit.
- A **read-only mirror** of the repo canon, regenerated from the repo after each merge.
  Destination for the mirror refresh only. Never a source you hand-edit. If the mirror
  and a repo file disagree, the repo file wins, and the next refresh must copy the repo.

Video approve/reject log: placeholder `NOTION_VIDEO_APPROVAL_LOG_URL` (URL not set yet).
Append Or's decision and his reason there. Creative reads that page before every job.
Do not store `HIGGSFIELD_API_KEY` or any other secret in an entry.

The task board Notion memory bot coordinates is not this source and not this destination.
Do not read a card as a knowledge fact, and do not write knowledge into a card.

## Other inputs

- **workflow_instances** — `ceo_package`, `ceo_decision`, `ceo_reviewed_at`,
  `aggregated_outputs`, `state` (to link decisions to the work that produced them).
- **tasks** — `output_data` (agent results that became knowledge), `workflow_step_order`,
  `input_data.shared_context`.
- **world_events** — decision, approval, rejection, and outcome events with timestamps.
- **Owner feedback** surfaced via Board Meeting / Approval Inbox outcomes, including
  approve/reject on a generated video (decision and reason, for the Notion video log).
- **Post-Launch Performance Pack** (Performance Analyst) — the live campaign evidence the Loop
  Closer runs on: Meta/Shopify figures, what went live, attribution linkage, blind spots. You
  consume this pack; you never query Meta or Shopify yourself. The lessons you write from it
  go to Notion, not into a canon file.
- **AI Cost Manager report** — the AI/token cost of a creative round, when available, so a
  lesson can carry what it cost to learn.
- **content_assets** — the artifacts that actually ran (what was live is a fact about the
  artifacts, not a memory).
