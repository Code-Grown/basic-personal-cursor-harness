# Context discipline · crystallize, don’t recompact

**Good practice:** do not grow chat context to re-summarize later.  
Use **clear, specific harness rules**; free what did not help.

## Principle
| Do | Don’t |
|---|---|
| Write critical points into memory/skills/compact | Mega “recompacted context” files |
| Crystallize **what worked** when the requirement/topic changes | Keep the whole thread “just in case” |
| Drop noise and failed detours | Treat chat history as working memory |

The open chat **continues**. A long window (up to 500k) is for operating, not a reason to start another chat. Do not recompact the thread or ask for a fresh chat to “reset”.

Continuity across chats lives on disk (`crystallize.md`): when a topic closes, one vignette in this repo’s `HARNESS.md` or skill. The next chat reads that. It does not read the previous transcript.

## When to crystallize (required)
1. **Requirement or topic change** (even in the same chat).  
2. End of a useful delivery / learning iteration.  
3. After a non-trivial fix that must survive the next session.  
4. **Pattern signal** (twice / always / routine / strategic) → same-turn bullet (`crystallize.md`). Personal/company → anticipate (`safety-rails`).

## Keep (critical)
- Invariants: endpoint, role, flow, schema, decision, convention, infra.  
- What **worked** (pattern to reuse) — 1–5 bullets in the right slot.  
- Stable anti-pattern (if it prevents repeats) — one line, not the error dump.

## Free (do not harness as context)
- Failed explorations, discarded hypotheses, temp dumps.  
- Re-reads already reflected in skill/compact.  
- Unused A/B options (unless a short ADR).  
- Ad-hoc “active-context” / transcript digests as SoT.

## Operating rule
1. On topic change → **first** crystallize the previous topic (`crystallize` + self-improve).  
2. Then load only compact + ONE skill (`read-budget`).  
3. Do not inflate generated context files as source of truth.  
4. Small diffs; refresh cache indexes only if the map changed.  
5. Version touched code (`close-versioning.md`).
