# AI product models · current catalog

When **implementing or updating product AI** (admin chat, assistant, `llm_client`, settings):

1. Load this file.  
2. Use the **API IDs** below in `MODEL_CATALOG` / defaults / UI.  
3. Keep **legacy** IDs as `tier: legacy` (do not delete — saved configs).  
4. On close: sync backend catalog (+ UI if hardcoded) and note `updated` date.

> Not the same as `model-routing.md` (Cursor agent models). This is for **product LLMs**.

**Updated:** 2026-08-09

## Recommended defaults (new installs)

| Provider | Default ID | Role |
|---|---|---|
| `gemini` | `gemini-3.6-flash` | Multimodal workhorse |
| `openai` | `gpt-5.6-luna` | High-volume / economical |
| `claude` | `claude-sonnet-5` | Balanced coding/chat |
| `cursor` | `gpt-5.6-luna` | OpenAI-compatible via `base_url` |

Premium options: `gpt-5.6-sol` · `claude-opus-5` · `claude-fable-5` · `gemini-3.1-pro-preview`.

## Catalog (API IDs)

### Gemini
`gemini-3.6-flash` (default) · `gemini-3.5-flash-lite` · `gemini-3.5-flash` · `gemini-flash-lite-latest` · `gemini-flash-latest` · `gemini-3.1-flash-lite` · `gemini-3.1-pro-preview` · legacy `gemini-2.5-*` / `2.0-*`

### OpenAI
`gpt-5.6-luna` (default) · `gpt-5.6-terra` · `gpt-5.6-sol` · `gpt-5.6` (→ Sol) · legacy `gpt-5*` / `gpt-4.1*` / `gpt-4o*` / `o4-mini`

### Anthropic
`claude-sonnet-5` (default) · `claude-opus-5` · `claude-fable-5` · `claude-opus-4-8` · `claude-haiku-4-5-20251001` · legacy `claude-sonnet-4-6` / `4-5` / `opus-4-6`

### Cursor
Prefer `gpt-5.6-*` + `claude-sonnet-5` via compatible `base_url`.

## Python shape

```python
DEFAULT_MODELS = {
    "gemini": "gemini-3.6-flash",
    "openai": "gpt-5.6-luna",
    "claude": "claude-sonnet-5",
    "cursor": "gpt-5.6-luna",
}
```

## Maintenance
Refresh when adding AI to a product or at least quarterly. Promote generic updates here + bump VERSION.
