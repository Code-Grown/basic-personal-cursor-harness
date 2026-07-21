# Changelog

Todos los cambios notables de este arnés se documentan aquí.

El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/)  
y este proyecto usa [Versionado Semántico](https://semver.org/lang/es/) (`MAJOR.MINOR.PATCH`).

## Cómo interpretar la versión

| Incremento | Cuándo |
|---|---|
| **MAJOR** (`X.0.0`) | Cambio que rompe el contrato del arnés para quien ya lo implementó (renombres de paths CORE, gate incompatible, eliminación de bridges sin reemplazo) |
| **MINOR** (`x.Y.0`) | Nueva capacidad compatible (adapter, skill opcional, fase nueva documentada) |
| **PATCH** (`x.y.Z`) | Aclaraciones, docs, typos, ajustes internos sin cambiar el contrato |

**Fuente de verdad del número:** archivo `VERSION` en la raíz.  
Al publicar: actualizar `VERSION` + esta entrada + referencias en `.ai/constitution/workspace.md` y `.ai/README.md`.

---

## [Unreleased]

---

## [2.1.1] — 2026-07-20

### Changed
- `project-template/` renombrado a `docs/getting-started/` (manual, no runtime)
- Aclaración: el nombre del proyecto consumidor es irrelevante; el arnés no detecta esa carpeta

### Added
- `docs/getting-started/README.md` explicando que no se copia obligatoriamente
- Evaluación de efectividad en `.ai/audit/architecture-score.md`

---

## [2.1.0] — 2026-07-20

Primera publicación ordenada del template multi-IA genérico (post-limpieza del legado de workspace ajeno).

### Added
- Núcleo `.ai/`: constitution, protocols (full / compact / ultra), harness (session-gate, discovery, checks, triggers, rollback)
- Bridges: Cursor (`.cursor/rules`), Copilot (`.github/`), Claude (`CLAUDE.md`), Gemini (`GEMINI.md`), Continue (`.continue/rules`)
- Adapters documentados: Windsurf, Aider, Cline, JetBrains, Ollama, Antigravity
- Skills: `confidentiality` (CORE), `trading-ml` (opcional, accesible a no expertos)
- `NEXT_STEPS.md`, guías de instalación / primera sesión
- README con guía de implementación paso a paso
- Versionado semántico: `VERSION` + este `CHANGELOG`

### Changed
- Protocols v2.1: tono conciliador, no asumir ultra-expertise, discovery obligatorio antes de proponer
- Absoluto++ / Arquitecto-Ejecutor / Núcleo viven en `.ai/protocols/` con variantes por presupuesto de tokens
- Ritmo default: `proponer-siempre`

### Removed
- Contenido de dominio PISEE/Interop y datos sensibles de memoria legacy
- Skills de stacks ajenos al template

### Security
- Política de confidencialidad CORE; redaction en memory; `.gitignore` para `.env` / secrets / cache efímero
