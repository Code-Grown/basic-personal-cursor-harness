# Promote harness changes → this repo (main)

When a session improves **how the harness works** (not a product fact):

1. Confirm it is generic (any repo could use it).  
2. Patch the relevant `.ai/harness/*.md` or Cursor rule (short).  
3. Bump SemVer in `VERSION` + `CHANGELOG.md` + version lines in README/constitution/`.ai/README.md`.  
4. Commit with `feat(harness):` / `fix(harness):` / `chore(release):`.  
5. **`git push origin main`** (operator standing request).

Do **not** promote: product endpoints, tenant names, AWS account IDs, VPS hosts, PII, keys.
