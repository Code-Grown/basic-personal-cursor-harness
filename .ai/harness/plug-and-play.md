---
description: "Plug-and-play — autonomía sin que el usuario edite el arnés (CORE)"
applyTo: "**"
priority: 960
---

# Plug-and-play (autónomo)

## Contrato con el usuario
El usuario **no modifica** `.ai/`, rules ni protocols. Solo:
1. Clona este repo (o lo abre).
2. Pone su código en `projects/<nombre-app>/` (cualquier nombre de carpeta).
3. Habla en el chat.

El **agente** hace el resto: descubrir, mapear, proponer, persistir, auto-mejorar.

## Bootstrap obligatorio (inicio de sesión / primer mensaje)
Ejecutar en silencio o con un resumen corto (≤8 líneas), **sin pedir que editen archivos del arnés**:

1. Listar `projects/*` (dirs de primer nivel, ignorar `.gitkeep` / README).
2. Si no hay proyectos → decir amablemente: “Deja tu app en `projects/nombre/` y dime cuando esté.” No inventar código.
3. Si hay proyectos → para cada uno (prioridad al que mencione el usuario):
   - Comprobar `projects/<app>/.ai/HARNESS.md` (ver `repo-pointer.md`); si falta → crear solo el mínimo (`templates/project-HARNESS.md`).
   - Detectar stack por evidencias: `package.json`, `go.mod`, `pyproject.toml`, `Cargo.toml`, `pom.xml`, `*.csproj`, `docker-compose.yml`, etc.
   - Si el stack es estable y aún no hay skill → crear/actualizar skill delgado (`tech-skills.md`).
   - Leer README del proyecto si existe (solo lo necesario).
   - Actualizar `.ai/memory/workspace.md` (el agente escribe; el usuario no).
   - No copiar el arnés completo dentro de cada app.
4. Completar `.ai/memory/operator-profile.md` con **inferencias + defaults**:
   - Ritmo: `proponer-siempre` (default)
   - Stack: el detectado
   - Idioma: el del chat del usuario
   - Nivel: `desconocido` hasta que se note en la conversación (calibrar jerga suave)
5. Preguntar **solo lo no inferible** (máx 2–3): objetivo de sesión y restricciones de riesgo/prod. El resto se asume con defaults seguros.
6. Anunciar en 3–5 líneas: qué encontró, qué asumió, y la propuesta A/B si ya hay pedido.

## Durante cada iteración
- Discovery sobre `projects/` (y roots del workspace), no sobre teoría.
- Tras cambio útil → update-trigger **sin pedir permiso** (memory/audit), sin secretos.  
  Si es patrón rutina/estratégico → 1 viñeta (`crystallize.md`). Si huele a personal/empresa → **anticipar** (`safety-rails.md`); no guardar en silencio.
- Feature/UI nueva, cualquier modelo → misma línea (`line-continuity.md`). No reinventar diseño/stack.
- Si el usuario está confundido → reexplicar como **guía de trabajo** (cómo el asistente hace el oficio); no exigir que lea el arnés.
- Nunca: “edita `.ai/memory/...`”. Si falta dato → el agente lo escribe o pregunta en chat.

## Qué es autónomo y qué no
| Autónomo (agente) | Requiere al menos 1 mensaje de chat |
|---|---|
| Mapear proyectos, stack, memory | Sí — no hay demonio en background |
| Gate A/B, comprehension | Sí |
| Auto-mejora en patterns/optimization | Sí, al cerrar turnos con aprendizaje |
| Editar código del usuario | Solo tras OK en no-trivial |

## Zona sagrada
No reescribir protocols/constitution/adapters salvo que el usuario pida explícitamente mejorar el arnés.  
Memory + audit + generated = zona de escritura autónoma del agente.
