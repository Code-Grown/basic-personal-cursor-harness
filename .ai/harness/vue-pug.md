# Vue/Nuxt · strict Pug

On **Vue / Nuxt** fronts: templates are **Pug**. Hard rule — no “later”.

Does not apply to Flutter, React, email HTML, `public/*.html`, SVG, Markdown.

## Required
1. **New** `.vue` → `<template lang="pug">` from the first line.  
2. **On touch** of a `.vue` with HTML `<template>` → **migrate that file now** (same iteration, same diff).  
3. **Same feature / folder** → migrate leftover HTML siblings.  
4. Do not add a temporary HTML template.  
5. If `pug` (or the repo plugin) is missing → add it to the front `package.json`. No other preprocessor.

## Craft
```pug
<template lang="pug">
v-card.pa-4
  h2.text-h6 {{ title }}
  v-btn(color="primary" variant="flat" @click="save") Save
</template>
```

- Vue attrs in parens: `v-if`, `v-for`, `@click`, `:to`.  
- Never `#[strong {{ expr }}]` — separate Pug tags.  
- Never TypeScript `!` in Pug attrs (`item!.id` → Pug reads `!=`). Use `?.`.  
- Indentation is the tree.

## Out of scope
Flutter · email HTML · bundler `index.html` / `app.html` · non-SFC files.

## Related
`ux-craft.md` · hub Nuxt skill. Do not undo tours/AI while converting (`change-strategy.md`).
