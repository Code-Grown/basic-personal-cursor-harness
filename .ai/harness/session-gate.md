---
description: "Session Gate — pre-evaluación, confirmación, comprensión (CORE)"
applyTo: "**"
priority: 950
---

# Session Gate

## Cuándo aplicar
Cambio de código, arquitectura, datos, infra o contratos. Excepción: trivial (typo, path, FAQ).

## Perfil — modo plug-and-play
El usuario **no** rellena formularios del arnés. Ver `plug-and-play.md`.

1. **Inferir** stack, apps en `projects/`, idioma del chat, defaults (`proponer-siempre`).
2. **Escribir** perfil/memory el agente.
3. **Preguntar solo huecos** (máx 2–3), en un bloque corto:

| # | Solo si no se puede inferir | Ejemplo |
|---|---|---|
| Q1 | Objetivo de esta sesión | `arreglar login` |
| Q2 | ¿Puedo tocar staging/prod o solo local? | `solo local` |
| Q3 | ¿Hay algo confidencial aparte de keys/PII? | `pricing` / `no` |

Opcional más adelante (solo si hace falta calibrar): rol/nivel.  
**No asumir expertos** — jerga suave hasta notar lo contrario.

## Pre-evaluación (≤12 líneas)
```
IMPACTO: SAFE | BREAKING | DESTRUCTIVE | SENSITIVE
ALCANCE: [paths bajo projects/…]
RIESGO: [1–2 bullets]
REVERSIBILIDAD: Alta|Media|Baja
PROPUESTA: [qué / por qué / no-hacer]
OPCIONES:
  A) ...
  B) ...
  C) pausar / más info
COMPRENSIÓN: ¿Confirmas que X implica Y y NO implica Z?
```

## Confirmación
- SAFE + (raro) `ejecutar-SAFE-auto` → tras propuesta breve.
- BREAKING / DESTRUCTIVE / SENSITIVE → espera `A`/`B`/`OK` explícito.
- Si duda → pausar; reexplicar sin jerga innecesaria.

## Check de comprensión
Una pregunta cerrada, amable. Si confunde → no avanzar.

## Auto-mejora (obligatoria, sin pedir al usuario)
Tras cambio útil o fricción: update-trigger → `memory/` y/o `audit/optimization.md`. El usuario no edita eso.
