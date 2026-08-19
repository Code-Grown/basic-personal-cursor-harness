# Quality bars (generic) · converge future work

Portable bars. Product-specific tours/AWS envs live in private hubs — here only what any app can inherit.

## Always (product apps under `projects/`)
1. **Guided help** — if the app has tour/onboarding/docs-in-UI, update them in the same iteration as the feature; if missing for a new operator flow, add a minimal guide.  
2. **Security first** — server-side checks; least privilege; see `safety-rails.md`.  
3. **Secrets configurable** — env/config UI only; never hardcode; never echo secrets.  
4. **Stability** — backend-first when cross-cutting; idempotent migrations; smoke what you touch.  
5. **Consistent UI** — reuse existing components/tokens; no new design system in one PR.  
   - **AI chat**: Enter sends · Shift+Enter newline (not Cmd/Ctrl+Enter).
6. **Use the stack well** — prefer established patterns over new deps.  
7. **Intuitive + chat-friendly** — clear errors; short A/B proposals; `read-budget.md`.  
8. **Flow-first UX** — on redesign / “less admin” / mobile usability: `ux-flow-first.md` (role home, pipelines, bridges; tour ≠ only map).  
8b. **Craft** — UI / copy / AI surfaces: `ux-craft.md`. Working guide; global chrome (dismissible toasts, 8px radius, modal buttons inside the frame, labels vs placeholders, fixed auth fields, mobile tables); voice on AI chat.  
8c. **IA-first** — `ia-first.md`: tours/learning persist as in-app chat context; optimize the working guide on every development.  
8d. **Gap-fill** — if they say it is missing / does not exist: `gap-fill.md` (create a careful compensation).  
8e. **Pug** — Vue/Nuxt: `vue-pug.md`. New templates in Pug; on touch, migrate HTML immediately.  
9. **Confirm → execute → record** — `confirm-execute.md`.  
10. **Change strategy** — evaluate A/B; do not undo prior fixes (`change-strategy.md`).  
11. **Maintainable code** — small diffs; clear names; crystallize invariants. Routine/strategic pattern → same-turn bullet; personal/company data → anticipate first (`safety-rails`).  
12. **Version at close** — always commit on the working branch; push only if a remote exists and user says yes (`close-versioning.md`). No tags/feature branches by habit — converge to main/env.

## Infra / multi-env (when the app uses it)
- Prefer defining **all target envs** in code (not “only dev”).  
- Ask whether the change applies to other envs; record the answer.  
- Respect established folder/state layout — improve code, don’t restructure for taste.  
- Automate avoidable human steps (DNS records, etc. in IaC); suggest apply **steps** that leave each env OK.

## Future operator lists
Append new convergence bullets here (generic) or in a domain skill (product-specific). Keep diffs small.
