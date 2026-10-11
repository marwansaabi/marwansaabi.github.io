---
name: Marwan El Saabi - Portfolio
description: A data science portfolio presented like a product page, one project at a time, with real screenshots as the hero imagery.
colors:
  bg: "#ffffff"
  bg-alt: "#f5f5f7"
  ink: "#1d1d1f"
  ink-2: "#6e6e73"
  ink-3: "#86868b"
  line: "#d2d2d7"
  link: "#0066cc"
  link-hover: "#004f9e"
typography:
  display:
    fontFamily: "Geist, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(3rem, 8.4vw, 6rem)"
    fontWeight: 700
    lineHeight: 1.04
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Geist, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(2.25rem, 5vw, 3.5rem)"
    fontWeight: 700
    lineHeight: 1.07
    letterSpacing: "-0.03em"
  title:
    fontFamily: "Geist, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.6rem, 2.6vw, 2rem)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "-0.025em"
  body:
    fontFamily: "Geist, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.47
  label:
    fontFamily: "Geist, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 400
rounded:
  sm: "6px"
  window: "16px"
  tile: "28px"
  pill: "980px"
spacing:
  xs: "14px"
  sm: "24px"
  md: "48px"
  lg: "72px"
  xl: "128px"
components:
  button-primary:
    backgroundColor: "{colors.link}"
    textColor: "{colors.bg}"
    rounded: "{rounded.pill}"
    padding: "0 22px"
    height: "44px"
  button-primary-hover:
    backgroundColor: "{colors.link-hover}"
    textColor: "{colors.bg}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.link}"
    rounded: "{rounded.pill}"
    padding: "0 22px"
    height: "44px"
  tile:
    backgroundColor: "{colors.bg}"
    rounded: "{rounded.tile}"
    padding: "44px 44px 0"
  window:
    backgroundColor: "{colors.bg}"
    rounded: "{rounded.window}"
---

# Design System: Marwan El Saabi - Portfolio

## Overview

**Creative North Star: "The Product Page"**

The portfolio is presented the way a product launch page presents a product: one idea per section, a headline that states the result, and the real thing shown big. Here the "products" are the projects, and the imagery is always a real screenshot of the live app or a real figure from the project's repo. The layout is generous, light and quiet so the work carries the page.

This replaced an earlier editorial "lab notebook" look (warm paper, serif type, terracotta accent, "Fig. NN" captions). None of that vocabulary carries over.

**Key Characteristics:**
- White and light-gray sections alternating; one blue for links and buttons, nothing else colored.
- One sans family (Geist) for everything, large and tightly tracked for headlines.
- Two-tone headlines: the subject in ink, the claim in gray, inside the same sentence.
- Real screenshots framed as soft-shadowed windows; no illustrations, no fake UI.
- Projects get different compositions by importance: full-width feature, split feature, then a bento of the rest.

## Colors

Neutral grays with a single blue, used only for things you can click.

### Primary
- **Link Blue** (`#0066cc`): every link, the primary pill buttons, the ghost-button outline, focus rings and text selection tint. Hover deepens to `#004f9e`.

### Neutral
- **White** (`#ffffff`): page background and the surface of tiles and screenshot windows.
- **Light Gray** (`#f5f5f7`): alternating section background and the footer.
- **Ink** (`#1d1d1f`): headlines, primary text, the nav name.
- **Gray 2** (`#6e6e73`): body copy, captions, secondary text. Passes AA on both backgrounds.
- **Gray 3** (`#86868b`): the muted half of two-tone headlines and the About statement. Large text only (it is 3.5:1 on white).
- **Hairline** (`#d2d2d7`): dividers in the toolkit and education lists, the footer top border.

### Named Rules
**The Blue Means Click Rule.** Blue appears only on interactive elements. Never use it for emphasis, decoration or headings.

## Typography

**Display, Body and Label Font:** Geist (with Helvetica Neue, Helvetica, Arial fallback)

**Character:** One neutral grotesk at very different sizes and weights. Hierarchy comes from scale and the ink/gray split, not from a second typeface. No monospace anywhere: numbers use tabular figures (`.num`) instead.

### Hierarchy
- **Display** (700, `clamp(3rem, 8.4vw, 6rem)`, line-height 1.04, tracking -0.035em): the hero headline only.
- **Headline** (700, `clamp(2.25rem, 5vw, 3.5rem)`, line-height 1.07, tracking -0.03em): section headlines. In the split feature it drops to `clamp(2rem, 3.4vw, 2.75rem)`.
- **Title** (700, `clamp(1.6rem, 2.6vw, 2rem)`, line-height 1.1): bento tile titles.
- **Statement** (600, `clamp(1.6rem, 3.3vw, 2.5rem)`, line-height 1.22): the About paragraph, gray with key sentences in ink.
- **Body** (400, `17px` to `19px`, line-height 1.47): descriptions, max about 62ch.
- **Label** (400, `12px` to `13px`): nav links, language switch, footer. Never uppercase.

### Named Rules
**The Two-Tone Headline Rule.** A section headline names the thing in ink and states the result in gray, in one sentence ending with a period: "Retail demand forecasting. 4.8% better than the strongest baseline." No eyebrow label above it.

**The No-Em-Dash Rule.** No em dash or en-dash separator in visible text. Ranges use a plain hyphen (`2025-2027`).

## Layout

Content sits in a `1080px` container (`860px` under `1068px`) with `22px` side padding (`16px` on phones). Sections are separated by background change and `128px` vertical padding (`96px` under `834px`, `80px` under `640px`).

Each section uses a different composition, in this order: centered hero with a fanned stack of three screenshots; full-width centered feature (Forecasting); two-column split feature (Drug Designer); a 12-column bento with three tiles of different sizes (RNA-seq 7, Alzheimer's 5, Melanoma 12); a large-type statement (About); three spec columns (Toolkit); a two-column record list (Education); a centered call to action (Contact).

Breakpoints: `1068px` (narrower container), `960px` (nav collapses to the menu; the full nav needs about 830px in Spanish and Galician), `834px` (split, bento and specs go single column), `640px` (phone spacing, smaller hero stack).

## Elevation & Depth

Depth is used only for the screenshot windows: `0 32px 64px -24px rgba(29,29,31,.28), 0 12px 24px -12px rgba(29,29,31,.14)`, an offset soft shadow that makes them read as objects on the page. Tiles and sections are flat; they separate by color, not shadow. The nav uses a translucent white with backdrop blur so content scrolls visibly under it.

### Named Rules
**The Only Windows Float Rule.** Shadows belong to screenshot windows. Do not add shadows to tiles, buttons or text blocks.

## Shapes

Buttons are full pills (`980px` radius). Screenshot windows are `16px`, bento tiles `28px` (`22px` on phones), images inside tiles `14px`. Focus rings are `6px`. The pill is reserved for buttons; nothing else is fully round.

## Components

### Buttons
- **Primary:** blue pill, white 17px medium text, 44px tall. Hover darkens; press scales to 0.98.
- **Ghost:** transparent with a 1px blue inset outline; fills blue on hover. Used for the secondary contact actions.
- **Small:** 30px tall, 13px text; the nav's Download CV.
- **Text link with chevron:** blue text plus a drawn 7x12 chevron that nudges right on hover. Used for "Try the live app", "View the code", "Live app", "Code".

### Screenshot Window
A real screenshot, top-aligned and cropped to 16:10, in a white frame with a 1px hairline border, `16px` radius and the window shadow. Never contains a mock-up drawn in HTML.

### Bento Tile
White on the light-gray section, `28px` radius, `44px` padding on three sides. Title, one paragraph, links, and the image anchored to the bottom edge, which rises 6px on hover. The wide Melanoma tile switches to a side-by-side layout because its figure is a wide strip.

### Navigation
Sticky 52px bar: name on the left, links in the middle, language switch and Download CV on the right. The translucent blur sits on a pseudo-element so the mobile menu (a fixed child) is not trapped inside the bar. At 960px and below, links move into a full-screen white menu with 28px semibold links and a Download CV pill; the language switch stays in the bar.

### Language Switch
- **Languages:** EN (source, in the HTML), ES, GL. Only the languages the owner speaks and can proofread.
- **Style:** three plain 12px buttons (`EN`, `ES`, `GL`), gray at rest, ink and semibold when active. No flags, no dropdown.
- **Behavior:** `?lang=` URL parameter, then the saved choice, then the browser language, then English. `aria-pressed` marks the active button; `<html lang>`, the tab title, meta description and image alt text switch too.
- **Translations:** every new visible string needs a `data-i18n` key with ES and GL strings that follow the same rules as the English (no em dash, real metrics only, official degree names). The paper title, citation and certificate issuer stay in their original language.

## Do's and Don'ts

### Do:
- **Do** state each project's real, verifiable result in its headline.
- **Do** use real screenshots or real repo figures for every image, framed as windows or tile media.
- **Do** keep blue for clickable things only (The Blue Means Click Rule).
- **Do** give a new project a composition that fits its importance instead of copying an existing section.

### Don't:
- **Don't** put an eyebrow or label above a headline; the two-tone headline carries it.
- **Don't** use an em dash or en-dash separator in visible text.
- **Don't** add a second accent color, gradients or gradient text.
- **Don't** add shadows outside screenshot windows.
- **Don't** use monospace for decoration; tabular figures handle numbers.
- **Don't** fill an empty spot with a placeholder or a drawn fake interface; leave it out until there is a real image.
