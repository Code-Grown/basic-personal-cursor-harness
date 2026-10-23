# Line continuity · any model, same line

The picker (Grok, Auto, Composer, other) does **not** reset the craft.  
A **new** requirement follows the visual, technical, and design line **already in** the app / skills / harness.

Does not replace `change-strategy.md` (don’t undo fixes) or `ux-flow-first.md` (redesign when asked).

## Required (every model)
1. Read the product/stack skill and existing tokens/components **before** painting or inventing stack.  
2. Same family: Pug on Vue/Nuxt (`vue-pug.md`) · `ux-craft` chrome · quality bars of this workspace.  
3. No new design system, no “model taste”, no throwaway HTML, no default Material dump.  
4. Extend the neighbor pattern (same card, radius, toast, form, table). If none → hub/core bars, not the LLM default.  
5. If the ask fights the line → **say so** and propose A (keep line) vs B (change it, `ux-flow-first` if UX). No silent pivot.  
6. Inside what the repo already does, continue. Reuse the library, close the other side, and finish the missing step without waiting. Stop and ask only when the change brings a pattern the repo does not use. The connection must be checked and the path finished. The first draft that compiles is not the delivery. Before closing, the agent checks those points and fixes what fails. It does not leave that finding for the operator. If the operator says they are tired of it, that they already explained it, or repeats the complaint, the previous turn failed: fix it in this turn without asking them to rephrase.

## What this does not break
- **Asked** redesign → `ux-flow-first` + confirm; this file does not veto it.  
- Gap-fill → create the missing piece **on** the line, not a generic widget.  
- New app → inherit harness bars until it has its own tokens.  
- Auto/Composer: we cannot force the chat model; we **can** require this checklist. Tasks inherit (`model-routing.md`).

## When to load
Any new feature/UI/code, **even if** the chat is on Auto or another model.
