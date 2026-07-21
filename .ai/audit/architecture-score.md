# Architecture Score — efectividad del arnés

**Evaluación:** 2026-07-20 · release `2.1.1`  
Escala 1–5. Sin datos sensibles. Basada en diseño + uso en esta sesión de construcción (aún sin piloto largo en proyecto de producción).

| Dimensión | Score | Nota |
|---|---|---|
| Separación módulos | 5 | Núcleo `.ai/` vs bridges delgados; skills opcionales; memory del consumidor |
| Token efficiency | 4 | compact/ultra + router; riesgo: alwaysApply de 3 rules en Cursor si el modelo carga de más |
| Reversibilidad / gate | 5 | proponer-siempre + A/B + BREAKING/SENSITIVE frena bien |
| Confidencialidad | 4 | Política clara; enforcement real depende de disciplina humana + CI (gitleaks) |
| Claridad operador | 5 | README paso a paso + FIRST_SESSION + tono no-experto |
| Multi-IA transversal | 4 | Bridges sólidos en Cursor/Copilot/Claude; resto documentado, no todos auto-cargan |
| Discovery / no inventar | 4 | Bien especificado; efectividad = que el modelo obedezca en cada turno |
| Completitud vs peso | 4 | Completo para empezar; un poco denso si se carga el full protocol sin necesidad |
| **Promedio** | **4.4** | **Muy efectivo como template de arranque; el techo lo pone la disciplina del agente/IDE** |

## Veredicto

**Efectivo para empezar (alto ROI)** si:
- Se usa compact/ultra (no full en cada chat),
- Se completa `memory/workspace.md` + perfil en el proyecto consumidor,
- El operador responde A/B (el gate no se salta).

**Límites honestos:**
- No es un runtime ejecutable: es gobernanza por prompts/rules; modelos locales débiles pueden ignorar el gate.
- Sin CI de secretos, confidentiality es “mejor esfuerzo”.
- La efectividad real se mide tras 2–3 sesiones en un repo con código (piloto).

## Cómo subir el score a ~4.8
1. Piloto en un proyecto real + 1 línea en `audit/optimization.md` por fricción.
2. Secret scanning en CI del consumidor.
3. Acortar alwaysApply si se observa sobre-contexto en Cursor.
