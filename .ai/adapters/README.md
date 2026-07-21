# Adapters — cómo cada herramienta ve el arnés

**Fuente de verdad**: siempre `.ai/` + `AGENTS.md`.  
Los bridges son delgados: apuntan al núcleo, no lo duplican.

| Herramienta | ¿Detecta sola? | Bridge en este repo |
|---|---|---|
| Cursor | Sí (`.cursor/rules`) | `adapters/cursor.md` |
| GitHub Copilot | Sí (`.github/copilot-instructions.md`) | `adapters/copilot.md` |
| Claude Code / Projects | Parcial (`CLAUDE.md`) | `adapters/claude.md` |
| Gemini CLI / Code Assist | Parcial (`GEMINI.md`) | `adapters/gemini.md` |
| Windsurf / Cascades | Parcial (lee `AGENTS.md` + rules) | `adapters/windsurf.md` |
| Continue.dev | Con config | `adapters/continue.md` |
| Aider / CLI agents | Manual / flags | `adapters/aider.md` |
| Cline / Roo | Parcial (`AGENTS.md`) | `adapters/cline.md` |
| JetBrains AI | Manual / project docs | `adapters/jetbrains.md` |
| Ollama / locales | Manual (contexto mínimo) | `adapters/ollama-local.md` |
| Antigravity / genérico | Manual | `adapters/antigravity.md` |

Si una herramienta no auto-carga nada: pega al inicio del chat  
`Sigue AGENTS.md y .ai/harness/session-gate.md. Modo compact (ultra si local).`
