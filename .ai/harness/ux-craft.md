# UX craft · working guide · fine finishing

Required on **every app** (existing, clone, or new) when touching UI, copy, or AI surfaces.

Internal name: harness.  
**Human name:** **working guide** — how the assistant does the craft in this app.  
ES: **guía de trabajo**.

> Flow-first stays in `ux-flow-first.md`. This is the **care**: real names, good interpretations, boxes and margins.  
> Do not rewrite screens “for looks”. Apply when you touch. Do not undo working tours/AI (`change-strategy.md`).

## 1. A name the user understands

In product copy (web, app, AI chat, tours, empty states):

| Use | Never (end user) |
|---|---|
| The **real concept name** the product already uses | harness, skill, compact, HARNESS, alwaysApply, prompt, bridge |
| “Help”, “Guide”, “Summary”, or the product’s own name | “the harness said…” |
| One line a non-expert can repeat | Internal IDs, raw JSON as the title |

If you must explain the system: *“it’s the working guide: the assistant uses everyday names and leaves the next step ready.”*

New/cloned app: inherit this bar from the first `HARNESS.md`. Do not copy the harness; do apply the craft.

## 2. AI interpretations (done well)

Each AI box / bubble / summary:

1. **Title** = real concept name.  
2. **One line** = what it means now, in the product language.  
3. **Useful detail** = only what helps act (no filler, no invented facts).  
4. **Next step** = one CTA or “continue in…”.

- One idea per box.  
- Correct and domain-specific. If you don’t know, don’t pad.  
- JSON dumps are secondary (pretty fence), **never** the main explanation.

## 3. AI boxes, margins, chrome

Reuse the app’s renderer and tokens. No new design system.

Done when:

- Even padding; last child does not leak margin out of the card.  
- Page rhythm: title → subtitle with air → box.  
- Radius/border/color from theme. Contrast in light mode.  
- Icon aligned to the text line.  
- Lists and rules with internal gap; inline code quiet; code blocks padded.

Anti-pattern: default card dump, raw markdown without a host, boxes flush to the edge, “No data”, lorem, TODO, tech keys as labels.

## 4. Fine finishing (fronts and apps)

- Consistent gap scale. Optical alignment.  
- One visible primary action. Empty states written with care.  
- Theme hover/focus/disabled.  
- Mobile ≠ admin clone (`ux-flow-first` bar 7).  
- No debug leftovers. UI language = product language.

Care = **detail you feel while using**, not more widgets.

## When to load
UI · copy · AI chat/markdown · tour · empty state · clone · new app with a screen.

## Related
Flow → `ux-flow-first.md` · LLM ids → `ai-product-models.md` · don’t undo → `change-strategy.md`.
