---
version: alpha
name: Vyn-Web-App-design
description: "A calm, desk-side operations console for utilities and infrastructure teams: white work surfaces framed by warm charcoal chrome (#2c2a29), one confident brand green (#548118) for action, and warm stone greys for everything structural. Type is Inter throughout, set small and dense (16px body, 20px H1) with a 150% line-height, because the product is read all day by people triaging video evidence, not skimmed once. Components are Bootstrap-shaped (4px radius, 1px borders, 48px form controls) with Material icons. The personality is practical and proven first, lightly playful second: the product earns trust by showing the evidence, not by decorating it."

colors:
  # Brand
  primary: "#548118"            # Green/600 — "Branding main green"
  primary-hover: "#548118"      # + State/hover-shade overlay (black 15%)
  primary-pressed: "#548118"    # + State/pressed-shade overlay (black 20%)
  on-primary: "#ffffff"
  brand-neon: "#98db40"         # Neon Green/800 — logo mark / accents on dark chrome only
  brand-neon-strong: "#8ecb3d"  # Neon Green/900
  # Surfaces
  canvas: "#ffffff"             # Background/bg-primary
  surface-1: "#f5f4f3"          # Background/bg-secondary (Grey/100)
  surface-2: "#ebeae8"          # Grey/200 — secondary button, disabled fill
  chrome: "#2c2a29"             # Background/bg-dark (Grey/800) — navbar + sidebar
  chrome-divider: "#403d3b"     # Grey/700
  chrome-control: "#585450"     # Grey/600 — icon-button fill on chrome
  hairline: "#d6d4d1"           # Input/input-border (Grey/300)
  hairline-subtle: "#ebeae8"    # Grey/200 — alert/tag default borders
  scrim: "rgba(0,0,0,0.5)"
  # Text
  ink: "#2c2a29"                # Text/text-primary (Grey/800)
  ink-muted: "#585450"          # Text/text-secondary (Grey/600)
  ink-disabled: "#a6a29e"       # Grey/400
  inverse-ink: "#ffffff"        # Text/text-white
  inverse-ink-muted: "#d6d4d1"  # Link/link-secondary-light (Grey/300)
  inverse-ink-subtle: "#a6a29e" # sidebar section labels
  # Semantic
  success: "#22c55e"            # Semantic Green/500 — fills for success chips
  success-text: "#166534"       # Text/text-success
  warning: "#ffa726"            # Orange/400 — warning chip fill
  warning-text: "#bf360c"       # Text/text-warning
  danger: "#c62828"             # Button/btn-danger (Red/700)
  danger-text: "#b71c1c"        # Text/text-danger, Input/input-danger (Red/800)
  success-bg: "#dcfce7"
  success-strong: "#14532d"
  warning-bg: "#fff3e0"
  danger-bg: "#ffebee"
  danger-strong: "#5f0f0f"
  info: "#f5f4f3"               # Info is neutral grey in this system, not blue
  info-text: "#403d3b"
  # Focus (Bootstrap defaults — see Known Gaps)
  focus-border: "#007bff"
  focus-ring: "rgba(128,189,255,0.4)"
  focus-border-error: "#dc3545"
  focus-ring-error: "rgba(220,53,69,0.4)"

typography:
  header-h1:
    fontFamily: Inter
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  header-h2:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  header-h3:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600          # also 400 / 500 variants
    lineHeight: 1.5
    letterSpacing: 0
  header-h4:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 600          # also 400 / 500 variants
    lineHeight: 1.5
    letterSpacing: 0
  body-p1:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400          # also 500 / 600 variants
    lineHeight: 1.5
    letterSpacing: 0
  body-p2:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-p3:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  body-p4:
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  label:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: 0
  button-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  button-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  button-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  nav-link:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0
  eyebrow:
    fontFamily: Inter
    fontSize: 10px
    fontWeight: 700
    lineHeight: 1
    letterSpacing: 2px       # set UPPERCASE in CSS

rounded:
  none: 0px
  sm: 4px        # --radius-s — default for buttons, inputs, alerts, menus
  md: 6px        # cards (not yet a token — see Known Gaps)
  lg: 8px        # --radius-l
  xl: 16px       # --radius-xl
  xxl: 24px      # --radius-xxl
  pill: 1000px   # --radius-pill — icon buttons, avatars, badges, status pills

spacing:
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
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
    height: 50px
    padding: 12px 24px
  button-primary-md:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button-md}"
    rounded: "{rounded.sm}"
    height: 39px
    padding: 8px 16px
  button-primary-sm:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button-sm}"
    rounded: "{rounded.sm}"
    height: 28px
    padding: 4px 12px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
  button-primary-pressed:
    backgroundColor: "{colors.primary-pressed}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
  button-primary-outline:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.primary}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
    padding: 12px 24px
  button-primary-text:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.primary}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
    padding: 12px 24px
  button-secondary:
    backgroundColor: "{colors.surface-2}"
    textColor: "{colors.ink}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
    padding: 12px 24px
  button-danger:
    backgroundColor: "{colors.danger}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
    padding: 12px 24px
  button-disabled:
    backgroundColor: "{colors.surface-2}"
    textColor: "{colors.ink-disabled}"
    typography: "{typography.button-lg}"
    rounded: "{rounded.sm}"
  icon-button:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.pill}"
    size: 32px
    padding: 6px
  icon-button-chrome:
    backgroundColor: "{colors.chrome-control}"
    textColor: "{colors.inverse-ink}"
    rounded: "{rounded.pill}"
    size: 40px
  text-input:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    height: 48px
    padding: 0 12px
  text-input-error:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    height: 48px
  text-input-disabled:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink-disabled}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    height: 48px
  text-input-addon:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
    size: 48px
    padding: 12px
  input-label:
    textColor: "{colors.ink}"
    typography: "{typography.label}"
  input-error-text:
    textColor: "{colors.danger-text}"
    typography: "{typography.body-p2}"
  dropdown-trigger:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    height: 48px
    padding: 12px
  dropdown-menu:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    rounded: "{rounded.sm}"
  dropdown-item:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-p1}"
    height: 48px
    padding: 12px
  card:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.md}"
    padding: 16px
  alert-success:
    backgroundColor: "{colors.success-bg}"
    textColor: "{colors.success-strong}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    padding: 12px 16px
  alert-warning:
    backgroundColor: "{colors.warning-bg}"
    textColor: "{colors.warning-text}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    padding: 12px 16px
  alert-danger:
    backgroundColor: "{colors.danger-bg}"
    textColor: "{colors.danger-strong}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    padding: 12px 16px
  alert-info:
    backgroundColor: "{colors.info}"
    textColor: "{colors.info-text}"
    typography: "{typography.body-p1}"
    rounded: "{rounded.sm}"
    padding: 12px 16px
  tab:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-p2}"
    padding: 12px 16px
  tab-selected:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-p2}"
    padding: 12px 16px
  badge:
    backgroundColor: "{colors.danger}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-p3}"
    rounded: "{rounded.pill}"
    height: 18px
    padding: 2px 4px
  avatar:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    size: 40px
  navbar:
    backgroundColor: "{colors.chrome}"
    textColor: "{colors.inverse-ink}"
    height: 64px
    padding: 12px 16px
  sidebar:
    backgroundColor: "{colors.chrome}"
    textColor: "{colors.inverse-ink-muted}"
    typography: "{typography.nav-link}"
    width: 249px
  sidebar-link:
    backgroundColor: "{colors.chrome}"
    textColor: "{colors.inverse-ink-muted}"
    typography: "{typography.nav-link}"
    padding: 12px 18px
  sidebar-link-active:
    backgroundColor: "{colors.chrome}"
    textColor: "{colors.inverse-ink}"
    typography: "{typography.nav-link}"
    padding: 12px 18px
  sidebar-section-label:
    backgroundColor: "{colors.chrome}"
    textColor: "{colors.inverse-ink-subtle}"
    typography: "{typography.eyebrow}"
    padding: 8px 12px
  filter-panel:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
    width: 300px
    padding: 16px
  drawer:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    padding: 24px
---

## Overview

Vyn is the web console for **Vyntelligence**. Customers and field crews record short guided videos, Vyn AI® analyses them, and desk teams use this app to review what came back, triage it and act on it. The two product lines are **CX** (Customer Experience) and **FX** (Field Experience). The core users are operations managers, back-office teams and supervisors at UK utilities (water, gas, energy, telecoms), and the US infrastructure market is next.

The brand audit sums up the feel in one line: *"a practical, proven, slightly playful engineering partner."* The UI should read the same way. It's a tool people trust with safety and compliance evidence, so it stays calm and legible, and the personality shows up in small places (the Vynnie icon, the brand words, the neon green mark on dark chrome) rather than in decoration.

The system is built on **Bootstrap-style primitives**: 4px corners, 1px borders, 48px form controls and Bootstrap's blue focus ring. It uses **Material icons** throughout and Material elevation values for shadows. On top of that sits a warm, Vyn-specific palette: stone greys with a brown undertone (`#2c2a29` → `#f5f4f3`) instead of Bootstrap's cool greys, and one brand green.

**Key characteristics:**
- **Dark chrome, light work area.** The navbar and sidebar are warm charcoal `{colors.chrome}`. Everything the user works on sits on white `{colors.canvas}`, with `{colors.surface-1}` for secondary panels such as filters.
- **One action color.** `{colors.primary}` Vyn green marks primary buttons, links, active inputs and the selected tab. It isn't used as a background for regions.
- **Dense, small type.** Inter at 16px body with a 20px H1. Hierarchy comes from weight (400/500/600), not size jumps. Every style uses a 1.5 line-height.
- **Warm neutrals do the structural work.** Borders, dividers, disabled states and secondary buttons all come from the Grey ramp. There's no pure black in the UI.
- **Status is neutral by default.** "Info" is grey, not blue. Color is saved for success, warning and danger, so it means something when it appears.
- **Bootstrap behaviour, Vyn skin.** When a pattern isn't specified here, fall back to the Bootstrap component and its usage guidance, then apply Vyn tokens.

> Sources: Figma file *Vyn Web App*, covering the Foundations Documentation, Grids, component pages (Button, Input Group, Dropdown, Cards, Alerts, Tabs, Navbar) and the Brand Feel audit. The marketing site (vyntelligence.com) couldn't be reached from the drafting environment, so brand voice comes from the audit frame, which quotes the site directly.

## Colors

### Brand & Accent
- **Vyn Green** (`{colors.primary}` #548118, `Green/600`): the single action color. Used for primary buttons, primary links, the active input border and the selected-tab underline. The Figma variable is described as *"Branding main green."*
- **Hover / Pressed:** don't pick new hex values. Overlay `State/hover-shade` (black 15%) or `State/pressed-shade` (black 20%) on the base fill. Use the `-tint` versions (white 15% / 20%) on dark surfaces.
- **Neon Green** (`{colors.brand-neon}` #98DB40): the logo-mark green. Use it only on dark chrome, where `Green/600` falls to 3.1:1 contrast. Never use it on white.
- **Green ramp** (100–900, #F1F7E9 → #1A2B05): tints for selected rows, highlight backgrounds and data visualisation. `Green/900` is also the documentation-header background.

### Surface
- **Canvas** (`{colors.canvas}` #FFFFFF): the main work area, cards, inputs, menus and drawers.
- **Surface 1** (`{colors.surface-1}` #F5F4F3): filter panels, input add-ons, disabled inputs and neutral alerts.
- **Surface 2** (`{colors.surface-2}` #EBEAE8): secondary-button fill and disabled-button fill.
- **Chrome** (`{colors.chrome}` #2C2A29): the navbar and sidebar. Its dividers use `{colors.chrome-divider}` #403D3B.
- **Hairline** (`{colors.hairline}` #D6D4D1): all 1px control and menu borders.
- **Scrim** (black 50%): behind drawers and modals.

### Text
- **Ink** (`{colors.ink}` #2C2A29): body, headings and input values. The same value as chrome, so the page reads as one material.
- **Ink Muted** (`{colors.ink-muted}` #585450): secondary text, metadata and helper text. It's the documented *"new secondary text color"* at 7.5:1 on white.
- **Ink Disabled** (#A6A29E): disabled labels and placeholders in disabled fields only. It sits at 2.1:1 on `surface-2`, which is acceptable only because disabled content is exempt from contrast rules.
- **On chrome:** default links use `Grey/300` #D6D4D1, the active link is white, section labels use `Grey/400` #A6A29E and disabled links use `Grey/500`.

### Semantic

| Role | Fill / Chip | Text | Alert bg | Alert border | Alert text |
|---|---|---|---|---|---|
| Success | `Semantic Green/500` #22C55E (chip: /300 #86EFAC) | #166534 | #DCFCE7 | #BBF7D0 | #14532D |
| Warning | `Orange/400` #FFA726 | #BF360C | #FFF3E0 | #FFE0B2 | #BF360C |
| Danger | `Red/700` #C62828 | #B71C1C | #FFEBEE | #FFCDD2 | #5F0F0F |
| Info / default | `Grey/100` #F5F4F3 | #403D3B | #F5F4F3 | #EBEAE8 | #403D3B |

Success uses its own **Semantic Green** ramp, a cooler Tailwind-style green, so that a "success" state is never confused with the brand-green primary action.

### Token architecture
Tokens come in two tiers, and components should only reference the semantic tier:
1. **Primitives** (external library): `Green`, `Grey`, `White`, `Red`, `Orange`, `Neon Green`, `Semantic Green`, plus `Functional/{Success|Danger|Warning|Info}` aliases.
2. **Semantic** (local "Color" collection): `Text/*`, `Background/*`, `Button/*`, `Input/*`, `Link/*`, `Alert/*`, `Tag/*`, `Chip/*`, `Focus/*`, `State/*`.

CSS variables follow the pattern `--color-{group}-{name}`, for example `--color-button-primary` and `--color-text-secondary`. Only a **Light** mode exists.

## Typography

### Font Family
- **Inter** (`--font-family-sans-serif`). Fallback: `system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`, which is Bootstrap's native stack.
- One family carries everything. Hierarchy comes from **weight** (Regular 400, Medium 500, Semi-Bold 600; Bold 700 appears only in eyebrow labels and badges) far more than from size.

### Hierarchy

| Token | Size | Weights | Line height | Use |
|---|---|---|---|---|
| `header-h1` | 20px | 600 | 1.5 | Page title, one per view |
| `header-h2` | 18px | 600 | 1.5 | Section title, drawer title |
| `header-h3` | 16px | 400 / 500 / 600 | 1.5 | Card title, panel heading |
| `header-h4` | 14px | 400 / 500 / 600 | 1.5 | Sub-group heading, table group |
| `body-p1` | 16px | 400 / 500 / 600 | 1.5 | Default body, input values, menu items, alerts (500) |
| `body-p2` | 14px | 400 / 500 / 600 | 1.5 | Dense body, table cells, helper and error text |
| `body-p3` | 12px | 400 / 500 / 600 | 1.5 | Captions, timestamps, badge counts |
| `body-p4` | 10px | 400 / 500 / 600 | 1.5 | Rare. Micro-labels only |
| `label` | 16px | 600 | 1.5 | Form field labels |
| `button-lg/md/sm` | 16 / 14 / 12px | 500 | 1.5 | Button labels by button size |
| `nav-link` | 16px | 500 | 1.5 | Sidebar links |
| `eyebrow` | 10px | 700, +2px tracking, UPPERCASE | 1 | Sidebar section labels ("WORKFLOW", "SETTINGS") |

Size primitives: `--font-xxs` 10 · `--font-xs` 12 · `--font-s` 14 · `--font-m` 16 · `--font-l` 18 · `--font-xl` 20.

### Principles
- **The scale is intentionally small.** The largest type is 20px, which suits a data-dense application where content (video, maps, case lists) is the hero and headings are signposts. Don't import Bootstrap's 2.5rem `h1` into app views.
- **Use weight before size.** To make one thing stand out from its neighbours, go Regular → Medium → Semi-Bold at the same size before stepping up a size.
- **Keep line-height at 1.5 everywhere.** This matches Bootstrap's `$line-height-base` and keeps an 8px-friendly rhythm (16 × 1.5 = 24).
- **Letter spacing stays at 0**, except the uppercase eyebrow at +2px.
- **Sentence case** for headings, buttons, tabs and menu items. Uppercase is reserved for eyebrow labels and the "BETA" pill.

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
| **Desktop** | Navbar (64px) + Sidebar (249px) + Content (fluid, 24px padding) | Default for list and detail pages: Cases, Analytics, Vyns |
| **Desktop + Filter panel** | Navbar + Sidebar + Filter panel (300px, `surface-1`, 16px padding) + Content | List views with persistent filtering. The content panel gets a 1px left border (black 12%) and a soft shadow so it sits above the filter rail |
| **Desktop + Vyn Viewer Drawer** | Desktop shell + 50% scrim + right-hand drawer | Opening a single Vyn (video + insights) without leaving the list. The drawer starts 289px from the left edge (sidebar + 40px), leaving the list visible behind the scrim for orientation |
| **Desktop + Full Page** | Navbar + Content (no sidebar) | Focused, single-task flows: settings wizards, storyboard editing, anything that needs full width |

**Navbar:** the Vyn logo, then the **Workflow switcher**, an outline button on chrome with a `Grey/500` border and 32px height. The right side holds the utility links: a notification icon button (40px, `Grey/600` fill, with a danger badge) and the avatar menu.

**Sidebar:** grouped links under eyebrow labels (WORKFLOW with a BETA pill, then SETTINGS), with a collapse chevron in the footer. Expanded and collapsed variants exist.

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
| 1 (hairline) | 1px `{colors.hairline}` or black 18% border | Inputs, cards, menus, alerts, accordion |
| 2 (raised) | `--effect-elevation-2-mui` | Card "Drop Shadow" variant, raised content panel beside filters |
| 8 (overlay) | `--effect-elevation-8-mui` | Dropdown menus, popovers, tooltips |
| XL / XXL drop | `--effect-elevation-xl-drop` / `-xxl-drop` | Drawers and modals over a scrim |
| Focus | 4px ring, `{colors.focus-ring}` (#80BDFF at 40%) | Every focusable control. Error fields use the red ring |

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
Video stills are the product's real imagery. Show them at their native aspect ratio, never crop evidence, frame them in 4px or 8px radius containers, and keep overlays such as timestamps and AI tags legible with a dark scrim. *(Detailed media and video-player specs are TBD in Figma.)*

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
- **Secondary** (grey `surface-2` fill): neutral actions like Cancel, Close or Back.
- **Danger:** destructive actions only (delete, revoke, reject). Pair each one with a confirmation step.
- **Disabled:** `surface-2` fill and `ink-disabled` text. Where possible, explain why in a tooltip or helper text, and prefer hiding an action to disabling it when the user can't do anything about the reason.
- **Order:** the primary button goes on the right in dialogs and forms, following Bootstrap's modal-footer convention.
- **Semantics:** use `<button>` for actions and `<a>` for navigation, even when they look the same.

### Inputs & Forms (Input Group, Textarea)
- **Anatomy:** label (16px Semi-Bold, 8px below it) → 48px field (1px `hairline`, 4px radius, 12px text padding) → optional helper, error text or character count (14px, 4px above).
- **Add-ons:** a 48 × 48 `surface-1` cap with a Material icon (for example `person-fill`) on the leading edge. This is Bootstrap's `.input-group-prepend` pattern.
- **States:**
  - Enabled.
  - Error: the border and message both switch to `Input/input-danger` #B71C1C.
  - Disabled: `surface-1` fill with `ink-disabled` text.
  - Active: `Input/input-primary-active` green border.
  - Focus: the blue focus ring.
- **Values:** Empty, Placeholder or Populated. Placeholder text is never a substitute for a label.
- **Required fields:** mark them with `*` after the label. When most fields are required, mark the optional ones instead.
- **Validation (Bootstrap):** validate on blur or submit, not on every keystroke. Show one specific message under the field, such as "Enter a postcode like SW1A 1AA" rather than "Invalid input".
- **Textarea:** same chrome as the text input. Show the character count by default ("0/100 characters") and use a scrollbar variant for long content.

### Dropdown
- **Trigger:** 48px tall, styled like an input, with optional label and icon. It has Collapsed, Expanded and Selected states.
- **Menu:** opens 8px below the trigger, with a 1px `hairline` border, 4px radius and elevation 8. Items are 48px tall with 12px padding in 16px Regular text, and have Enabled, Hover (black 15% overlay), Pressed (black 20%) and Selected states.
- **Menu headers** group items. They get extra top padding (16px) and a divider.
- Use a dropdown for **5 or more** mutually exclusive options. For 2–4 options, use radio buttons so all choices are visible, following Bootstrap's form guidance.

### Checkbox, Radio & Switch
- **Checkbox:** for multiple independent choices. The Vyn-specific **Excluded** state (from `.Checkbox-exclude`) lets filters express "everything except…". Groups can be vertical (default) or horizontal.
- **Radio Button:** a single choice among 2–5 visible options. Groups come preconfigured with 5 slots, and items should be set to fill in vertical groups.
- **Switch (Toggle):** an instant on/off setting that applies without a Save button. When the change only applies on submit, use a checkbox instead.
- All three support Required and Focus states.

### Cards & Containers
- **Card:** white, 1px black-18% border, 6px radius, 16px padding and 12px internal gap. It has a free-form **Content** slot. The **Drop Shadow** variant adds elevation 2 for cards that are clickable or draggable.
- **Accordion:** a stacked, expandable list for FAQs and progressive disclosure, with Expanded True/False and slot-based rows. *Per the Figma note, the Accordion isn't currently used in the Web App. Vyn Viewer AI insights use a modified card instead.*
- **Filter panel:** a 300px `surface-1` rail on the left of list views.
- **Drawer:** a right-hand panel over a 50% scrim, used to open a Vyn without losing list context. Close it with an explicit close button, Esc and a scrim click.

### Alerts
- Four types: **Success, Warning, Danger, Info** (Info is neutral grey). Each has a 1px tinted border, 4px radius, 12px 16px padding and 16px Medium text. There's an optional close button and a content slot for links or actions.
- Following Bootstrap: use alerts for **page- or section-level** feedback about the user's last action or the system state. Put field-level problems on the field itself.
- Don't rely on color alone. Start the message with the outcome ("Saved.", "Couldn't upload video.") or add an icon.
- Only make alerts dismissible when the message is no longer needed after it has been read.

### Tabs
- Each tab has 12px 16px padding, an optional icon and a count badge. States are Default, Hover (15% shade), Pressed (20% shade) and **Selected**, which gets a 2px `Link/link-primary` green bottom border.
- Use tabs to switch between **sibling views of the same object**, such as Details, Media and History on a Vyn. Don't use tabs for sequential steps; use a stepper or wizard for those.

### Badge, Avatar & Tooltip
- **Badge:** an 18px pill counter, positioned inline or top-right (absolute). Types are Primary, Secondary and Danger, and the navbar notification badge uses Danger. **Cap at "99+".**
- **Avatar:** 40px circle in three types. Text shows two initials from the user's first name, Image uses a photo fill, and Icon shows the profile silhouette. Sizes are S, M and L, with Enabled, Hover, Pressed and Inactive states.
- **Tooltip:** four positions with fixed or auto width. Following Bootstrap, tooltips are **supplementary only**. They open on hover *and* keyboard focus, never hold essential information or interactive content, and aren't used on disabled elements without a focusable wrapper.

### Navigation
- **Navbar** (64px, chrome): the logo, the workflow switcher, the notification icon button with its badge, and the avatar menu.
- **Sidebar** (249px, chrome): eyebrow-labelled groups with 20px icon + 16px Medium label links. Default links use `Grey/300`, and the active link is white. There are Expanded and Collapsed variants with a collapse chevron in the footer.
- The **BETA pill** marks pre-release sections. It currently uses an off-system purple (see Known Gaps).

### Not yet specified (Bootstrap defaults apply)
Breadcrumb, Chip and Tag (on hold, though tokens exist), Filters, Modal, Pagination, Progress, Table, and Video Player all have placeholder pages in Figma. Until they're designed, **use the Bootstrap component with Vyn tokens**: 4px radius, `hairline` borders, Inter type, green primary and warm greys.

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
- Keep `{colors.primary}` for actions: primary buttons, links, the active input and the selected tab.
- Build every screen from one of the four shell templates, and keep the 24px content padding.
- Use weight (400 → 500 → 600) to create hierarchy before reaching for a bigger size.
- Use the hover and pressed **overlays** (black 15% / 20%, white on dark) instead of inventing new hex values.
- Use 4px radius for anything with a text label and the pill radius for icon-only controls, avatars and badges.
- Separate regions with surface change (white / `surface-1` / chrome) and 1px hairlines.
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
- Don't use pure black (#000) for text or surfaces. The darkest value is `Grey/800` #2C2A29.
- Don't use cool Bootstrap greys (`$gray-*`). Every neutral comes from the warm Grey ramp.
- Don't put essential information in tooltips, or joke anywhere near safety or compliance content.

## Responsive Behavior

> The Figma file only defines **desktop at 1440px**. The breakpoints below are **proposed** from Bootstrap defaults and need confirmation. See Known Gaps.

### Breakpoints (Bootstrap)

| Name | Min width | Key changes |
|---|---|---|
| xxl | 1400px | Design target (1440). Full shell: sidebar expanded, filter rail visible |
| xl | 1200px | Sidebar expanded, filter rail visible, content columns compress |
| lg | 992px | **Sidebar collapses** to icon-only. Filter rail becomes a toggleable overlay |
| md | 768px | Sidebar becomes an off-canvas menu opened from the navbar. Drawer goes full width |
| sm / xs | < 768px | Single column. Tables become stacked cards. Review-only use is assumed |

### Touch Targets
- Standard controls already meet a 48px target: inputs, dropdown items and Large buttons.
- On touch viewports, promote Small (28px) and Medium (39px) buttons to Large, or add padding so the hit area reaches 44 × 44px.
- The 24px and 32px icon buttons need a 44px hit area on touch.

### Collapsing Strategy
- **Sidebar:** Expanded (249px) → Collapsed (icons only, using the existing `.Link-collapsed` variant) → off-canvas.
- **Filter panel:** persistent rail → an overlay drawer opened by a "Filters" button with an active-filter count badge.
- **Vyn Viewer drawer:** a 289px left inset at desktop → full screen below md.
- **Navbar:** the workflow switcher truncates, then moves into the off-canvas menu. The notification and avatar controls always stay visible.

## Accessibility

- **Contrast checks** (WCAG 2.2 AA):
  - Green/600 on white is 4.64:1. That passes AA for text but only just, so don't lighten it.
  - Grey/600 on white is 7.5:1.
  - White on Danger is 5.6:1.
  - Grey/300 on chrome is 9.7:1.
  - Grey/500 on white is 4.4:1, which fails for small text, so use it only for disabled or decorative content.
- **Focus:** every interactive element shows the 4px focus ring and must never have `outline: none` without it.
- **Color is never the only signal.** Pair status color with text or an icon, which applies to alerts, badges, tags and validation.
- **Keyboard:** drawers and modals trap focus and close on Esc. Dropdowns and tabs follow the WAI-ARIA patterns that Bootstrap implements.
- **Motion:** respect `prefers-reduced-motion` for drawer slide-ins and accordion expansion.

## Iteration Guide

1. Work on **one component at a time** and refer to it by its `components:` token name, for example `button-primary-outline` or `text-input-error`.
2. Start from the matching **Bootstrap component**, then swap in Vyn tokens: 4px radius, warm greys, Inter, green primary, blue focus ring.
3. Pick the **shell template** first (Desktop, + Filter panel, + Drawer, Full Page), then lay out content on the 12-column / 24px-gutter grid.
4. Default body text to `body-p1` (16/24 Regular) and dense views to `body-p2` (14/21).
5. Add new variants as separate component entries (`-hover`, `-selected`, `-error`) that reference existing tokens.
6. Before shipping, check new copy against the four voice principles, especially near safety or compliance content.
7. Run `npx @google/design.md lint DESIGN.md` after edits.

## Known Gaps

These came up while drafting and should be resolved in Figma or code:

- **Focus color is Bootstrap blue** (#007BFF border, #80BDFF ring). It's the only blue in the system. Decide whether that's intentional (a familiar, highly visible accessibility affordance) or should move to a green-based ring.
- **Documentation page vs. live variables:** the Foundations page Alert table lists `alert-success-bg` #E8F5E9, `alert-success-text` #1B5E20, `alert-warning-text` #E65100 and `alert-danger-text` #C62828. The live variables resolve to #DCFCE7, #14532D, #BF360C and #5F0F0F. **This file uses the live variable values.** Several Tag and Chip rows on that page also render as #000000 placeholders.
- **Card radius (6px) and card border (black 18%)** aren't tokens. Either add `--radius-m: 6px` and a `Border/border-subtle` token, or move cards to 4px or 8px.
- **Sidebar width of 249px** is off the 4/8px grid. Consider 248px or 256px.
- **BETA pill** uses off-system purples (#7C3AED text on #352D40 with a #4B3175 border) at 2.3:1 contrast, which fails AA. It needs a token and a contrast fix.
- **Font-size token naming:** the navbar workflow button binds to a variable named `xs` that resolves to 14px, while the local Typography collection defines `XS` as 12px. These probably come from two different libraries and need reconciling.
- **Secondary Outline buttons** use a `Grey/200` border (#EBEAE8), which is only about 1.2:1 against white. It's legible through the label, but weak as a boundary, so consider `Grey/300` or `Grey/400`.
- **Dark mode:** only a Light mode exists. The chrome is dark, but there's no dark theme for the work area.
- **Responsive:** only 1440px desktop frames exist. The breakpoints and collapsing behaviour above are proposals.
- **Undocumented components:** the header counts 33 component sets and 9 standalone components, and 15 are documented here. Breadcrumb, Chip/Tag, Drawer, Filters, Modal, Pagination, Progress, Table and Video Player are placeholders.
- **Bootstrap version:** the focus values match Bootstrap 4 (`$primary` #007BFF, `$input-focus-border-color` #80BDFF). Confirm whether the codebase is on Bootstrap 4 or 5, because breakpoints (5 adds `xxl`), utilities and form markup differ.
- **Motion:** no durations or easing are defined. Bootstrap defaults (0.15–0.35s ease-in-out) are assumed.
- **Marketing site:** vyntelligence.com couldn't be fetched while drafting. Voice guidance relies on the Brand Feel audit, which quotes the site directly.
