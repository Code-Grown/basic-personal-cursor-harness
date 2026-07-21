# Adapter: Ollama / modelos locales

## Carga obligatoria (solo esto)
1. `.ai/protocols/operating-mode.ultra.md`
2. `.ai/constitution/workspace.md`
3. `.ai/harness/session-gate.md` (o resumen 10 líneas si contexto <8k)
4. `.ai/skills/confidentiality.md`

## No cargar por defecto
agents/ · audit/ · skills de dominio · memory entera · modo full

## Ritmo
- Perfil: máx 4 preguntas/turno si contexto bajo (P1,P2,P5,P6).
- Propuestas ≤8 líneas + A/B.
- Tras OK: editar; cerrar ≤5 líneas + 1 check comprensión.
