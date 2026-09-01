# Close versioning

At the end of a **requirement / theme / useful delivery** that touched code: **always commit**. Push only when a remote exists and the user asks (or a documented exception).

## Commit (always)
In **each** app repo with code changes:

1. Review `git status` / diff.  
2. Conventional commit on the **current working branch**.  
3. One commit per repo if several apps changed.  
4. Never commit secrets. No release tags unless asked.  
5. Skip only if the user said “no commit”.

## Push (remote + ask)
1. Check `git remote -v`.  
2. **No remote** → do **not** push; local commit is enough; say so in one line.  
3. With remote → ask `Push to origin/<branch> for <repo>?` before pushing.  
4. Never assume push. Never force-push shared branches without explicit OK.

**Exception**: portable improvements to **this** template → bump VERSION + push `main` (`promote-harness.md`).

## Branches (generic defaults)
- Prefer committing on the branch you are on (`main`, `devel`, `cert`, `prod`/`master`, etc.).  
- Avoid long-lived `feature/*` branches; if used, **converge** back to the repo’s primary line (`main` / env branch).  
- Do not invent a feature branch “by habit”.  
- If unsure which env branch to converge to → ask.

## Close order
Verify → crystallize if needed → **commit** → if shipping, `deploy-parity.md` → ask push **only if remote exists** → summarize local vs remote.
