# Change strategy · do not undo prior fixes

Before non-trivial edits: **account for prior corrections** and **pick a strategy** with low regression risk.

## Why
A “cleanup” or blind rewrite often **breaks** what was already fixed. Prefer being conservative with working behavior.

## Pre-change checklist (required unless SAFE trivial)

1. **Prior-fix context** (minimum useful):
   - Recent `git log` / blame on the touched area.
   - Relevant skill / compact / ADR / product notes.
   - Nearby tests and intentional comments (`FIXME` / `NOTE` / decisions).
2. **Intent of current code**: odd shape may be a deliberate fix, not a bug.
3. **Strategies** (at least 2 when unsure):
   - **A** additive / surgical (preferred).
   - **B** refactor / rewrite (only if A cannot meet the ask).
   - For each: blast radius · prior behaviors preserved · rollback.
4. **Choose** the smallest radius that satisfies the request. If B risks a prior fix → justify or ask OK.
5. **Propose** via `confirm-execute.md` including: *what will not change* and *which prior fix is preserved*.

## Anti-regression rules
- Prefer **additive** edits and small diffs. Do not rewrite whole files for style.
- Do not remove guards, branches, flags, tests, or fix comments “because unused” without evidence.
- Do not “unify/simplify” converged patterns without reading the decision/skill.
- If the ask conflicts with a prior fix/ADR → **surface the conflict**; do not silently overwrite.
- After edits: sanity-check that prior behavior still holds (test/lint when cheap).
- Harness: additive core/template changes; do not delete modules for cleanup without intent/backup.

## When to load
- Features, bugfixes, refactors, schema, deploy, infra, non-trivial harness.
- SAFE trivial (typo, path, one-line FAQ): skip the full ritual; still do not delete neighboring fixes.

## Related
- Confirm → `confirm-execute.md`
- Safety → `safety-rails.md`
- Close → crystallize / self-improve (note *why not to touch X* when useful).
