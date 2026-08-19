# `.ai/` — Gobernanza portable multi-IA (genérica)

Versión 2.6.10 · chrome global · IA-first · gap-fill · UX craft → push main

(SemVer: `/VERSION` · historial: `/CHANGELOG.md`)

Usuario no edita esto. Apps en `/projects/`. Agente mantiene `memory/` y `audit/`.

## Estructura
```
.ai/
├── constitution/     regla maestra
├── protocols/        full | compact | ultra
├── harness/          session-gate, safety-rails, read-budget, quality-bars, confirm-execute, change-strategy, context-discipline, ux-flow-first, ux-craft, ia-first, gap-fill, ai-product-models, close-versioning, repo-pointer, tech-skills, model-routing, crystallize, promote-harness, triggers, checks, rollback
├── agents/           planner · coder · reviewer · validator
├── memory/           mapa + ADRs + patterns + perfil (sin secretos)
├── skills/           confidentiality · trading-ml (opcional) · + las del proyecto
├── adapters/         bridges por herramienta
├── orchestrator/     router + policies
├── audit/            compliance · optimization · scores
├── generated/        proposals efímeras
└── cache/            resúmenes reemplazables
```

## Relación con bridges
| Herramienta | Bridge |
|---|---|
| Cursor | `.cursor/rules/` |
| Copilot | `.github/copilot-instructions.md` |
| Claude | `CLAUDE.md` |
| Gemini | `GEMINI.md` |
| Continue | `.continue/rules/` |
| Otros | `AGENTS.md` + adapter |
