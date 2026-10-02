---
version: alpha
name: Vyn-Web-App-design-v2
description: "A calm, desk-side operations console for utilities and infrastructure teams: white work surfaces framed by charcoal chrome (background-dark), charcoal primary actions (button-primary), and neutral cool greys for everything structural. The neon brand green (Brand/Green) is reserved for Vyn AI outputs and the logo. Type is Inter throughout: 16px body at 150% line height, headings from 28px down to 12px at 120%, and display styles from 56px down to 40px for dashboard figures. Components are Bootstrap 5 components (4px radius, 1px borders, 48px form controls) with Material icons. The personality is practical and proven first, lightly playful second: the product earns trust by showing the evidence, not by decorating it."

# v2: values from the Vyn Global and Vyn Web App libraries as of 2026-10-02.
# Naming rule: every color key is the developer token minus --color-,
# so {colors.text-secondary} == --color-text-secondary == Figma "Text/text-secondary".
# Exception (D-011): tag-success-border, tag-warning and tag-danger are renamed here; Figma still uses the old names (Q-015).
# Semantic tokens are listed one per variable and are NEVER merged, even when
# two share a value today. To change a value, edit that one line.
colors:
  # --- Text ---
  text-primary: "#252628"                     # Text/text-primary → Grey/900
  text-secondary: "#535456"                   # Text/text-secondary → Grey/700
  text-white: "#ffffff"                       # Text/text-white → White
  text-success: "#235825"                     # Text/text-success → Functional/Success/700 → Semantic Green/700
  text-warning: "#6b3e00"                     # Text/text-warning → Functional/Warning/700 → Semantic Yellow/700
  text-danger: "#9b0810"                      # Text/text-danger → Functional/Danger/700 → Semantic Red/700
  # --- Background ---
  background-primary: "#ffffff"               # Background/bg-primary → White
  background-secondary: "#f6f7f8"             # Background/bg-secondary → Grey/100
  background-dark: "#252628"                  # Background/bg-dark → Grey/900
  # --- Border ---
  border: "#e8e9ea"                           # Border/border → Grey/200
  # --- Button ---
  button-primary: "#252628"                   # Button/btn-primary → Grey/900
  button-primary-text: "#ffffff"              # Button/btn-primary-text → White
  button-secondary: "#e8e9ea"                 # Button/btn-secondary → Grey/200
  button-secondary-text: "#252628"            # Button/btn-secondary-text → Grey/900
  button-danger: "#da1e28"                    # Button/btn-danger → Functional/Danger/600 → Semantic Red/600
  button-disabled: "#e8e9ea"                  # Button/btn-disabled → Grey/200
  button-disabled-text: "#a1a2a3"             # Button/btn-disabled-text → Grey/400
  # --- Input ---
  input-primary: "#ffffff"                    # Input/input-primary → White
  input-secondary: "#e8e9ea"                  # Input/input-secondary → Grey/200
  input-primary-active: "#535456"             # Input/input-primary-active → Grey/700
  input-disabled: "#f6f7f8"                   # Input/input-disabled → Grey/100
  input-text-primary: "#252628"               # Input/input-text-primary → Grey/900
  input-text-secondary: "#535456"             # Input/input-text-secondary → Grey/700
  input-text-disabled: "#828385"              # Input/input-text-disabled → Grey/500
  input-text-light: "#ffffff"                 # Input/input-text-light → White
  input-border: "#828385"                     # Input/input-border → Grey/500
  input-border-disabled: "#cbcccc"            # Input/input-border-disabled → Grey/300
  input-danger: "#da1e28"                     # Input/input-danger → Functional/Danger/600 → Semantic Red/600
  # --- Link ---
  link-primary: "#252628"                     # Link/link-primary → Grey/900
  link-primary-active: "#252628"              # Link/link-primary-active → Grey/900
  link-primary-disabled: "#a1a2a3"            # Link/link-primary-disabled → Grey/400
  link-secondary: "#535456"                   # Link/link-secondary → Grey/700
  link-secondary-active: "#535456"            # Link/link-secondary-active → Grey/700
  link-secondary-disabled: "#a1a2a3"          # Link/link-secondary-disabled → Grey/400
  link-secondary-light: "#cbcccc"             # Link/link-secondary-light → Grey/300
  link-secondary-light-active: "#ffffff"      # Link/link-secondary-light-active → White
  link-secondary-light-disabled: "#828385"    # Link/link-secondary-light-disabled → Grey/500
  # --- Alert ---
  alert-default-bg: "#f6f7f8"                 # Alert/alert-default-bg → Grey/100
  alert-default-border: "#e8e9ea"             # Alert/alert-default-border → Grey/200
  alert-default-text: "#434446"               # Alert/alert-default-text → Grey/800
  alert-success-bg: "#eaf6ea"                 # Alert/alert-success-bg → Functional/Success/100 → Semantic Green/100
  alert-success-border: "#cdeacf"             # Alert/alert-success-border → Functional/Success/200 → Semantic Green/200
  alert-success-text: "#235825"               # Alert/alert-success-text → Functional/Success/700 → Semantic Green/700
  alert-warning-bg: "#fff5e0"                 # Alert/alert-warning-bg → Functional/Warning/100 → Semantic Yellow/100
  alert-warning-border: "#ffe5b2"             # Alert/alert-warning-border → Functional/Warning/200 → Semantic Yellow/200
  alert-warning-text: "#6b3e00"               # Alert/alert-warning-text → Functional/Warning/700 → Semantic Yellow/700
  alert-danger-bg: "#fff0f1"                  # Alert/alert-danger-bg → Functional/Danger/100 → Semantic Red/100
  alert-danger-border: "#fedcde"              # Alert/alert-danger-border → Functional/Danger/200 → Semantic Red/200
  alert-danger-text: "#9b0810"                # Alert/alert-danger-text → Functional/Danger/700 → Semantic Red/700
  # --- Tag ---
  tag-default: "#f6f7f8"                      # Tag/tag-default → Grey/100
  tag-default-text: "#252628"                 # Tag/tag-default-text → Grey/900
  tag-default-border: "#e8e9ea"               # Tag/tag-default-border → Grey/200
  tag-success: "#eaf6ea"                      # Tag/tag-success → Functional/Success/100 → Semantic Green/100
  tag-success-text: "#235825"                 # Tag/tag-success-text → Functional/Success/700 → Semantic Green/700
  tag-success-border: "#cdeacf"               # Tag/chip-success-border → Functional/Success/200 → Semantic Green/200
  tag-warning: "#fff5e0"                      # Tag/tag-warning-bg → Functional/Warning/100 → Semantic Yellow/100
  tag-warning-text: "#6b3e00"                 # Tag/tag-warning-text → Functional/Warning/700 → Semantic Yellow/700
  tag-warning-border: "#ffe5b2"               # Tag/tag-warning-border → Functional/Warning/200 → Semantic Yellow/200
  tag-danger: "#fff0f1"                       # Tag/tag-danger-bg → Functional/Danger/100 → Semantic Red/100
  tag-danger-text: "#9b0810"                  # Tag/tag-danger-text → Functional/Danger/700 → Semantic Red/700
  tag-danger-border: "#fedcde"                # Tag/tag-danger-border → Functional/Danger/200 → Semantic Red/200
  # --- Chip ---
  chip-primary: "#434446"                     # Chip/chip-primary → Grey/800
  chip-primary-border: "#cbcccc"              # Chip/chip-primary-border → Grey/300
  chip-secondary: "#60a211"                   # Chip/chip-secondary → Green/600
  chip-success: "#9fd6a1"                     # Chip/chip-success → Functional/Success/300 → Semantic Green/300
  chip-success-text: "#235825"                # Chip/chip-success-text → Functional/Success/700 → Semantic Green/700
  chip-warning: "#ffb81f"                     # Chip/chip-warning → Functional/Warning/400 → Semantic Yellow/400
  chip-danger: "#da1e28"                      # Chip/chip-danger → Functional/Danger/600 → Semantic Red/600
  chip-danger-text: "#9b0810"                 # Chip/chip-danger-text → Functional/Danger/700 → Semantic Red/700
  chip-text-light: "#ffffff"                  # Chip/chip-text-light → White
  chip-text-dark: "#252628"                   # Chip/chip-text-dark → Grey/900
  # --- Focus ---
  focus-border-focus: "#007bff"               # Focus/border-focus
  focus-shadow-focus: "rgba(128,189,255,0.4)"  # Focus/shadow-focus
  focus-border-error-focus: "#dc3545"         # Focus/border-error-focus
  focus-shadow-error-focus: "rgba(220,53,69,0.4)"  # Focus/shadow-error-focus
  # --- State ---
  state-hover-shade: "rgba(0,0,0,0.15)"       # State/hover-shade
  state-hover-tint: "rgba(255,255,255,0.15)"  # State/hover-tint
  state-pressed-shade: "rgba(0,0,0,0.2)"      # State/pressed-shade
  state-pressed-tint: "rgba(255,255,255,0.2)"  # State/pressed-tint
  # --- Primitives referenced directly in Figma (no semantic token yet; see Q-003) ---
  brand-green: "#98db40"                    # Brand/Green (= Green/400): logo + Vyn AI outputs only
  grey-500: "#828385"                       # Grey/500: navbar workflow-switcher border
  grey-600: "#656668"                       # Grey/600: navbar icon-button fill
  grey-700: "#535456"                       # Grey/700: sidebar footer divider

typography:                # keys = Figma text-style names without the group (Heading/h1 → h1); see D-028
  h1:                       # Figma Heading/h1
    fontFamily: Inter
    fontSize: 28px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0
  h2:                       # Figma Heading/h2
    fontFamily: Inter
    fontSize: 22px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0
  h3:                       # Figma Heading/h3
    fontFamily: Inter
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0
  h4:                       # Figma Heading/h4
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0
  h5:                       # Figma Heading/h5
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0
  h6:                       # Figma Heading/h6
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0
  body-base:                # Figma Body/body-base
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-base-medium:         # Figma Body/body-base-medium
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  body-base-semibold:       # Figma Body/body-base-semibold
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  body-small:               # Figma Body/body-small
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-small-medium:        # Figma Body/body-small-medium
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  body-small-semibold:      # Figma Body/body-small-semibold
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  body-xsmall:              # Figma Body/body-xsmall
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-xsmall-medium:       # Figma Body/body-xsmall-medium
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  body-xsmall-semibold:     # Figma Body/body-xsmall-semibold
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  body-xxsmall:             # Figma Body/body-xxsmall
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-xxsmall-semibold:    # Figma Body/body-xxsmall-semibold
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  display-4:                # Figma Display/display-4
    fontFamily: Inter
    fontSize: 56px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0
  display-5:                # Figma Display/display-5
    fontFamily: Inter
    fontSize: 48px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0
  display-6:                # Figma Display/display-6
    fontFamily: Inter
    fontSize: 40px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0
  eyebrow:                  # Figma Utility/eyebrow
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.2
    letterSpacing: 1px

rounded:            # --radius-*
  s: 4px
  l: 8px
  xl: 16px
  xxl: 24px
  pill: 1000px

spacing:            # --space-*
  "0": 0px
  "2": 2px
  "4": 4px
  "8": 8px
  "12": 12px
  "16": 16px
  "24": 24px
  "32": 32px
  "40": 40px
  "80": 80px

components:
  button-primary:
    backgroundColor: "{colors.button-primary}"
    textColor: "{colors.button-primary-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    height: 50px
    padding: 12px 24px
  button-primary-md:
    backgroundColor: "{colors.button-primary}"
    textColor: "{colors.button-primary-text}"
    typography: "{typography.body-small-medium}"
    rounded: "{rounded.s}"
    height: 39px
    padding: 8px 16px
  button-primary-sm:
    backgroundColor: "{colors.button-primary}"
    textColor: "{colors.button-primary-text}"
    typography: "{typography.body-xsmall-medium}"
    rounded: "{rounded.s}"
    height: 28px
    padding: 4px 12px
  button-primary-outline:
    textColor: "{colors.button-primary}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-primary-text:
    textColor: "{colors.button-primary}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-secondary:
    backgroundColor: "{colors.button-secondary}"
    textColor: "{colors.button-secondary-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-secondary-outline:
    textColor: "{colors.button-secondary-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-danger:
    backgroundColor: "{colors.button-danger}"
    textColor: "{colors.button-primary-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-disabled:
    backgroundColor: "{colors.button-disabled}"
    textColor: "{colors.button-disabled-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
  icon-button:
    backgroundColor: "{colors.button-primary}"
    textColor: "{colors.button-primary-text}"
    rounded: "{rounded.pill}"
    size: 32px
    padding: 6px
  icon-button-sm:
    backgroundColor: "{colors.button-primary}"
    textColor: "{colors.button-primary-text}"
    rounded: "{rounded.pill}"
    size: 24px
    padding: 4px
  navbar-icon-button:
    backgroundColor: "{colors.grey-600}"
    rounded: "{rounded.pill}"
    size: 40px
  text-input:
    backgroundColor: "{colors.input-primary}"
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-base}"
    rounded: "{rounded.s}"
    height: 48px
    padding: 0 12px
  text-input-error:
    backgroundColor: "{colors.input-primary}"
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-base}"
    rounded: "{rounded.s}"
    height: 48px
  text-input-disabled:
    backgroundColor: "{colors.input-disabled}"
    textColor: "{colors.input-text-disabled}"
    typography: "{typography.body-base}"
    rounded: "{rounded.s}"
    height: 48px
  input-addon:
    backgroundColor: "{colors.input-secondary}"
    size: 48px
    padding: 12px
  input-label:
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-base-semibold}"
  input-error-text:
    textColor: "{colors.input-danger}"
    typography: "{typography.body-small}"
  dropdown-trigger:
    backgroundColor: "{colors.input-primary}"
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-base}"
    rounded: "{rounded.s}"
    height: 48px
    padding: 12px
  dropdown-menu:
    backgroundColor: "{colors.input-primary}"
    rounded: "{rounded.s}"
  dropdown-item:
    backgroundColor: "{colors.input-primary}"
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-base}"
    height: 48px
    padding: 12px
  card:
    backgroundColor: "{colors.background-primary}"
    rounded: 6px                  # Bootstrap 5 $border-radius (not a Vyn token)
    padding: 16px
  alert-default:
    backgroundColor: "{colors.alert-default-bg}"
    textColor: "{colors.alert-default-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 16px
  alert-success:
    backgroundColor: "{colors.alert-success-bg}"
    textColor: "{colors.alert-success-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 16px
  alert-warning:
    backgroundColor: "{colors.alert-warning-bg}"
    textColor: "{colors.alert-warning-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 16px
  alert-danger:
    backgroundColor: "{colors.alert-danger-bg}"
    textColor: "{colors.alert-danger-text}"
    typography: "{typography.body-base-medium}"
    rounded: "{rounded.s}"
    padding: 12px 16px
  tab:
    padding: 12px 16px
  tab-selected:
    padding: 12px 16px              # + 2px bottom border {colors.link-primary}
  badge:
    backgroundColor: "{colors.button-danger}"
    textColor: "{colors.button-primary-text}"
    rounded: "{rounded.pill}"
    height: 18px
    padding: 2px 4px
  avatar:
    backgroundColor: "{colors.background-primary}"
    textColor: "{colors.link-secondary}"
    rounded: "{rounded.pill}"
    size: 40px
  navbar:
    backgroundColor: "{colors.background-dark}"
    height: 64px
    padding: 12px 16px
  navbar-workflow-switcher:
    textColor: "{colors.link-secondary-light-active}"
    typography: "{typography.body-small-medium}"
    rounded: "{rounded.s}"
    height: 39px
    padding: 8px 16px
  sidebar:
    backgroundColor: "{colors.background-dark}"
    width: 250px
  sidebar-link:
    textColor: "{colors.link-secondary-light}"
    typography: "{typography.body-base-medium}"
    padding: 12px 18px
  sidebar-link-active:
    textColor: "{colors.link-secondary-light-active}"
    typography: "{typography.body-base-medium}"
    padding: 12px 18px
  sidebar-section-label:
    textColor: "{colors.link-secondary-disabled}"
    typography: "{typography.body-xxsmall-semibold}"  # + 1px letter spacing, uppercase; no text style applied in Figma (Q-022)
    padding: 8px 12px
  filter-panel:
    backgroundColor: "{colors.background-secondary}"
    width: 300px
    padding: 16px
  drawer:
    backgroundColor: "{colors.background-primary}"
    padding: 24px
---

## Overview

Vyn is the web console for **Vyntelligence**. Customers and field crews record short guided videos (**Vyns**). **Vyn AI®** runs several models over each one to write **AI summaries**, generate **labels** (sometimes with **evidence frames** attached), push **AI nudges** to field workers, and more. Desk teams, mainly supervisors and customer-care staff, use this app to review what came back, triage it and act on it. The summaries and labels appear in the **Vyn Viewer**. The web app also hosts the **Agentic Toolbox**, where users build and deploy their own agents on selected workflows, or have agents triage incoming Vyns into predefined categories. The two product lines are **CX** (Customer Experience) and **FX** (Field Experience). The core users are operations managers, back-office teams and supervisors at UK utilities (water, gas, energy, telecoms), and the US infrastructure market is next. The company is moving from a digital solutions platform to **Physical World AI**: technology that helps the people doing the work on site, where the tools still lag behind what's possible.

The brand audit sums up the feel in one line: *"a practical, proven, slightly playful engineering partner."* The UI should read the same way. It's a tool people trust with safety and compliance evidence, so it stays calm and legible, and the personality shows up in small places (Vynnie, the brand words, the neon brand green) rather than in decoration. The brand's own summary is **professional but playful**, and it should always feel **premium**, digitally and physically.

The codebase runs on **the latest Bootstrap (5.3.x)**, and most components are stock Bootstrap themed with Vyn tokens. That means 4px control corners, 1px borders, 48px form controls and a Bootstrap-width (0.25rem) focus ring in classic Bootstrap blue. It uses **Material icons** throughout and Material elevation values for shadows. On top of that sits a neutral, cool-grey palette (Grey/100 to Grey/900 in Vyn Global). Primary actions are charcoal, and the neon brand green (`Brand/Green`) is reserved for the logo and Vyn AI outputs.

**Key characteristics:**
- **Dark chrome, light work area.** The navbar and sidebar sit on charcoal `{colors.background-dark}`. Everything the user works on sits on white `{colors.background-primary}`, with `{colors.background-secondary}` for secondary panels such as filters.
- **Neon green belongs to Vyn AI.** The neon brand green marks Vyn AI outputs (and the logo), nothing else. This is a provisional rule; see *Vyn AI UI*.
- **Charcoal actions.** `{colors.button-primary}` and `{colors.link-primary}` (Grey/900), and `{colors.input-primary-active}` (Grey/700), mark primary buttons, links and active inputs. Color is kept for status and for Vyn AI.
- **Clear type hierarchy.** Inter with 16px body (`body-base`). Headings run from `h1` 28px down to `h6` 12px at a 1.2 line height, and display styles (`display-4` to `display-6`, 56–40px) are kept for dashboard figures.
- **Neutral greys do the structural work.** Borders, dividers, disabled states and secondary buttons all come from the Grey ramp. There's no pure black in the UI.
- **Status is neutral by default.** "Info" is grey, not blue. Color is saved for success, warning and danger, so it means something when it appears.
- **Bootstrap behaviour, Vyn skin.** When a pattern isn't specified here, fall back to the Bootstrap component and its usage guidance, then apply Vyn tokens.

> **Version 2 (2026-10-02).** This version follows the updated **Vyn Global** (primitives) and **Vyn Web App** (semantic tokens, text styles) libraries. The first pass (v1) is kept unchanged on branch `claude/figma-file-connection-of9n12` ([PR #1](https://github.com/maggiebrigleb/Vyn-DLS/pull/1)). What changed, and why, is in `DECISIONS.md` (D-023 to D-030). v2 is shown on two pages: the [v2 design-system page](https://claude.ai/artifact/SHWJ8Cx6KoboTtmGvQfEa4) and the [branded, interactive v2 page](https://claude.ai/artifact/PjtjrkSpD9PgtRG47w1q9g). The v1 page is unchanged.
>
> **Source of truth:** the Figma files' **live variables**. Where the Foundations Documentation page disagrees with a live variable, the variable wins, and every value in this file is taken from the variables.
>
> Sources: Figma file *Vyn Web App*, covering the Foundations Documentation, Grids, component pages (Button, Input Group, Dropdown, Cards, Alerts, Tabs, Navbar) and the Brand Feel audit. The marketing site (vyntelligence.com) couldn't be reached from the drafting environment, so brand voice comes from the audit frame, which quotes the site directly.

## Colors

### How color tokens work
- **The semantic tokens are the API.** Components, CSS and this file only ever reference the Vyn Web App **Color** collection's semantic tokens. Primitives come from the **Vyn Global** library and only feed those semantic tokens.
- **One key per Figma variable, no merging.** For example, `text-primary`, `input-text-primary`, `link-primary`, `button-primary` and `background-dark` all resolve to Grey/900 today, but they're separate so each can change on its own. **The DLS is under construction and these values will move.** Always use the most specific token for the job.
- **Naming rule:** key = developer token minus `--color-`. `{colors.alert-success-bg}` ↔ `--color-alert-success-bg` ↔ Figma `Alert/alert-success-bg`. The exceptions are the three Tag tokens renamed by D-011, because Figma still uses their old names (Q-015).
- **To change a value:** change the Figma variable, then update the matching line in the front matter and the table below. No other line in this file should hard-code that hex.
- Only a **Light** mode exists (D-015).

### Semantic tokens
Values are the live variable values (D-001), read on 2026-10-02. There are 79 tokens, including two that are new in v2: `border` and `input-border-disabled`.

**Text**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `text-primary` | `Text/text-primary` | `--color-text-primary` | Grey/900 | `#252628` |
| `text-secondary` | `Text/text-secondary` | `--color-text-secondary` | Grey/700 | `#535456` |
| `text-white` | `Text/text-white` | `--color-text-white` | White | `#ffffff` |
| `text-success` | `Text/text-success` | `--color-text-success` | Functional/Success/700 → Semantic Green/700 | `#235825` |
| `text-warning` | `Text/text-warning` | `--color-text-warning` | Functional/Warning/700 → Semantic Yellow/700 | `#6b3e00` |
| `text-danger` | `Text/text-danger` | `--color-text-danger` | Functional/Danger/700 → Semantic Red/700 | `#9b0810` |

**Background**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `background-primary` | `Background/bg-primary` | `--color-background-primary` | White | `#ffffff` |
| `background-secondary` | `Background/bg-secondary` | `--color-background-secondary` | Grey/100 | `#f6f7f8` |
| `background-dark` | `Background/bg-dark` | `--color-background-dark` | Grey/900 | `#252628` |

**Border**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `border` | `Border/border` | `--color-border` | Grey/200 | `#e8e9ea` |

**Button**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `button-primary` | `Button/btn-primary` | `--color-button-primary` | Grey/900 | `#252628` |
| `button-primary-text` | `Button/btn-primary-text` | `--color-button-primary-text` | White | `#ffffff` |
| `button-secondary` | `Button/btn-secondary` | `--color-button-secondary` | Grey/200 | `#e8e9ea` |
| `button-secondary-text` | `Button/btn-secondary-text` | `--color-button-secondary-text` | Grey/900 | `#252628` |
| `button-danger` | `Button/btn-danger` | `--color-button-danger` | Functional/Danger/600 → Semantic Red/600 | `#da1e28` |
| `button-disabled` | `Button/btn-disabled` | `--color-button-disabled` | Grey/200 | `#e8e9ea` |
| `button-disabled-text` | `Button/btn-disabled-text` | `--color-button-disabled-text` | Grey/400 | `#a1a2a3` |

**Input**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `input-primary` | `Input/input-primary` | `--color-input-primary` | White | `#ffffff` |
| `input-secondary` | `Input/input-secondary` | `--color-input-secondary` | Grey/200 | `#e8e9ea` |
| `input-primary-active` | `Input/input-primary-active` | `--color-input-primary-active` | Grey/700 | `#535456` |
| `input-disabled` | `Input/input-disabled` | `--color-input-disabled` | Grey/100 | `#f6f7f8` |
| `input-text-primary` | `Input/input-text-primary` | `--color-input-text-primary` | Grey/900 | `#252628` |
| `input-text-secondary` | `Input/input-text-secondary` | `--color-input-text-secondary` | Grey/700 | `#535456` |
| `input-text-disabled` | `Input/input-text-disabled` | `--color-input-text-disabled` | Grey/500 | `#828385` |
| `input-text-light` | `Input/input-text-light` | `--color-input-text-light` | White | `#ffffff` |
| `input-border` | `Input/input-border` | `--color-input-border` | Grey/500 | `#828385` |
| `input-border-disabled` | `Input/input-border-disabled` | `--color-input-border-disabled` | Grey/300 | `#cbcccc` |
| `input-danger` | `Input/input-danger` | `--color-input-danger` | Functional/Danger/600 → Semantic Red/600 | `#da1e28` |

**Link**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `link-primary` | `Link/link-primary` | `--color-link-primary` | Grey/900 | `#252628` |
| `link-primary-active` | `Link/link-primary-active` | `--color-link-primary-active` | Grey/900 | `#252628` |
| `link-primary-disabled` | `Link/link-primary-disabled` | `--color-link-primary-disabled` | Grey/400 | `#a1a2a3` |
| `link-secondary` | `Link/link-secondary` | `--color-link-secondary` | Grey/700 | `#535456` |
| `link-secondary-active` | `Link/link-secondary-active` | `--color-link-secondary-active` | Grey/700 | `#535456` |
| `link-secondary-disabled` | `Link/link-secondary-disabled` | `--color-link-secondary-disabled` | Grey/400 | `#a1a2a3` |
| `link-secondary-light` | `Link/link-secondary-light` | `--color-link-secondary-light` | Grey/300 | `#cbcccc` |
| `link-secondary-light-active` | `Link/link-secondary-light-active` | `--color-link-secondary-light-active` | White | `#ffffff` |
| `link-secondary-light-disabled` | `Link/link-secondary-light-disabled` | `--color-link-secondary-light-disabled` | Grey/500 | `#828385` |

**Alert**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `alert-default-bg` | `Alert/alert-default-bg` | `--color-alert-default-bg` | Grey/100 | `#f6f7f8` |
| `alert-default-border` | `Alert/alert-default-border` | `--color-alert-default-border` | Grey/200 | `#e8e9ea` |
| `alert-default-text` | `Alert/alert-default-text` | `--color-alert-default-text` | Grey/800 | `#434446` |
| `alert-success-bg` | `Alert/alert-success-bg` | `--color-alert-success-bg` | Functional/Success/100 → Semantic Green/100 | `#eaf6ea` |
| `alert-success-border` | `Alert/alert-success-border` | `--color-alert-success-border` | Functional/Success/200 → Semantic Green/200 | `#cdeacf` |
| `alert-success-text` | `Alert/alert-success-text` | `--color-alert-success-text` | Functional/Success/700 → Semantic Green/700 | `#235825` |
| `alert-warning-bg` | `Alert/alert-warning-bg` | `--color-alert-warning-bg` | Functional/Warning/100 → Semantic Yellow/100 | `#fff5e0` |
| `alert-warning-border` | `Alert/alert-warning-border` | `--color-alert-warning-border` | Functional/Warning/200 → Semantic Yellow/200 | `#ffe5b2` |
| `alert-warning-text` | `Alert/alert-warning-text` | `--color-alert-warning-text` | Functional/Warning/700 → Semantic Yellow/700 | `#6b3e00` |
| `alert-danger-bg` | `Alert/alert-danger-bg` | `--color-alert-danger-bg` | Functional/Danger/100 → Semantic Red/100 | `#fff0f1` |
| `alert-danger-border` | `Alert/alert-danger-border` | `--color-alert-danger-border` | Functional/Danger/200 → Semantic Red/200 | `#fedcde` |
| `alert-danger-text` | `Alert/alert-danger-text` | `--color-alert-danger-text` | Functional/Danger/700 → Semantic Red/700 | `#9b0810` |

**Tag**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `tag-default` | `Tag/tag-default` | `--color-tag-default` | Grey/100 | `#f6f7f8` |
| `tag-default-text` | `Tag/tag-default-text` | `--color-tag-default-text` | Grey/900 | `#252628` |
| `tag-default-border` | `Tag/tag-default-border` | `--color-tag-default-border` | Grey/200 | `#e8e9ea` |
| `tag-success` | `Tag/tag-success` | `--color-tag-success` | Functional/Success/100 → Semantic Green/100 | `#eaf6ea` |
| `tag-success-text` | `Tag/tag-success-text` | `--color-tag-success-text` | Functional/Success/700 → Semantic Green/700 | `#235825` |
| `tag-success-border` | `Tag/chip-success-border` *(renamed here, D-011)* | `--color-tag-success-border` | Functional/Success/200 → Semantic Green/200 | `#cdeacf` |
| `tag-warning` | `Tag/tag-warning-bg` *(renamed here, D-011)* | `--color-tag-warning` | Functional/Warning/100 → Semantic Yellow/100 | `#fff5e0` |
| `tag-warning-text` | `Tag/tag-warning-text` | `--color-tag-warning-text` | Functional/Warning/700 → Semantic Yellow/700 | `#6b3e00` |
| `tag-warning-border` | `Tag/tag-warning-border` | `--color-tag-warning-border` | Functional/Warning/200 → Semantic Yellow/200 | `#ffe5b2` |
| `tag-danger` | `Tag/tag-danger-bg` *(renamed here, D-011)* | `--color-tag-danger` | Functional/Danger/100 → Semantic Red/100 | `#fff0f1` |
| `tag-danger-text` | `Tag/tag-danger-text` | `--color-tag-danger-text` | Functional/Danger/700 → Semantic Red/700 | `#9b0810` |
| `tag-danger-border` | `Tag/tag-danger-border` | `--color-tag-danger-border` | Functional/Danger/200 → Semantic Red/200 | `#fedcde` |

**Chip**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `chip-primary` | `Chip/chip-primary` | `--color-chip-primary` | Grey/800 | `#434446` |
| `chip-primary-border` | `Chip/chip-primary-border` | `--color-chip-primary-border` | Grey/300 | `#cbcccc` |
| `chip-secondary` | `Chip/chip-secondary` | `--color-chip-secondary` | Green/600 | `#60a211` |
| `chip-success` | `Chip/chip-success` | `--color-chip-success` | Functional/Success/300 → Semantic Green/300 | `#9fd6a1` |
| `chip-success-text` | `Chip/chip-success-text` | `--color-chip-success-text` | Functional/Success/700 → Semantic Green/700 | `#235825` |
| `chip-warning` | `Chip/chip-warning` | `--color-chip-warning` | Functional/Warning/400 → Semantic Yellow/400 | `#ffb81f` |
| `chip-danger` | `Chip/chip-danger` | `--color-chip-danger` | Functional/Danger/600 → Semantic Red/600 | `#da1e28` |
| `chip-danger-text` | `Chip/chip-danger-text` | `--color-chip-danger-text` | Functional/Danger/700 → Semantic Red/700 | `#9b0810` |
| `chip-text-light` | `Chip/chip-text-light` | `--color-chip-text-light` | White | `#ffffff` |
| `chip-text-dark` | `Chip/chip-text-dark` | `--color-chip-text-dark` | Grey/900 | `#252628` |

**Focus**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `focus-border-focus` | `Focus/border-focus` | `--color-focus-border-focus` | — (local value) | `#007bff` |
| `focus-shadow-focus` | `Focus/shadow-focus` | `--color-focus-shadow-focus` | — (local value) | `rgba(128,189,255,0.4)` |
| `focus-border-error-focus` | `Focus/border-error-focus` | `--color-focus-border-error-focus` | — (local value) | `#dc3545` |
| `focus-shadow-error-focus` | `Focus/shadow-error-focus` | `--color-focus-shadow-error-focus` | — (local value) | `rgba(220,53,69,0.4)` |

**State**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `state-hover-shade` | `State/hover-shade` | `--color-state-hover-shade` | — (local value) | `rgba(0,0,0,0.15)` |
| `state-hover-tint` | `State/hover-tint` | `--color-state-hover-tint` | — (local value) | `rgba(255,255,255,0.15)` |
| `state-pressed-shade` | `State/pressed-shade` | `--color-state-pressed-shade` | — (local value) | `rgba(0,0,0,0.2)` |
| `state-pressed-tint` | `State/pressed-tint` | `--color-state-pressed-tint` | — (local value) | `rgba(255,255,255,0.2)` |

### Primitives (Vyn Global)
These come from the Vyn Global library. They're listed for reference only, so don't reference them from components.

| Ramp | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 |
|---|---|---|---|---|---|---|---|---|---|
| Green | #E8FBD0 | #CDF0A0 | #B3E670 | **#98DB40** (brand) | #7CC123 | #60A211 | #477B04 | #335804 | #141C08 |
| Grey | #F6F7F8 | #E8E9EA | #CBCCCC | #A1A2A3 | #828385 | #656668 | #535456 | #434446 | #252628 |
| Semantic Red | #FFF0F1 | #FEDCDE | #FBB7BA | #F88288 | #F4525B | #DA1E28 | #9B0810 | #62090E | #37080A |
| Semantic Yellow | #FFF5E0 | #FFE5B2 | #FFD175 | #FFB81F | #EB9800 | #AD6500 | #6B3E00 | #472A00 | #291900 |
| Semantic Green | #EAF6EA | #CDEACF | #9FD6A1 | #63BF67 | #39A73F | #267D2B | #235825 | #123013 | #051E0E |

- **Brand group:**
  - `Brand/Green` is #98DB40, the same value as Green/400.
  - `Brand/Black` is #2C2A29, described in Figma as *"For use with Vyn logo only"*.
  - `Brand/White` is #FFFFFF.
  - `White` is #FFFFFF.
- **Figma descriptions:**
  - Green/400: *"Vyn brand green: use is reserved for Vyn logo and VynAI only"* (see D-025).
  - Green/600: *"Branding main green"* (Q-007).
  - Grey/600: *"New secondary text color"*.
  - Semantic Green/500: *"Main color; fill for success buttons and chips"*.
- **Functional aliases:**
  - `Functional/Success` (100, 200, 300, 500, 700) → Semantic Green
  - `Functional/Danger` (100, 200, 300, 600, 700) → Semantic Red
  - `Functional/Warning` (100, 200, 300, 400, 700) → Semantic Yellow
  - `Functional/Info` (100, 200, 400, 500, 800) → Grey
- **Removed since v1:** the warm Grey ramp, the old Green ramp, the separate Neon Green ramp, and Red and Orange (replaced by Semantic Red and Semantic Yellow).

**Primitives used directly today:** four places in Figma bind a primitive because no semantic token exists yet. These are `brand-green` (the logo mark), `grey-500` (navbar workflow-switcher border), `grey-600` (navbar icon-button fill) and `grey-700` (sidebar footer divider). They're in the front matter under their primitive names so they're easy to find and replace once semantic tokens exist (Q-003).

### Usage guidance
- **Actions are charcoal, not green** (D-024). `button-primary`, `link-primary` and `link-primary-active` are Grey/900, and `input-primary-active` is Grey/700. The UI is neutral, and color is kept for status and for Vyn AI.
- **Never put a Primary Filled button on `background-dark`.** Both are Grey/900 today (1:1), so the button disappears. On dark chrome, use the outline treatment the workflow switcher uses (Q-016).
- **Hover and pressed are overlays, not new colors.** Layer `state-hover-shade` (black 15%) or `state-pressed-shade` (black 20%) over the base fill. On dark surfaces, use `state-hover-tint` / `state-pressed-tint` (white 15% / 20%).
- **Borders:**
  - `input-border` (Grey/500, 3.8:1 on white) outlines form controls.
  - `input-border-disabled` (Grey/300) outlines disabled controls.
  - `border` (Grey/200) is the general divider, used by the dropdown menu header and the Input Group documentation.
- **Status:** success, warning and danger alias Semantic Green, Yellow and Red through the Functional layer. Info and default are neutral grey (`alert-default-*`, `tag-default*`), not blue.
- **The neon brand green is for Vyn AI outputs and the logo only** *(provisional, D-012; now also written into the Green/400 description, D-025)*. Don't use it for buttons, links, success states, selection, highlights or decoration. See *Vyn AI UI* for how to apply it.
- **Neon on white is a fill, never a foreground.** Neon on `background-primary` is 1.7:1, which fails even the 3:1 minimum for non-text UI. Use it as a background behind `text-primary` (9:1), or as text and icons on `background-dark` (9:1).
- **On dark chrome** (`background-dark`), use the `link-secondary-light*` family for text.
- **`chip-secondary`** is the last semantic use of Green/600. White text on it is only 3.2:1, which fails AA for small text (Q-017).
- **Non-token values from Bootstrap:** the modal and offcanvas backdrop (black 50%) and the card border (`$border-color-translucent`, black 17.5%) are Bootstrap 5 defaults, not Vyn tokens.

## Typography

### Font Family
- **Inter** (`Family/sans-serif` in Vyn Global). Fallback: Bootstrap 5's native stack, `system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif`. In code, set `$font-family-sans-serif: Inter, <native stack>`.
- One family carries everything. Weights come from Vyn Global's `Weight/*` variables: Regular 400, Medium 500, Semi-Bold 600 and Bold 700. Letter spacing comes from `Letter Spacing/0` and `Letter Spacing/1`.

### Hierarchy
The keys are the Vyn Web App text-style names without their group (`Heading/h1` → `h1`, `Body/body-small-medium` → `body-small-medium`). No CSS developer tokens are published for the new styles yet (Q-021). The *Bootstrap* column is from the Typography page in Figma.

| Style | Size | Weight | Line height | Bootstrap | Use |
|---|---|---|---|---|---|
| `h1` | 28px (1.75rem) | 600 | 1.2 | `h1` | Page headings: Settings, Management, Workflows |
| `h2` | 22px (1.375rem) | 600 | 1.2 | `h2` | Content container headings |
| `h3` | 18px (1.125rem) | 600 | 1.2 | `h3` | Card container headings |
| `h4` | 16px (1rem) | 600 | 1.2 | `h4` | Headings used with regular body copy |
| `h5` | 14px (0.875rem) | 600 | 1.2 | `h5` | Headings used with smaller body copy |
| `h6` | 12px (0.75rem) | 600 | 1.2 | `h6` | |
| `body-base` | 16px | 400 | 1.5 | `p` | Default body copy, input values, menu items |
| `body-base-medium` | 16px | 500 | 1.5 | `p` + `$font-weight-medium` | Emphasized text that isn't a heading, Large button labels, sidebar links, alerts |
| `body-base-semibold` | 16px | 600 | 1.5 | `p` + `$font-weight-semibold` | Input labels (semantically not a heading) |
| `body-small` | 14px | 400 | 1.5 | `p` + `$small-font-size` | Small body copy, helper and error text |
| `body-small-medium` | 14px | 500 | 1.5 | `$small-font-size` + medium | Medium button labels, the workflow switcher |
| `body-small-semibold` | 14px | 600 | 1.5 | `$small-font-size` + semibold | |
| `body-xsmall` | 12px | 400 | 1.5 | — | Extra-small copy: captions, timestamps |
| `body-xsmall-medium` | 12px | 500 | 1.5 | — | Small button labels |
| `body-xsmall-semibold` | 12px | 600 | 1.5 | — | |
| `body-xxsmall` | 10px | 400 | 1.5 | — | Limited use only, because this size is generally too small to read comfortably |
| `body-xxsmall-semibold` | 10px | 600 | 1.5 | — | Limited use only |
| `eyebrow` | 12px | 500, +1px tracking | 1.2 | — | A short label directly above a main heading that gives it context |
| `display-4` | 56px (3.5rem) | 400 | 1.2 | `.display-4` | TBD. Likely analytics dashboards |
| `display-5` | 48px (3rem) | 400 | 1.2 | `.display-5` | |
| `display-6` | 40px (2.5rem) | 400 | 1.2 | `.display-6` | Display numbers in cards |

- **Hidden styles:** `Display/_display-1` (80px), `_display-2` (72px) and `_display-3` (64px) exist but are hidden, described as *"not in active use in Web App"*. Don't use them.
- **Size variables:** the Vyn Web App Typography collection is now named by pixel value: `10`, `12`, `14`, `16`, `18`, `22` and `28`.
- **Bootstrap mapping:** the display sizes match Bootstrap 5's own `.display-*` sizes, though Vyn uses weight 400 where Bootstrap uses 300. The heading sizes don't match Bootstrap's defaults. Set them explicitly:

| Sass variable | Value |
|---|---|
| `$h1-font-size` | 1.75rem |
| `$h2-font-size` | 1.375rem |
| `$h3-font-size` | 1.125rem |
| `$h4-font-size` | 1rem |
| `$h5-font-size` | 0.875rem |
| `$h6-font-size` | 0.75rem |
| `$headings-font-weight` | 600 |
| `$headings-line-height` | 1.2 |
| `$display-font-weight` | 400 |

### Principles
- **Headings are tight, body is relaxed.** Headings use a 1.2 line height and body uses 1.5, which matches Bootstrap's `$line-height-base` (16 × 1.5 = 24).
- **One `h1` per view,** for the page title. Use `h2` for content containers such as sections and drawers, and `h3` for cards.
- **Use weight before size.** Within body copy, go Regular → Medium → Semi-Bold before stepping up a size.
- **Display styles are for figures,** not prose. `display-6` is for numbers in cards, and `display-4` is likely for analytics dashboards.
- **Letter spacing stays at 0,** except `eyebrow` at +1px.
- **Sentence case** for headings, buttons, tabs and menu items.

## Layout

### Spacing System
- **Base unit:** 4px, with 8px as the working rhythm. Tokens: `--space-2`, `-4`, `-8`, `-12`, `-16`, `-24`, `-32`, `-40`, `-80`.
- **Content area padding:** 24px (`--space-24`) on every main content frame and drawer.
- **Panel padding:** 16px for filter panels and cards.
- **Control internals:** 12px horizontal padding in inputs and dropdown items, and 8px between an icon and its label.
- **Sidebar links:** 12px vertical padding with a 12px icon-to-label gap.
- **Stack spacing:** 8px from label to control, 4px from control to helper or error text, and 16px between form fields. The last value is inferred, so confirm it.

### App Shell & Page Templates
Every screen is one of four shells, all designed at **1440 × 900**:

| Template | Structure | Use |
|---|---|---|
| **Desktop** | Navbar (64px) + Sidebar (250px) + Content (fluid, 24px padding) | Default for list and detail pages: Cases, Analytics, Vyns |
| **Desktop + Filter panel** | Navbar + Sidebar + Filter panel (300px, `background-secondary`, 16px padding) + Content | List views with persistent filtering. The content panel gets a 1px left border (black 12%) and a soft shadow so it sits above the filter rail |
| **Desktop + Vyn Viewer Drawer** | Desktop shell + 50% scrim + right-hand drawer | Opening a single Vyn (video + insights) without leaving the list. The drawer starts 290px from the left edge (sidebar + 40px), leaving the list visible behind the scrim for orientation |
| **Desktop + Full Page** | Navbar + Content (no sidebar) | Focused, single-task flows: settings wizards, storyboard editing, anything that needs full width |

**Navbar:** the Vyn logo, then the **Workflow switcher**. This is a standard **Medium Button** (39px tall, 8px 16px padding, 14px `body-small-medium` label) in an outline style for chrome: transparent fill, `Grey/500` border, white label and a trailing dropdown caret. It should match the Button component exactly, not a one-off navbar size. The right side holds the utility links: a notification icon button (40px, `Grey/600` fill, with a danger badge) and the avatar menu.

**Sidebar:** grouped links under uppercase section labels (WORKFLOW, then SETTINGS), with a collapse chevron in the footer. Expanded and collapsed variants exist.

### Grid & Container
- **12-column grid** on the Full Page template: **48px outer margins**, **24px gutters**, stretch alignment, plus an **8px baseline row grid**. This matches Bootstrap's 12-column model and its default 24px (1.5rem) gutter.
- Inside the sidebar shells, content is fluid within the 24px content padding. Use Bootstrap's `.container-fluid` + `.row` + `.col-*` for internal layout.
- **No max content width** is defined. Operational views should fill the viewport. For reading-heavy content (settings forms, long text), cap the line length at around 720px. This cap is a suggestion to confirm.

### Whitespace Philosophy
Dense but not cramped. The product is a working surface, so vertical rhythm is tight (8/12/16px) and large gaps (40/80px) are rare. Separate areas with **surface change and 1px hairlines** (white content against the grey filter rail against the charcoal chrome) rather than large empty space.

## Elevation & Depth

| Level | Treatment | Use |
|---|---|---|
| 0 (flat) | No border, no shadow | Page canvas, chrome |
| 1 (hairline) | 1px `{colors.input-border}`, or Bootstrap's `$border-color-translucent` on cards | Inputs, cards, menus, alerts, accordion |
| 2 (raised) | `--effect-elevation-2-mui` | Card "Drop Shadow" variant, raised content panel beside filters |
| 8 (overlay) | `--effect-elevation-8-mui` | Dropdown menus, popovers, tooltips |
| XL / XXL drop | `--effect-elevation-xl-drop` / `-xxl-drop` | Drawers and modals over a scrim |
| Focus | 4px ring, `{colors.focus-shadow-focus}` plus a `{colors.focus-border-focus}` border | Every focusable control. Error fields use `{colors.focus-shadow-error-focus}` and `{colors.focus-border-error-focus}` |

Rules:
- **Hairlines first, shadows second.** Most containers are separated by a 1px border. Shadows are for things that float: menus, drawers, modals and the raised content panel.
- **The XXL drop is still tinted with the v1 warm grey** (`#57534F`), while the v2 palette is cool grey. Keep it as it is until design decides (Q-019).
- **Scrims are black 50%**, matching Bootstrap's `$modal-backdrop-opacity`.

## Shapes

### Border Radius Scale

| Token | Value | Use |
|---|---|---|
| `--radius-s` | 4px | **Default.** Buttons, inputs, dropdowns, menus, alerts, tooltips |
| *(card)* | 6px | Cards. This value isn't tokenized yet (see Q-002 in DECISIONS.md) |
| `--radius-l` | 8px | Larger containers, modals |
| `--radius-xl` | 16px | Feature panels, media frames |
| `--radius-xxl` | 24px | Hero or marketing surfaces only |
| `--radius-pill` | 1000px | Icon buttons, avatars, badges, status pills |

**Rule of thumb:** rectangles with text labels get 4px, and anything circular or icon-only gets the pill radius. Buttons with text labels never use the pill radius.

### Borders
`--border-1` (1px) for every control, card and divider, `--border-2` (2px) for the selected-tab underline, and `--border-8` (8px) for heavy accents such as left-edge status bars.

### Iconography
- **Material Design icons** (MUI set) are the default icon library and are already in the Vyn codebase. Use the outlined style for utilities (bell, chevrons) and filled glyphs in the sidebar.
- **Vynnie** is the Vyn mascot (see *Brand & Mascot*). A face-less Vynnie silhouette (`.vynnie no face`) is the sidebar icon for Cases and Vyns. The full smiling Vynnie is a brand asset, so keep it for brand moments (empty states, onboarding, Vyn AI identity) and don't use it as a generic icon.
- Sizes: 20px in the sidebar, 14–16px inside buttons, 22px in input add-ons, and 22.5px inside the 40px navbar icon button.

### Photography & Video
Video stills are the product's real imagery. Show them at their native aspect ratio, never crop evidence, frame them in 4px or 8px radius containers, and keep overlays such as timestamps and AI tags legible with a dark scrim. *(The Video Player component is TBD.)*

## Components

Where a component matches a Bootstrap component, **Bootstrap's usage guidance applies** unless this section says otherwise.

### Buttons
Figma defines 108 variants: **Type** (Primary / Secondary / Danger) × **Style** (Filled / Outline / Text) × **Size** (Large 50px / Medium 39px / Small 28px) × **State** (Enabled / Hover / Pressed / Disabled). There are optional left and right icons (Material, instance-swappable), and an **Icon-button** sub-component in 24/32px pill sizes.

| Size | Height | Padding | Label |
|---|---|---|---|
| Large | 50px | 12px 24px | 16px / 500 |
| Medium | 39px | 8px 16px | 14px / 500 |
| Small | 28px | 4px 12px | 12px / 500 |

- **Primary Filled** (`btn-primary`): the one main action in a view or dialog. **Use only one per view region**, as Bootstrap recommends.
- **Primary Outline:** the secondary action beside a primary one, for example "Save draft" next to "Submit". It fills with `button-primary` on hover.
- **Primary Text:** low-emphasis or inline actions such as "View all" or "Add another".
- **Secondary** (`button-secondary` fill, `button-secondary-text` label): neutral actions like Cancel, Close or Back.
- **Danger:** destructive actions only (delete, revoke, reject). Pair each one with a confirmation step.
- **Disabled:** `button-disabled` fill and `button-disabled-text` label. Where possible, explain why in a tooltip or helper text, and prefer hiding an action to disabling it when the user can't do anything about the reason.
- **Order:** the primary button goes on the right in dialogs and forms, following Bootstrap's modal-footer convention.
- **Semantics:** use `<button>` for actions and `<a>` for navigation, even when they look the same.

### Inputs & Forms (Input Group, Textarea)
- **Anatomy:** label (16px Semi-Bold, 8px below it) → 48px field (`input-primary` fill, 1px `input-border`, 4px radius, 12px text padding, `input-text-primary` value) → optional helper, error text or character count (14px, 4px above).
- **Add-ons:** a 48 × 48 `input-secondary` cap with an `input-border` stroke, with a Material icon (for example `person-fill`) on the leading edge. In code, this is Bootstrap 5's `.input-group` with an `.input-group-text` add-on.
- **States:**
  - Enabled.
  - Error: the border and message both switch to `input-danger`.
  - Disabled: `input-disabled` fill with `input-text-disabled` text.
  - Active: `input-primary-active` border.
  - Focus: the blue focus ring.
- **Values:** Empty, Placeholder or Populated. Placeholder text is never a substitute for a label.
- **Required fields:** mark them with `*` after the label. When most fields are required, mark the optional ones instead.
- **Validation (Bootstrap):** use `.is-invalid` on the control with an `.invalid-feedback` message. Validate on blur or submit, not on every keystroke. Show one specific message under the field, such as "Enter a postcode like SW1A 1AA" rather than "Invalid input".
- **Textarea:** same chrome as the text input. Show the character count by default ("0/100 characters") and use a scrollbar variant for long content.

### Dropdown
- **Trigger:** 48px tall, styled like an input, with optional label and icon. It has Collapsed, Expanded and Selected states.
- **Menu:** opens 8px below the trigger, with an `input-primary` fill, 1px `input-border` border, 4px radius and elevation 8. Items are 48px tall with 12px padding in 16px Regular text, and have Enabled, Hover (black 15% overlay), Pressed (black 20%) and Selected states.
- **Menu headers** group items. They get extra top padding (16px) and a divider.
- In code: use `.form-select` for a plain single-value select, and `.dropdown` + `.dropdown-menu` when items need icons, headers or custom rendering.
- Use a dropdown for **5 or more** mutually exclusive options. For 2–4 options, use radio buttons so all choices are visible, following Bootstrap's form guidance.

### Checkbox, Radio & Switch
- **Checkbox:** for multiple independent choices. The Vyn-specific **Excluded** state (from `.Checkbox-exclude`) lets filters express "everything except…". Groups can be vertical (default) or horizontal.
- **Radio Button:** a single choice among 2–5 visible options. Groups come preconfigured with 5 slots, and items should be set to fill in vertical groups.
- **Switch (Toggle):** Bootstrap's `.form-check.form-switch`. An instant on/off setting that applies without a Save button. When the change only applies on submit, use a checkbox instead.
- All three support Required and Focus states.

### Cards & Containers
- **Card:** Bootstrap 5's default `.card`. It's white with a 1px `$border-color-translucent` border (black 17.5%) and a 6px radius (`$border-radius`, 0.375rem), with 16px padding and a 12px internal gap. It's the only container that uses Bootstrap's default radius; buttons and inputs are overridden to 4px. It has a free-form **Content** slot. The **Drop Shadow** variant adds elevation 2 for cards that are clickable or draggable.
- **Accordion:** Bootstrap's `.accordion`. A stacked, expandable list for FAQs and progressive disclosure, with Expanded True/False and slot-based rows. *Per the Figma note, the Accordion isn't currently used in the Web App. Vyn Viewer AI insights use a modified card instead.*
- **Filter panel:** a 300px `background-secondary` rail on the left of list views.
- **Drawer:** Bootstrap's `.offcanvas.offcanvas-end`, sized to the 290px left inset. A right-hand panel over a 50% backdrop, used to open a Vyn without losing list context. Close it with an explicit close button, Esc and a scrim click.

### Alerts
- Four types: **Success, Warning, Danger, Info** (Info is neutral grey). Each has a 1px tinted border, 4px radius, 12px 16px padding and 16px Medium text. There's an optional close button and a content slot for links or actions.
- Following Bootstrap: use alerts for **page- or section-level** feedback about the user's last action or the system state. Put field-level problems on the field itself.
- Don't rely on color alone. Start the message with the outcome ("Saved.", "Couldn't upload video.") or add an icon.
- Only make alerts dismissible (`.alert-dismissible` + `.btn-close`) when the message is no longer needed after it has been read.

### Tabs
- Each tab has 12px 16px padding, an optional icon and a count badge. States are Default, Hover (15% shade), Pressed (20% shade) and **Selected**, which gets a 2px `link-primary` bottom border. In code, this maps to Bootstrap 5.3's `.nav-underline` with the underline color set to `--color-link-primary`.
- Use tabs to switch between **sibling views of the same object**, such as Details, Media and History on a Vyn. Don't use tabs for sequential steps; use a stepper or wizard for those.

### Badge, Avatar & Tooltip
- **Badge:** `.badge.rounded-pill`. An 18px pill counter, positioned inline or top-right (absolute). Types are Primary, Secondary and Danger, and the navbar notification badge uses Danger. **Cap at "99+".**
- **Avatar:** 40px circle in three types. Text shows two initials from the user's first name, Image uses a photo fill, and Icon shows the profile silhouette. Sizes are S, M and L, with Enabled, Hover, Pressed and Inactive states.
- **Tooltip:** four positions with fixed or auto width. Bootstrap 5 tooltips are opt-in, so initialize them in JS. Following Bootstrap, tooltips are **supplementary only**. They open on hover *and* keyboard focus, never hold essential information or interactive content, and aren't used on disabled elements without a focusable wrapper.

### Navigation
- **Navbar** (64px, chrome): the logo, the workflow switcher (a Medium outline Button, 14px label), the notification icon button with its badge, and the avatar menu.
- **Sidebar** (250px, chrome): groups under uppercase section labels (10px Semi-Bold, +1px tracking, `link-secondary-disabled`; no text style applied, see Q-022), with 20px icon + `body-base-medium` label links. Default links use `link-secondary-light`, and the active link uses `link-secondary-light-active`. There are Expanded and Collapsed variants with a collapse chevron in the footer.
- The **BETA pill** next to the WORKFLOW label is a **temporary placeholder**. Its purple colors aren't part of the Vyn system, so don't reuse them or build on them. If a pre-release marker is needed before one is designed, use a neutral Tag (`Tag/tag-default`).

### TBD components
Breadcrumb, Chip and Tag (on hold, though tokens exist), Filters, Modal, Pagination, Progress, Table and Video Player are **TBD**. They have placeholder pages in Figma but no design yet. Until they're designed, **use the stock Bootstrap 5 component with Vyn tokens**: 4px radius, `input-border` borders, Inter type and the semantic color tokens. Don't invent a bespoke version.

### Bootstrap theming map
Set these Bootstrap 5 Sass variables (or their `--bs-*` CSS variables) from Vyn tokens so that stock components pick up the brand:

Point each variable at the Vyn CSS variable rather than pasting a hex, so that a token change flows through automatically. Values live only in *Colors → Semantic tokens*.

| Bootstrap variable | Vyn token |
|---|---|
| `$primary` / `--bs-primary` | `var(--color-button-primary)` (Grey/900 in v2) |
| `$secondary` | `var(--color-button-secondary)` |
| `$danger` | `var(--color-button-danger)` |
| `$success` | `Functional/Success/500` primitive, Semantic Green/500 (no semantic token yet, see Q-004) |
| `$warning` | `Functional/Warning/400` primitive, Semantic Yellow/400 (no semantic token yet, see Q-004) |
| `$body-color` | `var(--color-text-primary)` |
| `$body-secondary-color` | `var(--color-text-secondary)` |
| `$body-bg` | `var(--color-background-primary)` |
| `$tertiary-bg` | `var(--color-background-secondary)` |
| `$border-color` | `var(--color-input-border)` |
| `$link-color` | `var(--color-link-primary)` |
| `$font-family-sans-serif` | `--font-family-sans-serif` (Inter + native stack) |
| `$btn-border-radius`, `$input-border-radius`, `$alert-border-radius`, `$dropdown-border-radius` | `--radius-s` (Bootstrap's default is 6px) |
| `$focus-ring-color` / `$input-focus-box-shadow` | `var(--color-focus-shadow-focus)`, 0.25rem |
| `$input-focus-border-color` | `var(--color-focus-border-focus)` |
| `$gray-100`…`$gray-900` | `--color-grey-100`…`--color-grey-900` primitives (Vyn Global) |

Sass needs literal values at compile time. If the build compiles Bootstrap from Sass, generate these assignments from the token file rather than typing hex by hand.

Keep Bootstrap's defaults for `$line-height-base` (1.5), `$grid-gutter-width` (1.5rem), `$border-radius` for cards (0.375rem), `$border-color-translucent`, and the modal and offcanvas backdrop opacity (0.5).

## Motion

Vyn uses **Bootstrap 5's default transitions** and defines no motion tokens of its own. Don't hand-roll durations. Use the Bootstrap component or its Sass variable.

| Interaction | Bootstrap default |
|---|---|
| Buttons, inputs, nav links (color, background, border, focus ring) | `.15s ease-in-out` (`$btn-transition`, `$input-transition`, `$nav-link-transition`) |
| Generic transitions | `all .2s ease-in-out` (`$transition-base`) |
| Fade-in elements: tooltips, popovers, toasts, alerts on dismiss | `opacity .15s linear` (`$transition-fade`) |
| Accordion / collapse expand | `height .35s ease` (`$transition-collapse`) |
| Accordion chevron rotation | `transform .2s ease-in-out` |
| Drawer (offcanvas) slide-in | `transform .3s ease-in-out` |
| Modal entrance | `transform .3s ease-out` from `translate(0, -50px)` |
| Progress bar fill | `width .6s ease` |

Dropdown menus open instantly, with no animation, which is also Bootstrap's default. Keep `$enable-reduced-motion: true` (the default) so that every transition is removed under `prefers-reduced-motion: reduce`.

## Vyn AI UI

> **Status: in progress.** The team is currently working to make Vyn AI's outputs more **transparent, helpful and actionable** for web-app users. Rules in this section are provisional, and there are no dedicated AI components or tokens in Figma yet. Treat this section as direction, not spec.

### Scope
This section covers **AI UI**: how Vyn AI's outputs are *presented in the desktop web app*, mainly in the **Vyn Viewer**.

| In scope | Out of scope |
|---|---|
| **AI summaries** of a Vyn | **AI nudges**, which are notifications sent to field workers in the *mobile app* |
| **AI-generated labels**, including their **evidence frames** | **Agentic Toolbox**, where users create and deploy custom agents and triage rules |
| Other Vyn AI outputs shown to supervisors and customer-care staff | Mobile capture UI |

### Neon marks Vyn AI (provisional)
- **Every Vyn AI output gets the same, consistent marker** so users can always tell AI content from human-entered content. The marker combines three things:
  1. the neon brand green (`brand-green`, Figma `Brand/Green`),
  2. a text label ("Vyn AI"), because color alone is never the only signal,
  3. optionally, the Vynnie mark.
- **Where it goes:** on the output's container, such as the summary card header or the label chip, not scattered through the content.
- **How to apply the color:**
  - **On light surfaces:** neon as a *fill* with `text-primary` on top, for example a small "Vyn AI" tag, or a header band on the summary card. Neon borders and underlines on white are decorative only, so always pair them with the text label.
  - **On dark surfaces:** neon text and icons are fine at 9:1.
- **Nothing else is neon.** If it isn't a Vyn AI output or the logo, it doesn't use neon. That's how the marker keeps its meaning.
- Per the Figma note, Vyn Viewer AI insights currently use a **modified Card**, not the Accordion. Build AI output containers on `card`.

### Make outputs transparent, helpful and actionable
These follow from the brand values (Trust: *show the evidence*; Mutuality: *everyone sees the same picture*):

- **Transparent: show where it came from.**
  - Attach the **evidence frame** or timestamp to every label that has one, and make it one click to jump to that moment in the video.
  - Say that it's AI-generated. Where confidence is available, express it in plain language ("Likely", "Check this"), not as unexplained percentages.
- **Helpful: summaries first, detail on demand.**
  - Lead with the outcome in one or two sentences ("Show, don't claim").
  - Let the supporting labels and frames sit underneath, so AI supports the human judgement rather than replacing it.
- **Actionable: put the next step on the output.**
  - Put the action right next to the AI output, for example *Accept label*, *Edit*, *Reject*, *Send to crew* or *Review Vyn*.
  - The person always makes the final call. Record human overrides visibly, so everyone sees the same record.
- **States:** design each output for processing ("Vyn AI is analysing this Vyn…"), no output ("Vyn AI didn't find anything to flag"), partial, and failed states. Never leave an empty neon container.

### AI copy
- **AI helps the people doing the work.** The brand is at the frontier of AI, in a space with a lot of fear about job loss, so the voice stays warm and human. Write "Vyn AI spotted…", "Suggested label" or "Check this frame", not language that implies the AI decides or replaces anyone.
- **Keep it factual about uncertainty.** No hype, and no false certainty ("Vyn AI has determined…"). Plain, specific and checkable.
- **Stay serious near risk.** AI outputs about safety, flooding, fines or compliance use no playful copy and no mascot expressions.

## Voice & Content

The Brand Feel audit defines four values and four voice principles. They apply to in-app copy (buttons, empty states, errors, onboarding) as well as marketing.

### Values → personality

| Value | As a trait | In the UI |
|---|---|---|
| **Simplicity** | Uncomplicated: takes the effort away | Fewer steps, plain labels, defaults that just work. "No new learning required." |
| **Velocity** | Quick, without cutting corners | Fast paths for frequent actions, and a clear "right first time" confirmation |
| **Trust** | Dependable: shows the evidence | Show the video, the timestamp and the reviewer. Don't just assert that something is "Approved" |
| **Mutuality** | Collaborative: everyone sees the same picture | Shared status, visible ownership, and desk and field seeing the same record |

### Voice principles

| Principle | Tactic | Example |
|---|---|---|
| **Show, don't claim** | Lead with the number. Cut the hedges | "3 jobs need re-work", not "Some jobs may potentially require attention" |
| **Talk to the person doing the work** | Name the job, not the tech. Say "you". Use plain words | "Film the job. Get it signed off." rather than "mobile & video first experience". "Your crews", not "stakeholders" |
| **Keep it moving** | Verbs first. One idea per sentence | Buttons: "Review Vyn", "Send to crew", "Approve". Split any line with more than one "and" |
| **Serious about safety, light about everything else** | Play only where the stakes allow. Never joke about risk | Playful in welcome and empty states. Never playful near fines, flooding, injuries or compliance |

### Brand & Mascot: Vynnie
- **Who Vynnie is:** the Vyntelligence mascot. Vynnie was born from the visual, human element of the first logo, and the face is made from the letters **v, y, n**.
- **What Vynnie stands for:** the core of the brand, **professional but playful**. That applies everywhere: the AI in the backend, how clients are engaged, and how people feel when they use the product.
- **The smile matters.** It carries a warm personality on purpose. At the frontier of AI, where many people worry about job loss, Vynnie signals that the technology is on the side of the people doing the work.
- **Always premium.** Vyn green against a black or dark backdrop is the signature pairing: playful energy meets a premium, professional look. Every version of the experience, digital or physical, should feel premium.
- **Vynnie has grown arms and legs** as Vyn moves into **Physical World AI**, taking the brand from the screen into on-site work.
- **In the web app:** use Vynnie sparingly. The face-less silhouette is the sidebar icon, and the full Vynnie is for brand moments (empty states, onboarding, Vyn AI identity). Never use Vynnie near safety-critical or compliance content, where it would read as flippant.

### Brand vocabulary
- **Names:** *Vyntelligence* (the company), *Vyn* (the product, and also one captured video/job, as in "every Vyn"), *Vyn AI®* (the analysis layer), *CX* and *FX* (the product lines), *Vynnie* (the mascot).
- **Product features:**
  - *AI summaries*, *labels* and *evidence frames* (Vyn AI outputs shown in the Vyn Viewer).
  - *AI nudges* (mobile notifications to field workers).
  - *Agentic Toolbox*. It's also called "Agent Toolbox" or "Smart Agent Toolbox", but use **Agentic Toolbox**, which matches the sidebar label.
  - *Physical World AI* (the company's focus area).
- **Coined words:** *Vynners* (users and staff) and *Vynified*. Use them sparingly, in welcome, onboarding and celebration moments only.
- **Recurring phrases:** "Seeing is believing" (the recommended brand promise), "right first time" and "digital eyes and ears".

## Do's and Don'ts

### Do
- Use the charcoal action tokens (`button-primary`, `link-primary`, `input-primary-active`) for actions: primary buttons, links, the active input and the selected tab.
- Use the most specific semantic token for every property, even when a different token has the same value today. Tokens will diverge as the DLS evolves.
- Build every screen from one of the four shell templates, and keep the 24px content padding.
- Use weight (400 → 500 → 600) to create hierarchy before reaching for a bigger size.
- Use the hover and pressed **overlays** (black 15% / 20%, white on dark) instead of inventing new hex values.
- Use 4px radius for anything with a text label and the pill radius for icon-only controls, avatars and badges.
- Separate regions with surface change (`background-primary` / `background-secondary` / `background-dark`) and 1px hairlines.
- Reference semantic tokens (`--color-button-primary`) in code, never primitives (`--color-green-600`) or raw hex.
- Fall back to the Bootstrap component and its usage guidance whenever a pattern isn't specified, then apply Vyn tokens.
- Show the evidence (video, time, person) next to any AI-generated status.
- Mark every Vyn AI output with the same neon + "Vyn AI" label treatment, and give it an action the user can take.

### Don't
- Don't put a Primary Filled button on dark chrome (`button-primary` on `background-dark` is 1:1). Use the outline treatment and the `link-secondary-light*` tokens there.
- Don't use neon brand green for anything except Vyn AI outputs and the logo (provisional): no neon buttons, links, highlights, selection or success states.
- Don't use neon as text, a thin border or a lone icon on light surfaces (1.7:1). On light surfaces it's a fill behind `text-primary`.
- Don't use the success green (`Semantic Green`) for primary actions, or the neon brand green for success states.
- Don't use more than one Primary Filled button in a view region.
- Don't use pill-shaped text buttons, or round inputs and cards beyond the documented radii.
- Don't use Bootstrap's default heading sizes (its 2.5rem `h1`). Set the Vyn sizes, where `h1` is 28px. Don't use the hidden `_display-1` to `_display-3` styles.
- Don't use pure black (#000) or raw hex for text or surfaces. Use the semantic text and background tokens.
- Don't use Bootstrap's default greys (`$gray-*`). Map them to the Vyn Global Grey ramp.
- Don't put essential information in tooltips, or joke anywhere near safety or compliance content.

## Responsive Behavior

**The Vyn Web App is desktop-only for now.** There are no tablet or mobile layouts, and new work shouldn't design them.

### Supported viewports
- **Design target:** 1440 × 900. Every shell template is drawn at this size.
- **Minimum supported width:** 1280px. This is the Navbar component's base width in Figma. Below 1280, let the page scroll horizontally rather than reflowing into a mobile layout.
- **Wide screens (1920+):** shells stay full width, and content areas stretch. Use the 12-column grid to add columns, not bigger type.
- Bootstrap 5's `xl` (1200px) and `xxl` (1400px) breakpoints are the only ones in play. Use them for density adjustments inside content, such as 3-up vs. 4-up card grids. Don't use `sm`, `md` or `lg` layouts.

### Sidebar
The sidebar collapses from 250px to icon-only (`.Link-collapsed`) when the user presses the chevron in its footer. It doesn't collapse automatically at any width.

### Pointer targets
Desktop pointer targets must be at least **24 × 24px** (WCAG 2.2, 2.5.8). The Small icon button (24px) is the smallest allowed. Don't shrink controls below the documented sizes.

## Accessibility

- **Contrast checks** (WCAG 2.2 AA) **at current token values.** Re-check whenever one of these tokens changes:
  - `text-primary`, `link-primary` and `button-primary` on `background-primary`: 15.2:1.
  - `text-secondary` on `background-primary`: 7.6:1. On `background-secondary` it's 7.1:1.
  - `button-primary-text` on `button-danger`: 5.0:1.
  - `link-secondary-light` on `background-dark`: 9.4:1. `link-secondary-disabled` (sidebar labels) on `background-dark` is 5.9:1.
  - `input-border` on white: 3.8:1, which passes the 3:1 minimum for control borders. `input-border-disabled` is 1.6:1 and `border` is 1.2:1, so use those only for disabled or decorative edges.
  - Alert text on its own background: 7.6:1 (success), 8.4:1 (warning), 7.8:1 (danger) and 9.1:1 (default).
  - `link-secondary-light-disabled` on `background-dark`: 4.0:1, and `button-disabled-text` on `button-disabled`: 2.1:1. Both are acceptable only because they're disabled.
  - **Failing pairs:**
    - `button-primary` on `background-dark` is 1:1 (Q-016).
    - `chip-text-light` on `chip-secondary` is 3.2:1 (Q-017).
    - The navbar icon button (`grey-600`) on `background-dark` is 2.6:1, below 3:1 for a control (Q-018).
- **Focus:** every interactive element shows the 4px focus ring (`focus-shadow-focus`, plus `focus-border-focus` on inputs) and must never have `outline: none` without it.
- **Color is never the only signal.** Pair status color with text or an icon, which applies to alerts, badges, tags and validation.
- **Keyboard:** drawers and modals trap focus and close on Esc. Dropdowns and tabs follow the WAI-ARIA patterns that Bootstrap implements.
- **Motion:** keep Bootstrap's `$enable-reduced-motion` on so drawers, modals and accordions don't animate under `prefers-reduced-motion`.

## Iteration Guide

1. Work on **one component at a time** and refer to it by its `components:` token name, for example `button-primary-outline` or `text-input-error`. Colors, type and radii are referenced by their token keys.
2. Start from the matching **Bootstrap 5 component**, themed with the variables in *Bootstrap theming map*. Don't restyle it with bespoke CSS.
3. Pick the **shell template** first (Desktop, + Filter panel, + Drawer, Full Page), then lay out content on the 12-column / 24px-gutter grid.
4. Default body text to `body-base` (16/24) and dense views to `body-small` (14/21).
5. Add new variants as separate component entries (`-hover`, `-selected`, `-error`) that reference existing tokens.
6. Before shipping, check new copy against the four voice principles, especially near safety or compliance content.
7. When a token value changes, update its front-matter line and its row in *Semantic tokens*, re-check the contrast pairs under *Accessibility*, then run `npx @google/design.md lint DESIGN.md`.

## Decisions, Deferred and Open Questions

The full record, with dates, owners, reasons and history, lives in [`DECISIONS.md`](DECISIONS.md). This section summarizes what's currently in force. Entries marked *proposed* were drafted by Claude and are awaiting confirmation.

**In force**
- **D-001:** the live Figma variables (Vyn Global + Vyn Web App) are the source of truth.
- **D-002:** the codebase uses Bootstrap 5.3.x.
- **D-003:** desktop-only. *(proposed: D-016, a 1280px minimum width)*
- **D-004:** Bootstrap 5 default motion.
- **D-005:** placeholder components are TBD, so use stock Bootstrap meanwhile.
- **D-006:** the focus ring stays classic Bootstrap blue. *(provisional)*
- **D-007:** the BETA pill is a placeholder.
- **D-008:** the sidebar is 250px, and the drawer inset is 290px.
- **D-009:** the Workflow switcher is a Medium Button with a 14px label.
- **D-010:** token names mirror the developer tokens and are never merged.
- **D-011:** the Tag token renames (Figma still has the old names, Q-015).
- **D-012:** the neon brand green is for Vyn AI outputs and the logo only. *(provisional)*
- **D-013:** AI UI scope is outputs in the web app, not nudges or Agentic Toolbox.
- **D-023:** the v2 palette (cool greys, Semantic Red, Yellow and Green, a rebuilt Green ramp).
- **D-024:** primary actions are charcoal, not green. *(supersedes D-017)*
- **D-025:** the brand green is `Brand/Green`, which equals Green/400 (#98DB40). The separate Neon Green ramp is gone.
- **D-026:** new semantic tokens `border` and `input-border-disabled`.
- **D-027:** the v2 type scale (h1–h6, body-base/small/xsmall/xxsmall, eyebrow, display-4 to 6). *(provisional: "Proposed / In-flight" in Figma)*
- **D-029:** v2 lives on the `v2` branch, and v1 is kept as it is.
- **D-030:** the v2 design-system page is separate from the v1 page.
- **D-031:** a Vyn-branded, interactive v2 page sits alongside the template page.
- **Proposed, awaiting confirmation:**
  - **D-018:** neon on light grounds is only a fill.
  - **D-019:** one Vyn AI marker.
  - **D-020:** cards keep Bootstrap's radius and border.
  - **D-021:** the standard name is "Agentic Toolbox".
  - **D-028:** type keys use the text-style names.

**Deferred.** Leave these as they are until resolved:
- **D-014:** the secondary outline button border (`button-secondary`, about 1.2:1 on white).
- **D-015:** dark mode. There's only a Light mode.

**Open:**
- **Q-001:** regenerate the Foundations page from the variables.
- **Q-002:** give the card radius and border token names?
- **Q-003:** semantic tokens for the primitives bound directly in Figma.
- **Q-004:** success and warning fill tokens.
- **Q-006:** `AI/*` tokens and an AI output component.
- **Q-007:** fix the Green/600 description.
- **Q-008:** do Agentic Toolbox outputs get the neon marker?
- **Q-009:** document the remaining component sets.
- **Q-010:** review the marketing site.
- **Q-011:** confirm the 1280px minimum width.
- **Q-012:** a logo for light backgrounds?
- **Q-014:** keep `DESIGN.md` and the design-system page in sync.
- **Q-015:** rename the Tag variables in Figma, or revert D-011?
- **Q-016:** `button-primary` equals `background-dark`.
- **Q-017:** `chip-secondary` contrast.
- **Q-018:** navbar icon-button contrast.
- **Q-019:** the XXL shadow tint.
- **Q-020:** `Brand/Black` vs `background-dark`.
- **Q-021:** CSS tokens for the v2 text styles.
- **Q-022:** sidebar labels don't use `Utility/eyebrow`.
