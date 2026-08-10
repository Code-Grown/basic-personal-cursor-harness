# Changelog

Formato [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) · [SemVer](https://semver.org/lang/es/).  
Canónico: archivo `VERSION`.

---

## [Unreleased]

---

## [2.6.6] — 2026-08-09

### Added
- `ai-product-models.md` — catálogo LLM vigente (Gemini 3.6 · GPT-5.6 Luna/Terra/Sol · Claude Sonnet/Opus/Fable 5) al implementar IA en productos

---

## [2.6.5] — 2026-08-09

### Changed
- `close-versioning` — commit siempre; sin remoto no push; preferir rama activa / main; evitar tags y feature branches (converger a principal/env)

---

## [2.6.4] — 2026-08-09

### Added
- `change-strategy.md` — evaluar estrategias A/B; no desarmar correcciones previas

### Changed
- `confirm-execute`, `quality-bars`, bridge — checklist pre-cambio con preservación de fixes

---

## [2.6.3] — 2026-08-08

### Changed
- `model-routing` — Grok/fuerte por defecto; Tasks **heredan**; Composer solo pedido explícito (rollback del forzaje Composer)

---

## [2.6.2] — 2026-08-05

### Changed
- `quality-bars` — chat IA: Enter envía · Shift+Enter salto de línea (convención UX)

---

## [2.6.1] — 2026-08-05

### Added
- `.ai/harness/close-versioning.md` — al cerrar requerimiento: commit en cada repo tocado; **preguntar** antes de push

### Changed
- `quality-bars`, `crystallize`, bridge — cierre con versionamiento local + oferta de push

---

## [2.6.0] — 2026-08-05

### Added
- `.ai/harness/quality-bars.md` — barras convergentes (guía, seguridad, secrets, UX, multi-env, mantenibilidad)
- `.ai/harness/confirm-execute.md` — proponer → confirmar → ejecutar → grabar

### Changed
- Bridge carga quality-bars + confirm-execute en trabajo no trivial
- Listas futuras del operador se anexan aquí (genérico) o en skills de dominio

---

## [2.5.0] — 2026-08-05

### Added
- `.ai/harness/promote-harness.md` — protocolo: mejora genérica del arnés → VERSION → **push `main`**
- Cierre de efficacy en `crystallize.md` (skills + promote)

### Changed
- `update-trigger` #11 · bridge `00-harness-core` — cristalizar y enviar mejoras “como arnés” a este repo

---

## [2.4.1] — 2026-08-05

### Changed
- `model-routing.md` — rutinario **obliga** Composer en Task/subagentes (no heredar Grok/caro); alta exigencia sigue con modelo fuerte
- Bridge: aviso de 1 línea si el chat es caro y la tarea es básica

### Notes
- El selector del chat lo controla el usuario; el arnés no puede cambiarlo, sí el `model` de subagentes.

---

## [2.4.0] — 2026-08-05

### Added
- `.ai/harness/tech-skills.md` — detectar tecnologías por evidencia y cristalizar en `.ai/skills/` cada iteración
- `.ai/harness/model-routing.md` — Composer (barato) vs modelo fuerte según tarea
- Trigger #10 en `update-trigger.md` (tech/stack → skills)

### Changed
- `discovery`, `plug-and-play`, `crystallize`, `session-gate`, `00-harness-core` — tech→skills en el ciclo
- `skills/README.md` — automejora documentada

---

## [2.3.0] — 2026-08-05

### Added
- `.ai/harness/safety-rails.md` — rails genéricos (secretos, irreversibles, confirmación)
- `.ai/harness/read-budget.md` — presupuesto de lectura (anti-sobrelectura)
- `.ai/harness/repo-pointer.md` + `templates/project-HARNESS.md` — puntero mínimo por app en `projects/` (anti-drift)
- `.ai/harness/crystallize.md` — continuidad en memory/audit, no en el chat

### Changed
- Bridge Cursor `00-harness-core.mdc` — carga on-demand de safety / read-budget / repo-pointer
- `plug-and-play.md` + `session-gate.md` — descubren/crean `HARNESS.md` sin copiar el arnés entero
- `.gitignore` — ignora `.DS_Store`

### Notes
- Solo best-of **genérico**; sin memory operativa de workspaces privados ni hubs de producto.

---

## [2.2.0] — 2026-07-20

### Added
- Modo **plug-and-play**: zona `projects/` para apps del usuario
- `.ai/harness/plug-and-play.md` + rule Cursor `04-plug-and-play.mdc`
- `harness.code-workspace`
- Bootstrap autónomo: agente escribe `memory/` sin que el usuario edite el arnés
- Preguntas mínimas Q1–Q3 (reemplaza bombardeo P1–P8 para usuarios finales)

### Changed
- Flujo recomendado: clonar arnés → soltar apps en `projects/` → chatear
- INSTALL pasa a “modo avanzado” (copiar arnés a otro repo)
- Defaults: proponer-siempre, solo local, perfil AUTO

### Notes
- Autonomía = al chatear (no hay proceso background 24/7)

---

## [2.1.1] — 2026-07-20

### Changed
- `project-template/` → `docs/getting-started/` (manual, no runtime)

### Added
- Score de efectividad en `.ai/audit/architecture-score.md`

---
