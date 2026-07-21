# Workspace Map — (rellena al implementar el arnés en un proyecto)

**Actualizado**: YYYY-MM-DD  
**Dominio**: _(lo define el proyecto consumidor)_  
**Advertencia**: sin secretos ni IDs reales de cuenta/infra.

## Módulos
| Módulo | Rol | Stack | Notas |
|---|---|---|---|
| _(ej. api)_ | _(HTTP)_ | _(…)_ | — |
| _(ej. web)_ | _(UI)_ | _(…)_ | — |
| _(ej. worker)_ | _(jobs)_ | _(…)_ | — |

## Flujos (alto nivel)
```
_(ej. cliente → api → db)_
```

## Entornos
| Env | Uso |
|---|---|
| local | desarrollo |
| staging | validación |
| prod | solo con confirmación en cambios BREAKING/DESTRUCTIVE |

## Entry points del arnés
- Constitución: `.ai/constitution/workspace.md`
- Gate: `.ai/harness/session-gate.md`
- Modo: `.ai/protocols/operating-mode.compact.md` (ultra en local)
