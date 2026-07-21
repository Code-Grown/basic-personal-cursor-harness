# Adapter: GitHub Copilot (VS Code / github.com)

## ¿Por qué existe `.github/`?
Copilot (y parte del ecosistema GitHub) carga **automáticamente**:
- `.github/copilot-instructions.md`
- opcionalmente `.github/instructions/*.instructions.md` y prompts

Sin esa carpeta, Copilot **no** ve el arnés. Cursor usa `.cursor/`; Claude usa `CLAUDE.md`.  
`.github/` no es ruido: es el bridge de Copilot.

## Wiring
1. Mantener `copilot-instructions.md` corto (<80 líneas) → apunta a `.ai/`.
2. Prompts en `.github/prompts/` para modos compact/ultra.
3. Stack del proyecto: `.github/instructions/` (lo añade el consumidor).
