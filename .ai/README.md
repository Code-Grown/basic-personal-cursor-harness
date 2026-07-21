# `.ai/` — Gobernanza portable multi-IA (genérica)

Versión 2.1.0 · Token-first · Confidentiality-first · Domain-agnostic  
(SemVer: `/VERSION` · historial: `/CHANGELOG.md`)

## Estructura
```
.ai/
├── constitution/     regla maestra
├── protocols/        full | compact | ultra
├── harness/          session-gate, triggers, checks, rollback
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
