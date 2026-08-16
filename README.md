# AI Harness Template — plug-and-play multi-IA

**Versión:** `2.6.9` · [`VERSION`](VERSION) · [`CHANGELOG.md`](CHANGELOG.md) · [`VERSIONING.md`](VERSIONING.md)

Arnés para Cursor, Copilot, Claude, Gemini, Continue, Ollama y más.  
**Los usuarios no editan el arnés.** Solo dejan su código y chatean.

---

## Plug-and-play (3 pasos)

### 1) Abre este repo
Clona y abre la carpeta en Cursor (recomendado: `harness.code-workspace`).

### 2) Pon tu app aquí
```bash
git clone <url-de-tu-app> projects/mi-app
# o: cp -R ~/codigo/mi-app projects/mi-app
```
Cualquier nombre de carpeta sirve. Puedes tener varias: `projects/api`, `projects/web`, …

### 3) Escribe en el chat
```
Hola — trabaja sobre projects/mi-app. Quiero <objetivo en una frase>.
```

El agente **solo** debería:
- detectar la app y el stack,
- cristalizar tecnologías estables en `.ai/skills/` (automejora por iteración),
- asegurar un puntero mínimo `projects/<app>/.ai/HARNESS.md` (sin copiar el arnés entero),
- actualizar `.ai/memory/` (tú no lo tocas),
- proponer A/B antes de cambios importantes,
- ir guardando aprendizajes (crystallize / skills / memory),
- respetar safety-rails, read-budget y model-routing (menos tokens, menos riesgo).

Manual corto: [`projects/README.md`](projects/README.md) · guion: [`docs/getting-started/FIRST_SESSION.md`](docs/getting-started/FIRST_SESSION.md).

---

## Qué es automático (y qué no)

| Automático al chatear | No es un demonio 24/7 |
|---|---|
| Activar rules/bridges al abrir el workspace | Hace falta **abrir** el repo + **un mensaje** de chat |
| Mapear `projects/`, inferir stack, escribir memory | No corre solo con el Mac en idle |
| Gate, discovery, confidentiality, tono | Modelos muy débiles pueden fallar; por eso existe modo ultra |
| Auto-mejora en `memory/` + `audit/` tras turnos útiles | Si el chat no ocurre, no hay qué aprender |

**Sinergia:** sí, sesión a sesión, sin que edites `.ai/` ni `.cursor/`.

---

## Dónde está Absoluto++ / protocolos

| Archivo | Uso |
|---|---|
| [`.ai/protocols/operating-mode.md`](.ai/protocols/operating-mode.md) | Full |
| [`.ai/protocols/operating-mode.compact.md`](.ai/protocols/operating-mode.compact.md) | Default |
| [`.ai/protocols/operating-mode.ultra.md`](.ai/protocols/operating-mode.ultra.md) | Ollama / poco contexto |

También: `plug-and-play` · `session-gate` · `discovery` en `.ai/harness/`.

---

## Por IA

| Herramienta | Activación |
|---|---|
| Cursor | `.cursor/rules/` (automático) |
| Copilot | `.github/copilot-instructions.md` |
| Claude | `CLAUDE.md` |
| Gemini | `GEMINI.md` |
| Continue | `.continue/rules/` |
| Ollama | modo ultra + primer mensaje citando `AGENTS.md` |

---

## Confidencialidad

No pegues keys en el chat. Usa `.env` dentro de tu app bajo `projects/`.  
El agente no debe volcar secretos a `memory/`.

---

## Estructura

```
projects/                 ← TÚ pones las apps (plug-and-play)
.ai/                      ← arnés (el agente lo mantiene; tú no lo editas)
.cursor/ .github/ …       ← bridges
docs/getting-started/     ← manual opcional (no runtime)
harness.code-workspace
```

Efectividad: [`.ai/audit/architecture-score.md`](.ai/audit/architecture-score.md) · extras: [`NEXT_STEPS.md`](NEXT_STEPS.md).

---

## Modo avanzado (opcional)

Si alguien quiere **copiar** el arnés dentro de otro repo (en vez de usar `projects/`), ver [`docs/getting-started/INSTALL.md`](docs/getting-started/INSTALL.md).  
Para usuarios finales el camino recomendado es solo **plug-and-play** arriba.
