# Close versioning

At the end of a **requirement / theme / useful delivery** that touched code:

## Commit (default yes)
In **each** app repo under `projects/` (or workspace root) with code changes:

1. Review `git status` / diff.  
2. Conventional commit with a clear message for that requirement.  
3. One commit per repo if several apps changed.  
4. Never commit secrets.  
5. Skip only if the user said “no commit”.

## Push (ask / suggest — do not assume)
- Do **not** push product/app repos by default.  
- End the close with one line, e.g.  
  `Push to origin/<branch> for <repo>? (yes / no)`  
- Push only after explicit yes.  
- Exception: portable harness improvements to **this** template repo → bump VERSION + push `main` (`promote-harness.md`).

## Close order
Verify change → crystallize if needed → **commit** → **ask push** → summarize local vs remote.
