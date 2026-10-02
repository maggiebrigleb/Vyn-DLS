# Vyn-DLS

This repo holds the Vyn Web App design system spec: `DESIGN.md` (the current state) and `DECISIONS.md` (the running log of decisions, open questions and changes).

## Logging rule (required)

Every change to `DESIGN.md`, or to a Vyn Web App design-system page (v1 https://claude.ai/artifact/CqA1i9k2gzTpfXUNT2hRJi, v2 template https://claude.ai/artifact/SHWJ8Cx6KoboTtmGvQfEa4, v2 branded https://claude.ai/artifact/PjtjrkSpD9PgtRG47w1q9g, source `site/design-system-v2.html`), must update `DECISIONS.md` **in the same commit**:

- **Always** add a *Changelog* row: today's date, a one-line description, and the PR link. A commit can't reference its own hash.
- **When the user decides something,** add a `D-` row with status `firm` or `provisional`, attributed to them.
- **When you decide something** they haven't confirmed, add a `D-` row with status `proposed`, attributed to Claude.
- **For a new open question or to-do,** add a `Q-` row. When one is answered, move it to *Resolved questions* and point it at the decision.
- **Never delete or renumber entries.** Mark a replaced decision `superseded by D-0xx`.
- Keep `DESIGN.md`'s *Decisions, Deferred and Open Questions* summary in step with the log.
- **Keep `DESIGN.md` and the v2 template page in sync (D-032).** Any design-system change made in `DESIGN.md` must also be made on the template page in the same piece of work, so a design that references the page as its design system stays accurate. Update the branded page too where it shows the change, on a best-effort basis: it can't be referenced as a working design system. Say in the changelog row which surfaces were updated.
- **Icons:** use the Figma exports from Vyn Global's Iconography page (MUI and Bootstrap sets). Never redraw or approximate an icon (D-035).

## Spec rules

- **Live Figma variables are the source of truth** (D-001). Files: Vyn Web App `LNixxQjUWEwccxM0LgcW6g` (semantic tokens, text styles) and Vyn Global `PXB9RwThJHEP09SPoKZg4J` (primitives).
- **Token keys mirror the developer tokens,** and semantic tokens are never merged, even when values match (D-010). Values appear only in the front matter and the *Semantic tokens* table, so don't hard-code hex values elsewhere.
- **After editing `DESIGN.md`, run** `npx -y @google/design.md lint DESIGN.md`. Aim for 0 errors. The expected warnings are orphaned tokens, the disabled-state contrast and `missing-primary`.
