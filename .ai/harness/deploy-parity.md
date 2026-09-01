# Deploy parity · local is not prod

An AI patch on a local app (hand SQL, custom insert, `.env`, a file on disk) does **not** ride along with pull + restart.  
Before deploy, or when touching schema / data / env: **evaluate** what would be missing. Not a playbook per host.

## Evaluate (do not assume)
1. Does **this** repo’s deploy script/skill already apply the change? (migrate, seed, compose, service).  
2. Is there state that exists **only** locally?
   - hand `INSERT` / `UPDATE` / `ALTER`  
   - catalog rows, roles, kinds, flags  
   - new env/secrets (in the example **and** in prod env?)  
   - files, cron, redis, nginx, volumes  
3. If yes → put it in an **idempotent** migration/seed, **or** list it as an explicit deploy step (and confirm).  
4. **Minimal** backup of what prod will touch **first**. Seed does not restore live work (`safety-rails`).  
5. Smoke the touched flow after. If it fails because “an insert is missing”, that insert was the change’s debt.

## What this is not
- Do not rewrite the repo’s deploy.  
- Do not copy local data to prod.  
- Do not run `pytest` / `drop_all` against the product DB.  
- Typo or CSS with no schema/env → skip this file.

## When
Deploy · “ship to prod” · schema · seed · new env · close with a real host.

## Related
`dev-cycle.md` · `confirm-execute.md` · `safety-rails.md` · `close-versioning.md` (commit; this is the **after** if there is a deploy).
