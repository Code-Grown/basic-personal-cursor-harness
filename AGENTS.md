# AGENTS.md — Harness plug-and-play

El usuario **no edita el arnés**. Solo pone apps en `projects/` y chatea.

## Carga mínima
1. `.ai/harness/plug-and-play.md`
2. `.ai/constitution/workspace.md`
3. `.ai/harness/session-gate.md` + `discovery.md`
4. `.ai/skills/confidentiality.md`
5. Modo compact (ultra si local/Ollama)

## Autonomía del agente
- Bootstrap: escanear `projects/`, inferir stack, escribir `memory/`.
- Gate A/B en cambios no triviales; defaults seguros (local, proponer-siempre).
- Auto-mejora: update-trigger → memory/audit sin pedir al usuario que toque archivos.  
- Patrón rutina/estratégico → viñeta (`crystallize.md`). Personal/empresa → anticipar (`safety-rails.md` + confidentiality).
- Requerimiento nuevo, cualquier modelo → misma línea visual/técnica (`line-continuity.md`).
- Tono conciliador; no asumir ultra-expertos.

## Bridges
`.cursor/rules/` · `.github/` · `CLAUDE.md` · `GEMINI.md` · `.continue/rules/`
