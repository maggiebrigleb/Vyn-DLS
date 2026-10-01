# Vyn Web App design system: decisions, questions and changes

A running log for [`DESIGN.md`](DESIGN.md) and the Vyn Web App design system as a whole: the Figma file, the design-system page and the codebase conventions. `DESIGN.md` describes the system as it is now. This file records **why** it's that way, what's still open, and what changed when.

**How to use this file**
- **Never delete an entry.** When something changes, mark the old entry `superseded by D-0xx` and add a new one, so the history stays readable.
- **IDs are permanent:** `D-` for decisions, `Q-` for open questions and to-dos.
- **When a question is answered,** move it to *Resolved questions* with a pointer to the decision that answered it.
- **Every change to `DESIGN.md`** or the design-system page adds a *Changelog* line in the same commit.
- **Statuses:**
  - **firm:** decided and in force.
  - **provisional:** in force, but expected to change.
  - **proposed:** written into `DESIGN.md` by Claude and not yet confirmed. Treat it as a draft until someone confirms it.
  - **deferred:** deliberately parked, so leave it as is.
  - **superseded:** replaced by a later entry.

**Links**
- Figma: [Vyn Web App](https://www.figma.com/design/LNixxQjUWEwccxM0LgcW6g/Vyn-Web-App)
- Design-system page (private, shared from its own Share menu): https://claude.ai/artifact/CqA1i9k2gzTpfXUNT2hRJi
- PR: [maggiebrigleb/Vyn-DLS#1](https://github.com/maggiebrigleb/Vyn-DLS/pull/1)

---

## Decisions

| ID | Date | Decision | Status | Decided by | Why / notes |
|---|---|---|---|---|---|
| D-001 | 2026-09-29 | **Live Figma variables are the source of truth.** Where the Foundations Documentation page disagrees with a variable, the variable wins. | firm | Maggie | The documentation page is out of date (see Q-001). |
| D-002 | 2026-09-29 | **The codebase uses the latest Bootstrap (5.3.x).** Where Figma is silent, Bootstrap's components and usage guidance apply, themed with Vyn tokens. | firm | Maggie | The brand uses many stock Bootstrap components. |
| D-003 | 2026-09-29 | **The web app is desktop-only for now.** The design target is 1440×900, and there are no tablet or mobile layouts. | firm | Maggie | The 1280px minimum width is a separate proposal (D-016). |
| D-004 | 2026-09-29 | **Motion uses Bootstrap 5's default transitions.** There are no Vyn motion tokens, and `$enable-reduced-motion` stays on. | firm | Maggie | |
| D-005 | 2026-09-29 | **Placeholder components are TBD:** Breadcrumb, Chip/Tag, Filters, Modal, Pagination, Progress, Table and Video Player. Until they're designed, use the stock Bootstrap 5 component with Vyn tokens. | firm | Maggie | The fallback follows from D-002. |
| D-006 | 2026-09-29 | **The focus ring stays classic Bootstrap blue** (#007BFF border, #80BDFF ring at 40%, 0.25rem). It's intentionally the only blue in the system. | provisional | Maggie | "For now." Bootstrap 5's own default would derive the ring from `$primary`. |
| D-007 | 2026-09-29 | **The BETA pill is a temporary placeholder.** Its purples (#7C3AED, #352D40, #4B3175) aren't system colors. Don't reuse them. | firm | Maggie | |
| D-008 | 2026-09-29 | **The sidebar is 250px wide** when expanded, and the Vyn Viewer drawer's left inset follows at 290px. | firm | Maggie | Replaces 249px, which was off the 4/8px grid. |
| D-009 | 2026-09-29 | **The Workflow switcher is a Medium Button** with a 14px (`--font-s`) label, and matches the Button component as a whole. | firm | Maggie | |
| D-010 | 2026-09-29 | **Token names mirror the developer tokens.** Each key is the CSS variable minus its category prefix (`text-secondary` = `--color-text-secondary` = Figma `Text/text-secondary`). Semantic tokens are **never merged**, even when values match. | firm | Maggie | The DLS is under construction and values will change, so each token must stay separate and easy to swap. |
| D-011 | 2026-09-29 | **Tag token renames:** `tag-chip-success-border` → `tag-success-border`, `tag-warning-bg` → `tag-warning`, `tag-danger-bg` → `tag-danger`. | firm | Maggie | Commit `69bad5b`. |
| D-012 | 2026-09-29 | **Neon green (Neon Green/800) is reserved for Vyn AI outputs and the logo.** | provisional | Maggie | Part of making AI outputs more transparent, helpful and actionable. Subject to change. |
| D-013 | 2026-09-29 | **AI UI scope** covers how Vyn AI's outputs (summaries, labels, evidence frames) are presented in the desktop web app. AI nudges (the mobile app) and Agentic Toolbox are out of scope. | firm | Maggie | From the assignment brief. |
| D-014 | 2026-09-29 | **Secondary outline button border:** keep `button-secondary` (Grey/200, about 1.2:1 on white) for now. | deferred | Maggie | To be resolved at a later date. |
| D-015 | 2026-09-29 | **Dark mode:** there's only a Light mode. Don't build dark themes for the work area. | deferred | Maggie | To be resolved at a later date. |
| D-016 | 2026-09-29 | **Minimum supported width is 1280px.** Below that, the page scrolls horizontally rather than reflowing. | proposed | Claude | Taken from the Navbar component's base width in Figma. Needs confirming (Q-011). |
| D-017 | 2026-09-29 | **Two greens with separate jobs:** "action green" (Green/600, `button-primary`) for UI actions, and "neon brand green" for Vyn AI and the logo. | proposed | Claude | Follows from D-012. Figma still calls Green/600 "Branding main green" (Q-007). |
| D-018 | 2026-09-29 | **Neon on light grounds is only a fill behind `text-primary`.** It's never text, a thin border or a lone icon on white (1.7:1). On `background-dark` it can be text or a mark (8.5:1). | proposed | Claude | A WCAG contrast requirement that follows from D-012. |
| D-019 | 2026-09-29 | **One Vyn AI marker:** every AI output combines neon, a "Vyn AI" text label and, optionally, the Vynnie mark, placed on the output's container. | proposed | Claude | A direction, not a spec. There are no AI components in Figma yet (Q-006). |
| D-020 | 2026-09-29 | **Cards keep Bootstrap 5's default radius (0.375rem) and border** (`$border-color-translucent`). Every other control uses `radius-s` (4px). | proposed | Claude | Matches the Figma card exactly (6px, black ~18%). |
| D-021 | 2026-09-29 | **Standard name: "Agentic Toolbox"** (not "Agent Toolbox" or "Smart Agent Toolbox"). | proposed | Claude | Matches the sidebar label. |
| D-022 | 2026-10-01 | **This file is the running log** of decisions, questions and changes. `CLAUDE.md` requires every design-system change to update it. | firm | Maggie | |

## Open questions and to-dos

| ID | Raised | Question / to-do | Owner | Notes |
|---|---|---|---|---|
| Q-001 | 2026-09-29 | Regenerate the Figma Foundations Documentation page from the live variables. Its Alert table is out of date, and several Tag and Chip rows render #000000. | Design | See D-001. |
| Q-002 | 2026-09-29 | Should the card radius and border get Vyn token names (for example `--radius-m: 6px` and `Border/border-translucent`)? | Design | See D-020. |
| Q-003 | 2026-09-29 | Add semantic tokens for the primitives Figma binds directly: `grey-500` (workflow-switcher border), `grey-600` (navbar icon button), `grey-700` (sidebar divider) and `neon-green-800` (logo). | Design | They currently can't be swapped like the rest. |
| Q-004 | 2026-09-29 | Add semantic tokens for success and warning fills, so Bootstrap's `$success` and `$warning` don't map to primitives. | Design | |
| Q-005 | 2026-09-29 | Add a Figma text style for the sidebar eyebrow label (10px Bold, +2px, uppercase)? | Design | It's currently composed from primitives. |
| Q-006 | 2026-09-29 | Create `AI/*` semantic tokens and an AI output card or tag component, so the provisional neon rule can change in one place. | Design | See D-012 and D-019. |
| Q-007 | 2026-09-29 | Update the Figma description of Green/600 ("Branding main green"), since neon is the brand color. | Design | See D-017. |
| Q-008 | 2026-09-29 | Do results produced by Agentic Toolbox agents (for example auto-triage categories) count as Vyn AI outputs that get the neon marker? | Maggie | The Toolbox UI itself is out of scope (D-013). |
| Q-009 | 2026-09-29 | Document the remaining component sets. Figma counts 33 sets and 9 standalone components, and 15 are documented. | Design | |
| Q-010 | 2026-09-29 | Review the marketing site (vyntelligence.com) for voice. It couldn't be fetched from the drafting environment. | Maggie | Voice currently relies on the Brand Feel audit. |
| Q-011 | 2026-09-29 | Confirm the 1280px minimum supported width. | Maggie | See D-016. |
| Q-012 | 2026-09-29 | Is a logo version for light backgrounds needed? Figma only has the dark-background logo. | Design | |
| Q-013 | 2026-09-29 | In Figma, rebind the Workflow switcher label to the `S` font-size variable. It currently binds a variable named `xs` that resolves to 14px. | Design | See D-009. |
| Q-014 | 2026-10-01 | Keep `DESIGN.md` and the design-system page in sync. They're separate, so changing one doesn't update the other. Decide whether one should be generated from the other. | Maggie | Until then, `CLAUDE.md` requires checking both. |

## Resolved questions

| ID | Raised | Question | Resolved | Answer |
|---|---|---|---|---|
| R-001 | 2026-09-28 | Which Bootstrap version does the codebase use? | 2026-09-29 | The latest, 5.3.x (D-002). |
| R-002 | 2026-09-28 | Does the app need tablet or mobile layouts? | 2026-09-29 | No, it's desktop-only (D-003). |
| R-003 | 2026-09-28 | Is there a dark mode? | 2026-09-29 | Deferred (D-015). |
| R-004 | 2026-09-28 | What should happen with the ~27 undocumented components? | 2026-09-29 | The placeholders are TBD (D-005). The rest is tracked in Q-009. |
| R-005 | 2026-09-29 | What motion values should be used? | 2026-09-29 | Bootstrap 5 defaults (D-004). |
| R-006 | 2026-09-29 | Keep the blue focus ring or switch to green? | 2026-09-29 | Keep blue for now (D-006). |
| R-007 | 2026-09-29 | Should the BETA pill's purples be tokenized? | 2026-09-29 | No, it's a placeholder (D-007). |
| R-008 | 2026-09-29 | The 249px sidebar is off-grid. What width? | 2026-09-29 | 250px (D-008). |
| R-009 | 2026-09-29 | Two font-size variables (`xs` = 14px and `XS` = 12px) are in play. Which applies? | 2026-09-29 | 14px (S), matching the Button component (D-009). Figma cleanup is Q-013. |
| R-010 | 2026-09-29 | Should token names be invented roles (`ink`, `canvas`) or match the system? | 2026-09-29 | Match the developer tokens and never merge them (D-010). |
| R-011 | 2026-09-29 | Some Tag token names were inconsistent (`chip-` prefix, `-bg` suffix). | 2026-09-29 | Renamed (D-011). |
| R-012 | 2026-09-29 | The Foundations page and the live variables disagree. Which is right? | 2026-09-29 | The live variables (D-001). |

## Changelog

Newest first. Each entry links to its commit or PR.

| Date | Change | Ref |
|---|---|---|
| 2026-10-01 | Repo renamed to `maggiebrigleb/Vyn-DLS`. Updated the git remote, the PR links in this file and the `CLAUDE.md` heading. `DESIGN.md` and the design-system page are unchanged. | [#1](https://github.com/maggiebrigleb/Vyn-DLS/pull/1) |
| 2026-10-01 | Added `DECISIONS.md` and the `CLAUDE.md` logging rule. Backfilled the decisions, questions and changes made so far. `DESIGN.md`'s Decisions, Deferred and Known Gaps sections now summarize this log. | [#1](https://github.com/maggiebrigleb/Vyn-DLS/pull/1) |
| 2026-09-29 | Design-system page (v2) published from the Design System artifact type. It includes the tokens from the live variables, the brand book, 18 component previews, the Vyn Viewer example, and the logo and icons exported from Figma. | [artifact](https://claude.ai/artifact/CqA1i9k2gzTpfXUNT2hRJi) |
| 2026-09-29 | Applied the Tag renames to the lookup table and removed the resolved naming gap. | `4295b52` |
| 2026-09-29 | Tag token renames (D-011). | `69bad5b` (Maggie) |
| 2026-09-29 | Added Vyn AI UI guidance, the Vynnie mascot section and the provisional neon rule (D-012, D-013, D-017 to D-019). | `7d2b57c` |
| 2026-09-29 | Renamed every token after the developer tokens. Added the semantic token lookup table and removed duplicated hex values from the prose (D-010). | `3efb601` |
| 2026-09-29 | Recorded the focus ring, BETA pill, sidebar width and Workflow switcher decisions (D-006 to D-009, D-014, D-015). | `a185bbb` |
| 2026-09-29 | Targeted Bootstrap 5, made the app desktop-only, added Bootstrap motion defaults and marked placeholders TBD (D-001 to D-005). | `871edd3` |
| 2026-09-29 | First draft of `DESIGN.md`, built from the Figma file. | `797a6b2` |
