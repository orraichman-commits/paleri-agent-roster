# Training Room — יומן אישור וידאו

Owner video gate for generated ads. Or (Owner) decided this on 2026-09-27.
The rule is temporary. The log is permanent: creative reads it before every new job.

Hebrew is the Owner-facing rule. Field names stay in English so a handoff can quote them.

## הכלל

כל סרטון שנוצר עובר לאור לאישור או לדחייה **לפני** שהוא ממשיך ל־`marketing` ול־Gate 2.
ההחלטה והנימוק נכתבים כאן כמו שנאמרו. דחייה חוזרת ל־`video-editor` ול־`visual-producer`
עם הנימוק. זו החזרה של **שלב הייצור** (שלב אחד, לא שניים), והיא נספרת ב־STOP RULE
שב־`funnels.md`. החזרה אחת של השלב הזה היא תיקון, לא עצירה. אם שלב אחר באותו ריצה
כבר הוחזר בגלל כשל סטנדרט, העצירה חלה.

השער זמני, בתחילת הדרך. כששיעור האישורים יציב, אור יכול לרפות אותו לאוטונומיה.
אף סוכן לא מרפה אותו לבד, ולא מוחק שורה מהיומן כדי "לנקות" דחייה.

`knowledge` רושם את ההחלטה. הוא לא הופך נימוק לכלל קנון באותה כתיבה. כלל חדש
(מותג, טון, מה לא לנסות) הוא הצעה נפרדת, ומחכה לאישור אור כמו כל שינוי ב־Training Room.

## Who reads it

Before a new creative job, read the log:

- `visual-producer` and `video-editor` — required, every job, before generation.
- `creative-strategist` and `copywriter` — required, every job, before the brief or the script.
- The CEO — when building the Gate 2 deck, so Or sees his own earlier reasons next to the new cut.

An empty log means there is no prior reason yet. Do not invent one.

## Who writes it

`knowledge` appends one entry when Or approves or rejects a generated video.
Copy the reason in his words. Do not soften, merge, or drop a rejection.
Do not store `HIGGSFIELD_API_KEY` or any other secret in an entry.

## Entry

```
## <YYYY-MM-DD> — <product> — <approve | reject>
Video: <variant / output ref>
Foreplay ref: <url or id the cut was built from>
Decision: <approve | reject>
Reason: <Or's reason, in his words>
Returned to: <— | video-editor + visual-producer>
Stop-rule note: <production-stage correction | stacks with <other stage> → stop>
Logged by: knowledge
```

## Log

No entries yet.
