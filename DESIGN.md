---
version: alpha
name: Vyn-Web-App-design
description: "A calm, desk-side operations console for utilities and infrastructure teams: white work surfaces framed by warm charcoal chrome (background-dark), one confident brand green (button-primary) for action, and warm stone greys for everything structural. Type is Inter throughout, set small and dense (16px body, 20px H1) with a 150% line-height, because the product is read all day by people triaging video evidence, not skimmed once. Components are Bootstrap-shaped (4px radius, 1px borders, 48px form controls) with Material icons. The personality is practical and proven first, lightly playful second: the product earns trust by showing the evidence, not by decorating it."

# Naming rule: every key is the developer token minus its category prefix,
# so {colors.text-secondary} == --color-text-secondary == Figma "Text/text-secondary".
# Semantic tokens are listed one per variable and are NEVER merged, even when
# two share a value today. To change a value, edit that one line.
colors:
  # --- Text ---
  text-primary: "#2c2a29"                   # Text/text-primary → Grey/800
  text-secondary: "#585450"                 # Text/text-secondary → Grey/600
  text-white: "#ffffff"                     # Text/text-white → White/100
  text-success: "#166534"                   # Text/text-success → Functional/Success/800 → Semantic Green/800
  text-warning: "#bf360c"                   # Text/text-warning → Functional/Warning/900 → Orange/900
  text-danger: "#b71c1c"                    # Text/text-danger → Functional/Danger/800 → Red/800
  # --- Background ---
  background-primary: "#ffffff"             # Background/bg-primary → White/100
  background-secondary: "#f5f4f3"           # Background/bg-secondary → Grey/100
  background-dark: "#2c2a29"                # Background/bg-dark → Grey/800
  # --- Button ---
  button-primary: "#548118"                 # Button/btn-primary → Green/600
  button-primary-text: "#ffffff"            # Button/btn-primary-text → White/100
  button-secondary: "#ebeae8"               # Button/btn-secondary → Grey/200
  button-secondary-text: "#2c2a29"          # Button/btn-secondary-text → Grey/800
  button-danger: "#c62828"                  # Button/btn-danger → Functional/Danger/700 → Red/700
  button-disabled: "#ebeae8"                # Button/btn-disabled → Grey/200
  button-disabled-text: "#a6a29e"           # Button/btn-disabled-text → Grey/400
  # --- Input ---
  input-primary: "#ffffff"                  # Input/input-primary → White/100
  input-secondary: "#f5f4f3"                # Input/input-secondary → Grey/100
  input-primary-active: "#548118"           # Input/input-primary-active → Green/600
  input-disabled: "#f5f4f3"                 # Input/input-disabled → Grey/100
  input-text-primary: "#2c2a29"             # Input/input-text-primary → Grey/800
  input-text-secondary: "#585450"           # Input/input-text-secondary → Grey/600
  input-text-disabled: "#a6a29e"            # Input/input-text-disabled → Grey/400
  input-text-light: "#ffffff"               # Input/input-text-light → White/100
  input-border: "#d6d4d1"                   # Input/input-border → Grey/300
  input-danger: "#b71c1c"                   # Input/input-danger → Functional/Danger/800 → Red/800
  # --- Link ---
  link-primary: "#548118"                   # Link/link-primary → Green/600
  link-primary-active: "#548118"            # Link/link-primary-active → Green/600
  link-primary-disabled: "#a6a29e"          # Link/link-primary-disabled → Grey/400
  link-secondary: "#2c2a29"                 # Link/link-secondary → Grey/800
  link-secondary-active: "#2c2a29"          # Link/link-secondary-active → Grey/800
  link-secondary-disabled: "#a6a29e"        # Link/link-secondary-disabled → Grey/400
  link-secondary-light: "#d6d4d1"           # Link/link-secondary-light → Grey/300
  link-secondary-light-active: "#ffffff"    # Link/link-secondary-light-active → White/100
  link-secondary-light-disabled: "#7c7874"  # Link/link-secondary-light-disabled → Grey/500
  # --- Alert ---
  alert-default-bg: "#f5f4f3"               # Alert/alert-default-bg → Grey/100
  alert-default-border: "#ebeae8"           # Alert/alert-default-border → Grey/200
  alert-default-text: "#403d3b"             # Alert/alert-default-text → Grey/700
  alert-success-bg: "#dcfce7"               # Alert/alert-success-bg → Functional/Success/100 → Semantic Green/100
  alert-success-border: "#bbf7d0"           # Alert/alert-success-border → Functional/Success/200 → Semantic Green/200
  alert-success-text: "#14532d"             # Alert/alert-success-text → Functional/Success/900 → Semantic Green/900
  alert-warning-bg: "#fff3e0"               # Alert/alert-warning-bg → Functional/Warning/100 → Orange/100
  alert-warning-border: "#ffe0b2"           # Alert/alert-warning-border → Functional/Warning/200 → Orange/200
  alert-warning-text: "#bf360c"             # Alert/alert-warning-text → Functional/Warning/900 → Orange/900
  alert-danger-bg: "#ffebee"                # Alert/alert-danger-bg → Functional/Danger/100 → Red/100
  alert-danger-border: "#ffcdd2"            # Alert/alert-danger-border → Functional/Danger/200 → Red/200
  alert-danger-text: "#5f0f0f"              # Alert/alert-danger-text → Functional/Danger/900 → Red/900
  # --- Tag ---
  tag-default: "#f5f4f3"                    # Tag/tag-default → Grey/100
  tag-default-text: "#2c2a29"               # Tag/tag-default-text → Grey/800
  tag-default-border: "#ebeae8"             # Tag/tag-default-border → Grey/200
  tag-success: "#dcfce7"                    # Tag/tag-success → Functional/Success/100 → Semantic Green/100
  tag-success-text: "#14532d"               # Tag/tag-success-text → Functional/Success/900 → Semantic Green/900
  tag-success-border: "#bbf7d0"        # Tag/tag-success-border → Functional/Success/200 → Semantic Green/200
  tag-warning: "#fff3e0"                 # Tag/tag-warning → Functional/Warning/100 → Orange/100
  tag-warning-text: "#bf360c"               # Tag/tag-warning-text → Functional/Warning/900 → Orange/900
  tag-warning-border: "#ffe0b2"             # Tag/tag-warning-border → Functional/Warning/200 → Orange/200
  tag-danger: "#ffebee"                  # Tag/tag-danger → Functional/Danger/100 → Red/100
  tag-danger-text: "#b71c1c"                # Tag/tag-danger-text → Functional/Danger/800 → Red/800
  tag-danger-border: "#ffcdd2"              # Tag/tag-danger-border → Functional/Danger/200 → Red/200
  # --- Chip ---
  chip-primary: "#2c2a29"                   # Chip/chip-primary → Grey/800
  chip-primary-border: "#d6d4d1"            # Chip/chip-primary-border → Grey/300
  chip-secondary: "#548118"                 # Chip/chip-secondary → Green/600
  chip-success: "#86efac"                   # Chip/chip-success → Functional/Success/300 → Semantic Green/300
  chip-success-text: "#14532d"              # Chip/chip-success-text → Functional/Success/900 → Semantic Green/900
  chip-warning: "#ffa726"                   # Chip/chip-warning → Functional/Warning/400 → Orange/400
  chip-danger: "#c62828"                    # Chip/chip-danger → Functional/Danger/700 → Red/700
  chip-danger-text: "#5f0f0f"               # Chip/chip-danger-text → Functional/Danger/900 → Red/900
  chip-text-light: "#ffffff"                # Chip/chip-text-light → White/100
  chip-text-dark: "#2c2a29"                 # Chip/chip-text-dark → Grey/800
  # --- Focus ---
  focus-border-focus: "#007bff"             # Focus/border-focus
  focus-shadow-focus: "rgba(128,189,255,0.4)"  # Focus/shadow-focus
  focus-border-error-focus: "#dc3545"       # Focus/border-error-focus
  focus-shadow-error-focus: "rgba(220,53,69,0.4)"  # Focus/shadow-error-focus
  # --- State ---
  state-hover-shade: "rgba(0,0,0,0.15)"     # State/hover-shade
  state-hover-tint: "rgba(255,255,255,0.15)"  # State/hover-tint
  state-pressed-shade: "rgba(0,0,0,0.2)"    # State/pressed-shade
  state-pressed-tint: "rgba(255,255,255,0.2)"  # State/pressed-tint
  # --- Primitives referenced directly in Figma (no semantic token yet — see Known Gaps) ---
  grey-500: "#7c7874"                     # Grey/500 — navbar workflow-switcher border
  grey-600: "#585450"                     # Grey/600 — navbar icon-button fill
  grey-700: "#403d3b"                     # Grey/700 — sidebar footer divider
  neon-green-800: "#98db40"               # Neon Green/800 — logo mark on dark chrome

typography:
  header-h1-semi-bold:                # --font-header-h1-semi-bold
    fontFamily: Inter
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  header-h2-semi-bold:                # --font-header-h2-semi-bold
    fontFamily: Inter
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  header-h3-regular:                # --font-header-h3-regular
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  header-h3-medium:                # --font-header-h3-medium
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  header-h3-semi-bold:                # --font-header-h3-semi-bold
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  header-h4-regular:                # --font-header-h4-regular
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  header-h4-medium:                # --font-header-h4-medium
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  header-h4-semi-bold:                # --font-header-h4-semi-bold
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  body-p1-regular:                # --font-body-p1-regular
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-p1-medium:                # --font-body-p1-medium
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  body-p1-semi-bold:                # --font-body-p1-semi-bold
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  body-p2-regular:                # --font-body-p2-regular
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-p2-medium:                # --font-body-p2-medium
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  body-p2-semi-bold:                # --font-body-p2-semi-bold
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  body-p3-regular:                # --font-body-p3-regular
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-p3-medium:                # --font-body-p3-medium
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  body-p3-semi-bold:                # --font-body-p3-semi-bold
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  body-p4-regular:                # --font-body-p4-regular
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-p4-medium:                # --font-body-p4-medium
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  body-p4-semi-bold:                # --font-body-p4-semi-bold
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  eyebrow:            # NOT a Figma text style — composed from --font-xxs, --font-weight-bold, --font-letter-spacing-2; set UPPERCASE in CSS
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 700
    lineHeight: 1
    letterSpacing: 2px

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
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    height: 50px
    padding: 12px 24px
  button-primary-md:
    backgroundColor: "{colors.button-primary}"
    textColor: "{colors.button-primary-text}"
    typography: "{typography.body-p2-medium}"
    rounded: "{rounded.s}"
    height: 39px
    padding: 8px 16px
  button-primary-sm:
    backgroundColor: "{colors.button-primary}"
    textColor: "{colors.button-primary-text}"
    typography: "{typography.body-p3-medium}"
    rounded: "{rounded.s}"
    height: 28px
    padding: 4px 12px
  button-primary-outline:
    textColor: "{colors.button-primary}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-primary-text:
    textColor: "{colors.button-primary}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-secondary:
    backgroundColor: "{colors.button-secondary}"
    textColor: "{colors.button-secondary-text}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-secondary-outline:
    textColor: "{colors.button-secondary-text}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-danger:
    backgroundColor: "{colors.button-danger}"
    textColor: "{colors.button-primary-text}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 24px
  button-disabled:
    backgroundColor: "{colors.button-disabled}"
    textColor: "{colors.button-disabled-text}"
    typography: "{typography.body-p1-medium}"
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
    typography: "{typography.body-p1-regular}"
    rounded: "{rounded.s}"
    height: 48px
    padding: 0 12px
  text-input-error:
    backgroundColor: "{colors.input-primary}"
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-p1-regular}"
    rounded: "{rounded.s}"
    height: 48px
  text-input-disabled:
    backgroundColor: "{colors.input-disabled}"
    textColor: "{colors.input-text-disabled}"
    typography: "{typography.body-p1-regular}"
    rounded: "{rounded.s}"
    height: 48px
  input-addon:
    backgroundColor: "{colors.input-secondary}"
    size: 48px
    padding: 12px
  input-label:
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-p1-semi-bold}"
  input-error-text:
    textColor: "{colors.input-danger}"
    typography: "{typography.body-p2-regular}"
  dropdown-trigger:
    backgroundColor: "{colors.input-primary}"
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-p1-regular}"
    rounded: "{rounded.s}"
    height: 48px
    padding: 12px
  dropdown-menu:
    backgroundColor: "{colors.input-primary}"
    rounded: "{rounded.s}"
  dropdown-item:
    backgroundColor: "{colors.input-primary}"
    textColor: "{colors.input-text-primary}"
    typography: "{typography.body-p1-regular}"
    height: 48px
    padding: 12px
  card:
    backgroundColor: "{colors.background-primary}"
    rounded: 6px                  # Bootstrap 5 $border-radius (not a Vyn token)
    padding: 16px
  alert-default:
    backgroundColor: "{colors.alert-default-bg}"
    textColor: "{colors.alert-default-text}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 16px
  alert-success:
    backgroundColor: "{colors.alert-success-bg}"
    textColor: "{colors.alert-success-text}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 16px
  alert-warning:
    backgroundColor: "{colors.alert-warning-bg}"
    textColor: "{colors.alert-warning-text}"
    typography: "{typography.body-p1-medium}"
    rounded: "{rounded.s}"
    padding: 12px 16px
  alert-danger:
    backgroundColor: "{colors.alert-danger-bg}"
    textColor: "{colors.alert-danger-text}"
    typography: "{typography.body-p1-medium}"
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
    typography: "{typography.body-p2-medium}"
    rounded: "{rounded.s}"
    height: 39px
    padding: 8px 16px
  sidebar:
    backgroundColor: "{colors.background-dark}"
    width: 250px
  sidebar-link:
    textColor: "{colors.link-secondary-light}"
    typography: "{typography.body-p1-medium}"
    padding: 12px 18px
  sidebar-link-active:
    textColor: "{colors.link-secondary-light-active}"
    typography: "{typography.body-p1-medium}"
    padding: 12px 18px
  sidebar-section-label:
    textColor: "{colors.link-secondary-disabled}"
    typography: "{typography.eyebrow}"
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

Vyn is the web console for **Vyntelligence**. Customers and field crews record short guided videos, Vyn AI® analyses them, and desk teams use this app to review what came back, triage it and act on it. The two product lines are **CX** (Customer Experience) and **FX** (Field Experience). The core users are operations managers, back-office teams and supervisors at UK utilities (water, gas, energy, telecoms), and the US infrastructure market is next.

The brand audit sums up the feel in one line: *"a practical, proven, slightly playful engineering partner."* The UI should read the same way. It's a tool people trust with safety and compliance evidence, so it stays calm and legible, and the personality shows up in small places (the Vynnie icon, the brand words, the neon green mark on dark chrome) rather than in decoration.

The codebase runs on **the latest Bootstrap (5.3.x)**, and most components are stock Bootstrap themed with Vyn tokens. That means 4px control corners, 1px borders, 48px form controls and a Bootstrap-width (0.25rem) focus ring in classic Bootstrap blue. It uses **Material icons** throughout and Material elevation values for shadows. On top of that sits a warm, Vyn-specific palette: stone greys with a brown undertone (`#2c2a29` → `#f5f4f3`) instead of Bootstrap's cool greys, and one brand green.

**Key characteristics:**
- **Dark chrome, light work area.** The navbar and sidebar sit on warm charcoal `{colors.background-dark}`. Everything the user works on sits on white `{colors.background-primary}`, with `{colors.background-secondary}` for secondary panels such as filters.
- **One action color.** Vyn green (`{colors.button-primary}`, `{colors.link-primary}`, `{colors.input-primary-active}`) marks primary buttons, links, active inputs and the selected tab. It isn't used as a background for regions.
- **Dense, small type.** Inter at 16px body with a 20px H1. Hierarchy comes from weight (400/500/600), not size jumps. Every style uses a 1.5 line-height.
- **Warm neutrals do the structural work.** Borders, dividers, disabled states and secondary buttons all come from the Grey ramp. There's no pure black in the UI.
- **Status is neutral by default.** "Info" is grey, not blue. Color is saved for success, warning and danger, so it means something when it appears.
- **Bootstrap behaviour, Vyn skin.** When a pattern isn't specified here, fall back to the Bootstrap component and its usage guidance, then apply Vyn tokens.

> **Source of truth:** the Figma file's **live variables**. Where the Foundations Documentation page disagrees with a live variable, the variable wins, and every value in this file is taken from the variables.
>
> Sources: Figma file *Vyn Web App*, covering the Foundations Documentation, Grids, component pages (Button, Input Group, Dropdown, Cards, Alerts, Tabs, Navbar) and the Brand Feel audit. The marketing site (vyntelligence.com) couldn't be reached from the drafting environment, so brand voice comes from the audit frame, which quotes the site directly.

## Colors

### How color tokens work
- **The semantic tokens are the API.** Components, CSS and this file only ever reference the local **Color** collection's semantic tokens. Primitives (`Green/600`, `Grey/300`…) are there to feed those semantic tokens, not to be used directly.
- **One key per Figma variable, no merging.** `text-primary`, `input-text-primary`, `link-secondary` and `button-secondary-text` all resolve to #2C2A29 today, but they're separate so each can change on its own. **The DLS is under construction and these values will move.** Always use the most specific token for the job, even when another token has the same value right now.
- **Naming rule:** key = developer token minus `--color-`. `{colors.alert-success-bg}` ↔ `--color-alert-success-bg` ↔ Figma `Alert/alert-success-bg`. Search any of the three to find the others.
- **To change a value:** change the Figma variable, then update the matching line in the front matter and the table below. No other line in this file should hard-code that hex.
- Only a **Light** mode exists.

### Semantic tokens
Values are the live variable values, which are the source of truth.

**Text**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `text-primary` | `Text/text-primary` | `--color-text-primary` | Grey/800 | `#2c2a29` |
| `text-secondary` | `Text/text-secondary` | `--color-text-secondary` | Grey/600 | `#585450` |
| `text-white` | `Text/text-white` | `--color-text-white` | White/100 | `#ffffff` |
| `text-success` | `Text/text-success` | `--color-text-success` | Functional/Success/800 → Semantic Green/800 | `#166534` |
| `text-warning` | `Text/text-warning` | `--color-text-warning` | Functional/Warning/900 → Orange/900 | `#bf360c` |
| `text-danger` | `Text/text-danger` | `--color-text-danger` | Functional/Danger/800 → Red/800 | `#b71c1c` |

**Background**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `background-primary` | `Background/bg-primary` | `--color-background-primary` | White/100 | `#ffffff` |
| `background-secondary` | `Background/bg-secondary` | `--color-background-secondary` | Grey/100 | `#f5f4f3` |
| `background-dark` | `Background/bg-dark` | `--color-background-dark` | Grey/800 | `#2c2a29` |

**Button**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `button-primary` | `Button/btn-primary` | `--color-button-primary` | Green/600 | `#548118` |
| `button-primary-text` | `Button/btn-primary-text` | `--color-button-primary-text` | White/100 | `#ffffff` |
| `button-secondary` | `Button/btn-secondary` | `--color-button-secondary` | Grey/200 | `#ebeae8` |
| `button-secondary-text` | `Button/btn-secondary-text` | `--color-button-secondary-text` | Grey/800 | `#2c2a29` |
| `button-danger` | `Button/btn-danger` | `--color-button-danger` | Functional/Danger/700 → Red/700 | `#c62828` |
| `button-disabled` | `Button/btn-disabled` | `--color-button-disabled` | Grey/200 | `#ebeae8` |
| `button-disabled-text` | `Button/btn-disabled-text` | `--color-button-disabled-text` | Grey/400 | `#a6a29e` |

**Input**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `input-primary` | `Input/input-primary` | `--color-input-primary` | White/100 | `#ffffff` |
| `input-secondary` | `Input/input-secondary` | `--color-input-secondary` | Grey/100 | `#f5f4f3` |
| `input-primary-active` | `Input/input-primary-active` | `--color-input-primary-active` | Green/600 | `#548118` |
| `input-disabled` | `Input/input-disabled` | `--color-input-disabled` | Grey/100 | `#f5f4f3` |
| `input-text-primary` | `Input/input-text-primary` | `--color-input-text-primary` | Grey/800 | `#2c2a29` |
| `input-text-secondary` | `Input/input-text-secondary` | `--color-input-text-secondary` | Grey/600 | `#585450` |
| `input-text-disabled` | `Input/input-text-disabled` | `--color-input-text-disabled` | Grey/400 | `#a6a29e` |
| `input-text-light` | `Input/input-text-light` | `--color-input-text-light` | White/100 | `#ffffff` |
| `input-border` | `Input/input-border` | `--color-input-border` | Grey/300 | `#d6d4d1` |
| `input-danger` | `Input/input-danger` | `--color-input-danger` | Functional/Danger/800 → Red/800 | `#b71c1c` |

**Link**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `link-primary` | `Link/link-primary` | `--color-link-primary` | Green/600 | `#548118` |
| `link-primary-active` | `Link/link-primary-active` | `--color-link-primary-active` | Green/600 | `#548118` |
| `link-primary-disabled` | `Link/link-primary-disabled` | `--color-link-primary-disabled` | Grey/400 | `#a6a29e` |
| `link-secondary` | `Link/link-secondary` | `--color-link-secondary` | Grey/800 | `#2c2a29` |
| `link-secondary-active` | `Link/link-secondary-active` | `--color-link-secondary-active` | Grey/800 | `#2c2a29` |
| `link-secondary-disabled` | `Link/link-secondary-disabled` | `--color-link-secondary-disabled` | Grey/400 | `#a6a29e` |
| `link-secondary-light` | `Link/link-secondary-light` | `--color-link-secondary-light` | Grey/300 | `#d6d4d1` |
| `link-secondary-light-active` | `Link/link-secondary-light-active` | `--color-link-secondary-light-active` | White/100 | `#ffffff` |
| `link-secondary-light-disabled` | `Link/link-secondary-light-disabled` | `--color-link-secondary-light-disabled` | Grey/500 | `#7c7874` |

**Alert**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `alert-default-bg` | `Alert/alert-default-bg` | `--color-alert-default-bg` | Grey/100 | `#f5f4f3` |
| `alert-default-border` | `Alert/alert-default-border` | `--color-alert-default-border` | Grey/200 | `#ebeae8` |
| `alert-default-text` | `Alert/alert-default-text` | `--color-alert-default-text` | Grey/700 | `#403d3b` |
| `alert-success-bg` | `Alert/alert-success-bg` | `--color-alert-success-bg` | Functional/Success/100 → Semantic Green/100 | `#dcfce7` |
| `alert-success-border` | `Alert/alert-success-border` | `--color-alert-success-border` | Functional/Success/200 → Semantic Green/200 | `#bbf7d0` |
| `alert-success-text` | `Alert/alert-success-text` | `--color-alert-success-text` | Functional/Success/900 → Semantic Green/900 | `#14532d` |
| `alert-warning-bg` | `Alert/alert-warning-bg` | `--color-alert-warning-bg` | Functional/Warning/100 → Orange/100 | `#fff3e0` |
| `alert-warning-border` | `Alert/alert-warning-border` | `--color-alert-warning-border` | Functional/Warning/200 → Orange/200 | `#ffe0b2` |
| `alert-warning-text` | `Alert/alert-warning-text` | `--color-alert-warning-text` | Functional/Warning/900 → Orange/900 | `#bf360c` |
| `alert-danger-bg` | `Alert/alert-danger-bg` | `--color-alert-danger-bg` | Functional/Danger/100 → Red/100 | `#ffebee` |
| `alert-danger-border` | `Alert/alert-danger-border` | `--color-alert-danger-border` | Functional/Danger/200 → Red/200 | `#ffcdd2` |
| `alert-danger-text` | `Alert/alert-danger-text` | `--color-alert-danger-text` | Functional/Danger/900 → Red/900 | `#5f0f0f` |

**Tag**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `tag-default` | `Tag/tag-default` | `--color-tag-default` | Grey/100 | `#f5f4f3` |
| `tag-default-text` | `Tag/tag-default-text` | `--color-tag-default-text` | Grey/800 | `#2c2a29` |
| `tag-default-border` | `Tag/tag-default-border` | `--color-tag-default-border` | Grey/200 | `#ebeae8` |
| `tag-success` | `Tag/tag-success` | `--color-tag-success` | Functional/Success/100 → Semantic Green/100 | `#dcfce7` |
| `tag-success-text` | `Tag/tag-success-text` | `--color-tag-success-text` | Functional/Success/900 → Semantic Green/900 | `#14532d` |
| `tag-chip-success-border` | `Tag/chip-success-border` | `--color-tag-chip-success-border` | Functional/Success/200 → Semantic Green/200 | `#bbf7d0` |
| `tag-warning-bg` | `Tag/tag-warning-bg` | `--color-tag-warning-bg` | Functional/Warning/100 → Orange/100 | `#fff3e0` |
| `tag-warning-text` | `Tag/tag-warning-text` | `--color-tag-warning-text` | Functional/Warning/900 → Orange/900 | `#bf360c` |
| `tag-warning-border` | `Tag/tag-warning-border` | `--color-tag-warning-border` | Functional/Warning/200 → Orange/200 | `#ffe0b2` |
| `tag-danger-bg` | `Tag/tag-danger-bg` | `--color-tag-danger-bg` | Functional/Danger/100 → Red/100 | `#ffebee` |
| `tag-danger-text` | `Tag/tag-danger-text` | `--color-tag-danger-text` | Functional/Danger/800 → Red/800 | `#b71c1c` |
| `tag-danger-border` | `Tag/tag-danger-border` | `--color-tag-danger-border` | Functional/Danger/200 → Red/200 | `#ffcdd2` |

**Chip**

| Key | Figma variable | CSS variable | Aliases | Value |
|---|---|---|---|---|
| `chip-primary` | `Chip/chip-primary` | `--color-chip-primary` | Grey/800 | `#2c2a29` |
| `chip-primary-border` | `Chip/chip-primary-border` | `--color-chip-primary-border` | Grey/300 | `#d6d4d1` |
| `chip-secondary` | `Chip/chip-secondary` | `--color-chip-secondary` | Green/600 | `#548118` |
| `chip-success` | `Chip/chip-success` | `--color-chip-success` | Functional/Success/300 → Semantic Green/300 | `#86efac` |
| `chip-success-text` | `Chip/chip-success-text` | `--color-chip-success-text` | Functional/Success/900 → Semantic Green/900 | `#14532d` |
| `chip-warning` | `Chip/chip-warning` | `--color-chip-warning` | Functional/Warning/400 → Orange/400 | `#ffa726` |
| `chip-danger` | `Chip/chip-danger` | `--color-chip-danger` | Functional/Danger/700 → Red/700 | `#c62828` |
| `chip-danger-text` | `Chip/chip-danger-text` | `--color-chip-danger-text` | Functional/Danger/900 → Red/900 | `#5f0f0f` |
| `chip-text-light` | `Chip/chip-text-light` | `--color-chip-text-light` | White/100 | `#ffffff` |
| `chip-text-dark` | `Chip/chip-text-dark` | `--color-chip-text-dark` | Grey/800 | `#2c2a29` |

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

### Primitives
These are the external primitives library. They're listed for reference only, so don't reference them from components.

| Ramp | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 |
|---|---|---|---|---|---|---|---|---|---|
| Green | #F1F7E9 | #DEECCB | #C3DD9D | #A2CB6B | #7FB23D | **#548118** (brand) | #3F6310 | #2D470A | #1A2B05 |
| Grey | #F5F4F3 | #EBEAE8 | #D6D4D1 | #A6A29E | #7C7874 | #585450 | #403D3B | #2C2A29 | — |
| Red | #FFEBEE | #FFCDD2 | #EF9A9A | #E57373 | #EF5350 | #D32F2F | #C62828 | #B71C1C | #5F0F0F |
| Orange | #FFF3E0 | #FFE0B2 | #FFB74D | #FFA726 | #FF9800 | #EF6C00 | #E65100 | #D84315 | #BF360C |
| Semantic Green | #DCFCE7 | #BBF7D0 | #86EFAC | #4ADE80 | #22C55E | #16A34A | #15803D | #166534 | #14532D |
| Neon Green | — | — | — | — | — | — | — | #98DB40 | #8ECB3D |
| White | #FFFFFF | | | | | | | | |

`Functional/Success`, `Functional/Danger`, `Functional/Warning` and `Functional/Info` are alias layers over Semantic Green, Red, Orange and Grey respectively.

**Primitives used directly today:** four places in Figma bind a primitive because no semantic token exists yet. These are `grey-500` (navbar workflow-switcher border), `grey-600` (navbar icon-button fill), `grey-700` (sidebar footer divider) and `neon-green-800` (logo mark). They're in the front matter under their primitive names so they're easy to find and replace once semantic tokens exist.

### Usage guidance
- **Brand green is for action.** `button-primary`, `link-primary`, `input-primary-active` and the selected tab's `link-primary` underline. Don't use it as a background for regions.
- **Hover and pressed are overlays, not new colors.** Layer `state-hover-shade` (black 15%) or `state-pressed-shade` (black 20%) over the base fill. On dark surfaces, use `state-hover-tint` / `state-pressed-tint` (white 15% / 20%).
- **Success isn't brand.** Success tokens alias the cooler Semantic Green ramp, so a success state never reads as a primary action.
- **Info and default are neutral grey** (`alert-default-*`, `tag-default*`), not blue. Color is kept for success, warning and danger.
- **On dark chrome** (`background-dark`), use the `link-secondary-light*` family for text. Brand green drops to 3.1:1 there, so the logo uses Neon Green instead.
- **Non-token values from Bootstrap:** the modal and offcanvas backdrop (black 50%) and the card border (`$border-color-translucent`, black 17.5%) are Bootstrap 5 defaults, not Vyn tokens.

## Typography

### Font Family
- **Inter** (`--font-family-sans-serif`). Fallback: Bootstrap 5's native stack, `system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", "Liberation Sans", Arial, sans-serif`. In code, set `$font-family-sans-serif: Inter, <native stack>`.
- One family carries everything. Hierarchy comes from **weight** (Regular 400, Medium 500, Semi-Bold 600; Bold 700 appears only in eyebrow labels and badges) far more than from size.

### Hierarchy
Keys match the Figma text styles and `--font-*` developer tokens exactly (`body-p2-medium` ↔ `--font-body-p2-medium` ↔ Figma "P2 - Medium"). All are Inter, 1.5 line-height and 0 letter spacing.

| Style | Size | Weights available | Use |
|---|---|---|---|
| `header-h1-semi-bold` | 20px | 600 | Page title, one per view |
| `header-h2-semi-bold` | 18px | 600 | Section title, drawer title |
| `header-h3-{regular,medium,semi-bold}` | 16px | 400 / 500 / 600 | Card title, panel heading |
| `header-h4-{regular,medium,semi-bold}` | 14px | 400 / 500 / 600 | Sub-group heading, table group |
| `body-p1-{regular,medium,semi-bold}` | 16px | 400 / 500 / 600 | Default body and input values (regular), button L and sidebar links (medium), form labels (semi-bold) |
| `body-p2-{regular,medium,semi-bold}` | 14px | 400 / 500 / 600 | Dense body, helper and error text (regular), button M and workflow switcher (medium) |
| `body-p3-{regular,medium,semi-bold}` | 12px | 400 / 500 / 600 | Captions, timestamps (regular), button S (medium) |
| `body-p4-{regular,medium,semi-bold}` | 10px | 400 / 500 / 600 | Rare. Micro-labels only |
| `eyebrow` *(not a Figma style)* | 10px | 700, +2px tracking, UPPERCASE | Sidebar section labels ("WORKFLOW", "SETTINGS") |

Button labels match the Medium body style at each button size. Size primitives: `--font-xxs` 10 · `--font-xs` 12 · `--font-s` 14 · `--font-m` 16 · `--font-l` 18 · `--font-xl` 20.

### Principles
- **The scale is intentionally small.** The largest type is 20px, which suits a data-dense application where content (video, maps, case lists) is the hero and headings are signposts. Don't import Bootstrap's 2.5rem `h1` into app views.
- **Use weight before size.** To make one thing stand out from its neighbours, go Regular → Medium → Semi-Bold at the same size before stepping up a size.
- **Keep line-height at 1.5 everywhere.** This matches Bootstrap's `$line-height-base` and keeps an 8px-friendly rhythm (16 × 1.5 = 24).
- **Letter spacing stays at 0**, except the uppercase eyebrow at +2px.
- **Sentence case** for headings, buttons, tabs and menu items. Uppercase is reserved for eyebrow labels.

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

**Navbar:** the Vyn logo, then the **Workflow switcher**. This is a standard **Medium Button** (39px tall, 8px 16px padding, 14px / `--font-s` Medium label) in an outline style for chrome: transparent fill, `Grey/500` border, white label and a trailing dropdown caret. It should match the Button component exactly, not a one-off navbar size. The right side holds the utility links: a notification icon button (40px, `Grey/600` fill, with a danger badge) and the avatar menu.

**Sidebar:** grouped links under eyebrow labels (WORKFLOW, then SETTINGS), with a collapse chevron in the footer. Expanded and collapsed variants exist.

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
- **The XXL drop is tinted warm** (`#57534F`, not black) to stay in the stone palette. Keep new shadows warm too.
- **Scrims are black 50%**, matching Bootstrap's `$modal-backdrop-opacity`.

## Shapes

### Border Radius Scale

| Token | Value | Use |
|---|---|---|
| `--radius-s` | 4px | **Default.** Buttons, inputs, dropdowns, menus, alerts, tooltips |
| *(card)* | 6px | Cards. This value isn't tokenized yet (see Known Gaps) |
| `--radius-l` | 8px | Larger containers, modals |
| `--radius-xl` | 16px | Feature panels, media frames |
| `--radius-xxl` | 24px | Hero or marketing surfaces only |
| `--radius-pill` | 1000px | Icon buttons, avatars, badges, status pills |

**Rule of thumb:** rectangles with text labels get 4px, and anything circular or icon-only gets the pill radius. Buttons with text labels never use the pill radius.

### Borders
`--border-1` (1px) for every control, card and divider, `--border-2` (2px) for the selected-tab underline, and `--border-8` (8px) for heavy accents such as left-edge status bars.

### Iconography
- **Material Design icons** (MUI set) are the default icon library and are already in the Vyn codebase. Use the outlined style for utilities (bell, chevrons) and filled glyphs in the sidebar.
- The **"Vynnie"** is a custom camera/box glyph taken from the logo mark. It represents Vyns and Cases in the sidebar. It's a brand asset, so keep it for Vyn-specific objects.
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
- **Primary Outline:** the secondary action beside a primary one, for example "Save draft" next to "Submit". It fills solid green on hover.
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
- **Sidebar** (250px, chrome): eyebrow-labelled groups with 20px icon + 16px Medium label links. Default links use `Grey/300`, and the active link is white. There are Expanded and Collapsed variants with a collapse chevron in the footer.
- The **BETA pill** next to the WORKFLOW label is a **temporary placeholder**. Its purple colors aren't part of the Vyn system, so don't reuse them or build on them. If a pre-release marker is needed before one is designed, use a neutral Tag (`Tag/tag-default`).

### TBD components
Breadcrumb, Chip and Tag (on hold, though tokens exist), Filters, Modal, Pagination, Progress, Table and Video Player are **TBD**. They have placeholder pages in Figma but no design yet. Until they're designed, **use the stock Bootstrap 5 component with Vyn tokens**: 4px radius, `input-border` borders, Inter type and the semantic color tokens. Don't invent a bespoke version.

### Bootstrap theming map
Set these Bootstrap 5 Sass variables (or their `--bs-*` CSS variables) from Vyn tokens so that stock components pick up the brand:

Point each variable at the Vyn CSS variable rather than pasting a hex, so that a token change flows through automatically. Values live only in *Colors → Semantic tokens*.

| Bootstrap variable | Vyn token |
|---|---|
| `$primary` / `--bs-primary` | `var(--color-button-primary)` |
| `$secondary` | `var(--color-button-secondary)` |
| `$danger` | `var(--color-button-danger)` |
| `$success` | `Functional/Success/500` primitive (no semantic token yet, see Known Gaps) |
| `$warning` | `Functional/Warning/400` primitive (no semantic token yet, see Known Gaps) |
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
| `$gray-100`…`$gray-800` | `--color-grey-100`…`--color-grey-800` primitives |

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

### Brand vocabulary
- **Names:** *Vyntelligence* (the company), *Vyn* (the product, and also one captured video/job, as in "every Vyn"), *Vyn AI®* (the analysis layer), *CX* and *FX* (the product lines).
- **Coined words:** *Vynners* (users and staff) and *Vynified*. Use them sparingly, in welcome, onboarding and celebration moments only.
- **Recurring phrases:** "Seeing is believing" (the recommended brand promise), "right first time" and "digital eyes and ears".

## Do's and Don'ts

### Do
- Keep brand green (`button-primary`, `link-primary`, `input-primary-active`) for actions: primary buttons, links, the active input and the selected tab.
- Use the most specific semantic token for every property, even when a different token has the same value today. Tokens will diverge as the DLS evolves.
- Build every screen from one of the four shell templates, and keep the 24px content padding.
- Use weight (400 → 500 → 600) to create hierarchy before reaching for a bigger size.
- Use the hover and pressed **overlays** (black 15% / 20%, white on dark) instead of inventing new hex values.
- Use 4px radius for anything with a text label and the pill radius for icon-only controls, avatars and badges.
- Separate regions with surface change (`background-primary` / `background-secondary` / `background-dark`) and 1px hairlines.
- Reference semantic tokens (`--color-button-primary`) in code, never primitives (`--color-green-600`) or raw hex.
- Fall back to the Bootstrap component and its usage guidance whenever a pattern isn't specified, then apply Vyn tokens.
- Show the evidence (video, time, person) next to any AI-generated status.

### Don't
- Don't put `Green/600` text on dark chrome, where it's 3.1:1. Use white, `Grey/300` or Neon Green there.
- Don't use Neon Green on white backgrounds. It's a dark-surface accent only.
- Don't use the success green (`Semantic Green`) for primary actions, or the brand green for success states.
- Don't use more than one Primary Filled button in a view region.
- Don't use pill-shaped text buttons, or round inputs and cards beyond the documented radii.
- Don't import Bootstrap's large display headings (2.5rem h1) into app views. 20px is the top of the scale.
- Don't use pure black (#000) or raw hex for text or surfaces. Use the semantic text and background tokens.
- Don't use cool Bootstrap greys (`$gray-*`). Every neutral comes from the warm Grey ramp.
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
  - `button-primary` / `link-primary` on `background-primary`: 4.64:1. That passes AA for text but only just.
  - `text-secondary` on `background-primary`: 7.5:1.
  - `button-primary-text` on `button-danger`: 5.6:1.
  - `link-secondary-light` on `background-dark`: 9.7:1.
  - `link-secondary-light-disabled` on `background-dark`: 3.3:1, which is acceptable only because it's disabled.
  - `button-disabled-text` on `button-disabled`: 2.1:1, also acceptable only because it's disabled.
- **Focus:** every interactive element shows the 4px focus ring (`focus-shadow-focus`, plus `focus-border-focus` on inputs) and must never have `outline: none` without it.
- **Color is never the only signal.** Pair status color with text or an icon, which applies to alerts, badges, tags and validation.
- **Keyboard:** drawers and modals trap focus and close on Esc. Dropdowns and tabs follow the WAI-ARIA patterns that Bootstrap implements.
- **Motion:** keep Bootstrap's `$enable-reduced-motion` on so drawers, modals and accordions don't animate under `prefers-reduced-motion`.

## Iteration Guide

1. Work on **one component at a time** and refer to it by its `components:` token name, for example `button-primary-outline` or `text-input-error`. Colors, type and radii are referenced by their token keys.
2. Start from the matching **Bootstrap 5 component**, themed with the variables in *Bootstrap theming map*. Don't restyle it with bespoke CSS.
3. Pick the **shell template** first (Desktop, + Filter panel, + Drawer, Full Page), then lay out content on the 12-column / 24px-gutter grid.
4. Default body text to `body-p1-regular` (16/24) and dense views to `body-p2-regular` (14/21).
5. Add new variants as separate component entries (`-hover`, `-selected`, `-error`) that reference existing tokens.
6. Before shipping, check new copy against the four voice principles, especially near safety or compliance content.
7. When a token value changes, update its front-matter line and its row in *Semantic tokens*, re-check the contrast pairs under *Accessibility*, then run `npx @google/design.md lint DESIGN.md`.

## Decisions Log

- **Focus ring stays classic Bootstrap blue for now** (#007BFF border, #80BDFF ring at 40%, 0.25rem). It's intentionally the only blue in the system, as a high-visibility accessibility affordance. Don't swap it for a green ring.
- **The BETA pill is a temporary placeholder.** Its purples (#7C3AED, #352D40, #4B3175) aren't system colors.
- **Sidebar width is 250px** (expanded). The Vyn Viewer drawer's left inset follows at 290px.
- **The Workflow switcher is a Medium Button** with a 14px (`--font-s`) label, and matches the Button component as a whole.

## Deferred

These will be resolved at a later date. Until then, keep things as they are:

- **Secondary Outline button border:** it uses `button-secondary` (currently Grey/200), which is only about 1.2:1 against white. Don't change it ad hoc.
- **Dark mode:** only a Light mode exists. Don't build dark themes for the work area.

## Known Gaps

Still open, to resolve in Figma or code:

- **Foundations documentation page is out of date.** Its Alert table (for example, success bg #E8F5E9) and several Tag and Chip rows (which render #000000) don't match the live variables. This file follows the variables, so the page should be regenerated from them.
- **Card radius and border** come from Bootstrap defaults (0.375rem, `$border-color-translucent`) rather than Vyn tokens. That's fine, but consider adding `--radius-m: 6px` and a `Border/border-translucent` token so Figma and code share names.
- **Primitives bound directly in Figma:** the navbar workflow-switcher border (`grey-500`), the navbar icon-button fill (`grey-600`), the sidebar footer divider (`grey-700`) and the logo (`neon-green-800`) use primitives. Semantic tokens such as `Background/bg-dark-control` and `Border/border-dark` would let these swap like everything else.
- **No semantic token for success and warning fills** used by Bootstrap's `$success` and `$warning`. They're mapped to primitives for now.
- **Token naming inconsistencies in Figma:** `Tag/chip-success-border` sits in the Tag group but is named `chip-`. Background suffixes also vary (`tag-default` and `tag-success` vs. `tag-warning-bg` and `tag-danger-bg`). Keys here mirror the Figma names exactly, so renaming in Figma means renaming here too.
- **Eyebrow label** (10px Bold, +2px, uppercase) has no Figma text style. It's composed from primitives. Consider adding a style.
- **Undocumented components:** the header counts 33 component sets and 9 standalone components, and 15 are documented here. The TBD components are listed under *Components → TBD components*.
- **Marketing site:** vyntelligence.com couldn't be fetched while drafting. Voice guidance relies on the Brand Feel audit, which quotes the site directly.
