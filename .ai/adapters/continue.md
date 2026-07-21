# Adapter: Continue.dev

## Wiring
1. Copiar o symlink reglas hacia `.continue/rules/` o referenciar en `config.yaml` / `config.json`.
2. System message sugerido: contenido de `AGENTS.md` (corto).
3. Docs index: incluir `.ai/constitution`, `.ai/harness/session-gate.md`, `memory/` — excluir `generated/`, `cache/`, `.env*`.

## Ejemplo (concepto)
```yaml
# .continue/config.yaml (adaptar a tu versión de Continue)
rules:
  - name: harness
    description: AI harness core
    # apuntar a AGENTS.md o pegar resumen
```

Mantén Continue como **lector** del núcleo; no forks del protocolo.
