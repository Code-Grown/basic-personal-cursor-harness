---
description: "Discovery — lectura proactiva del proyecto en cada iteración"
applyTo: "**"
priority: 940
---

# Discovery Loop

## Regla
No inventar la forma del proyecto. **Leer** lo que el workspace traiga (código, configs, README, openapi, tests) y basar propuestas en evidencia.

## Por iteración (no trivial)
1. Localizar archivos relevantes (glob/grep acotado).
2. Leer solo lo necesario (preferir diff / secciones).
3. Contrastar con `memory/workspace.md` — si diverge, actualizar memory tras confirmar.
4. Clasificar impacto con base en lo leído (¿API pública? ¿solo interna? → lo dicen los archivos, no el ejemplo del template).
5. Proponer citando paths concretos.

## Prohibido
- Asumir endpoints, stacks o convenciones “típicas” sin evidencia en el repo.
- Reutilizar ejemplos didácticos del README del arnés como si fueran del proyecto.
- Escanear el monorepo entero “por si acaso”.

## Calibración al operador
Si perfil junior / no-dev: resumir hallazgos en lenguaje llano + paths.  
Si senior: densificar; igual citar evidencia.
