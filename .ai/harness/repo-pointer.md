# Repo pointer (generic) · anti-drift

**No** copies the full harness into each app under `projects/`.  
Each app only declares **where** the shared harness lives + an optional local compact.

## Canonical file in each app

```
projects/<app>/.ai/HARNESS.md
```

Minimal frontmatter:

```yaml
---
harness: v1
hub: ../..
ai: ../../.ai
product: <app-name>
skill: <optional skill id under .ai/skills>
---
```

Body: ≤15 lines. No constitution dump, no secrets, no full skill copies.

Paths are relative to `projects/<app>/` (so `hub: ../..` = this harness repo root).

## Optional local compact

```
projects/<app>/.ai/cache/summaries/workspace-compact.md
```

Only facts about **this** app (ports, stack, gaps). Keep short.

## What must NOT live in `projects/<app>/.ai/`

- Full constitution / agents / operating-mode packs  
- Duplicate copies of this harness  
- Secrets, `.env`, PII  

Domain learnings go in the harness `.ai/memory/` (agent-written) or a dedicated skill — not duplicated per app.

## Discovery (agent)

When focusing an app under `projects/`:

1. If `projects/<app>/.ai/HARNESS.md` exists → use `hub` / `ai` / `skill`.  
2. Else if only a local compact exists → treat as legacy; create `HARNESS.md`.  
3. Else → create **only** the minimal pointer (template below). Do **not** install a fat harness inside the app.  
4. Never harness credential dirs (`.aws`, kubeconfigs, secret mounts).  
5. UI / AI / clone: inherit `ux-craft.md` + `ia-first.md` + `gap-fill.md`. Vue/Nuxt → `vue-pug.md`. Do not copy the modules.

## Template

See `templates/project-HARNESS.md`.
