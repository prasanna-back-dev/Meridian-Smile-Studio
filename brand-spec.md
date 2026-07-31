# Meridian Smile Studio — Brand Specification

## Brand Overview

- **Name:** Meridian Smile Studio
- **Tagline:** Where artistry meets dentistry
- **Business Type:** Premium cosmetic dental practice
- **Location:** 88 Battery St, Suite 500, San Francisco, CA 94111 (Financial District)
- **Founder:** Dr. Elena Cross, DDS
- **Founded:** 2009
- **Positioning:** High-end cosmetic dentistry for discerning patients who want personalized, digitally-planned smile transformations — not a assembly-line dental clinic.

---

## Color Tokens (CSS Custom Properties)

```css
:root {
  --ivory: #F7F3EC;
  --ivory-warm: #F0EBE1;
  --white: #FFFFFF;
  --charcoal: #211E1A;
  --charcoal-soft: #3D3832;
  --muted: #8A8279;
  --muted-light: #B5AFA6;
  --border: #E0D9CE;
  --border-light: #EBE5DA;
  --brass: #A98552;
  --brass-light: #C4A46E;
  --brass-dark: #8A6A3E;
  --surface: #FAF8F5;
  --danger: #B54A4A;
}
```

### Color Rationale

- **Ivory base** (`#F7F3EC`): Warm, not clinical. Avoids the sterile-white dental office feel. Reads as editorial/lifestyle rather than medical.
- **Charcoal text** (`#211E1A`): Near-black with warm brown undertone. Avoids pure black (#000) which causes eye strain and feels harsh.
- **Brass accent** (`#A98552`): Muted gold/brass. Communicates luxury without being flashy. Used at maximum 2x per screen.
- **No navy, no blue**: Differentiates from the sea of blue医疗 branding. The warm palette signals cosmetic/aesthetic rather than medical/clinical.

---

## Typography Tokens

```css
:root {
  --font-display: 'Fraunces', Georgia, serif;
  --font-body: 'Work Sans', -apple-system, BlinkMacSystemFont, sans-serif;
}
```

### Font Rationale

- **Fraunces** (display): Variable optical size serif with soft terminals. More distinctive than Playfair Display (now overused in AI-generated designs). The "friendly premium" feel matches a dental practice better than sharp modern serifs.
- **Work Sans** (body): Geometric sans with humanist touches. Cleaner than Inter (overused) but warmer than system fonts. Excellent readability at body sizes.

### Google Fonts Link

```html
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&family=Work+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
```

---

## Logo

### Mark
- Single letter "M" in Fraunces serif, brass color, inside a thin brass circle
- Used as: favicon, social avatar, header mark

### Wordmark
- "Meridian Smile Studio" in Fraunces, charcoal color
- "Financial District, SF" subtitle in Work Sans, muted, uppercase, tracked

### Files
- `logo.svg` — Vector mark (M in circle)
- `logo.png` — Raster version (placeholder, needs designer to create proper PNG)

---

## Voice & Tone

### Brand Personality (3 adjectives)
1. **Precise** — We plan digitally, execute by hand, measure twice
2. **Warm** — We're not a clinical assembly line; every patient is known by name
3. **Confident** — We don't oversell; our work speaks for itself

### Voice Chart

| We are | We are not |
|--------|------------|
| Direct and specific | Vague or filler-heavy |
| Warm but professional | Cold or clinical |
| Confident in our expertise | Arrogant or dismissive |
| Patient and explanatory | Condescending |
| Honest about what's possible | Making promises we can't keep |

### Writing Rules

- Use real numbers when available ($1,200/tooth, 15 years, 4,000+ veneers)
- Avoid: "seamless," "innovative," "cutting-edge," "industry-leading," "leverage," "synergy," "holistic," "passionate," "dedicated to excellence"
- Limit em dashes to 1–2 per page
- Headlines should pass the competitor swap test (if you swap "Meridian" for a competitor name, the copy should break)
- Use patient-first language: "your smile" not "our services"

---

## Layout Posture Rules

1. **Warm backgrounds only.** Ivory (`#F7F3EC`) and warm white (`#FAF8F5`). Never pure white (`#FFFFFF`) as page background. Never cool grey.
2. **Asymmetric layouts.** Break the 3-column grid intentionally. Use `1fr 1.3fr` and `1.2fr 1fr` splits.
3. **Generous whitespace.** Sections breathe. No cramped layouts. Minimum `4rem` vertical section padding.
4. **Editorial rhythm.** Alternate section backgrounds (ivory → warm → white → charcoal). No two adjacent sections with the same background.
5. **One accent, used twice.** Brass appears at most 2 times per visible screen. One eyebrow + one CTA is the standard pair.
6. **Borders over shadows.** Cards use `1px` borders, not drop shadows. Shadows only on hover.
7. **Sharp corners.** Buttons and inputs use `4px` radius. Cards use `14px` max. No pill-shaped elements.

---

## Photography Direction

### When Real Photos Are Available

- **Color grading:** Warm, editorial lighting. Avoid clinical white-background headshots.
- **Subject:** Dr. Cross in the treatment room, candid patient interactions, the studio space itself.
- **Style:** Kinfolk/Monocle editorial. Not stock-photo perfect. Natural light preferred.
- **Treatment room:** Show the space as designed — warm, not clinical.

### Placeholder Strategy (Current)

- Labeled grey blocks with italic description text
- SVG image icons for placeholder frames
- Replace with real photography before launch

---

## Accessibility Requirements

- WCAG 2.1 AA compliance minimum
- All colors meet 4.5:1 contrast ratio for body text
- All interactive elements have visible focus indicators (brass outline)
- Skip navigation link on every page
- ARIA landmarks on all sections
- Form labels associated with inputs
- Reduced motion support via `prefers-reduced-motion`

---

## Technical Constraints

- **Single-page scroll** for primary site (index.html)
- **Blog** as separate page (blog.html)
- **Self-contained HTML** with inline CSS (no external stylesheets except Google Fonts)
- **No JavaScript frameworks** — vanilla JS only
- **Vercel deployment** — static hosting, no server-side rendering
- **Performance target:** Lighthouse > 90 on all metrics
