# Crystallize (generic) · continuity without chat

Chat is **not** the source of truth. After useful work, write durable notes.

## Where
| Finding | Destination |
|---|---|
| Workspace map / ports | `.ai/memory/workspace.md` |
| Stable technology / stack | `.ai/skills/<stack>.md` (`tech-skills.md`) |
| Decision / ADR | `.ai/memory/decisions.md` |
| Reusable pattern | `.ai/memory/patterns.md` or a skill |
| Token/friction / harness efficacy lesson | `.ai/audit/optimization.md` |
| **Harness-level** improvement (portable) | This repo’s `.ai/harness/*` + bump VERSION + **push `main`** |

## Efficacy close (required if learning happened)
1. Update skill or compact for the app under `projects/`.  
2. Version code: `close-versioning.md` — commit touched repos; **ask** before push.  
3. If the lesson is **generic harness behavior** (safety, read-budget, discovery, crystallize, model-routing, tech→skills, repo-pointer, quality-bars):  
   - Edit the harness file here  
   - Bump `VERSION` + `CHANGELOG.md`  
   - Commit and **`git push origin main`** (`promote-harness.md`)  
4. Never push secrets, PII, or client/VPS/AWS private facts into this template.

## How
- 1–5 bullets or one index row — no essays.  
- No secrets / PII.  
- Prefer small diffs over rewriting whole skills.  
- Refresh `.ai/cache/` if the map changed.
