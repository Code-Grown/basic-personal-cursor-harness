---
description: "Update Trigger — persistir memoria ante eventos clave"
applyTo: "**"
priority: 850
---

# Harness: Update Trigger

Antes de cerrar sesión con cambio exitoso, evaluar eventos. Si aplica → actualizar memory (sin secretos).

| # | Evento | Archivo |
|---|---|---|
| 1 | endpoint / API pública nueva o cambiada | `memory/workspace.md` |
| 2 | auth / permisos / roles | `memory/decisions.md` |
| 3 | ruta UI o flujo de operador | `memory/workspace.md` |
| 4 | convención o patrón nuevo | `memory/patterns.md` |
| 5 | decisión arquitectónica | `memory/decisions.md` (ADR) |
| 6 | schema DB / contrato de datos | `memory/workspace.md` |
| 7 | infra / deploy / entorno crítico | `memory/decisions.md` + `patterns.md` |
| 8 | perfil operador actualizado | `memory/operator-profile.md` |
| 9 | mejora del arnés detectada | `audit/optimization.md` |
| 10 | tecnología/stack nueva o cambiada | `skills/*.md` (+ `skills/README.md`) vía `tech-skills.md` |

## ADR
```markdown
## ADR-NNN · YYYY-MM-DD · <módulo> · <título>
**Contexto**: …
**Decisión**: …
**Archivos**: …
**Lección**: …
**Reversibilidad**: Alta|Media|Baja
**Estado**: Aplicado|Pendiente|Rechazado
```

## Patrón
```markdown
### P-NNN: <título>
<1–3 líneas>
```
