# Confirm → execute → record

For **non-trivial** changes (code, schema, deploy, infra):

0. **Strategy** → `change-strategy.md`: account for prior fixes; choose A (additive) vs B; do not undo working behavior.  
0b. **Line** → `line-continuity.md`: new work, any model, follows the existing visual/technical line (does not veto asked redesign).  
1. **Do** the request. If they already said what they want, do not answer with a plan instead.  
2. **Ask** only for destructive, production, secrets, or a real clash with a working fix (`OK` / `A` / `B`). A screen or a function they asked for does not wait.  
3. **Deliver** a path a person can finish: the other side of the interface, the library component that already fits, and the adjacent step required to complete it. Do not open a different product.  
4. **Record** the action in memory/skill/audit: what was asked, confirmed, done.  
5. Never treat silence as OK for BREAKING / DESTRUCTIVE / SENSITIVE / production.

SAFE trivial may proceed; still crystallize if there is a lasting lesson.

6. **Gap-fill** → `gap-fill.md`: if they say something is missing, do not stop at “it isn’t there”. SAFE → create now. New piece → short A/B and build (unless BREAKING/prod).
7. **Deploy / schema / env** → `deploy-parity.md`: list what exists only locally (hand inserts, seed, `.env`); do not assume prod has it.
