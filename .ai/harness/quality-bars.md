# Quality bars (generic) · converge future work

Portable bars. Product-specific tours/AWS envs live in private hubs — here only what any app can inherit.

## Always (product apps under `projects/`)
1. **Guided help** — if the app has tour/onboarding/docs-in-UI, update them in the same iteration as the feature; if missing for a new operator flow, add a minimal guide.  
2. **Security first** — server-side checks; least privilege; see `safety-rails.md`.  
3. **Secrets configurable** — env/config UI only; never hardcode; never echo secrets.  
4. **Stability** — backend-first when cross-cutting; idempotent migrations; smoke what you touch.  
5. **Consistent UI** — reuse existing components/tokens; no new design system in one PR.  
6. **Use the stack well** — prefer established patterns over new deps.  
7. **Intuitive + chat-friendly** — clear errors; short A/B proposals; `read-budget.md`.  
8. **Confirm → execute → record** — `confirm-execute.md`.  
9. **Maintainable code** — small diffs; clear names; crystallize invariants.

## Infra / multi-env (when the app uses it)
- Prefer defining **all target envs** in code (not “only dev”).  
- Ask whether the change applies to other envs; record the answer.  
- Respect established folder/state layout — improve code, don’t restructure for taste.  
- Automate avoidable human steps (DNS records, etc. in IaC); suggest apply **steps** that leave each env OK.

## Future operator lists
Append new convergence bullets here (generic) or in a domain skill (product-specific). Keep diffs small.
