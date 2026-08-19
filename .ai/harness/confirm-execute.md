# Confirm → execute → record

For **non-trivial** changes (code, schema, deploy, infra):

0. **Strategy** → `change-strategy.md`: account for prior fixes; choose A (additive) vs B; do not undo working behavior.  
1. **Propose** (≤12 lines): impact · scope · options A/B · what will not be done · which prior fix is preserved.  
2. **Ask** for explicit confirmation (`OK` / `A` / `B`) unless SAFE trivial (typo, path, FAQ).  
3. **Execute** only after confirmation (or SAFE trivial); do not expand scope “while here”.  
4. **Record** the action in memory/skill/audit: what was asked, confirmed, done.  
5. Never treat silence as OK for BREAKING / DESTRUCTIVE / SENSITIVE / production.

SAFE trivial may proceed; still crystallize if there is a lasting lesson.

6. **Gap-fill** → `gap-fill.md`: if they say something is missing, do not stop at “it isn’t there”. SAFE → create now. New piece → short A/B and build (unless BREAKING/prod).
