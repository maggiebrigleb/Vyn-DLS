# Vyn Web App design system: What We Did and How to Keep It Running

## Summary
We turned the Vyn Web App's Figma files into a written design system guide (`DESIGN.md`), a running log of every decision (`DECISIONS.md`), and two web pages that show the system visually. A first version (v1) was kept as it was. A second version (v2) was built when the Figma libraries changed, and has since been checked component by component against Figma. The most important thing to remember: **Figma is the source of truth, and the guide and the reference page must always be updated together.**

## Steps
1. **Read the Figma files.** We connected to the two Figma files, Vyn Web App (colors, text styles, components) and Vyn Global (the base color ramps and icons), and listed what the design system contained and what was missing.
2. **Wrote the first guide (v1).** We wrote `DESIGN.md`, a single document describing the colors, type, spacing, components, voice and AI rules. It follows the format of a public example (IBM's). Where Figma said nothing, we followed Bootstrap, the ready-made component library the app is built on.
3. **Renamed tokens to match the real system.** Color names first followed the IBM example. At Maggie's request, every name was changed to match the names developers already use, and colors were never merged even when they share a value. That way each one can be changed on its own while the system is still being built.
4. **Started a decision log.** `DECISIONS.md` records every decision, open question and change, with dates and who decided. A rules file for the assistant (`CLAUDE.md`) requires the log to be updated with every change.
5. **Built the first visual page (v1).** A private web page shows the colors, type and components, so people can see the system instead of reading about it.
6. **Built v2 from the updated Figma libraries.** The design team changed the colors (cooler greys, charcoal buttons instead of green) and the type sizes. We updated the guide on a separate branch (a parallel copy of the project), so v1 stayed untouched.
7. **Built two v2 pages.** One is a "template" page in a standard design-system format, which other designs can point to as their reference. The other is a "branded" page styled like the Vyn app itself, where you can click and try the components.
8. **Checked the components against Figma and fixed them.** Maggie spotted six problems. Each was traced to its cause: either a mistake on the pages, or something the guide never described. The fixes:
   - The checkbox tick now shows, in Figma's dark grey.
   - Alerts no longer have icons Figma doesn't have, and the close button lines up with the text.
   - Primary buttons now lighten on hover, as in Figma (other buttons darken).
   - Every icon is now an exact copy of the Figma icon. A made-up search icon was removed.
   - The dropdown now shows the same blue focus outline as other form fields.
   - The sidebar in the Vyn Viewer example is no longer cut off.

   The guide was filled in wherever it had been silent, so these mistakes are less likely to come back.
9. **Recorded two decisions.** The guide and the template page must always be updated together. The sidebar's section labels use the "eyebrow" text style.
10. **Saved everything.** All changes are saved on the `v2` branch of the Vyn-DLS repository on GitHub.

## Maintenance
- **Routine upkeep:**
  - Whenever the Figma libraries change, update `DESIGN.md` **and** the template page at the same time, then add a line to `DECISIONS.md`.
  - The branded page should follow too, but it's lower priority, because nothing points to it as the official reference.
  - After editing `DESIGN.md`, run the checker (`npx -y @google/design.md lint DESIGN.md`). It should report 0 errors. The warnings it reports are expected.
- **If something breaks:**
  - **A page shows the wrong color or style:** check the live Figma variables first. They win over anything written elsewhere.
  - **Icons look wrong:** replace them with exports from Vyn Global's Iconography page. Don't redraw them.
  - **Saving to GitHub fails with "access denied":** the repository was renamed to Vyn-DLS, and the project's saved address sometimes reverts to the old name. Point it back at `maggiebrigleb/Vyn-DLS`.
- **Where things live:**
  - `DESIGN.md`: the guide, describing the system as it is now.
  - `DECISIONS.md`: why things are the way they are, plus open questions.
  - `CLAUDE.md`: the rules the assistant follows when it edits this project.
  - `site/design-system-v2.html`: the source of the branded page.
  - The v1 page: https://claude.ai/artifact/CqA1i9k2gzTpfXUNT2hRJi
  - The v2 template page: https://claude.ai/artifact/SHWJ8Cx6KoboTtmGvQfEa4
  - The v2 branded page: https://claude.ai/artifact/PjtjrkSpD9PgtRG47w1q9g

## Cautions
- Don't delete or renumber entries in `DECISIONS.md`. Mark old decisions as replaced instead, so the history stays readable.
- Don't make changes on the v1 branch. It's kept as a record of the first pass.
- The pages are private. Share them from each page's Share menu, and only with people who should see them.
- Don't merge two colors into one, even if they currently look identical. They're expected to change separately.

## Open items
- Several questions are waiting on the design team. They're listed in `DECISIONS.md`. The newest are:
  - Q-024: Primary pressed button border color.
  - Q-025: which search icon to use.
  - Q-026: checkbox focus color.
  - Q-027: the default icon set.
  - Q-028: updating the sidebar labels in Figma.
- A few rules were drafted by the assistant and are marked "proposed" until someone confirms them. One example is "use only Figma icons" (D-035).
- The v2 type sizes are marked "Proposed / In-flight" in Figma, so expect them to change.
- The pages were tested in a browser simulation at desktop and phone sizes. The real Vyn font couldn't load in that test environment, so the font itself wasn't checked.
- No pull request (a formal request to merge the changes) has been opened for v2 yet.
