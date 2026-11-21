# Decisions Log — ADR

Formato: `ADR-NNN · Fecha · Módulo · Título`  
Sin secretos ni detalle propietario sensible.

---

## ADR-001 · 2026-11-21 · harness · Estándares mínimos apuntados desde la regla core

**Contexto**: Cada repo repetía su propio piso y los cloud agents no compartían una spec mínima ni un piso de frontend.
**Decisión**: El texto vive en `estandares/` y `plantillas/`. `00-harness-core.mdc` solo apunta. El CI de ejemplo no se copia a `.github/workflows/` de este repo.
**Archivos**: `estandares/sdd-minimo.md`, `estandares/piso-frontend.md`, `plantillas/spec-app.md`, `plantillas/pitch.md`, `plantillas/ci-estandares.yml`, `.cursor/rules/00-harness-core.mdc`
**Lección**: Lint, pruebas, build y la línea `Pitch:` exigen el piso en la app. Axe y Lighthouse avisan.
**Reversibilidad**: Alta
**Estado**: Aplicado

<!-- Añade ADRs del proyecto consumidor aquí. Ejemplo:

## ADR-001 · YYYY-MM-DD · api · Versionado URI /v1

**Contexto**: …
**Decisión**: …
**Archivos**: …
**Lección**: …
**Reversibilidad**: Alta
**Estado**: Aplicado
-->
