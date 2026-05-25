# DESIGN.md — Novaspand

<!-- SEED: No code exists yet. This file was written from strategic brief. Re-run /impeccable document (without --seed) once tokens are implemented in code. -->

## 01 Overview

**Creative North Star: "The Considered Studio."**

Warm off-white space. Grounded serif headlines. A single terracotta accent that arrives rarely and lands every time. The site feels like a well-made physical object — like opening a book from a publisher that takes quality seriously. Nothing decorates. Everything communicates.

Motion is slow and intentional. Elements reveal with weight, not bounce. The overall register is editorial authority meeting technical precision.

## 02 Colors

| Token | Value | Description |
|---|---|---|
| `--color-bg` | `#FAF7F4` | Warm off-white, linen-like. Never pure white. |
| `--color-surface` | `#F3EFE9` | Slightly deeper warm white for subtle section separation |
| `--color-text-primary` | `#1C1A18` | Deep warm charcoal. Never pure black. |
| `--color-text-secondary` | `#6B6560` | Muted warm grey for supporting copy |
| `--color-text-tertiary` | `#A09890` | Captions, labels, metadata |
| `--color-accent` | `#C4622D` | Terracotta / burnt orange. The signature. Used sparingly. |
| `--color-accent-light` | `#E8845A` | Lighter terracotta for hover states only |
| `--color-border` | `#E2DBD3` | Warm grey-beige for dividers and borders |
| `--color-border-strong` | `#C8BFB5` | Stronger border for emphasis |

**Color rules:**
- The accent appears on: one word or phrase in the hero, active nav state, links on hover, one deliberate moment per section. Never as background fills.
- Never use accent for large blocks of color.
- Never use cool greys — all neutrals tint warm.
- Never gradient the accent color.

## 03 Typography

**Display / Headlines:** Libre Baskerville (serif)
**Body / UI:** Mulish (sans-serif)

| Role | Font | Weight | Size | Line Height |
|---|---|---|---|---|
| Hero headline | Libre Baskerville | 700 | clamp(56px, 8vw, 120px) | 1.0 |
| Section title | Libre Baskerville | 700 | clamp(36px, 5vw, 72px) | 1.1 |
| Subheading | Libre Baskerville | 400 italic | 24–32px | 1.3 |
| Body | Mulish | 400 | 16–18px | 1.75 |
| Body strong | Mulish | 600 | 16–18px | 1.75 |
| Label / eyebrow | Mulish | 600 | 11px | 1.5 |
| Caption | Mulish | 400 | 13px | 1.6 |

**Typography rules:**
- Eyebrow labels: ALL CAPS, letter-spacing: 0.12em, color: `--color-text-tertiary`
- Headlines lead. Body supports. Never compete.
- Serif headlines may use italic weight for emphasis phrases — used once per section maximum.
- Never use Libre Baskerville for body copy. Never use Mulish for hero headlines.
- Line length: body copy max 68 characters. Never full-width.

## 04 Elevation

Flat by default. This is a light, editorial surface — shadows are rare and intentional.

- **Level 0:** No shadow. Default state for all elements.
- **Level 1:** `0 1px 3px rgba(28,26,24,0.06)` — cards on hover only
- **Level 2:** `0 4px 16px rgba(28,26,24,0.08)` — modals, dropdowns if needed

**Rules:**
- No decorative shadows.
- Shadow only appears as a response to interaction state (hover, focus, active).
- Never stack shadows.
- Borders (`--color-border`) do the separation work that shadows would do elsewhere.

## 05 Components

**Navigation**
- Transparent background on scroll-top, `--color-bg` with bottom border on scroll
- Logo: Libre Baskerville, tracking loose
- Links: Mulish, 11px, ALL CAPS, letter-spacing 0.1em, `--color-text-secondary`
- Active/hover: `--color-text-primary`, underline via border-bottom not text-decoration
- CTA button: outlined, `--color-text-primary` border and text, fills to `--color-accent` on hover

**Hero**
- Full viewport height
- Headline: Libre Baskerville 700, large, one or two lines maximum
- One word or short phrase in `--color-accent` — not the whole headline
- Supporting line: Mulish, 18px, `--color-text-secondary`, max-width 520px
- Single CTA, no secondary button competing with it
- No illustration, no background image, no hero graphic — the type IS the hero

**Section Eyebrows**
- Pattern: `// 01 — label text`
- Mulish, 11px, ALL CAPS, `--color-text-tertiary`, letter-spacing 0.12em
- Always above the section headline, never below

**Cards / Work Items**
- Border: 1px `--color-border`
- Background: `--color-bg` or `--color-surface`
- No border-radius or very subtle (2px max) — square feels more considered
- Hover: border upgrades to `--color-border-strong`, shadow Level 1 appears
- No gradient overlays on cards

**Dividers**
- Horizontal rules: 1px `--color-border`, full width
- Use sparingly — space alone should separate sections when possible

**Buttons**
- Primary: `--color-accent` background, white text, no border-radius
- Ghost: transparent, `--color-border-strong` border, `--color-text-primary` text
- No rounded pill buttons — square or very subtle radius only
- Hover transitions: 200ms ease

**Links**
- Body links: `--color-text-primary`, underline on hover only
- Never use blue for links — the accent terracotta serves this role

## 06 Do's and Don'ts

**Do:**
- Let whitespace do the separation work before reaching for dividers
- Use Libre Baskerville italic for one meaningful phrase per section
- Keep the terracotta accent to 1–2 moments per section — scarcity is the point
- Use ALL CAPS Mulish labels to create hierarchy without size
- Keep body copy lines under 68 characters
- Square corners everywhere — the geometry is part of the identity
- Slow transitions (300–500ms) for reveals, 200ms for interactions

**Don't:**
- Never use pure white (`#FFFFFF`) or pure black (`#000000`)
- Never gradient the accent color or use it as a large background fill
- Never use border-radius greater than 2px on structural elements
- Never animate more than one thing at a time on page load
- Never put two competing CTAs side by side
- Never use stock imagery or generic tech illustrations
- Never fill a section with decorative elements — empty space is intentional
- Never use the accent color on more than one element in the same visual cluster
- Never use Inter, Roboto, or system fonts
- Never glassmorphism, never frosted backgrounds
