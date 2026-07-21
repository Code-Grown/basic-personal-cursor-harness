# Modo avanzado — copiar el arnés a otro repo

**Usuarios finales:** no uses esto. Usa plug-and-play: deja apps en `projects/` del repo del arnés (ver README raíz).

Esto es solo si necesitas el arnés **dentro** de un repo ya existente (sin carpeta `projects/` del template).

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
```

En ese modo, adapta mentalmente: el código puede estar en la raíz de `TARGET` en vez de `projects/`. El agente debe discovery sobre la raíz.
