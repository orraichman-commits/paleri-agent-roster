# Skill: Competitor-led production — Video Editor

How a video job starts. The Visual Producer uses the same sequence for the images
(`visual-producer/skills/competitor-led-production.md`). Your deliverable is the
short-form video, generated and cut for Meta. You do not publish it, and you do not
wake `shopify` until Or has approved it.

Do not cut a video for a product on `knowledge/memory/niches-to-avoid.md`. Meta policy
in `knowledge/memory/meta-ads-structure.md` still applies. Captions do not add a promise
the copy refused. Hook craft, Hebrew captions, and the format set stay in
`skills/video-editing.md`.

## 1. Collect the inputs

Do not start the cut until these are in the company-group handoff. If one is missing, say so and send the package back. Do not guess it. There is no `tasks` table.

- Product and offer.
- Research (`research-alpha`, `research-beta`).
- Customer-intelligence avatar and pains.
- Creative-strategist angle, hooks, and format mix.
- Copywriter text (script, hooks, on-screen lines).
- Visual Producer assets, each labelled, with the same competitor-ad ref.
- Competitor ad references: the exact **Foreplay** link or ID. An Ads Library URL is
  kept when that was the source, and it does not replace a Foreplay ID that existed
  upstream.

## 2. Read the video log

Read the Notion video log ([NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)) before the job. Also read the
current do-not-repeat list in the Notion Training Room ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)) when
one exists. A reason Or already gave is a constraint on this
cut. An empty log means he has not judged a video yet. It is not permission to skip
the gate on this one.

## 3. Open the competitor ad

Before any generation, open Foreplay and look at the specific ads those links and IDs
point to. Do this yourself. A summary from research, the strategist, or the copywriter
is not a substitute for the video. If the handoff has no Foreplay link or ID, do not
invent one and do not generate. Send the package back to `visual-producer`. If the
only exact ref is an Ads Library URL, watch that URL and flag `Foreplay: none`.

## 4. Cross-check, then resolve

Compare the other agents' information with the competitor video itself:

| Check | Against the video |
|---|---|
| Hook | First 2–3 seconds: does their hook match what the video actually opens on? |
| Structure | Beat order, proof, offer, CTA — as the video plays, not as the brief remembers it. |
| Pacing | Where it holds and where it cuts. |
| Visuals | What is on screen versus the assets you were given. |
| Offer | The offer on screen versus the offer in the copy. |
| Claims | Any line that the video "proves" but we are not allowed to say. |

Flag every contradiction. Resolve it before the cut.

- Build **around** that ad's proven structure. Adapt it to our angle, avatar, copy,
  and brand. Do not paste their claims, their brand, or their footage.
- Our compliant copy and angle win when the competitor's claim would break policy
  or the denylist.
- When the agents disagree about the video, the video decides what the video is.
  Name the contradiction and send the wrong piece back one stage.
- Do not bury a contradiction in captions or music.

## 5. Generate the video

Generate the video this job needs on the Higgsfield API. Authenticate with the secret
`HIGGSFIELD_API_KEY`. Never write the key, a token, or a billing figure into the
repo, the prompt, the captions, or the output.

Generation is allowed. Publishing is not. Buying credits, changing the plan, or any
spend that is not that generation is not. Other paid render tools still need the CEO's
approval. You do not ask Or. Unlicensed music and footage stay forbidden.

The first 3 seconds are the hook. Hebrew captions are RTL and readable on mobile.
Deliver 9:16, 4:5, and 1:1 unless the brief names a smaller set. ABO still groups by
angle / avatar / copy / hook. Do not mix this video into a stills ad set unless the
brief explicitly says scale-stage ASC.

If the API is unwired or the key is absent, deliver an edit plan / EDL and mark
`requires connector`. Do not claim a rendered file.

## 6. The CEO requests Or's gate, then the next agent

A cut that meets the contract goes to the CEO (`paleri os ceo`) for Or's approve or reject. You do not message Or. It does not wake
`shopify`, `marketing`, or Gate 2.

`knowledge` (Notion memory bot) logs the decision and the reason in the Notion video log
([NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)).

- **Approve.** After the CEO relays the approval and `knowledge` has logged it, you wake `shopify`.
- **Reject.** The CEO relays the reason to you and to `visual-producer`. Change the cut.
  Do not resubmit the same video. This is one production-stage send-back. One return
  is a correction. If another stage on this run was already sent back for failing the
  standard, stop and tell the CEO. Do not message Or. The halt stays until Or lifts it through the CEO.

The gate is temporary. Or may later relax it. You do not.
