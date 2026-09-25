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
הרוטינות ומחכים לאור. הסופרוויזר אוכף את זה. שלב אחד שהחזיר פעם אחת הוא תיקון, לא עצירה.

שערי בעלים נשארים בינתיים בנקודות המפתח. אישור אור אינו ויתור על הסטנדרט, והסטנדרט אינו
אישור להוציא כסף או לפרסם.

אין תקרת הוצאת מטא חודשית. אישור הוא לפי קמפיין. אין התראת תקרת מחזור.

## A. Main funnel

```
Or (brief, or "hunt")
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

0. **Start.** Or writes a brief, or tells research to hunt on its own.
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
4. **GATE 1.** The CEO sends Or a **NotebookLM deck**. Or approves, sends the work
   back to the start, or stops. A return to the start is Or's decision. It is not a
   standard-failure send-back between bots, and it does not by itself trip the stop rule.
5. **Creative, then the store draft.** The four creative stages, in order. Then
   `shopify` drafts the product page. Prices are **without VAT**.
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
8. **GATE 2.** The CEO sends Or a NotebookLM deck of **everything since Gate 1**.
   Or approves and publishes manually.

## B. Post-publish funnel

```
Or confirms launch (campaign name + ID)
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

Reports 3 and 4 go to Or **together**, inside `board-ops`' Thursday review. They are
not two separate owner pings.

No monthly Meta spend ceiling. No turnover-ceiling alert. Or is an exempt dealer; do
not warn that revenue is approaching an osek-patur threshold.

## D. Ops funnel

`supervisor` and `board-ops`.

**Supervisor.** Tracks every handoff: completion, whether it met the standard, and the
send-back count. A stage with **no output for 2 hours** gets **one nudge**, then an
alert to the CEO, who updates Or. **LIO's wait for the supplier is excluded** from that
clock. The supervisor enforces the stop rule and makes sure temporary routines stop
(LIO's 15-minute check stops when the supplier has replied, or when the stop rule
halts everything). A daily health log is kept and sent to Or **only when there is a
problem**.

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
next gate deck, or into a message to Or if it is urgent. The CEO still decides. The
denylist is not bypassed by an "enter."

## F. CEO products table

The CEO keeps the potential-products table in `ceo/memory/products-table.md` and pulls
it when Or asks. Or is an **עוסק פטור** (VAT-exempt dealer). Prices are without VAT.

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
| Or's brief or hunt order | `research-alpha`, `research-beta`; `customer-intelligence` once a product is in hand | — |
| `research-alpha` / `research-beta` | `market-analyst` | each other only to cross-check, not as a failed stage |
| `market-analyst` (route) | CEO, and the LIO handoff | `research-alpha` or `research-beta` |
| `customer-intelligence` | CEO | `market-analyst` if the product picture is too thin |
| Gate 1 approved | `creative-strategist` | Or may send the whole thing back to the start |
| `creative-strategist` | `copywriter` | `customer-intelligence` |
| `copywriter` | `visual-producer` | `creative-strategist` |
| `visual-producer` | `video-editor` | `copywriter` |
| `video-editor` | `shopify` | `visual-producer` |
| `shopify` | `marketing` | `video-editor` |
| `marketing` (ABO plan) | `finance-controller` | `shopify` or `creative-strategist` |
| `finance-controller` (opinion) | CEO, for Gate 2 | `marketing` |
| Gate 2 approved | Or publishes. Then `marketing` starts the 24h read | — |
