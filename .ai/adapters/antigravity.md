# Adapter: Antigravity / agentes genéricos

Cualquier runner que no tenga bridge propio cae aquí.

## Wiring
1. System preamble = `AGENTS.md` (o `GEMINI.md` si el producto es Gemini-first).
2. Adjuntar: constitution → session-gate → confidentiality → compact|ultra.
3. Memory solo on-demand.

## CLI ejemplo
```bash
agent --system AGENTS.md \
  --context .ai/constitution/workspace.md \
  --context .ai/harness/session-gate.md \
  --context .ai/protocols/operating-mode.compact.md
```
