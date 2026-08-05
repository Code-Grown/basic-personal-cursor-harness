# Changelog

Formato [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) · [SemVer](https://semver.org/lang/es/).  
Canónico: archivo `VERSION`.

---

## [Unreleased]

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
