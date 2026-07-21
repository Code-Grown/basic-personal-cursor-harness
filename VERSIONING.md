# Versionado semántico del arnés

## Archivos a tocar en cada release

1. `VERSION` ← número canónico (`MAJOR.MINOR.PATCH`)
2. `CHANGELOG.md` ← mover `[Unreleased]` → `[X.Y.Z] — YYYY-MM-DD`
3. `.ai/constitution/workspace.md` ← línea de versión
4. `.ai/README.md` ← línea de versión
5. Tag git: `vX.Y.Z` (anotado)

## Comandos sugeridos

```bash
# 1) Editar VERSION / CHANGELOG / refs
# 2) Commit
git add VERSION CHANGELOG.md VERSIONING.md .ai/constitution/workspace.md .ai/README.md
git commit -m "chore(release): v$(cat VERSION)"

# 3) Tag
git tag -a "v$(cat VERSION)" -m "Release v$(cat VERSION)"

# 4) Push (cuando decidas)
# git push origin main --tags
```

## Ejemplos

| Cambio | Versión |
|---|---|
| Fix typo en README | `2.1.0` → `2.1.1` |
| Nuevo adapter (p.ej. Zed) | `2.1.0` → `2.2.0` |
| Renombrar `.ai/protocols/` rompiendo paths documentados | `2.1.0` → `3.0.0` |
