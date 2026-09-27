# Skill: Competitor-led production — Visual Producer

How a visual job starts. The Video Editor uses the same sequence for the cut
(`video-editor/skills/competitor-led-production.md`). Your deliverable is the
images and source visuals, generated on Higgsfield. You do not publish them.

Do not generate for a product on `knowledge/memory/niches-to-avoid.md`. A competitor
ad that already runs is not a waiver. Meta policy in `knowledge/memory/meta-ads-structure.md`
still applies: no before/after body, no medical result, no personal-attribute call-out,
no claim the Copywriter refused.

## 1. Collect the inputs

Do not open a generation until these are in `upstream_outputs`. If one is missing,
flag `missing_upstream` and send the package back. Do not guess it.

- Product and offer.
- Research (`research-alpha`, `research-beta`).
- Customer-intelligence avatar and pains.
- Creative-strategist angle, hooks, and format mix.
- Copywriter text (what will be on the image or spoken later).
- Competitor ad references: the exact **Foreplay** link or ID each earlier agent
  used. An Ads Library URL is kept when that was the source, and it does not
  replace a Foreplay ID that existed upstream.

## 2. Read the video log

Read the Notion video log ([NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)) before the job. Also read the
current do-not-repeat list in the Notion Training Room ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)) when
one exists. A reason Or already gave is a constraint on this
job. An empty log is not a free hand — it only means he has not judged a video yet.

## 3. Open the competitor ad

Before any generation, open Foreplay and look at the specific ads those links and IDs
point to. The written summary is not a substitute for the ad. If the handoff has no
Foreplay link or ID, do not invent one and do not generate. Send the package back to
`copywriter` (the stage that handed it to you). If they only have an Ads Library URL,
use that exact URL for the cross-check and flag `Foreplay: none` on the asset.

## 4. Cross-check, then resolve

Compare what the other agents wrote with the ad itself:

| Check | Against the ad |
|---|---|
| Hook | Does their hook match the opening the ad actually uses? |
| Structure | Does the beat order they described match the video? |
| Pacing | Does the length and speed they assumed match what plays? |
| Visuals | Is the product-in-action / problem / emotion actually there? |
| Offer | Is the offer they named the offer on screen? |
| Claims | Did anyone import a claim the ad makes that we cannot say? |

Flag every contradiction. Resolve it before generation.

- Our angle, avatar, and compliant copy win over the competitor's claim.
- The competitor's **structure** is the skeleton you adapt. It is not permission to
  copy a prohibited claim, a denylisted promise, or a brand name.
- If the agents disagree with each other about the ad, the ad decides what the ad is.
  Send the wrong description back one stage with the contradiction named.
- Do not generate "and fix it in the edit."

## 5. Build the visuals on that structure

Generate what this job needs on the Higgsfield API. Authenticate with the secret
`HIGGSFIELD_API_KEY`. Never write the key, a token, or a billing figure into the
repo, the prompt, or the output.

Generation of images (and a source clip the brief needs as an asset) is allowed.
Publishing is not. Buying credits, changing the plan, or any spend that is not
that generation is not. Other paid tools still need Level 1 approval.

Adapt the competitor's structure to our angle, avatar, copy, and brand. The first
frame is the hook (product in action, the problem, or the emotion). A logo card is
not a hook. Label every file by format (9:16, 4:5, 1:1) and placement. Pass the
same Foreplay link or ID downstream so the Video Editor opens the same ad.

ABO still groups by angle / avatar / copy / hook (`knowledge/memory/meta-ads-structure.md`).
Do not mix stills and video in one ad set unless the brief explicitly says scale-stage ASC.

If the API is unwired or the key is absent, deliver specs and mark
`requires connector`. Do not claim a file exists.

## 6. After Or rejects a video

A rejection in the log names you and `video-editor`. Read the reason, change the
visuals that caused it, and do not resubmit the same picture with a new filename.
That return is one production-stage correction. If another stage on this run was
already sent back for failing the standard, stop and wait for Or.
