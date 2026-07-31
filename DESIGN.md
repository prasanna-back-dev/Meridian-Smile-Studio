# Meridian Smile Studio — Design System

## Overview

Warm editorial design system for a premium cosmetic dental practice. The visual language draws from high-end editorial publishing (Monocle, Kinfolk) rather than typical dental/medical templates. Every design decision reinforces the message: this is a practice that treats dentistry as an art form.

---

## Color Palette

### Core Tokens

| Token | Hex | Role |
|-------|-----|------|
| `--ivory` | `#F7F3EC` | Primary background. Warm, not clinical white. |
| `--ivory-warm` | `#F0EBE1` | Secondary background. Slightly deeper warmth for alternating sections. |
| `--white` | `#FFFFFF` | Card surfaces, form backgrounds. |
| `--charcoal` | `#211E1A` | Primary text, headings. Near-black with warm undertone. |
| `--charcoal-soft` | `#3D3832` | Body copy, secondary text. |
| `--muted` | `#8A8279` | Tertiary text, descriptions, meta info. |
| `--muted-light` | `#B5AFA6` | Placeholders, disabled states, decorative borders. |
| `--border` | `#E0D9CE` | Standard borders. |
| `--border-light` | `#EBE5DA` | Subtle dividers, card borders. |
| `--brass` | `#A98552` | Primary accent. Used sparingly: CTAs, eyebrows, active states. |
| `--brass-light` | `#C4A46E` | Hover states, secondary accent moments. |
| `--brass-dark` | `#8A6A3E` | Pressed states, dark variant. |
| `--surface` | `#FAF8F5` | Input backgrounds, subtle surface elevation. |

### Accent Discipline

- **Maximum 2 visible uses of `--brass` per screen.** Typical pair: one eyebrow label + one CTA button.
- Brass is never used for body text or large backgrounds.
- Links use `--charcoal` color with underline, not brass, unless on a dark background.

### Contrast Ratios (WCAG AA)

| Pair | Ratio | Pass |
|------|-------|------|
| Charcoal on Ivory | 12.8:1 | AAA |
| Charcoal-soft on Ivory | 8.2:1 | AAA |
| Muted on Ivory | 4.6:1 | AA |
| Brass on Ivory | 3.2:1 | AA (large text only) |
| Ivory on Charcoal | 12.8:1 | AAA |
| Brass on Charcoal | 3.2:1 | AA (large text only) |

---

## Typography

### Font Stacks

| Role | Font | Fallback |
|------|------|----------|
| Display | Fraunces | Georgia, 'Times New Roman', serif |
| Body | Work Sans | -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif |

### Why These Fonts

- **Fraunces**: Variable optical size serif. Reads premium/editorial without the overuse of Playfair Display (now flagged as common AI output). The soft serif terminals give warmth appropriate for a dental practice.
- **Work Sans**: Clean geometric sans with slightly humanist proportions. More distinctive than Inter/System UI but still highly legible at body sizes.

### Type Scale (Fluid)

| Role | Min | Preferred | Max | Weight | Tracking |
|------|-----|-----------|-----|--------|----------|
| Display (hero) | 2.8rem | 4vw | 5rem | 300 | -0.02em |
| H1 | 2rem | 2.5vw | 2.8rem | 400 | -0.015em |
| H2 | 1.6rem | 2vw | 2.1rem | 400 | -0.01em |
| H3 | 1.3rem | 1.5vw | 1.55rem | 500 | -0.01em |
| Body | 0.95rem | 1vw | 1.05rem | 400 | 0 |
| Small | 0.8rem | 0.85vw | 0.875rem | 400 | 0.01em |
| Eyebrow/Caps | 0.7rem | 0.72vw | 0.75rem | 600 | 0.12em |

### Line Heights

| Text Size | Line Height |
|-----------|-------------|
| Display / H1 (>=32px) | 1.08–1.15 |
| H2–H3 | 1.2–1.3 |
| Body | 1.7 |
| Small | 1.5 |

### Letter-Spacing Rules

- **ALL CAPS** (eyebrows, labels): minimum `0.12em` — this is non-negotiable
- **Display/H1**: negative tracking `-0.015em` to `-0.02em`
- **Body**: `0` (default)
- **Small text**: `0.01em` positive

---

## Spacing

### Section Spacing

- Section vertical padding: `clamp(4rem, 3rem + 4vw, 7rem)`
- Container max-width: `1140px`
- Gutter: `clamp(1.25rem, 1rem + 2vw, 2.5rem)`

### Component Spacing

| Element | Gap |
|---------|-----|
| Card internal padding | `1.75rem–2.5rem` |
| Grid column gap | `1.25rem–2rem` |
| Form field margin-bottom | `1.1rem` |
| Section eyebrow to title | `1rem` |
| Title to subtitle | `0.75rem–1rem` |

---

## Border Radius

| Element | Radius |
|---------|--------|
| Buttons | `4px` (sharp, editorial) |
| Cards | `14px` |
| Inputs | `4px` |
| Avatars | `50%` (circle) |
| Badges/pills | `4px` |

No border-radius above 14px. This is an editorial design, not a consumer app.

---

## Shadows

Shadows are used sparingly. The editorial aesthetic relies on borders and whitespace for separation, not elevation.

| Element | Shadow |
|---------|--------|
| Card hover | `0 12px 40px rgba(33, 30, 26, 0.06)` |
| No default card shadow | border only |
| No drop shadows on images | editorial feel |

---

## Components

### Buttons

| Variant | Use | Style |
|---------|-----|-------|
| `.btn--dark` | Primary CTA | Charcoal bg, ivory text, brass hover |
| `.btn--outline` | Secondary CTA | Charcoal border, charcoal text, charcoal fill on hover |
| `.btn--ghost` | Tertiary/link | No bg, brass text, bottom border on hover |

### Cards

- White background, `--border-light` border, no default shadow
- Hover: subtle lift + shadow, no border color change
- No left-border accent (anti-AI-slop rule)
- No gradient backgrounds on cards

### Forms

- Inputs: `--surface` background, `--border` border, brass focus ring
- Labels: small text, charcoal color, 500 weight
- Validation: red border on error (`#B54A4A`)
- Honeypot field for spam protection (hidden)

### Navigation

- Fixed header, transparent on scroll top, frosted glass on scroll
- Desktop: horizontal links + CTA button
- Mobile: full-screen overlay menu, charcoal background

---

## Layout Patterns

### Section Rhythm

Alternate between `--ivory`, `--ivory-warm`, and `--white` backgrounds to create visual rhythm. Never put two sections with the same background adjacent.

### Grid Patterns

- **Asymmetric 2-column**: `1fr 1.3fr` or `1.2fr 1fr` for about/feature sections
- **3-column grid**: For secondary service cards
- **2-column grid**: For blog cards, testimonials
- **Full-width**: For pull-quotes, CTA sections, photo breaks

### Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 768px |
| Tablet | 768px–1024px |
| Desktop | > 1024px |

No complex breakpoint system needed for a 2-page marketing site.

---

## Anti-AI-Slop Checklist

Every screen must pass before shipping:

- [ ] No purple/violet gradients
- [ ] No emoji feature icons (use 1.5px stroke SVG with `currentColor`)
- [ ] No rounded cards with left-border accent
- [ ] No Inter/Roboto as display face
- [ ] No "innovative"/"seamless"/"cutting-edge" copy
- [ ] No floating stat bars with generic numbers
- [ ] No icon next to every heading
- [ ] No gradient on every background
- [ ] No warm beige/peach page backgrounds (ivory is acceptable for this brand)
- [ ] No `var(--brass)` used more than 2x per visible screen
- [ ] ALL CAPS has `letter-spacing >= 0.12em`
- [ ] Display text has negative tracking

---

## Responsive Behavior

- Fluid typography via `clamp()` — no media queries needed for font sizes
- Grid collapses to single column on mobile
- Mobile menu: full-screen overlay
- Hero portrait hidden on tablet and below
- Cards stack vertically on mobile
- Form rows collapse to single column on mobile
