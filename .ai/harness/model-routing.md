# Model routing (generic)

Save cost **without** losing quality when the task is hard.

## Honest limit
- The **chat model** is chosen in the Cursor UI. The harness cannot switch it.
- The harness **must** set Task/subagent `model` so routine work does **not** inherit an expensive parent (e.g. Grok).

## Matrix

| Task class | Chat (recommend) | Task / subagent `model` |
|---|---|---|
| **Routine** — typo, one file, rename, narrow explore, lint, short docs | Prefer **Composer** | **`composer-2.5-fast`** (do not omit if parent is expensive) |
| **Standard** — local bug, small feature | Composer usually enough | Composer default |
| **High stakes** — architecture, security, production incident | Strong model (user choice) | Strong / inherit |
| Explicit user model request | Always honor | Always honor |

## Anti-waste
1. Expensive chat + routine task → one-line note that Composer would save; still execute.  
2. Routine Task: always pass Composer; never omit `model` if that inherits Grok/Sonnet/GPT.  
3. Do not spawn Task when one agent is enough.  
4. Do not “upgrade” to expensive models by habit — only by difficulty/risk or ask.  
5. Best outcome wins on high-stakes work.
