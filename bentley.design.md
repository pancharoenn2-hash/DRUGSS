---
version: alpha
name: "Bentley"
website: "https://www.bentleymotors.com"
description: >-
  A British ultra-luxury automotive brand (VW Group) whose marketing site pairs a near-black
  canvas (#040404) with a single muted forest green (#394d45 — the house's "Bentley Race Green")
  as the sole chromatic accent, used exclusively on primary CTA fills and structural borders.
  Type runs Bentley — a proprietary humanist sans — at featherweight 300 across every tier,
  with display sitting at 38–48px at that same light weight, signaling restraint-as-authority
  in a system where photography of hand-stitched leather interiors and hand-beaten aluminum
  coachwork carries the visual weight. Button radius is a sharp 0px. The blush cream (#e7cfb9)
  wired as `--bm-primary-blush` signals the interior material palette but does not render
  in the captured marketing surface.

seo:
  title: "Bentley Design System in Race Green and Featherweight Type"
  metaDescription: "Bentley's near-black #040404 canvas, Race Green #394d45 as the only accent and its own typeface at weight 300 on every tier. For React and AI tools."
  highlights:
    - "Weight 300 at every tier — Bentley's typeface runs from 48px display to 11px caption at the same featherweight, with no bold tier anywhere in the marketing surface"
    - "Race Green CTA — #394d45 (Bentley Race Green, wired as --bm-primary-living-green) is the sole chromatic brand accent; the entire hero and body canvas is monochrome dark"
    - "Near-black canvas at #040404 — 407 combined occurrences as text and border; a fractional step from pure black that prevents digital harshness"
    - "Uppercase tracked labels at 1.3px — 13px / 400 / uppercase / 1.3px appears on nav and category chips, distinct from the light body weight"
    - "Blush cream and moss palette — #e7cfb9 (--bm-primary-blush) and #dcd8c0 (--bm-primary-moss) are declared in CSS as material-reference tokens but absent from the rendered marketing surface"
  tags:
    - "Automotive"
  lastUpdated: "2026-05-19"
  author:
    name: "Dov Azencot"
    url: "https://x.com/dovazencot"
  opening: |
    Bentley's marketing site uses weight 300 for everything. The 48px hero heading at weight 300. The 24px section headings at weight 300. The 16px body paragraphs at weight 300. The 11px navigation items at weight 400 — the single instance where the weight steps above featherweight. This is not a technical accident; it is the brand's most specific design decision, and it separates Bentley from every other automotive brand in this directory. Where Rolls-Royce uses a thin serif, Ferrari holds to weight 500, and Cadillac goes to weight 100 with extreme tracking, Bentley grounds everything in a single humanist sans at 300, and trusts the photography of quilted leather, engine-turned aluminum, and hand-stitched wool carpet to deliver the material luxury that the typeface refuses to shout about.

    The DESIGN.md file packages the Bentley marketing design system into a machine-readable spec. Inside: 12 color tokens from the extracted palette (near-black, Bentley Race Green, white, muted teal, and the blush and moss cream declared in CSS but absent from rendered surfaces), 11 typography tokens running the Bentley proprietary humanist sans at weights 300 and 400 across display through caption tiers, the brand's 0px button radius, 9 spacing tokens on an 8px base, and 16 component definitions covering the primary CTA, nav, hero heading, editorial cards, the Mulliner custom-configurator section, and the ownership-portal link. The CSS variable system (`--bm-spacer-*`, `--bm-primary-*`) reveals a structured token architecture not fully exposed by the marketing surface alone.

    Feed this file to Claude or Cursor to reproduce Bentley's discipline: near-black #040404 canvas, Bentley humanist sans at weight 300 for every non-label tier, Race Green (#394d45) reserved exclusively for the primary CTA button fill and border, 0px sharp corners, and full-bleed vehicle photography filling the hero and Mulliner sections. The move worth borrowing only if your brand has comparable photographic assets is the confidence to let weight 300 text sit alone on a dark canvas — the typography does not carry the emotional weight; the photography of a hand-built Continental GT does.
  related:
    - href: "/design"
      title: "Browse all design systems"
      description: "The full directory of DESIGN.md files on shadcn.io, with live mockups for each."
    - href: "https://www.bentleymotors.com"
      title: "Bentley Motors — official site"
      description: "Bentley's public marketing site — the source of truth for the live tokens captured in this file."
    - href: "https://github.com/google-labs-code/design.md"
      title: "The DESIGN.md specification"
      description: "Google Labs' open spec for machine-readable design system files — the format this page is built on."
  questions:
    - id: "primary-color"
      title: "What is Bentley's primary brand color?"
      answer: "Bentley's sole chromatic brand accent is Race Green — #394d45, wired as `--bm-primary-living-green` in the CSS. It appears 12 times in the captured surface: 6 as background fill (the primary CTA button), 6 as border. The entire remainder of the marketing site is monochrome near-black (#040404) and white (#ffffff). The system also declares `--bm-primary-teal` (#637a77) and `--bm-primary-blush` (#e7cfb9), but neither appears in the rendered marketing surface — they belong to interior material references and the Mulliner personalization palette. The restraint is intentional: Bentley Race Green is the livery color the brand has used on racing programs since the 1920s Le Mans wins; deploying it once, on the single primary CTA, is the appropriate digital expression."
    - id: "typography"
      title: "What typeface does Bentley use, and what weight is it?"
      answer: "Bentley uses a proprietary humanist sans named Bentley, with fallbacks to arial, helvetica, sans-serif. Weight 300 (light) is the default across every display, body, and label tier. The single exception is the uppercase navigation and category-chip labels at 13px / weight 400 / 1.3px tracking — one step above featherweight for the smallest, most legible contexts. Display headlines run 38–48px at weight 300 with normal letter-spacing. Body runs 16px at weight 300 with 0.16px tracking. This means the 48px hero heading and the 11px fine-print label share the same weight — hierarchy comes from size alone. For open-source substitution, Raleway at weight 300 or Jost Light at weight 300 approximates the proportions; avoid Inter and Neue Haas Grotesk, which are too mechanical for the humanist construction."
    - id: "canvas-color"
      title: "Why does Bentley use #040404 instead of pure black?"
      answer: "The canvas is #040404 — a fractional step from pure black that prevents the digital harshness that #000000 produces when photographic content sits against it at high contrast. At 407 combined occurrences (text + border), the near-black is the page's primary color, and the difference from pure black is invisible to casual view. The distinction matters when rendering vehicle photography: pure black can cause dark-area photo clipping to read as flat; #040404 allows the shadow areas of a car photograph to separate from the canvas by a perceptible margin. The same reasoning applies at Ferrari (#181818) and Rolls-Royce dark surfaces."
    - id: "race-green-usage"
      title: "Where does Bentley Race Green appear on the site, and why not elsewhere?"
      answer: "Bentley Race Green (#394d45, `--bm-primary-living-green`) appears in exactly two roles: as the background fill of the primary CTA button (6 background occurrences), and as the border of that same button (6 border occurrences). It does not appear as text, on any card surface, or as a section background. The tonal partner `--bm-primary-teal` (#637a77) is declared in CSS but not rendered. This scarcity replicates how the color functions on physical vehicles: the Bentley race cars at Le Mans wore it as the full body livery, but on the road cars it appears only as a color option — not as chrome, trim, or badging. The digital system makes the same distinction."
    - id: "use-in-project"
      title: "Can I use this DESIGN.md to build an ultra-luxury brand marketing site?"
      answer: "Yes — feed the file to Claude, Cursor, or any AI tool that reads structured design tokens. The agent will reproduce Bentley's discipline: near-black #040404 canvas, Bentley humanist sans at weight 300, Race Green (#394d45) on the single primary CTA only, uppercase-tracked 13px / 400 / 1.3px labels for navigation, and 0px sharp corners. The 16 component definitions cover the major marketing surfaces — hero, model cards, Mulliner section, editorial grid, ownership link. Important note: the weight-300 typography only holds as the authority signal when combined with vehicle photography at the quality Bentley produces; on a token-only prototype without high-quality imagery, weight 300 at small body sizes can read as thin rather than restrained. Plan for strong photography from the start."

mockups:
  - "marketing-hero"
  - "media-grid"

colors:
  primary: "#394d45"
  primary-teal: "#637a77"
  blush: "#e7cfb9"
  ink: "#040404"
  ink-black: "#000000"
  canvas: "#ffffff"
  surface-1: "#f0f0f0"
  hairline: "#ffffff"

typography:
  display-xl:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 48px
    fontWeight: 300
    lineHeight: 54px
    letterSpacing: normal
  display-md:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 38px
    fontWeight: 300
    lineHeight: 44px
    letterSpacing: normal
  heading-md:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 24px
    fontWeight: 300
    lineHeight: 28px
    letterSpacing: normal
  heading-sm:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 20px
    fontWeight: 300
    lineHeight: 28px
    letterSpacing: 0.16px
  body-md:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 16px
    fontWeight: 300
    lineHeight: 24px
    letterSpacing: 0.16px
  body-sm:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 13px
    fontWeight: 300
    lineHeight: 18px
    letterSpacing: 0.13px
  button-md:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 16px
    fontWeight: 300
    lineHeight: 24px
    letterSpacing: 0.16px
  nav-link:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 16px
    fontWeight: 300
    lineHeight: 24px
    letterSpacing: 0.16px
  label-caps:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 13px
    fontWeight: 400
    lineHeight: 16px
    letterSpacing: 1.3px
  label-caps-wide:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 16px
    letterSpacing: 1.6px
  caption:
    fontFamily: "Bentley, arial, helvetica, sans-serif"
    fontSize: 11px
    fontWeight: 400
    lineHeight: 16px
    letterSpacing: 0.11px

rounded:
  none: "0px"

spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  base: "16px"
  lg: "24px"
  xl: "32px"
  2xl: "40px"
  3xl: "48px"
  4xl: "64px"

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.canvas}"
    typography: "{typography.button-md}"
    rounded: "{rounded.none}"
    padding: "16px 22px"
    height: "50px"
    borderColor: "{colors.primary}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.canvas}"
    typography: "{typography.button-md}"
    rounded: "{rounded.none}"
    padding: "12px 18px"
    height: "44px"
    borderColor: "{colors.canvas}"
  top-nav:
    backgroundColor: "transparent"
    textColor: "{colors.canvas}"
    typography: "{typography.nav-link}"
    rounded: "{rounded.none}"
    padding: "0px 48px"
    height: "55px"
  nav-link:
    backgroundColor: "transparent"
    textColor: "{colors.canvas}"
    typography: "{typography.nav-link}"
    padding: "8px 0px"
  hero-heading:
    backgroundColor: "transparent"
    textColor: "{colors.canvas}"
    typography: "{typography.display-xl}"
    padding: "0px"
  section-heading:
    backgroundColor: "transparent"
    textColor: "{colors.canvas}"
    typography: "{typography.heading-md}"
    padding: "0px"
  section-heading-dark:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.heading-md}"
    padding: "0px"
  body-paragraph:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.body-md}"
  body-paragraph-light:
    backgroundColor: "transparent"
    textColor: "{colors.canvas}"
    typography: "{typography.body-md}"
  label-caps:
    backgroundColor: "transparent"
    textColor: "{colors.canvas}"
    typography: "{typography.label-caps}"
    padding: "8px 0px"
  editorial-card:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.canvas}"
    typography: "{typography.body-md}"
    rounded: "{rounded.none}"
    padding: "24px"
  model-card:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.canvas}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.none}"
    padding: "16px"
  mulliner-section:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.canvas}"
    typography: "{typography.heading-md}"
    rounded: "{rounded.none}"
    padding: "40px 48px"
  editorial-light-section:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-md}"
    rounded: "{rounded.none}"
    padding: "40px 48px"
  card:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-md}"
    rounded: "{rounded.none}"
    padding: "24px"
  text-input:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-md}"
    rounded: "{rounded.none}"
    padding: "12px 16px"
    height: "48px"
    borderColor: "{colors.surface-1}"
---

## Overview

Bentley's marketing site is built on a single typographic conviction: **weight as restraint**. The Bentley proprietary humanist sans runs at weight 300 from the 48px hero heading down to the 16px body paragraph — the same featherweight regardless of scale. Where Rolls-Royce uses thin-stroke serif to signal old-money heritage, where Bentley's corporate sibling Porsche holds display at weight 700, and where Ferrari stops at weight 500, Bentley goes lighter than all of them. The logic is not minimalism for its own sake; it is the typographic equivalent of the hand-stitched leather and hand-beaten aluminum the brand builds into every vehicle — the restraint is the product.

The chromatic palette is near-monochrome. A near-black canvas at #040404 (407 combined occurrences) holds white text and photography. The single chromatic accent is Race Green at #394d45 — Bentley's historic Le Mans racing livery color, appearing in exactly 12 occurrences: 6 as the primary CTA fill, 6 as its border. Nothing else carries color. The CSS declares `--bm-primary-blush` (#e7cfb9) and `--bm-primary-moss` (#dcd8c0) — references to the interior material palette — but neither renders in the captured marketing surface. The marketing site stays monochrome and delegates material warmth entirely to photography.

The shape language is **zero-radius sharp**, consistent with the brand's architectural DNA: the Bentley grille is a strict rectilinear mesh, the Flying B mascot extends on a straight line. Every button, card, and editorial surface carries 0px corners.

**Key Characteristics:**
- Weight 300 at every typographic tier from 48px display to 16px body — the featherweight-as-authority move, unique in this directory at this scale.
- Race Green (#394d45) appears in exactly 12 occurrences — CTA fill and border only — making it the most color-restrained automotive brand in the directory.
- Near-black canvas at #040404 with 407 combined occurrences as the page's structural color.
- White canvas bands (#ffffff, 307 occurrences) appear inside the editorial Bentley Motors section and model-grid areas.
- Uppercase label tier at 13px / weight 400 / 1.3px tracking — the only weight-400 tier in the system, reserved for the smallest navigational labels.
- 0px border-radius universally.
- The CSS spacer system (`--bm-spacer--3` through `--bm-spacer--13`) maps to 16–112px on an 8px base, revealing structured spacing discipline not visible from the marketing surface alone.

## Colors

### Brand

- **Primary** (`{colors.primary}` — #394d45): frequency 12. Used as background (6), border (6). Bentley Race Green — the exact green of the 1920s Le Mans Bentley Boys team cars, wired as `--bm-primary-living-green`. Never as text; never as a section background. The single color in an otherwise monochrome system.
- **Primary Teal** (`{colors.primary-teal}` — #637a77): wired as `--bm-primary-teal`. A lighter, more muted version of the Race Green — declared but absent from the rendered marketing surface; likely reserved for the Mulliner personalization configurator.
- **Blush** (`{colors.blush}` — #e7cfb9): wired as `--bm-primary-blush` and `--bm-primary-moss`. A warm pale cream referencing the interior material palette — Bentley's hand-stitched leather and wool carpet. Absent from the rendered marketing surface; a material-reference token rather than a marketing-surface color.

### Canvas & Surfaces

- **Ink** (`{colors.ink}` — #040404): frequency 407. Used as text (201), border (201), background (5). The near-black page canvas — a fractional step from pure black that prevents photographic dark-area clipping. Wired across multiple `--bm-*` variables as the base structural tone.
- **Canvas** (`{colors.canvas}` — #ffffff): frequency 307. Used as text (149), border (143), background (10), gradient (5). The white editorial-band surface and the nav/label text on the dark canvas. Wired as `--bm-basic-white` and `--bm-primary-moss--10`.
- **Ink Black** (`{colors.ink-black}` — #000000): frequency 10. A pure-black accent layer for overlay gradients and scrim backgrounds, wired as `--bm-basic-black` and `--bm-transparent`.
- **Surface-1** (`{colors.surface-1}` — #f0f0f0): frequency 2. A near-white gradient stop — used in editorial transitions between dark and light bands.
- **Hairline** (`{colors.hairline}` — #ffffff): used at low opacity as the border tone on dark surfaces, 143 occurrences. White-with-alpha is the only hairline tone that reads against near-black.

## Typography

### Font Family

The system runs **Bentley** — a proprietary humanist sans that shares proportions with Gill Sans or Optima but at a clearly custom point of difference. Fallbacks walk to arial, helvetica, sans-serif. There is no secondary family; Bentley carries every tier from caption to display. The humanist construction (slightly modulated stroke widths, open apertures) is visible at 38–48px display sizes and is why the weight-300 setting reads as restrained craft rather than as hollow thinness.

### Hierarchy

| Token | Size | Weight | Line Height | Letter Spacing | Use |
|---|---|---|---|---|---|
| `{typography.display-xl}` | 48px | 300 | 54px | normal | Hero h1 / h3 ("New Continental GT S") |
| `{typography.display-md}` | 38px | 300 | 44px | normal | Large section headings, Mulliner feature heading |
| `{typography.heading-md}` | 24px | 300 | 28px | normal | Section h2 ("Models", "Bentley Motors") |
| `{typography.heading-sm}` | 20px | 300 | 28px | 0.16px | Sub-heading / label surfaces |
| `{typography.body-md}` | 16px | 300 | 24px | 0.16px | Default running body text; nav link size |
| `{typography.body-sm}` | 13px | 300 | 18px | 0.13px | Fine print, model subtext |
| `{typography.button-md}` | 16px | 300 | 24px | 0.16px | Primary CTA label |
| `{typography.nav-link}` | 16px | 300 | 24px | 0.16px | Top-nav links |
| `{typography.label-caps}` | 13px | 400 | 16px | 1.3px | Uppercase category and nav labels — only weight-400 tier |
| `{typography.label-caps-wide}` | 16px | 400 | 16px | 1.6px | Wider uppercase caps for emphasis labels |
| `{typography.caption}` | 11px | 400 | 16px | 0.11px | Metadata, fine print, footnotes |

### Principles

Weight 300 is the single setting for every body, heading, button, and display tier — eight of the eleven typography tokens share this weight. The hierarchy is size-only. This is an intentionally difficult constraint: at small sizes, weight 300 requires precise rendering and good screen clarity; on substandard displays it reads as thin. The system accepts that risk because the ultra-luxury audience encounters the brand on high-resolution devices in contexts where the rendering quality is reliable.

### Font Substitutes

Bentley is proprietary. **Raleway** at weight 300 is the closest open-source humanist substitute — the moderate-contrast stroke structure and open apertures carry over. **Jost** Light (300) is slightly more geometric but works at body sizes. Avoid weight 300 of mechanically neutral fonts like Inter at small sizes — the lack of stroke modulation makes ultra-light text read as a rendering artifact rather than a typographic decision.

## Layout

### Spacing System

- **Base unit:** 8px. The CSS declares `--bm-spacer--3` (16px) through `--bm-spacer--13` (112px) on a structured ladder.
- **Tokens:** `{spacing.xs}` 4px · `{spacing.sm}` 8px · `{spacing.md}` 12px · `{spacing.base}` 16px · `{spacing.lg}` 24px · `{spacing.xl}` 32px · `{spacing.2xl}` 40px · `{spacing.3xl}` 48px · `{spacing.4xl}` 64px.
- **Grid margin:** `--bm-grid-margin` 48px — the outer page margin on desktop.
- **Grid gutter:** `--bm-grid-gutter` 24px — the column gutter between editorial grid cells.
- **Section padding:** 40px on the Mulliner and editorial-light sections; 48px on the model grid.

### Grid & Container

- **Hero:** full-bleed vehicle photography at 1440px, with the headline and CTA positioned at the lower-left of the image (not centered) — a compositional preference that reads as editorial magazine rather than standard SaaS hero.
- **Model grid:** 4-column editorial card grid on desktop, each card containing a vehicle photograph, name, and Race Green CTA button.
- **Bentley Motors editorial:** white canvas section with running body paragraph and then 4-column photo editorial strip.
- **Mulliner section:** Race Green (#394d45) full-bleed panel — the single large-surface application of the brand accent color.

### Rhythm

The page alternates: near-black hero (photography-dominant) → white editorial band → near-black model grid → Race Green Mulliner panel → gold vehicle close-up photography → white ownership/app section. The rhythm is sparser than most automotive sites — fewer bands, more pause per band — consistent with the "hand-crafted takes time" brand positioning.

## Elevation

No shadow tier appears in the captured surface. The near-black canvas creates depth through two mechanisms: photography (the vehicle images create the only spatial depth on the page) and the white editorial band's contrast with the surrounding dark canvas. There are no drop shadows on buttons, cards, or navs.

- **Flat (no shadow):** 100% of captured surfaces.
- **Depth from photography:** the hero and model photography provide the page's only spatial dimensionality.
- **Hairline borders:** the 1px white hairline (white-alpha) separates nav from hero on dark surfaces; it is the page's finest structural line.

## Shapes

The radius scale is absolute zero, consistent with every ultra-luxury automotive brand in this directory. Every component — primary button, secondary button, model card, editorial card, Mulliner panel — carries 0px border-radius. The sharp geometry is the digital translation of the Bentley grille's rectilinear mesh: precision lines rather than softened curves. Unlike Cloudflare, which uses a pill for its primary CTA, Bentley applies the sharp rule even to the single most important action surface.

## Components

**`button-primary`** — Race Green (#394d45) fill, white text, Bentley 16px / 300 / 0.16px tracking, 0px radius, 16×22px padding, 50px height. The single chromatic CTA in the system. "Explore" is the canonical label instance.

**`button-secondary`** — Transparent fill, white text, 1px white border, 0px radius, 12×18px padding, 44px height. Used for secondary navigation actions on dark-canvas surfaces.

**`top-nav`** — Transparent background over the hero photography, white text in nav-link (16px / 300), 48px horizontal page margin, 55px height. The Bentley winged-B mark centered above the nav; links flush right.

**`nav-link`** — Transparent background, white text, 16px / 300 / 0.16px, 8px top/bottom padding.

**`hero-heading`** — White text on photography overlay, Bentley 48px / 300 / normal tracking. Lower-left positioned rather than center-aligned — the editorial compositional move.

**`section-heading`** — White text at 24px / 300, used on dark-canvas sections ("Models").

**`section-heading-dark`** — Ink text at 24px / 300, used on white-canvas editorial sections ("Bentley Motors").

**`body-paragraph`** — Ink text at 16px / 300 / 0.16px — the editorial body in white-canvas sections.

**`body-paragraph-light`** — White text at 16px / 300 / 0.16px — the body on dark-canvas sections.

**`label-caps`** — The uppercase label tier: 13px / 400 / 1.3px tracking — the only weight-400 surface, used for category navigation and chip labels. Transparent background, white text on dark.

**`editorial-card`** — Near-black fill, white text, 0px radius, 24px padding. Model cards in the lineup grid.

**`model-card`** — Near-black fill, white body-sm text, 0px radius, 16px padding. The smaller tile format for secondary model links.

**`mulliner-section`** — Race Green (#394d45) fill, white text, 40px × 48px padding. The single large application of the brand accent color, used for the Mulliner custom-configurator section.

**`editorial-light-section`** — White canvas fill, ink text, 40px × 48px padding. The "Bentley Motors" editorial band between the model grid and the Mulliner section.

**`card`** — White canvas, ink text, 0px radius, 24px padding. The content card used on light-canvas surfaces.

**`text-input`** — White canvas, ink text, surface-1 (#f0f0f0) border, 0px radius, 12×16px padding, 48px height.

## Do's and Don'ts

**Do** hold every typographic tier at weight 300. The move is indivisible — the moment a heading steps to weight 500 or 700, the discipline that distinguishes Bentley from other dark-canvas automotive brands disappears. Weight 300 at 48px reads as ultra-luxury precisely because it takes confidence in the photography to leave the heading so light.

**Do** keep Race Green (#394d45) off every surface except the primary CTA button and its border. The 12 total occurrences in the captured surface are not a bug — they are the entire chromatic statement. Using the color on section dividers, labels, or secondary buttons would dilute the single-voltage discipline.

**Do** use the lower-left headline positioning in hero sections rather than center-aligned. Bentley's hero typography sits at the bottom-left of the vehicle image, reading as editorial magazine rather than SaaS landing page — the vehicle composition fills the right two-thirds of the frame.

**Do** use the uppercase tracked label tier (`{typography.label-caps}` — 13px / 400 / 1.3px) for every navigation label and category chip. It is the only tier where the system breaks from weight 300, and its tracked uppercase provides the navigational legibility that the light-weight body would not at 13px.

**Don't** introduce the blush cream (#e7cfb9, wired as `--bm-primary-blush`) on the marketing surface. It is a material-reference token for the Mulliner configurator interior palette — deployed on digital surfaces outside the configurator context, it reads as a generic warm cream rather than as a reference to Bentley's hand-stitched leather.

**Don't** add drop shadows to the Race Green CTA button or any card surface. The system has zero shadow occurrences; the button reads as the sole elevated element purely through its Race Green fill against the near-black canvas. A shadow would add visual weight that contradicts the featherweight-text discipline.

**Don't** round the primary button corners above 0px. At 16px padding and 50px height, even 4px rounding softens the sharp geometry that echoes the Bentley grille's rectilinear matrix. The button is a precision object, not a tappable pill.

**Don't** run Bentley typeface below 11px at weight 300. The humanist construction's modulated stroke widths become ambiguous at very small sizes in weight 300; the system avoids this by stepping to weight 400 at the 11px caption tier, and you should maintain that floor.

## Known Gaps

- **Configurator surfaces:** the Bentley configurator and Mulliner personalization tools at `bentleymotors.com/en/configurator` carry their own token layer — material swatches, exterior color pickers, interior leather options — using the blush (#e7cfb9) and moss (#dcd8c0) tokens not present in the marketing capture.
- **Ownership portal / app:** the `{component.ownership}` section links to the Bentley Connect app, which likely carries a distinct mobile-surface token set.
- **Hover and focus states:** no hover captures were present in the extracted components; the primary button hover state is not documented here.
- **Dark-mode / light-mode toggle:** the CSS declares no explicit dark/light toggle variable, suggesting the site is dark-by-default without a user preference API.
- **EWB / Mulsanne model pages:** individual model deep-dive pages (e.g., Bentayga EWB) may expose additional accent tones for trim and specification tables not present in the homepage capture.
- **Motion:** the hero photography transitions and the Mulliner section scroll reveal are not captured — the spec covers end-state values only.
