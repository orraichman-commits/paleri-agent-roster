# Copywriter Skills

The Copywriter's craft, split by concern. **Runtime wiring:** specialists are executed by
the `agent-runtime` edge function, whose system prompt is composed at deploy time from
`supabase/functions/_shared/agentInstructions.ts`. That file is generated from the
canonical Markdown below (base identity + always-on Hebrew/compliance craft + a format
skill selected per task by deterministic keyword match). Edge Functions cannot read the
repository at runtime, so the generated TypeScript embeds the Markdown at deploy time.

After editing any canonical Copywriter file, run `npm run copywriter:generate`, then
redeploy `agent-runtime` via the Supabase MCP connector — the generated file only reaches
production at deploy time. Run `npm run copywriter:check` before deploying (it fails when
the generated runtime file is stale); the production build also runs this check
automatically. Never edit `agentInstructions.ts` directly.

| Skill | Concern | Runtime |
|---|---|---|
| `copywriting.md` | core craft: awareness levels, So-What chain, specificity, proof, editing | always loaded in base |
| `hebrew-craft.md` | gendered address, register, mechanics, trust markers, anti-AI-tells | always loaded |
| `meta-compliance.md` | the seven rejection traps + compliant-rewrite procedure | always loaded |
| `hooks-and-ads.md` | Meta ads: hook taxonomy, 125-char rule, video/UGC scripts | keyword-selected |
| `landing-page-copy.md` | product page / lander section flow, objections, CTAs | keyword-selected |
| `messaging-copy.md` | WhatsApp / email / SMS drafts and sequences | keyword-selected |
| `operating-procedure.md` | boundary, escalation, copy-chief pass | always loaded in base |

Provenance: format skills adapt robpalmer99/claude-code-copywriting-skills (CC-BY-4.0,
Rob Palmer — attribution preserved here and in file footers) and rampstackco/claude-skills
(MIT); `hebrew-craft.md` and `messaging-copy.md` are PALERI-original. Nothing was copied
verbatim; everything was rewritten Hebrew-first.

The Copywriter is a **craft agent**: strategy (product, audience, angle, offer, pricing)
arrives decided in the Creative Brief. Skills here teach how to *write*, never what to sell.
