# Tech → skills · automejora por iteración

En cada iteración no trivial: **detectar tecnologías por evidencia** y **cristalizar** en `.ai/skills/` (y memory si es mapa). Así las siguientes generaciones mejoran sin re-descubrir el stack.

## Detectar (evidencia en `projects/<app>/`, no inventar)

| Evidencia | Acción |
|---|---|
| `package.json` + nuxt/vue | skill frontend + **`vue-pug.md`** (Pug estricto) |
| `package.json` + next/react | skill `frontend-<stack>.md` (no Pug) |
| `pyproject.toml` / `requirements.txt` + FastAPI/Django/Flask | skill `backend-python.md` (o stack concreto) |
| `go.mod` | skill `go.md` |
| `pubspec.yaml` | skill `flutter.md` |
| `*.tf` | skill `terraform.md` |
| `Dockerfile` / compose | viñetas infra en skill o `memory/workspace.md` |
| ORM / migraciones | skill `database.md` o sección en backend |

Leer solo manifests + 1–2 archivos clave (`read-budget.md`).

## Dónde escribir

| Hallazgo | Destino |
|---|---|
| Stack estable | `.ai/skills/<nombre>.md` (delgado) |
| Mapa app/puertos | `.ai/memory/workspace.md` |
| Convención repetible | skill checklist (≤15 líneas nuevas) o `memory/patterns.md` |
| One-off de un ticket | no skill |

Registrar skills nuevas en `skills/README.md` y, si aplica, `orchestrator/router.yaml`.

## Reglas
- Diff **pequeño** — no reescribir skills enteros.
- Sin secretos ni PII.
- Si la tech no cambió → no tocar.
- Al cerrar iteración con aprendizaje tech: obligatorio evaluar este archivo.

## Plantilla mínima de skill nueva
```markdown
# <Stack> · skill

Evidencia: <paths>
Checklist:
- …
Anti-patrones:
- …
```

Skill de **dominio/producto**: ver `templates/domain-skill.md`.
