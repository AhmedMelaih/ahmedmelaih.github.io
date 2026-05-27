---
meta:
  version: "1.0.0"
  author: "Ahmed Melaih"
  url: "https://ahmedmelaih.github.io"
  description: "Design tokens and visual identity for Ahmed Melaih's portfolio"

colors:
  navy:          "#0a192f"
  navy-light:    "#112240"
  navy-lighter:  "#1d3461"
  navy-hover:    "#152a4a"
  slate:         "#8892b0"
  slate-light:   "#a8b2d8"
  slate-lighter: "#ccd6f6"
  white:         "#e6f1ff"
  teal:          "#64ffda"
  teal-bg:       "rgba(100,255,218,0.08)"
  teal-bg-hover: "rgba(100,255,218,0.15)"
  teal-border:   "rgba(100,255,218,0.2)"
  overlay:       "rgba(2,12,27,0.75)"
  card-border:   "rgba(255,255,255,0.06)"
  divider:       "rgba(255,255,255,0.04)"

typography:
  sans:
    fontFamily: "'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    weights: [400, 500, 600, 700]
    source: "https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700"
  mono:
    fontFamily: "'JetBrains Mono', 'Courier New', monospace"
    weights: [400, 500]
    source: "https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500"
  scale:
    2xs:  { value: "0.67rem", usage: "dates, labels, tag text" }
    xs:   { value: "0.7rem",  usage: "badges, nav links, section titles, metrics" }
    sm:   { value: "0.75rem", usage: "company names, school names" }
    base: { value: "0.82rem", usage: "tagline, small body copy" }
    md:   { value: "0.875rem", usage: "project descriptions, timeline bullets" }
    lg:   { value: "0.95rem", usage: "about body, roles, degree names" }
    xl:   { value: "0.975rem", usage: "project titles" }
    2xl:  { value: "1.1rem",  usage: "social icons" }
    3xl:  { value: "1.3rem",  usage: "hamburger icon" }
    4xl:  { value: "1.6rem",  usage: "sidebar name heading" }
    5xl:  { value: "1.75rem", usage: "project icon" }

dimensions:
  sidebar-mobile:       "280px"
  sidebar-desktop:      "300px"
  sidebar-wide:         "340px"
  mob-header-height:    "56px"
  avatar-size:          "72px"
  nav-bar-default:      "28px"
  nav-bar-active:       "48px"
  section-padding:      "2.5rem 0"
  card-radius:          "6px"
  item-radius:          "5px"
  badge-radius:         "3px"
  max-content-width:    "740px"
  max-page-width:       "1300px"

animation:
  ease:          "cubic-bezier(0.4, 0, 0.2, 1)"
  fast:          "0.15s"
  base:          "0.2s"
  medium:        "0.22s"
  slow:          "0.28s"
  reveal:        "0.5s"

breakpoints:
  tablet: "768px"
  desktop: "1100px"

components:
  avatar:
    size:         "{dimensions.avatar-size}"
    borderRadius: "50%"
    border:       "2px solid {colors.teal}"
    objectFit:    "cover"
    objectPosition: "top center"

  badge:
    fontFamily:   "{typography.mono}"
    fontSize:     "{typography.scale.xs}"
    color:        "{colors.teal}"
    background:   "{colors.teal-bg}"
    border:       "1px solid {colors.teal-border}"
    borderRadius: "{dimensions.badge-radius}"
    padding:      "3px 10px"
    hoverBg:      "{colors.teal-bg-hover}"
    hoverBorder:  "{colors.teal}"

  proj-card:
    background:   "{colors.navy-light}"
    border:       "1px solid {colors.card-border}"
    borderRadius: "{dimensions.card-radius}"
    padding:      "1.5rem"
    hoverTranslate: "translateY(-4px)"
    hoverShadow:  "0 16px 36px rgba(2,12,27,0.6)"
    hoverBorder:  "rgba(100,255,218,0.35)"
    hoverBg:      "{colors.navy-hover}"

  timeline-item:
    padding:      "1.1rem"
    borderRadius: "{dimensions.item-radius}"
    hoverBg:      "{colors.navy-light}"

  nav-link:
    fontFamily:   "{typography.mono}"
    fontSize:     "{typography.scale.xs}"
    fontWeight:   500
    letterSpacing: "0.12em"
    textTransform: "uppercase"
    color:        "{colors.slate}"
    activeColor:  "{colors.teal}"

  section-title:
    fontFamily:   "{typography.mono}"
    fontSize:     "{typography.scale.xs}"
    fontWeight:   600
    letterSpacing: "0.15em"
    textTransform: "uppercase"
    color:        "{colors.teal}"
    marginBottom: "1.75rem"

  metric:
    fontFamily:   "{typography.mono}"
    fontSize:     "{typography.scale.xs}"
    color:        "{colors.slate-light}"
    background:   "rgba(255,255,255,0.04)"
    border:       "1px solid rgba(255,255,255,0.07)"
    borderRadius: "{dimensions.badge-radius}"
    padding:      "2px 8px"
    strongColor:  "{colors.teal}"

  tag:
    fontFamily:   "{typography.mono}"
    fontSize:     "0.68rem"
    color:        "{colors.slate}"
    prefix:       "#"
    prefixColor:  "{colors.teal}"
---

## Overview

Ahmed Melaih's portfolio is a dark-themed, single-page application targeting Data Scientists and hiring managers in the MENA region. The design is inspired by Brittany Chiang's reference portfolio — restrained, developer-aesthetic, and navigation-first.

The visual language prioritizes **legibility at a glance**: teal accent on a deep navy background creates maximum contrast without harshness. The monospace font anchors technical credibility; Inter handles body copy with warmth.

## Colors

The palette has three layers:

1. **Background stack** — Three navy shades (`#0a192f`, `#112240`, `#1d3461`) create subtle depth without imagery. Cards lift one shade; hover states lift two.
2. **Text stack** — Three slate tones (`#8892b0`, `#a8b2d8`, `#ccd6f6`) plus near-white (`#e6f1ff`) map to hierarchy: metadata → body → label → heading.
3. **Accent** — A single teal (`#64ffda`) carries every interactive affordance: active nav, badge borders, icon color, link color, tag prefixes. Never use teal for large fill areas; keep it as a signal color only.

Teal transparency at 8% (`rgba(100,255,218,0.08)`) is the correct background for non-hovered badges and resume buttons. Jump to 15% on hover, never higher.

## Typography

Two families only, no exceptions:

- **Inter** (sans) — headings, body, roles, about text.
- **JetBrains Mono** (mono) — nav labels, section titles, badge text, dates, tag text, metrics, footer. Anything that feels "terminal" or "label-like" uses mono.

Letter-spacing on mono items: `0.12em` for nav links, `0.15em` for section titles, `0.06em` for dates. Do not apply letter-spacing to body copy.

Line-height is `1.6` for the document root, `1.75–1.8` for body paragraphs, `1.35` for card titles, `1.15` for the sidebar name heading.

## Layout

Two-column layout above 768px: **fixed-width sidebar** (300px → 340px at 1100px) + **fluid main content** capped at 740px. The sidebar is `position: sticky; height: 100vh` — it never scrolls.

Below 768px, the sidebar collapses off-screen and slides in via a hamburger menu fixed at 56px height. A semi-transparent overlay (`rgba(2,12,27,0.75)`) dims the content when the drawer is open.

Main content padding: `5.5rem 4rem 5rem 3.5rem` (desktop), `68px 1.25rem 3rem` (mobile). The extra top padding accounts for the mobile header.

Sections are separated by `1px solid rgba(255,255,255,0.04)` dividers, not spacing alone. The last section has no border.

## Elevation & Depth

Three elevation levels:

| Level | Use | CSS |
|-------|-----|-----|
| 0 | Page background | `#0a192f` |
| 1 | Cards, hovered timeline items | `#112240` |
| 2 | Card hover state | `#152a4a` |

Shadows are used only on card hover: `0 16px 36px rgba(2,12,27,0.6)`. No box-shadows at rest — elevation is expressed through color, not shadow.

The sidebar has a right border `1px solid rgba(255,255,255,0.05)` to subtly separate it from the main column without a hard edge.

## Shapes

Corners are deliberately minimal:
- **Project cards**: `6px`
- **Timeline / education items**: `5px`
- **Badges, metrics, tags**: `3px`
- **Avatar**: `50%` (circle)
- **Resume button**: `3px`

Avoid larger radii — they soften the technical aesthetic.

## Components

### Navigation Links

Each nav link has an animated horizontal bar (`<span class="nav-bar">`). At rest the bar is 28px wide; on hover/active it expands to 48px. The bar uses `currentColor` so it matches the link's text color automatically. Active links are teal; the link text and bar animate together.

Active state is driven by IntersectionObserver, not scroll position math. The observer uses `rootMargin: '-25% 0px -65% 0px'` to fire when the section is well into view.

### Badges

Badges are non-interactive labels. They show teal text on a near-transparent teal background with a teal border. Do not make them clickable unless they link somewhere meaningful. The hover state darkens the background to 15% — a soft affordance that signals interactivity only where it exists.

### Project Cards

Cards use a three-part structure: header row (icon + GitHub link), title + description, then metrics row + tag row. Metrics use a pill with a neutral background; tags use `#prefix` styling with no background. On hover the card lifts `4px`, gains a teal-tinted border, and picks up a deep shadow.

Icon is Font Awesome at `1.75rem`; GitHub link icon is `1.1rem`. Both use teal coloring; the GitHub link starts slate and transitions to teal on hover.

### Timeline Items

Full-bleed hover background (`border-radius: 5px`) with no border. The role text transitions to teal on item hover. Bullet points use `list-style: none` with `padding-left: 1rem` for alignment. Bold text inside bullets uses `slate-lighter`, not white or teal.

### Reveal Animation

Every section carries the class `reveal` (opacity 0, translateY 16px). An IntersectionObserver with `threshold: 0.07` adds class `in` on entry, which transitions to opacity 1 / translateY 0 over 500ms with the global ease curve. The observer unobserves after first reveal — animations do not repeat.

## Do's and Don'ts

**Do:**
- Use teal exclusively as an accent/signal color — never for large surfaces.
- Keep mono typography for all labels, metadata, and technical strings.
- Maintain the three-shade navy stack for depth; never use pure black or pure white.
- Animate the nav bar width on hover/active; it is a key identity element.
- Apply `scroll-margin-top` to sections to account for fixed headers (72px mobile, 100px desktop).

**Don't:**
- Add a third typeface. Inter + JetBrains Mono is the complete set.
- Use rounded corners larger than 6px — it breaks the technical aesthetic.
- Add drop shadows at rest state; shadows are hover-only on cards.
- Replace the teal accent with any other hue.
- Skip the `backdrop-filter: blur(10px)` on the mobile header — it is a key polish detail.
- Use `position: fixed` for the sidebar on desktop — it must be `sticky` so it stays within the grid column.
