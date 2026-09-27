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

אין תקרת הוצאת מטא חודשית. אישור הוא לפי קמפיין. אין התראת תקרת מחזור.

## A. Main funnel

```
Or (brief, or "hunt") → CEO
  → research-alpha + research-beta + market-analyst
  → customer-intelligence (in parallel; hands to the CEO)
  → CEO sends product name + screenshot to LIO   [after research finishes]
  → GATE 1 (NotebookLM deck → Or)
  → creative-strategist → copywriter → visual-producer → video-editor
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
5. **Creative, then the store draft.** The four creative stages, in order. The video approve/reject is Or's decision, requested by the CEO. `video-editor` does not ask Or. Then
   `shopify` drafts the product page. Prices are **without VAT**. The draft is not a publish.
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
8. **GATE 2.** The CEO requests Or's approval with a NotebookLM deck of **everything since Gate 1**.
   Or approves and publishes manually. No other agent asks him to publish.

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

**Fatigue.** Marketing flags it. Work returns to `creative-strategist`. The new round
passes **Gate 2 again** before Or republishes.

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
| `video-editor` | `shopify` | `visual-producer` |
| `shopify` | `marketing` | `video-editor` |
| `marketing` (ABO plan) | `finance-controller` | `shopify` or `creative-strategist` |
| `finance-controller` (opinion) | CEO, for Gate 2 | `marketing` |
| Gate 2 approved | Or publishes by hand. The CEO passes the campaign name and ID. Then `marketing` starts the 24h read | — |

## G. Go-live channels, lifecycle, groups

There is no GOD Runtime and no database. Real coordination:

- **Company group** — every agent. Handoffs and deliverables.
- **Management group** — `ceo`, `supervisor`, `board-ops`, `finance-controller`, `marketing`.
- **Board group** — `ceo`, `board-ops`, `supervisor`, `finance-controller`, `ai-cost-manager`, `knowledge`.
- **DM** to the CEO bot `paleri os ceo`.
- **PALERI task board** in Notion. Written only by the Notion memory bot, which is `knowledge`.
- **Training Room living layer** in Notion: lessons, do-not-repeat, video approval log. Same bot writes it.
- **Canon** stays in this repo, under `knowledge/memory/`.

`LIO` is unchanged and external.

**Lifecycle.** Every bot starts in SETUP. Its only action is one message in its own chat asking Or to connect the list under **Setup connections** in its `tools/` file. Then it stops. After verification it is STANDBY. It becomes ACTIVE only when the CEO sends ACTIVATE, and it runs a routine only after the CEO names that routine.

The CEO does not wait for ACTIVATE from another agent. After Or verifies the CEO's own connections, Or's next working message in the CEO's chat puts the CEO on duty. The CEO is the one who sends ACTIVATE.

After SETUP, no agent except the CEO contacts Or. Gate 1, Gate 2, and the video approve/reject stay Or's decisions. The CEO requests them. Or publishes by hand.

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
