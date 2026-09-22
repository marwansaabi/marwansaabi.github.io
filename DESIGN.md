---
name: Marwan El Saabi — Portfolio
description: A lab-notebook-styled data science and bioinformatics portfolio, editorial and evidence-first.
colors:
  paper: "#F4F0E6"
  paper-alt: "#EAE2CE"
  ink: "#1B1712"
  ink-soft: "#6B6355"
  line: "#D6CBAE"
  accent: "#9C3B1D"
  accent-deep: "#6E2A14"
typography:
  display:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "clamp(2.3rem, 5vw, 4.4rem)"
    fontWeight: 400
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "clamp(2.1rem, 4.2vw, 3rem)"
    fontWeight: 400
    lineHeight: 1.2
  title:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "1.3rem"
    fontWeight: 500
    lineHeight: 1.25
  body:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "Fragment Mono, Courier New, monospace"
    fontSize: "11px"
    fontWeight: 400
    letterSpacing: "0.08em"
rounded:
  sm: "3px"
  md: "6px"
  lg: "8px"
spacing:
  xs: "0.5rem"
  sm: "1rem"
  md: "1.5rem"
  lg: "2.5rem"
  xl: "4rem"
  "2xl": "7rem"
components:
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "13px 28px"
  button-outline-hover:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    rounded: "{rounded.sm}"
  tag:
    backgroundColor: "transparent"
    textColor: "{colors.ink-soft}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    padding: "3px 10px"
  project-tile:
    backgroundColor: "{colors.paper}"
    rounded: "{rounded.lg}"
    padding: "1.8rem 1.9rem 2rem"
---

# Design System: Marwan El Saabi — Portfolio

## Overview

**Creative North Star: "The Lab Notebook"**

This is a data-science and bioinformatics portfolio built to be read the way a reviewer reads a methods section: claims are numbered, figures are captioned, and every result links back to the app or repo that produced it. The system borrows its authority from scientific publication rather than from product marketing — warm paper, a serif built for long reading, a monospace reserved for labels and data, and a single terracotta accent used the way a red pen marks a proof. Nothing is decorative; every mark on the page is either content or the structure that organizes it.

It is restrained and academic by deliberate contrast with the genre it replaced: this project previously used an emerald-on-white "creative dev portfolio" look (custom cursor, emoji icons, pill buttons, percentage-bar skill widgets). The rejection of that language is load-bearing, not incidental — see Do's and Don'ts.

**Key Characteristics:**
- Warm paper background with a single burnt-terracotta accent; no second brand color, ever.
- Spectral serif for both display and body copy; Fragment Mono reserved for labels, data, and UI chrome.
- Flat by current implementation: zero shadows anywhere; depth comes from 1px hairline borders and paper/paper-alt tonal shifts.
- Sharp-leaning corner radius (3–8px); no pill shapes.
- Every project claim is evidence-backed: a real screenshot or a real methodology figure, a live-app link, a code link.

## Colors

Warm and desaturated, with exactly one saturated color in the entire system.

### Primary
- **Burnt Terracotta** (`#9C3B1D`): the single accent. Used for hover fills, the active nav underline, section-category labels, the contact card's top rule, and the emphasized word in the hero headline (as italic text color). Nothing else on the page carries color.
- **Deep Terracotta** (`#6E2A14`, reserved): a darker step of the accent, defined as `--accent-deep` for future pressed/active states. Not yet wired to a live component — use it before inventing a new shade if a component ever needs an accent darker than hover state.

### Neutral
- **Warm Paper** (`#F4F0E6`): page background.
- **Paper Alt** (`#EAE2CE`): secondary surface — tile-visual placeholders, the skills-ledger category padding, the contact card background. One step darker than the page, never a separate "card white."
- **Espresso Ink** (`#1B1712`): primary text and default button/border color. Not pure black.
- **Soft Ink** (`#6B6355`): secondary/supporting text — descriptions, captions, nav labels at rest.
- **Hairline** (`#D6CBAE`): every border, divider, and rule on the page. This color *is* the structural system (see Shapes).

### Named Rules
**The One Accent Rule.** Terracotta is the only saturated color anywhere in the system. A second brand color, a status-color palette, or a gradient is a system violation, not a stylistic option.

## Typography

**Display Font:** Spectral (with Georgia, serif fallback)
**Body Font:** Spectral (with Georgia, serif fallback) — the same family as Display
**Label/Mono Font:** Fragment Mono (with Courier New, monospace fallback)

**Character:** One serif carries every reading task, from the hero headline down to a project description, so the page never breaks voice the way a display/body font pairing can. Fragment Mono is the deliberate second voice: it never appears in prose, only in machine-legible chrome — navigation, tags, captions, data labels — so a reader can tell "this is UI" from "this is content" by typeface alone before reading a word.

### Hierarchy
- **Display** (400, `clamp(2.3rem, 5vw, 4.4rem)`, line-height 1.15): the hero headline only. Emphasis within it is italic in the same family, colored with the accent — never a second typeface for emphasis.
- **Headline** (400, `clamp(2.1rem, 4.2vw, 3rem)`, line-height 1.2): section titles ("Selected Work", "Technical Expertise", "Academic Background").
- **Title** (500, `1.3rem`, line-height 1.25): project titles, degree names, skill-row names (at `1.06rem`).
- **Body** (400, `1rem`, line-height 1.7–1.8): project/section/contact descriptions. Runs in Soft Ink, not full Ink, for anything that isn't a heading.
- **Label** (400, `10.5–12px`, letter-spacing `0.03–0.14em`, uppercase, Fragment Mono): nav links, buttons, tags, `project-number`/`fig-caption` figure labels, skill levels, education years, footer.

### Named Rules
**The No-Em-Dash Rule.** No em dash (`—`) or en dash used as a separator (`–`) appears anywhere in visible text — titles, captions, body copy, dates, attribution. Ranges and compounds use a plain hyphen (`2025-2027`, not `2025–2027`). This was fixed once across the entire site; do not reintroduce it.

## Layout

The page is a single static document, `max-width: 1400px`, centered, with generous vertical rhythm: `7rem` top/bottom padding per section, `4rem` between a section header and its content. The hero is the exception at `min-height: 100vh` with its own `8rem/4rem` padding.

Two structural grid patterns:
- **Uniform tile grid** (Projects): `grid-template-columns: repeat(2, 1fr)`, `2.5rem` gap, collapsing to one column under `768px`. All five project cards share this one layout family — no featured/full-width outlier card.
- **Bordered ledger grid** (Skills, Education): a shared-hairline grid (`border-top` + `border-left` on the container, each cell closing its own right/bottom edge) so the dividing lines are structural, not decorative — removing one cell doesn't leave a dangling border.

Lists that would default to a middle-dot-separated inline string instead use hairline-divided rows or `border-left` between inline items (see the expertise strip below the hero). Middle dots are rationed to one per line (e.g., `MSc Bioinformatics · A Coruña, Spain`).

Responsive collapse happens at two breakpoints: `768px` (nav becomes a slide-in drawer, project grid becomes one column) and `968px` (education/skills grids collapse to one column).

## Elevation & Depth

The implemented system currently uses **zero shadows** anywhere — no `box-shadow` exists in the codebase. Depth is conveyed entirely through 1px hairline borders (`--line`) and tonal contrast between `--paper` and `--paper-alt`. This is the current state, not a locked invariant: a future component may introduce a shadow if there's a real reason. If one is added, tint it warm to match the paper (never a neutral or pure-black shadow) and keep it as understated as the rest of the system — a generic drop shadow would be the most visible tonal break in the whole page.

## Shapes

Corner radius is a small, sharp-leaning three-step scale: `3px` for interactive controls (buttons, tags), `6px` for the contact card, `8px` for project tiles. Nothing in the system uses a fully rounded/pill shape.

Hairlines (`1px solid var(--line)`) are the system's primary organizing device — more load-bearing than radius or fill. They border every card, divide every ledger row, underline the hero label, separate expertise-strip items, and frame every figure caption. Read the page as a sequence of ruled boxes, not a stack of shadowed cards.

### Named Rules
**The No-Pill Rule.** Maximum corner radius anywhere in the system is `8px`. A `border-radius: 9999px` / pill-shaped button or badge is a system violation.

## Components

Every interactive control in the system is built from one outline-based language: transparent/bordered at rest, filled only on interaction. There is no solid-filled button anywhere at default state.

### Buttons
- **Shape:** `3px` radius, `1px solid var(--ink)` border.
- **Default:** transparent background, Ink text, Fragment Mono label styling (uppercase, `0.06–0.1em` tracking).
- **Hover / Focus:** background fills to Ink, text inverts to Paper; contact-links fill to the accent instead of Ink on hover. `translateY(-2px)` lift on hover, `0.3s` ease.
- **Variants:** identical language at three sizes — hero CTA (`13px 28px`), nav CV button (`7px 18px`), contact links (`11px 22px`, with a leading 14px SVG icon).

### Chips (Tags)
- **Style:** transparent background, Soft Ink text, `1px solid var(--line)` border, `3px` radius, `3px 10px` padding, Fragment Mono `10.5px` uppercase-adjacent (tags are not uppercased, unlike labels).

### Cards / Containers (Project Tiles)
- **Corner Style:** `8px` radius.
- **Background:** Paper (page background continues through; only the border separates it).
- **Shadow Strategy:** none — see Elevation & Depth.
- **Border:** `1px solid var(--line)`.
- **Internal Padding:** `1.8rem 1.9rem 2rem` for the text body; the image slot is full-bleed (`object-fit: cover`, top-aligned) or letterboxed on Paper Alt when the source image's aspect ratio doesn't match (`contain-fit` variant).

### Navigation
- **Style:** fixed top bar, translucent Paper (`rgba(244,240,230,0.88)`) with `blur(8px)` backdrop filter; gains a hairline bottom border once scrolled (via `IntersectionObserver` on a sentinel element, never a raw scroll listener).
- **Typography:** Fragment Mono, `12px`, uppercase, `0.06em` tracking.
- **States:** default Soft Ink; hover/active Ink with a `1px` accent underline that animates in from `width: 0`.
- **Mobile:** below `768px`, collapses to a hamburger opening a full-height right-side drawer on blurred Paper.

### Signature: Ledger Row
The skills section's alternative to a percentage/progress-bar widget: each skill is a row with the name in serif Title weight on the left, the level (`Advanced` / `Intermediate` / `Interm./Adv.`) in Fragment Mono on the right, separated by a `1px` top hairline from the row above. A supporting detail line runs below in Soft Ink at `0.88rem`. This pattern exists specifically to avoid the "arbitrary skill percentage" pattern the previous design used — see Do's and Don'ts.

### Signature: Figure Caption
Every project visual that has a real image carries a `fig-caption` strip directly beneath it: `Fig. 0N. <one-line factual description>`, Fragment Mono, `10.5px`, Soft Ink, separated from the image by a `1px` top hairline. This is the site's evidentiary device — it never contains an em dash, never enumerates decoratively, and always describes the actual visible content of the image, not a category label.

## Do's and Don'ts

### Do:
- **Do** keep terracotta as the only saturated color on the page (The One Accent Rule).
- **Do** use hairline borders and paper/paper-alt tonal shifts for depth; never a generic shadow.
- **Do** back every project claim with a real screenshot, a real methodology figure, a live-app link, or a code link — never a placeholder panel standing in for evidence.
- **Do** reserve Fragment Mono for labels, data, and UI chrome; keep prose in Spectral.
- **Do** caption real images with the `Fig. 0N.` pattern, describing what's actually visible.

### Don't:
- **Don't** use an em dash (`—`) or an en-dash separator (`–`) anywhere in visible text (The No-Em-Dash Rule). Use a plain hyphen.
- **Don't** introduce a second accent color, a status-color system, or a gradient (The One Accent Rule).
- **Don't** use a pill-shaped or fully-rounded button/badge; the system caps at `8px` radius (The No-Pill Rule).
- **Don't** default any button to a filled/solid state; every button in this system is outline-at-rest, filled-on-hover.
- **Don't** replace a real project image with an empty numbered placeholder panel when no screenshot exists yet — either source a real image (including a real figure from the project's own repo) or state plainly that there's no public demo, as the Alzheimer's ML Pipeline card does.
