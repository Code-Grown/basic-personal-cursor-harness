# Gap-fill · if it is missing, create it

When the operator says something **does not exist**, is missing, or “should be there”:

**Do not** stop at “it isn’t there”. **Create** a compensation in the same iteration, with care and craft (`ux-craft` + `change-strategy`).

## What to create
- UI gap → written empty state + CTA, or the control/screen they expected.  
- Flow gap → “continue in…” bridge or a usable stub (not a mute 404).  
- Guide gap → tour step / in-situ `?` (`ux-craft` §5c).  
- AI gap → chat entry or a real-name interpretation.  
- Data gap → honest empty + how to load it; do not invent facts.

Care = tokens, 8px radius, buttons inside the frame, tours current, do not undo what works.  
Craft = the compensation feels like the product, not a generic placeholder.

## Pace
| Kind | Action |
|---|---|
| SAFE (empty state, button, voice, toast X, tour step, label) | Do it now |
| Non-trivial new piece | Short A/B (≤8 lines) and **build** in the same turn unless they asked for design only |
| BREAKING / prod / destructive / secrets | `confirm-execute` + `safety-rails` |

## Avoid
“Not in the repo” with nothing created. Invented endpoints or data. Drive-by rewrites.

## Related
`confirm-execute.md` · `change-strategy.md` · `ia-first.md`.
