# Crystallize (generic) · continuity without chat

Chat is **not** the source of truth. After useful work **or when the requirement/topic changes**, write durable notes.

Memory discipline: `context-discipline.md` — crystallize critical points / what worked; do not recompact surplus as chat context.

## Where
| Finding | Destination |
|---|---|
| Workspace map / ports | `.ai/memory/workspace.md` |
| Stable technology / stack | `.ai/skills/<stack>.md` (`tech-skills.md`) |
| Decision / ADR | `.ai/memory/decisions.md` |
| Reusable pattern | `.ai/memory/patterns.md` or a skill |
| Token/friction / harness efficacy lesson | `.ai/audit/optimization.md` |
| **Harness-level** improvement (portable) | This repo’s `.ai/harness/*` + bump VERSION + **push `main`** |
| Tour / working guide / learning pack | Persist for the **in-app AI chat** (`ia-first.md`); suggest 1–3 command/guide improvements at close |

## Efficacy close (required if learning happened or topic changed)
1. What worked / critical invariant → skill or compact (1–5 bullets).  
2. Drop noise — do not dump the thread into generated “recompacted context”.  
3. Version code: `close-versioning.md` — commit touched repos; push only with remote + ask.  
4. If the lesson is **generic harness behavior**: edit harness here → bump `VERSION` + `CHANGELOG` → **`git push origin main`** (`promote-harness.md`).  
5. Never push secrets, PII, or client/VPS/AWS private facts into this template.

## Pattern trigger (same turn — don’t wait for “harness this”)
Signal: asked **twice** · “always / never / everywhere” · every-feature routine · strategic (more than one app).

Same turn: 1 bullet on the right floor. Not the thread. Not `generated/`.  
Operator-kept chat logs = **their** backup; do not ingest whole. If they ask “what slipped?”, keywords + short window.

If the bullet would include **personal or company** data → `safety-rails.md` (anticipate). Do not write silently.

## How
- 1–5 bullets or one index row — no essays.  
- No secrets / PII.  
- Prefer small diffs over rewriting whole skills.  
- Refresh `.ai/cache/` if the map changed.
