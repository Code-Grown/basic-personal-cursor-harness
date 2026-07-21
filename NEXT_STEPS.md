# Siguientes pasos — potenciar el arnés (sin hinchar el CORE)

Este archivo sugiere herramientas y capas **opcionales**.  
El arnés actual ya es el mínimo completo para empezar. No instales todo a la vez.

## Prioridad alta (mejor ROI con este template)

| Paso | Qué | Por qué |
|---|---|---|
| 1 | Copiar arnés a 1 proyecto real y completar `memory/workspace.md` + perfil | Valida el gate en la práctica |
| 2 | Añadir 1–2 skills de dominio delgadas | El router empieza a ahorrar tokens de verdad |
| 3 | Elegir 1 IDE primario + 1 backup (p.ej. Cursor + Claude o Copilot) | Evita divergencia de reglas |
| 4 | Secret scanning en CI (gitleaks / trufflehog) | Refuerza confidentiality fuera del chat |
| 5 | Pre-commit (hooks) alineado a quality.yaml | El agente no es el único gate |

## Herramientas de mercado que encajan bien

### IDEs / agentes en editor
| Herramienta | Encaje con el arnés | Nota |
|---|---|---|
| **Cursor** | Nativo via `.cursor/rules` | Mejor default hoy para este repo |
| **VS Code + Copilot** | Nativo via `.github/` | Por eso existe `.github` |
| **Claude Code** | `CLAUDE.md` | Bueno en repos grandes con CLI |
| **Windsurf** | `AGENTS.md` + rules | Cuidado con sobre-indexar `.ai/` |
| **JetBrains AI** | Attach selectivo | Manual pero sólido en monorepos JVM |
| **Continue.dev** | `.continue/rules` | Open, multi-modelo, bueno con Ollama |
| **Cline / Roo** | Custom instructions | Alta autonomía → respetar gate |
| **Zed AI** | Rules / AGENTS | Ligero; cargar ultra/compact |

### CLI / automatización
| Herramienta | Encaje | Nota |
|---|---|---|
| **Aider** | `--read` de archivos CORE | Ideal git-native |
| **OpenAI Codex CLI / similares** | System = AGENTS.md | Misma disciplina de gate |
| **Gemini CLI** | `GEMINI.md` | Bridge ya incluido |
| **Ollama + Continue/Aider** | modo `ultra` | Priorizar tokens |

### Memoria / conocimiento (opcional, ADVANCED)
| Herramienta | Cuándo | Riesgo |
|---|---|---|
| **Repo-local `memory/` (ya incluido)** | Siempre | Ninguno si sin secretos |
| **Notion/Linear como fuente** | Solo resúmenes en memory | No volcar tickets sensibles |
| **RAG sobre el monorepo** | Repos enormes | Puede quemar tokens; preferir índices |
| **MCP servers** (docs, issue tracker, DB readonly) | Cuando el agente deba consultar sistemas vivos | Scope mínimo; nunca MCP con secretos en claro |

### Calidad / seguridad
| Herramienta | Rol |
|---|---|
| **gitleaks / trufflehog** | Secretos en git |
| **Semgrep / CodeQL** | Patrones inseguros |
| **Dependabot / Renovate** | Supply chain |
| **Policy-as-code** (OPA, etc.) | Si hay compliance formal |

## Qué NO añadir al CORE todavía
- Más packs de dominio pesados (terraform, etc.) → skills delgadas en el proyecto
- Duplicar protocols en cada bridge
- Auto-apply total sin gate
- Memoria cloud con datos de negocio

Nota: `trading-ml.md` ya es pack **opcional** accesible (no asume expertos); actívalo solo si el repo es de mercados.

## Cómo usar este archivo
1. El agente, tras una sesión, puede sugerir **un** ítem de aquí si aporta.
2. Registrar adopción en `audit/optimization.md` (1 línea).
3. Si una herramienta nueva necesita bridge → crear `.ai/adapters/<nombre>.md` + entry root si auto-carga (como `CLAUDE.md`).

## Próxima revisión sugerida del arnés
- [ ] ¿Algún bridge sobra o falta en tu flujo real?
- [ ] ¿El modo ultra basta en Ollama 7–14B?
- [ ] ¿Session-gate se respeta o hay que acortarlo más?
