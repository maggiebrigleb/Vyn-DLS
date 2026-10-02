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
- Figma: [Vyn Web App](https://www.figma.com/design/LNixxQjUWEwccxM0LgcW6g/Vyn-Web-App) (semantic tokens, text styles) · [Vyn Global](https://www.figma.com/design/PXB9RwThJHEP09SPoKZg4J/Vyn-Global) (primitives)
- Branches: `claude/figma-file-connection-of9n12` (v1, PR #1) · `v2`
- Design-system pages (private, shared from each page's Share menu): v1 https://claude.ai/artifact/CqA1i9k2gzTpfXUNT2hRJi · v2 (template) https://claude.ai/artifact/SHWJ8Cx6KoboTtmGvQfEa4 · v2 (branded, interactive) https://claude.ai/artifact/PjtjrkSpD9PgtRG47w1q9g
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
| D-017 | 2026-09-29 | **Two greens with separate jobs:** "action green" (Green/600, `button-primary`) for UI actions, and "neon brand green" for Vyn AI and the logo. | superseded by D-024 | Claude | Follows from D-012. Figma still calls Green/600 "Branding main green" (Q-007). |
| D-018 | 2026-09-29 | **Neon on light grounds is only a fill behind `text-primary`.** It's never text, a thin border or a lone icon on white (1.7:1). On `background-dark` it can be text or a mark (8.5:1). | proposed | Claude | A WCAG contrast requirement that follows from D-012. Still holds in v2: neon on white is 1.7:1, and on `background-dark` it's 9:1. |
| D-019 | 2026-09-29 | **One Vyn AI marker:** every AI output combines neon, a "Vyn AI" text label and, optionally, the Vynnie mark, placed on the output's container. | proposed | Claude | A direction, not a spec. There are no AI components in Figma yet (Q-006). |
| D-020 | 2026-09-29 | **Cards keep Bootstrap 5's default radius (0.375rem) and border** (`$border-color-translucent`). Every other control uses `radius-s` (4px). | proposed | Claude | Matches the Figma card exactly (6px, black ~18%). |
| D-021 | 2026-09-29 | **Standard name: "Agentic Toolbox"** (not "Agent Toolbox" or "Smart Agent Toolbox"). | proposed | Claude | Matches the sidebar label. |
| D-022 | 2026-10-01 | **This file is the running log** of decisions, questions and changes. `CLAUDE.md` requires every design-system change to update it. | firm | Maggie | |
| D-023 | 2026-10-02 | **v2 palette from the updated libraries.** Vyn Global replaces the warm stone greys with cool greys (Grey/100 #F6F7F8 to Grey/900 #252628), Red and Orange with **Semantic Red** and **Semantic Yellow**, retints Semantic Green and rebuilds the Green ramp. Vyn Web App re-points its semantic tokens to these. | firm | Maggie / design team (Figma libraries) | Read from the live variables (D-001). Values are in `DESIGN.md`, *Semantic tokens* and *Primitives*. |
| D-024 | 2026-10-02 | **Primary actions are charcoal, not green.** `button-primary`, `link-primary` and `link-primary-active` are Grey/900, and `input-primary-active` is Grey/700. | firm | Maggie / design team (Figma libraries) | Supersedes D-017. Raises Q-016, because `button-primary` now equals `background-dark`. |
| D-025 | 2026-10-02 | **The brand green is `Brand/Green`, which equals Green/400 (#98DB40)** in Vyn Global, and the separate Neon Green ramp is gone. Green/400's description now reads *"Vyn brand green: use is reserved for Vyn logo and VynAI only"*. | firm | Maggie / design team (Figma libraries) | Writes D-012 into the library. D-012 stays provisional. `DESIGN.md` uses the key `brand-green`. |
| D-026 | 2026-10-02 | **New semantic tokens** `Border/border` (Grey/200) and `Input/input-border-disabled` (Grey/300). The Web App Color collection now has 79 variables. | firm | Maggie / design team (Figma libraries) | `border` is used by the Dropdown menu header. `input-border-disabled` is used by disabled Input Group fields. |
| D-027 | 2026-10-02 | **v2 type scale** (Vyn Web App text styles): <ul><li>Heading `h1`–`h6`: 28, 22, 18, 16, 14 and 12px, Semi-Bold, 1.2 line height.</li><li>Body `body-base`, `body-small`, `body-xsmall` and `body-xxsmall`: 16, 14, 12 and 10px with Medium and Semi-Bold variants, 1.5 line height.</li><li>`Utility/eyebrow`: 12px Medium, +1px.</li><li>Display `display-4` to `display-6`: 56, 48 and 40px. `_display-1` to `_display-3` are hidden.</li></ul> The size variables are renamed by value (`10` to `28`), and letter spacing `2` becomes `1`. | provisional | Maggie / design team (Figma libraries) | The Figma Typography page labels it *"Proposed / In-flight"*. It replaces the v1 `header-h*` / `body-p*` scale. |
| D-028 | 2026-10-02 | **Type keys in `DESIGN.md` are the text-style names without their group** (`Heading/h1` → `h1`, `Body/body-small-medium` → `body-small-medium`). | proposed | Claude | No CSS developer tokens are published for the v2 styles yet (Q-021). |
| D-029 | 2026-10-02 | **v2 lives on its own `v2` branch.** The first pass stays unchanged on `claude/figma-file-connection-of9n12` (PR #1). | firm | Maggie | So v1 isn't overwritten. |
| D-030 | 2026-10-02 | **The v2 design-system page is separate from v1:** https://claude.ai/artifact/SHWJ8Cx6KoboTtmGvQfEa4. The v1 page stays unchanged so it remains viewable. | firm | Maggie | Answers Q-023. |
| D-031 | 2026-10-02 | **A Vyn-branded, interactive v2 page sits alongside the template page.** The template's own frame can't be restyled, so the branded page is a separate custom page (https://claude.ai/artifact/PjtjrkSpD9PgtRG47w1q9g). Both are kept: the template page is the structured reference, and the branded page shows the system in use. | firm | Maggie | Chosen over replacing the template page or staying template-only. |

## Open questions and to-dos

| ID | Raised | Question / to-do | Owner | Notes |
|---|---|---|---|---|
| Q-001 | 2026-09-29 | Regenerate the Figma Foundations Documentation page from the live variables. Its Alert table is out of date, and several Tag and Chip rows render #000000. | Design | See D-001. |
| Q-002 | 2026-09-29 | Should the card radius and border get Vyn token names (for example `--radius-m: 6px` and `Border/border-translucent`)? | Design | See D-020. |
| Q-003 | 2026-09-29 | Add semantic tokens for the primitives Figma binds directly: `grey-500` (workflow-switcher border), `grey-600` (navbar icon button), `grey-700` (sidebar divider) and `neon-green-800` (logo). | Design | They currently can't be swapped like the rest. **v2:** still true for `grey-500`, `grey-600` and `grey-700`, and the logo now binds `Brand/Green`. |
| Q-004 | 2026-09-29 | Add semantic tokens for success and warning fills, so Bootstrap's `$success` and `$warning` don't map to primitives. | Design | |
| Q-006 | 2026-09-29 | Create `AI/*` semantic tokens and an AI output card or tag component, so the provisional neon rule can change in one place. | Design | See D-012 and D-019. |
| Q-007 | 2026-09-29 | Update the Figma description of Green/600 ("Branding main green"), since neon is the brand color. | Design | See D-017. **v2:** Green/400 now carries the brand description (D-025), but Green/600 still says "Branding main green", and only `chip-secondary` still uses it. |
| Q-008 | 2026-09-29 | Do results produced by Agentic Toolbox agents (for example auto-triage categories) count as Vyn AI outputs that get the neon marker? | Maggie | The Toolbox UI itself is out of scope (D-013). |
| Q-009 | 2026-09-29 | Document the remaining component sets. Figma counts 33 sets and 9 standalone components, and 15 are documented. | Design | |
| Q-010 | 2026-09-29 | Review the marketing site (vyntelligence.com) for voice. It couldn't be fetched from the drafting environment. | Maggie | Voice currently relies on the Brand Feel audit. |
| Q-011 | 2026-09-29 | Confirm the 1280px minimum supported width. | Maggie | See D-016. |
| Q-012 | 2026-09-29 | Is a logo version for light backgrounds needed? Figma only has the dark-background logo. | Design | |
| Q-014 | 2026-10-01 | Keep `DESIGN.md` and the design-system page in sync. They're separate, so changing one doesn't update the other. Decide whether one should be generated from the other. | Maggie | Until then, `CLAUDE.md` requires checking both. **2026-10-02:** there are now three v2 surfaces (`DESIGN.md`, the template page and the branded page). The branded page's colors and type are generated from the same token file as the template page, but its copy is written by hand. |
| Q-015 | 2026-10-02 | Figma still uses the old Tag names (`Tag/tag-warning-bg`, `Tag/tag-danger-bg`, `Tag/chip-success-border`), while D-011 renamed them in `DESIGN.md`. Rename them in Figma, or revert D-011? | Maggie | Until this is settled, `DESIGN.md` keeps the D-011 names and notes the Figma names. |
| Q-016 | 2026-10-02 | `button-primary` and `background-dark` are both Grey/900, so a Primary Filled button disappears on the navbar and sidebar (1:1). Is that intended, and should dark surfaces get their own button token? | Design | See D-024. |
| Q-017 | 2026-10-02 | `chip-secondary` is still Green/600 (#60A211), and `chip-text-light` on it is 3.2:1, which fails AA for small text. Should it move to charcoal, or use dark text? | Design | It's the last semantic use of Green/600. |
| Q-018 | 2026-10-02 | The navbar icon-button fill (`grey-600`, #656668) on `background-dark` is 2.6:1, below the 3:1 minimum for a control boundary. | Design | It was 3.1:1 in v1. |
| Q-019 | 2026-10-02 | The `Elevation/XXL Drop` shadow is still tinted with the v1 warm grey (#57534F). Should it be retinted to the cool palette? | Design | |
| Q-020 | 2026-10-02 | `Brand/Black` (#2C2A29, the old charcoal) is reserved "for use with Vyn logo only", while the chrome behind the logo is `background-dark` (Grey/900 #252628). Which should sit behind the logo? | Design | |
| Q-021 | 2026-10-02 | Publish CSS developer tokens for the v2 text styles and size variables. The v1 names (`--font-header-h1-semi-bold`, `--font-xs`) no longer match. | Design / Dev | See D-028. |
| Q-022 | 2026-10-02 | The sidebar section labels (WORKFLOW, SETTINGS) are 10px Semi-Bold with +1px tracking, uppercase, and have no text style applied. The new `Utility/eyebrow` is 12px Medium. Should the labels use it? | Design | Replaces Q-005 (see R-013). |

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
| R-013 | 2026-09-29 | (Q-005) Should there be a Figma text style for the sidebar eyebrow label? | 2026-10-02 | A `Utility/eyebrow` style now exists (D-027), but the sidebar labels don't use it. Follow-up is Q-022. |
| R-014 | 2026-09-29 | (Q-013) Rebind the Workflow switcher label to the `S` font-size variable. | 2026-10-02 | It's now bound to the size-named Typography variable `14` (D-027), which matches D-009. |
| R-015 | 2026-10-02 | (Q-023) Should the design-system page be updated to v2 in place, or as a separate page? | 2026-10-02 | As a separate page (D-030). |

## Changelog

Newest first. Each entry links to its commit or PR.

| Date | Change | Ref |
|---|---|---|
| 2026-10-02 | **Published the branded, interactive v2 page** (https://claude.ai/artifact/PjtjrkSpD9PgtRG47w1q9g), source at `site/design-system-v2.html`. The page itself uses the Vyn Web App shell: charcoal navbar and sidebar, v2 tokens, Inter and inline Vyn icons. It has:<ul><li>copy-on-click swatches for all 79 semantic tokens and the primitive ramps</li><li>an editable type specimen</li><li>a button configurator that shows the Bootstrap classes</li><li>a validating form, keyboard dropdown, tri-state checkbox, switches, tabs, accordion, dismissible alerts, a badge counter, tooltips, and a collapsible sidebar</li><li>a Vyn AI card with its states and Accept/Edit/Reject</li><li>a Vyn Viewer drawer that closes on Esc and the backdrop</li></ul>Also on the v2 template page: the logo and icons are now inline SVG in the previews (they weren't loading from the asset store), and the brand book links to the branded page. `DESIGN.md` gained a link to the branded page. | branch `v2` |
| 2026-10-02 | **Published the v2 design-system page** (https://claude.ai/artifact/SHWJ8Cx6KoboTtmGvQfEa4). It's built from v2 `DESIGN.md`: 148 color tokens (the 79 semantic tokens plus the Vyn Global primitives and Functional aliases), the v2 heading, body, utility and display styles, the font-size variables, the stylesheet and previews retargeted to v2 tokens, sidebar icons re-exported in their v2 grey, the brand-book Color, Neon and Typography sections rewritten, and the cover recoloured. The v1 page is unchanged. `DESIGN.md` gained a link to the page. | branch `v2` |
| 2026-10-02 | **DLS v2 on branch `v2`.** Updated `DESIGN.md` from the changed Vyn Global and Vyn Web App libraries: all 79 semantic tokens and their aliases, the Vyn Global primitive ramps, the v2 type scale and its Bootstrap mapping, the contrast checks, and the prose that relied on action green or warm greys. Logged D-023 to D-029, Q-015 to Q-023 and R-013/R-014. Added the Vyn Global file key to `CLAUDE.md`. The **design-system page was not updated** and still shows v1 (Q-023). | branch `v2` |
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
