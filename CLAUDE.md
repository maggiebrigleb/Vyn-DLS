# Vyn-DLS

This repo holds the Vyn Web App design system spec: `DESIGN.md` (the current state) and `DECISIONS.md` (the running log of decisions, open questions and changes).

## Logging rule (required)

Every change to `DESIGN.md`, or to the Vyn Web App design-system page (https://claude.ai/artifact/CqA1i9k2gzTpfXUNT2hRJi), must update `DECISIONS.md` **in the same commit**:

- **Always** add a *Changelog* row: today's date, a one-line description, and the PR link. A commit can't reference its own hash.
- **When the user decides something,** add a `D-` row with status `firm` or `provisional`, attributed to them.
- **When you decide something** they haven't confirmed, add a `D-` row with status `proposed`, attributed to Claude.
- **For a new open question or to-do,** add a `Q-` row. When one is answered, move it to *Resolved questions* and point it at the decision.
- **Never delete or renumber entries.** Mark a replaced decision `superseded by D-0xx`.
- Keep `DESIGN.md`'s *Decisions, Deferred and Open Questions* summary in step with the log.
- `DESIGN.md` and the design-system page are separate. When one changes, say in the changelog row whether the other was updated too (see Q-014).

## Spec rules

- **Live Figma variables are the source of truth** (D-001). File: `LNixxQjUWEwccxM0LgcW6g`.
- **Token keys mirror the developer tokens,** and semantic tokens are never merged, even when values match (D-010). Values appear only in the front matter and the *Semantic tokens* table, so don't hard-code hex values elsewhere.
- **After editing `DESIGN.md`, run** `npx -y @google/design.md lint DESIGN.md`. Aim for 0 errors. The expected warnings are orphaned tokens, the disabled-state contrast and `missing-primary`.
