# Instalar el arnés en un proyecto destino

## Opción A — rsync (recomendada)

```bash
HARNESS=/ruta/a/basic-personal-cursor-harness
TARGET=/ruta/a/tu-proyecto

mkdir -p "$TARGET/.github/prompts" "$TARGET/docs"

rsync -a "$HARNESS/.ai/" "$TARGET/.ai/"
rsync -a "$HARNESS/.cursor/" "$TARGET/.cursor/"
rsync -a "$HARNESS/.continue/" "$TARGET/.continue/"
cp "$HARNESS/AGENTS.md" "$HARNESS/CLAUDE.md" "$HARNESS/GEMINI.md" "$TARGET/"
cp "$HARNESS/.github/copilot-instructions.md" "$TARGET/.github/"
cp "$HARNESS/.github/prompts/"*.md "$TARGET/.github/prompts/" 2>/dev/null || true
cp "$HARNESS/README.md" "$TARGET/docs/HARNESS.md"
cp "$HARNESS/NEXT_STEPS.md" "$TARGET/docs/HARNESS_NEXT_STEPS.md"
```

## Opción B — solo núcleo (Ollama / contexto estrecho)

- `.ai/constitution/`
- `.ai/protocols/operating-mode.ultra.md`
- `.ai/harness/session-gate.md` + `update-trigger.md`
- `.ai/skills/confidentiality.md`
- `.ai/memory/` (plantillas)
- `AGENTS.md`

## Después

1. Edita `.ai/memory/workspace.md` (mapa real, sin secretos).
2. Primer mensaje: ver `FIRST_SESSION.md`.
3. Añade skills de dominio en `.ai/skills/` (ver README ahí).
4. No copies `memory/` sensible a repos públicos.
