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

## 5. Global chrome (every app inherits)

Same token on cards, panels, dialogs, menus, toasts. Apply when you touch; do not restyle the whole site.

| Piece | Done when… |
|---|---|
| **Radius** | `--radius-panel: 8px` (half of typical 16/xl). Never >12 on cards. Same everywhere. |
| **Proportion** | Same-type cards: same padding (16) and radius. Do not mix 8 with 24. |
| **Toast** | Always dismissible: **X** and swipe. Never timeout-only. |
| **Modal / popup** | Actions **inside** the frame (footer with panel padding). No overflow, no clash. |
| **Modal buttons** | Desktop: grouped right (secondary + primary). Mobile: full-width stack or group + overflow; size by viewport; gap 8. |
| **Label vs placeholder** | Label outside or persistent outlined. Placeholder ≠ title. Hint below. No collision. |
| **Auth fields** | Login/register/etc.: **fixed** surface bg at rest and focus. Do not darken on blur. `on-surface` text. |
| **Mobile tables** | Do not crush columns. Card-per-row **or** scroll + sticky first col + row actions. Compact, readable. |
| **Help ?** | Non-obvious field/control: `?` icon next to the **label**. One precise sentence. See §5c. |

Anti-pattern: `rounded-xl`/24px per card; snackbar without X; dialog buttons clipped at 320px; same text as label and placeholder; field goes dark when idle; wide data-table on a phone.

## 5c. Help ? (short · accurate · precise)

Fields, metrics, or actions the **label does not explain** get an in-situ `?`. Does not replace the tour or AI chat.

**Done when:**
1. Theme icon (`mdi-help-circle-outline` / Flutter outline). ~18px. Next to the label, not instead of it.  
2. Hover **and** tap. Real `aria-label` (“What this means”).  
3. Copy: **one idea**, 1–2 sentences. Real concept name. Product fact — if you don’t know, skip the `?`.  
4. Reuse the app helper (`v-tooltip`, existing Help component). No new widget per screen.

**Not:**
- A `?` on every obvious field (Name, Email).  
- A paragraph, lorem, harness jargon, “click to learn more”, invented facts.  
- A replacement for the tour or page lead. Tour = first use; `?` = always, that concept.

When you touch a non-obvious form/metric with no `?` → add it in the same iteration.

## 6. Voice on every AI chat
Every AI composer has **voice input**. Reuse the app composable if it exists. If the browser lacks SpeechRecognition, the mic stays visible and explains the fallback. Enter sends · Shift+Enter newline.

## When to load
UI · copy · AI chat · tour · empty state · clone · new app · toast/modal/form/table.

## Related
Flow → `ux-flow-first.md` · IA-first → `ia-first.md` · missing → `gap-fill.md` · models → `ai-product-models.md` · don’t undo → `change-strategy.md`.
