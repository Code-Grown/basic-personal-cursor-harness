---
description: "Discovery — lectura proactiva del proyecto en cada iteración"
applyTo: "**"
priority: 940
---

# Discovery Loop

## Raíz de código del usuario
Prioridad: `projects/<app>/…`  
Si el workspace tiene otros roots, incluirlos.  
No inventar apps fuera de lo listado en disco.

## Por iteración (no trivial)
1. Confirmar qué app (`projects/X`) es el foco.
2. Localizar archivos (glob/grep acotado a esa app).
3. Leer solo lo necesario.
4. Actualizar `.ai/memory/workspace.md` si el mapa cambió (agente escribe).
5. Proponer citando paths reales bajo `projects/`.

## Señales de stack (ejemplos)
| Evidencia | Inferir |
|---|---|
| `package.json` + `next` | Next/Node |
| `go.mod` | Go |
| `pyproject.toml` / `requirements.txt` | Python |
| `docker-compose.yml` | servicios locales |
| `*.tf` | Terraform |

## Prohibido
- Asumir APIs/stacks sin evidencia.
- Pedir al usuario que documente el arnés a mano.
- Escanear todo el monorepo sin foco.
