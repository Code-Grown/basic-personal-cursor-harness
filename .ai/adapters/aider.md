# Adapter: Aider / CLIs de edición

## Wiring
```bash
aider --read AGENTS.md \
  --read .ai/constitution/workspace.md \
  --read .ai/harness/session-gate.md \
  --read .ai/protocols/operating-mode.compact.md \
  --read .ai/skills/confidentiality.md
```

Local/pequeño: sustituye compact por `operating-mode.ultra.md`.

## Comportamiento
Antes del primer `/commit` no trivial: exigir propuesta A/B en el chat.
No pasar `.env` ni secrets al contexto (`--ignore` / `.aiderignore`).
