---
description: "Session Gate — pre-evaluación, confirmación, comprensión (CORE)"
applyTo: "**"
priority: 950
---

# Session Gate

## Cuándo aplicar
Cambio de código, arquitectura, datos, infra o contratos. Excepción: trivial (typo, path, FAQ).

## Perfil del operador — para qué sirve
Este repo es un **template**. Quien lo implementa añade su código, módulos y contexto.  
P1–P8 se responden **en el proyecto consumidor**, no al mantener el template vacío.

Si `memory/operator-profile.md` está `INCOMPLETO` en un proyecto con código, preguntar en **un solo bloque** (máx 8).  
En el template puro (sin app del usuario): no bloquear mejoras del arnés por perfil vacío.

**No asumir expertos:** si P1 indica junior/no-dev o está vacío, explicar con claridad y ejemplos del repo leído.

### Preguntas (con ejemplo de respuesta corta)

| # | Pregunta | Ejemplo de respuesta |
|---|---|---|
| P1 | ¿Rol y nivel técnico? | `fullstack mid` / `founder no-dev` / `principal backend` |
| P2 | ¿Objetivo de esta sesión en 1 frase? | `arreglar auth JWT` / `diseñar módulo de pagos` |
| P3 | ¿Stack principal del repo? | `Next+Postgres` / `Go+K8s` / `aún vacío` |
| P4 | ¿Restricciones de riesgo? | `solo staging` / `prod ok con PR` / `datos personales regulados` |
| P5 | ¿Qué categorías son confidenciales aquí? | `keys, PII clientes, pricing` (sin pegar secretos) |
| P6 | ¿Ritmo? | `proponer-siempre` (default) / `ejecutar-SAFE-auto` |
| P7 | ¿Qué IAs usas? | `Cursor + Claude` / `Copilot` / `Ollama local` |
| P8 | ¿Hay ADR/decisión previa que limite esto? | `no` / `sí: ver decisions ADR-003` |

Persistir en `memory/operator-profile.md` (sin secretos).

## Pre-evaluación (≤12 líneas)
```
IMPACTO: SAFE | BREAKING | DESTRUCTIVE | SENSITIVE
ALCANCE: [archivos/módulos]
RIESGO: [1–2 bullets]
REVERSIBILIDAD: Alta|Media|Baja
PROPUESTA: [qué / por qué / no-hacer]
OPCIONES:
  A) ...
  B) ...
  C) pausar / más info
COMPRENSIÓN: ¿Confirmas que X implica Y y NO implica Z?
```
Diagrama mermaid solo si aclara (máx 1, ≤15 nodos).

## Confirmación
- SAFE + ritmo `ejecutar-SAFE-auto` → puede ejecutar tras propuesta breve.
- BREAKING / DESTRUCTIVE / SENSITIVE → espera `A`/`B`/`OK`/`aprobado` explícito.
- Si duda → pausar; reexplicar; no editar.

## Check de comprensión
Una pregunta cerrada post-propuesta y post-cambio.
Si respuesta confusa → no avanzar.

## Auto-mejora
Tras sesión útil: bullet en `patterns.md` o ADR si aplica update-trigger.
Fallo del arnés → 1 línea en `audit/optimization.md`.
