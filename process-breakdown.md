# Vyn Web App design system: What We Did and How to Keep It Running

## Summary
We turned the Vyn Web App's Figma files into a written design system guide (`DESIGN.md`), a running log of every decision (`DECISIONS.md`), and web pages that show the system visually. A first version (v1) was kept as it was. A second version (v2) was built when the Figma libraries changed, and then checked component by component against Figma. The most important thing to remember: **Figma is the source of truth, and the guide and the v2 template page must always be updated together.**

## Steps
1. **Read the Figma files** - We connected to Vyn Web App (colors, text styles, components) and Vyn Global (base color ramps and icons), then listed what the system contained and what was missing.
   - **Why:** The design system lives in those files, so everything else is built from them.
   - **How:** Through the Figma connector in Claude Code, which can read variables, styles and component details directly.
2. **Wrote the first guide (v1)** - `DESIGN.md` describes the colors, type, spacing, components, voice and Vyn AI rules in one document.
   - **Why:** Maggie asked for a file like the public IBM example on getdesign.md, so designs and code have one written reference.
   - **How:** A structured header holds the exact values, and plain prose below it explains usage. A free checker tool (`@google/design.md`) checks the file for errors.
3. **Renamed the tokens to match the real system** - Every color name ("token") now matches the name developers already use, such as `text-secondary` for `--color-text-secondary`.
   - **Why:** Maggie asked why the first draft used invented names, and said the semantic tokens must stay separate and easy to find while the system is under construction.
   - **How:** Each name is the developer name minus its `--color-` prefix.
4. **Set up a decision log** - `DECISIONS.md` records each decision, open question and change, with a date and who decided.
   - **Why:** Maggie wanted a running list of all decisions, questions and changes.
   - **How:** A rules file for the assistant (`CLAUDE.md`) requires the log to be updated with every change, in the same save.
5. **Built the first visual page (v1)** - A private web page shows the colors, type and components.
   - **Why:** Maggie asked for a visual page like the IBM example's preview.
   - **How:** It's built from a ready-made "Design System" page template on claude.ai.
6. **Built v2 from the updated Figma libraries** - The design team changed the colors (cooler greys, charcoal buttons) and the type sizes, and the guide was updated to match.
   - **Why:** Maggie asked for the changes to go on a separate branch (a parallel copy of the project), so the first pass wasn't overwritten.
   - **How:** On a branch called `v2`. The v1 work stays on its own branch.
7. **Built two v2 pages** - A "template" page in the standard format, and a "branded" page styled like the Vyn app, where people can click and try the components.
   - **Why:** Maggie wanted v2 as a separate page, and then wanted the page itself in Vyn branding with interactive components. The template's outer frame can't be restyled, so the branded version had to be a separate page.
   - **How:** The branded page's colors and type come from the same token file as the template page, but its text is written by hand.
8. **Fixed icons that didn't show** - The template page's icons are now built into the page itself.
   - **Why:** Icons stored as separate files didn't load inside the page's preview boxes.
9. **Checked the components against Figma and fixed them** - Maggie spotted six problems: the checkbox tick, the alert icons, the Primary button hover, a search icon, the dropdown focus outline, and a cut-off sidebar. Each one was fixed on both pages.
   - **Why:** Each problem was traced to its cause, either a mistake on the pages or something the guide never described. The guide was filled in, so the mistakes are less likely to come back.
   - **How:** We read the exact Figma specs for each component (colors, sizes, states) and exported the real icon shapes from Vyn Global.
10. **Agreed to keep the guide and the template page in sync** - Every change to `DESIGN.md` is now also made on the template page, at the same time.
    - **Why:** Designs will reference the template page as the design system, so it must be accurate. The branded page can't be referenced that way, so it's updated on a best-effort basis.
11. **Saved everything to GitHub** - All work is on the `v2` branch of the Vyn-DLS repository. The repository was renamed from `design-tests` to `Vyn-DLS` at Maggie's request.

## Design decisions
- **Live Figma variables win over the Figma documentation page:** the documentation page is out of date, and Maggie said to trust the variables.
- **Follow Bootstrap 5.3 wherever Figma is silent:** the app is built on the latest Bootstrap and uses many of its standard components.
- **Desktop only, with Bootstrap's default motion:** the app currently appears to be desktop-only, and Maggie said to keep Bootstrap's animation defaults.
- **Keep the blue focus outline:** Maggie decided to keep it "for now", so it's the only blue in the system on purpose.
- **Sidebar is 250px wide:** this replaces Figma's 249px, which was off the 4px/8px spacing grid.
- **Neon green is only for Vyn AI and the logo:** Maggie asked for this so AI results stand out. It's marked provisional and may change.
- **Primary buttons are charcoal, not green:** this came from the design team's updated Figma libraries in v2. One side effect: a charcoal button disappears on the charcoal navbar, which is still an open question.
- **Never merge two tokens, even if they share a value:** the values are expected to change separately while the system is being built.
- **v1 and v2 stay separate:** on separate branches and separate pages, so the first pass remains viewable.
- **Hover depends on the button type:** Primary buttons lighten, while Secondary and Danger buttons darken. Both rules come straight from the Figma button variants, so the earlier "always darken" rule was wrong.
- **Only real Figma icons, never redrawn:** a hand-drawn search icon didn't match anything in the file. This rule was drafted by the assistant and is waiting for confirmation.
- **Alerts have no status icons:** the Figma Alert component has none, so the pages no longer add them.
- **Sidebar section labels use the "eyebrow" text style:** decided by Maggie (see Open items).
- **Light mode only, for now:** dark mode was deliberately put off until later.

## Maintenance
- **Routine upkeep:**
  - Whenever the Figma libraries change, update `DESIGN.md` **and** the template page in the same piece of work.
  - Add a line to `DECISIONS.md` each time.
  - Update the branded page too, where it shows the change.
  - After editing `DESIGN.md`, run the checker (`npx -y @google/design.md lint DESIGN.md`). It should report 0 errors. The warnings it shows are expected.
- **If something breaks:**
  - **A page shows the wrong color or style:** compare it with the live Figma variables first. They win.
  - **An icon looks wrong:** replace it with the export from Vyn Global's Iconography page.
  - **Saving to GitHub is refused:** the project's saved address sometimes reverts to the old repository name. Point it back at `maggiebrigleb/Vyn-DLS`.
- **Where things live:**
  - `DESIGN.md`: the guide, describing the current state.
  - `DECISIONS.md`: why things are the way they are, and what's still open.
  - `CLAUDE.md`: the rules the assistant follows when it edits this project.
  - `site/design-system-v2.html`: the source of the branded page.
  - The pages: v1 https://claude.ai/artifact/CqA1i9k2gzTpfXUNT2hRJi · v2 template https://claude.ai/artifact/SHWJ8Cx6KoboTtmGvQfEa4 · v2 branded https://claude.ai/artifact/PjtjrkSpD9PgtRG47w1q9g

## Cautions
- Don't delete or renumber entries in `DECISIONS.md`. Mark an old decision as replaced instead.
- Don't edit the v1 branch or the v1 page. They're the record of the first pass.
- Share the pages only through their Share menu, and only with people who should see them.

## Open items
- **Waiting on the design team:**
  - Q-024: why the Primary Pressed button's border is darker than its fill.
  - Q-025: which search icon to use.
  - Q-026: the checkbox focus color.
  - Q-027: which icon set to use by default.
  - Q-028: updating the sidebar labels in Figma.
  - Several earlier questions, such as the charcoal button on the charcoal navbar.
- **Drafted by the assistant, not yet confirmed:** for example, the 1280px minimum screen width and the "only Figma icons" rule. These are marked "proposed" in the log.
- **Eyebrow labels in the sidebar:** the reason wasn't stated.
- **Type sizes may change:** they're labelled "Proposed / In-flight" in Figma.
- **Testing:** the pages were tested in a simulated browser at desktop and phone sizes. The Inter font couldn't load in that environment, so the font itself wasn't checked.
- **No pull request yet:** nobody has opened a request to merge v2 into the main project.
