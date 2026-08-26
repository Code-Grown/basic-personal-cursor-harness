# Model routing (generic)

Prefer **quality and understanding**. Forcing cheap models on Tasks often missed requirements and did not save tokens in practice.

## Honest limit
- The **chat model** is chosen in the Cursor UI. The harness cannot switch it.
- Recommend a strong chat model (e.g. Grok 4.5 when available).
- Task/subagents: **inherit** the parent (`inherit` or omit `model`). Do **not** force Composer.

## Matrix

| Task class | Chat (recommend) | Task / subagent `model` |
|---|---|---|
| **Default** — routine, standard, or high stakes | Strong model (user choice; prefer Grok when used) | **inherit** |
| Explicit user model request | Always honor | Always honor |

## Rules
1. Do not downgrade to Composer for “savings” or routine work.  
2. Do not spawn Task when one agent is enough.  
3. Composer / other models only when the user asks **explicitly**.  
4. Best outcome wins.  
5. **Any model** (Auto included): new work follows the existing visual/technical line (`line-continuity.md`). The picker does not reset the craft.
