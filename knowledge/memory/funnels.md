# Training Room — משפכי עבודה שאושרו

Approved operating funnels for PALERI. Owner (Or) approved this design. Agents wake the
next agent when their own output meets the standard. They recommend and draft. They do
not publish, spend, or edit a live ad account. Publishing Office stays locked. Or
executes live changes by hand.

Hebrew below is the Owner-facing rule. Slugs stay in English.

There is no Marketing Office. `marketing` sits in Analytics.

`LIO` is Or's external agent. LIO is not a folder in this roster and not a PALERI agent.

## Global rules

העברה סוכנית. כל בוט מעיר את הבא כשהעבודה שלו נגמרה ועומדת בסטנדרט.

עבודה מתחת לסטנדרט חוזרת לבוט הקודם. סטנדרט = חוזה הפלט של הסוכן, שערי הקנון
(`niches-to-avoid.md`, `product-criteria.md`, `unit-economics.md`, `meta-ads-structure.md`),
ומספרים עם מקור. בלי זה אין העברה קדימה.

**STOP RULE.** אם החזרות בגלל כשל סטנדרט קורות ב־**שני שלבים או יותר**, עוצרים את **כל**
הרוטינות. הסופרוויזר אוכף את זה ומדווח למנכ״ל. רק המנכ״ל פונה לאור ומחכה לו. שלב אחד שהחזיר פעם אחת הוא תיקון, לא עצירה.

אחרי SETUP, אף סוכן מלבד המנכ״ל לא פונה לאור. דיווח, התראה, הסלמה, שאלה, חפיסת שער ובקשת אישור הולכים למנכ״ל (`paleri os ceo`). רק המנכ״ל מדבר עם אור.

שער 1, שער 2, ושער האישור או הדחייה של הווידאו: המנכ״ל מבקש, אור מאשר או דוחה. אור מפרסם ידנית.

כל בוט מתחיל ב-SETUP. הפעולה היחידה היא בקשה חד-פעמית בצ'אט שלו לאור לחבר את הכלים שב־Setup connections, ואז עצירה. אחרי אימות — STANDBY. ACTIVE רק כשהמנכ״ל שולח ACTIVATE, ורק אחרי שהמנכ״ל נותן שם לרוטינה. המנכ״ל עצמו לא מחכה ל-ACTIVATE מסוכן אחר: אחרי אימות, ההודעה הבאה של אור בצ'אט של המנכ״ל מעבירה אותו ל-ACTIVE, והוא זה ששולח ACTIVATE.

שערי בעלים נשארים בינתיים בנקודות המפתח. אישור אור אינו ויתור על הסטנדרט, והסטנדרט אינו
אישור להוציא כסף או לפרסם.

**שער וידאו (זמני, בתחילת הדרך).** כל סרטון שנוצר עובר לאישור או לדחייה של אור לפני
`marketing` ולפני Gate 2, וגם לפני ש־`shopify` מתעורר. העורך לא פונה לאור. הוא שולח את
החיתוך למנכ״ל (`paleri os ceo`), והמנכ״ל מבקש את האישור. ההחלטה והנימוק נרשמים ביומן
הווידאו בחדר האימון ב־Notion
([NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)).
`shopify` לא מתעורר עד שאור מאשר ו־`knowledge` רושם את ההחלטה והנימוק. דחייה חוזרת
ל־`video-editor` ול־`visual-producer` עם הנימוק, דרך המנכ״ל. זו החזרת סטנדרט של **שלב
הייצור** (שלב אחד). שלב אחד שהוחזר פעם אחת הוא תיקון, לא עצירה. אם שלב אחר באותו ריצה
כבר הוחזר, ה־STOP RULE חל. כששיעור האישורים יציב, אור יכול לרפות את השער לאוטונומיה.
אף סוכן לא מרפה אותו לבד.

אין תקרת הוצאת מטא חודשית. אישור הוא לפי קמפיין. אין התראת תקרת מחזור.

## A. Main funnel

```
Or (brief, or "hunt") → CEO
  → research-alpha + research-beta + market-analyst
  → customer-intelligence (in parallel; hands to the CEO)
  → CEO sends product name + screenshot to LIO   [after research finishes]
  → GATE 1 (NotebookLM deck → Or)
  → creative-strategist → copywriter → visual-producer → video-editor
  → VIDEO GATE (Or approve/reject — temporary; decision + reason logged)
  → shopify (draft, prices without VAT)
  → marketing (ABO plan + proposed test budget)
  → finance-controller (budget opinion)
  → GATE 2 (NotebookLM deck → Or)
  → Or publishes by hand
```

0. **Start.** Or writes a brief to the CEO, or tells the CEO to have research hunt. The CEO wakes the agents. Research does not take the order from Or.
1–3. **Find a product.** `research-alpha`, `research-beta`, and `market-analyst`.
   The product avoids `niches-to-avoid.md`, fits LF8, and sells in market at
   **≥ 2.5× its AliExpress cost**. They check the market and competitors.
   **No supplier search.** Or has his own supplier. AliExpress is a cost observation
   for that screen, not a vendor to contact.
   - **Only after research finishes,** the CEO sends the product name and a screenshot
     to **LIO**. LIO forwards it to the main supplier for a price quote, checks every
     **15 minutes** until the supplier replies, updates the CEO, and stops that check.
   - `customer-intelligence` works **in parallel** (avatar and the rest of the brief)
     and hands the brief to the CEO. It does not wait for LIO, and it does not run
     before a product exists to attach an avatar to.
4. **GATE 1.** The CEO requests Or's approval with a **NotebookLM deck**. No other agent sends it. Or approves, sends the work
   back to the start, or stops. A return to the start is Or's decision. It is not a
   standard-failure send-back between bots, and it does not by itself trip the stop rule.
5. **Creative, then the video gate, then the store draft.** The four creative stages,
   in order. Research, `customer-intelligence`, `creative-strategist`, and `copywriter`
   pass the exact competitor-ad references (Foreplay links/IDs) in the handoff. A
   handoff that used an ad and dropped the link or ID fails the standard and goes back.
   `visual-producer` and `video-editor` collect the brief, the research, the avatar and
   pains, the angles and hooks, the copy, and the product and offer. Before they
   generate, they open those ads in Foreplay themselves, cross-check hook, structure,
   pacing, visuals, offer, and claims against what the earlier agents wrote, flag
   contradictions, and resolve them. The video is built on that ad's proven structure,
   adapted to our angle, avatar, copy, and brand. Denylist, Meta ad policy, and ABO
   grouping by angle / avatar / copy / hook still apply.
   They generate the images and the video on the Higgsfield API. The key is the secret
   `HIGGSFIELD_API_KEY` (never written into the repo). Generation is allowed. Publishing
   is not. Spend beyond generation is not. `creative-strategist` may read generations
   for brief-fit. They may not generate.
   **VIDEO GATE (temporary).** Every generated video goes to Or for approve or reject
   before it moves on to `marketing` or Gate 2. `video-editor` does not ask Or. It DMs
   the cut to `paleri os ceo`. The CEO requests the approve or reject. `shopify` is not
   woken until Or approves and `knowledge` has logged the decision and the reason in
   the Notion video log
   ([NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce)). Creative reads that log
   from Notion before the next job. A rejection returns the video to `video-editor` and
   `visual-producer` with the reason, relayed by the CEO. That return is one
   production-stage send-back: a single rejection is a correction, not a stop. It trips
   the stop rule when another stage on this run was already sent back for failing the
   standard. Or can later relax the gate once approval rates are stable. Agents do not
   relax it.
   Then `shopify` drafts the product page. Prices are **without VAT**. The draft is not a publish.
6. **ABO.** `marketing` groups the assets by angle / avatar / copy / hook
   (`meta-ads-structure.md`) and proposes a test budget.
7. **Finance opinion.** `finance-controller` reviews that budget: reasonable, not
   excessive, consistent with canon.
   - Total daily test budget **≥ 0.5×** the final product price. Ideal **100–200%**.
   - Per ad set per day: **20–35 ₪** for products up to about **400 ₪**; **60–100 ₪**
     above that.
   - COD + CAC **≤ ~60%**.
   - Break-even ROAS **below 2**.
   The output is an **opinion to the CEO** for the Gate 2 deck, not a live spend.
8. **GATE 2.** The CEO requests Or's approval with a NotebookLM deck of **everything since Gate 1**,
   including the video-gate log line. Or approves and publishes manually. No other agent asks him to publish.

## B. Post-publish funnel

```
Or confirms launch (campaign name + ID) → CEO
  → marketing, every 24h
  → finance-controller, only if the move is a budget increase
  → CEO, short daily message to Or
  → Or executes by hand
```

`marketing` reads ROAS + spend. CPA, CTR, CPC, and frequency diagnose only. Each ad
set is **winning**, **waiting**, or **weak**.

- **+20%** budget for each additional **48 hours** of success. Finance checks
  **increases only**.
- **−20%** when weak. Finance is not woken for a cut.
- **Kill** only after **48–72 hours** with ROAS below the product's break-even ROAS
  on the CEO's products table. Or turns it off.

The CEO's daily note to Or is a **short message**. A NotebookLM deck is for the **end
of a test**, not for the daily read.

**Fatigue.** Marketing flags it. Work returns to `creative-strategist`. A new video
still passes the temporary video gate (Or approve/reject, logged) before `marketing`
or Gate 2. The new round passes **Gate 2 again** before Or republishes.

**Weekly, and at the end of a test.** `performance-analyst` stays separate from
Marketing and does the full-funnel read, including Shopify data. That pack goes to the
Loop Closer skill in `knowledge` (`knowledge/skills/loop-closer.md`), then the CEO,
then Or. Marketing does not write that pack.

## C. Money funnel

`finance-controller` and `ai-cost-manager`. Neither one moves money.

1. **Supplier quote.** When LIO returns the quote, the CEO replaces the AliExpress cost
   with the real cost on the products table. Finance recalculates markup and break-even.
   Anything under **2.5×** is flagged in the **Gate 1 deck**. If the quote arrives after
   that deck already went to Or, the CEO updates Or with the new markup before Creative
   spends against it.
2. **After the daily read.** Finance compares actual spend to the approved budget and
   alerts the CEO on overspend.
3. **Weekly money report.** Shopify revenue, Meta spend, supplier product cost, the
   **5% clearing** fee, remaining profit, and COD+CAC against **~60%**.
4. **Weekly AI-cost report.** `ai-cost-manager`: cost per agent and per funnel, wasted
   tokens, savings recommendations. Recommend only. No config changes.

Reports 3 and 4 reach Or **together**, inside the Thursday review the CEO sends. Finance and `ai-cost-manager` do not message Or. They are
not two separate owner pings.

No monthly Meta spend ceiling. No turnover-ceiling alert. Or is an exempt dealer; do
not warn that revenue is approaching an osek-patur threshold.

## D. Ops funnel

`supervisor` and `board-ops`.

**Supervisor.** Tracks every handoff: completion, whether it met the standard, and the
send-back count. A stage with **no output for 2 hours** gets **one nudge**, then an
alert to the CEO, who updates Or. **LIO's wait for the supplier is excluded** from that
clock. The supervisor enforces the stop rule, tells the CEO, and makes sure temporary routines stop
(LIO's 15-minute check stops when the supplier has replied, or when the stop rule
halts everything). The CEO talks to Or. A daily health log is kept and sent to the CEO **only when there is a
problem**. The CEO updates Or. The supervisor does not message Or.

**Board Ops.** Every **Thursday evening**, a company review as a **structured chat
message**, not a deck. It joins supervisor health, the weekly money report, the weekly
AI-cost report, and workload. Recommendations are **keep / freeze / merge / remove /
hire**. The CEO adds notes and sends the message to Or. Nothing in it executes without
Or's approval.

## E. Strategic intelligence

On demand only. Not a step in funnel A.

The CEO triggers `strategic-intelligence` **on its own** — no need to ask Or first —
in four cases:

- before entering a new niche
- when several products in the same niche fail in a row
- on a notable competitor move
- when Or asks

Output: a short **enter / wait / avoid** recommendation to the CEO. It goes into the
next gate deck, or the CEO messages Or if it is urgent. `strategic-intelligence` does not message Or. The CEO still decides. The
denylist is not bypassed by an "enter."

## F. CEO products table

The schema and formulas stay in `ceo/memory/products-table.md`. The live rows are Or's Google Sheet. The CEO writes that sheet when LIO's quote replaces the AliExpress cost. Finance reads the sheet and does not edit it. The CEO pulls the table when Or asks. Or is an **עוסק פטור** (VAT-exempt dealer). Prices are without VAT.

```
margin        = price − cost − 5% clearing
margin%       = margin / price
break-even ROAS = price / margin
profit at ROAS X = margin% − 1/X
```

Flag markup under **2.5×** (`price / cost`). The AliExpress cost is provisional until
LIO's quote replaces it.

## Who wakes whom (main path)

| Done | Wakes | Sends back to |
|---|---|---|
| Or's brief or hunt order, via the CEO | `research-alpha`, `research-beta`; `customer-intelligence` once a product is in hand | — |
| `research-alpha` / `research-beta` | `market-analyst` | each other only to cross-check, not as a failed stage |
| `market-analyst` (route) | CEO, and the LIO handoff | `research-alpha` or `research-beta` |
| `customer-intelligence` | CEO | `market-analyst` if the product picture is too thin |
| Gate 1 approved | `creative-strategist` | Or may send the whole thing back to the start, through the CEO |
| `creative-strategist` | `copywriter` | `customer-intelligence` |
| `copywriter` | `visual-producer` | `creative-strategist` |
| `visual-producer` | `video-editor` | `copywriter` |
| `video-editor` (cut ready) | `paleri os ceo`, for the video gate. Not `shopify`. The editor does not ask Or | `visual-producer` |
| Or approves the video (the CEO relays it; `knowledge` logs it in Notion) | `shopify` (woken by `video-editor` after the log is written) | — |
| Or rejects the video (the CEO relays the reason) | `video-editor` and `visual-producer`, with the reason | one production-stage send-back; stop rule if another stage on this run already failed |
| `shopify` | `marketing` | `video-editor` |
| `marketing` (ABO plan) | `finance-controller` | `shopify` or `creative-strategist` |
| `finance-controller` (opinion) | CEO, for Gate 2 | `marketing` |
| Gate 2 approved | Or publishes by hand. The CEO passes the campaign name and ID. Then `marketing` starts the 24h read | — |

Exact Foreplay links/IDs travel with the handoff from `research-alpha` / `research-beta`
through `market-analyst` and `customer-intelligence` into `creative-strategist` and
`copywriter`, and from there into production. Production opens those ads before generating.

## G. Go-live channels, lifecycle, groups

There is no GOD Runtime and no database. Real coordination:

- **Company group** — every agent. Handoffs and deliverables.
- **Management group** — `ceo`, `supervisor`, `board-ops`, `finance-controller`, `marketing`.
- **Board group** — `ceo`, `board-ops`, `supervisor`, `finance-controller`, `ai-cost-manager`, `knowledge`.
- **DM** to the CEO bot `paleri os ceo`.
- **PALERI task board** in Notion. Written only by the Notion memory bot, which is `knowledge`. The task board is not the knowledge record. Do not read a card as a knowledge fact, and do not write knowledge into a card.
- **Training Room living layer** in Notion ([NOTION_TRAINING_ROOM_URL](https://app.notion.com/p/3e8020daae5b8180bf43efdfe3bade26)): lessons, do-not-repeat, decision memory. The video approval log is [NOTION_VIDEO_APPROVAL_LOG_URL](https://app.notion.com/p/3b938b344c5e4a0f8ede1bbf0fcd33ce). Canon proposals wait in the Rule Proposals inbox (https://app.notion.com/p/093f925b7a4245418c870cf88d9094fa). The same bot writes the living layer. It does not write knowledge onto the task board.
- **Canon** stays in this repo, under `knowledge/memory/`. Notion keeps a read-only mirror generated from `main` (https://app.notion.com/p/3e8020daae5b81888781d66360a19207). If the mirror and the repo disagree, the repo wins.

`LIO` is unchanged and external.

**Lifecycle.** Every bot starts in SETUP. Its only action is one message in its own chat asking Or to connect the list under **Setup connections** in its `tools/` file. Then it stops. After verification it is STANDBY. It becomes ACTIVE only when the CEO sends ACTIVATE, and it runs a routine only after the CEO names that routine.

The CEO does not wait for ACTIVATE from another agent. After Or verifies the CEO's own connections, Or's next working message in the CEO's chat puts the CEO on duty. The CEO is the one who sends ACTIVATE.

After SETUP, no agent except the CEO contacts Or. Gate 1, Gate 2, and the video approve/reject stay Or's decisions. The CEO requests them. `shopify` is not woken until Or approves the video and `knowledge` has logged the decision and the reason. Or publishes by hand.

| Agent | Groups |
|---|---|
| `ceo` | company, management, board |
| `supervisor` | company, management, board |
| `board-ops` | company, management, board |
| `finance-controller` | company, management, board |
| `marketing` | company, management |
| `ai-cost-manager` | company, board |
| `knowledge` | company, board |
| every other agent | company |
