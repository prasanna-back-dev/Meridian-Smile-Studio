# Meridian Smile Studio — Project Overview

## Project Summary

A premium cosmetic dental practice website for Meridian Smile Studio, San Francisco. Designed for portfolio presentation with emphasis on anti-AI-slop design principles, content depth, and technical rigor.

---

## Business Information

| Field | Value |
|-------|-------|
| Business Name | Meridian Smile Studio |
| Owner | Dr. Elena Cross, DDS |
| Phone | (415) 555-0142 |
| Email | hello@meridiansmilestudio.com |
| Address | 88 Battery St, Suite 500, San Francisco, CA 94111 |
| Website | https://meridiansmilestudio.com |
| Business Type | Cosmetic dental practice |
| Specialties | Porcelain veneers, Invisalign, full smile makeovers |

---

## Deliverables

### Website Files

| File | Purpose |
|------|---------|
| `index.html` | Homepage — single-page scroll with all sections |
| `blog.html` | Blog listing page with 3 sample posts |
| `404.html` | Custom branded 404 error page |
| `logo.svg` | Vector logo mark (M in circle) |

### Deployment

| File | Purpose |
|------|---------|
| `vercel.json` | Vercel deployment config (headers, clean URLs, caching) |
| `sitemap.xml` | XML sitemap for search engines |
| `robots.txt` | Crawl rules for search engines |

### SEO Documentation

| File | Purpose |
|------|---------|
| `meta-tags.md` | All meta tags for every page |
| `schema-markup.md` | Structured data documentation |
| `seo-strategy.md` | Complete SEO strategy |
| `local-seo.md` | Local SEO strategy (Google Business Profile, citations, reviews) |
| `technical-seo.md` | Technical SEO checklist |
| `keyword-research.md` | Target keywords with volume and difficulty |

### Brand & Design

| File | Purpose |
|------|---------|
| `DESIGN.md` | Design system documentation (colors, typography, components) |
| `brand-spec.md` | Brand tokens, voice, and guidelines |

### Research & Strategy

| File | Purpose |
|------|---------|
| `competitor-analysis.md` | SF cosmetic dentistry competitor landscape |
| `persona-sarah.md` | Buyer persona: Sarah Chen (34, tech PM) |
| `persona-michael.md` | Buyer persona: Michael Torres (47, finance MD) |
| `persona-jennifer.md` | Buyer persona: Jennifer Park (28, UX designer) |
| `content-strategy.md` | Content pillars, calendar, and distribution |
| `analytics-setup.md` | Google Analytics 4 setup guide |
| `conversion-tracking.md` | Conversion events and tracking implementation |
| `search-console.md` | Google Search Console setup guide |

### Client Handover

| File | Purpose |
|------|---------|
| `LAUNCH-CHECKLIST.md` | Pre-launch verification steps |
| `POST-LAUNCH.md` | First 30 days after launch |
| `MAINTENANCE-GUIDE.md` | Ongoing site maintenance |
| `ADMIN-GUIDE.md` | How to update content |
| `CONTACT-SUPPORT.md` | Support contact information |

### Internal Project Files

| File | Purpose |
|------|---------|
| `phase9-launch.md` | Launch phase documentation |
| `phase10-post-launch.md` | Post-launch phase plan |
| `post-sale-checklist.md` | 30/60/90 day post-sale plan |
| `case-study-template.md` | Portfolio case study template |
| `technical-audit.md` | Pre-project technical audit |
| `performance-report.md` | Performance testing results |
| `accessibility-report.md` | Accessibility audit results |
| `security-report.md` | Security audit results |

---

## Design Decisions

### Typography
- **Display:** Fraunces (variable optical serif) — premium, editorial, less flagged as AI output than Playfair Display
- **Body:** Work Sans — clean, humanist sans, more distinctive than Inter/System UI

### Color Palette
- **Background:** Warm ivory (#F7F3EC) — avoids clinical white, feels editorial
- **Text:** Warm charcoal (#211E1A) — near-black with warm undertone
- **Accent:** Muted brass (#A98552) — luxury without flash, used max 2x per screen

### Layout
- Single-page scroll for primary site (no page-load friction)
- Asymmetric grids to break the "AI 3-column" tell
- Pull-quote and full-bleed photo section for rhythm variation
- Warm editorial aesthetic throughout

### Anti-AI-Slop Measures
- No purple/violet gradients
- No emoji feature icons (1.5px stroke SVG instead)
- No floating stat bars with generic numbers
- Real credentials (AACD, Kois Center, Invisalign Premier)
- Transparent pricing ($1,200/tooth)
- Copy passes the competitor swap test

---

## Technical Stack

| Component | Technology |
|-----------|-----------|
| HTML | Semantic HTML5 |
| CSS | Custom properties, fluid typography (clamp), Grid, Flexbox |
| JavaScript | Vanilla JS (no frameworks) |
| Fonts | Google Fonts (Fraunces + Work Sans) |
| Hosting | Vercel (static) |
| Analytics | Google Analytics 4 |
| SEO | Schema.org structured data, meta tags, sitemap |

---

## Performance Targets

| Metric | Target |
|--------|--------|
| Lighthouse Performance | > 90 |
| Lighthouse Accessibility | > 90 |
| Lighthouse Best Practices | > 90 |
| Lighthouse SEO | > 90 |
| LCP | < 2.5s |
| CLS | < 0.1 |
| TBT | < 200ms |

---

## File Count

| Category | Count |
|----------|-------|
| Website files (HTML) | 3 |
| Deployment/SEO files | 3 |
| Brand/design docs | 2 |
| Research files | 5 |
| SEO docs | 6 |
| Client handover docs | 5 |
| Internal project docs | 8 |
| **Total** | **32** |

---

## How to Run Locally

This is a static site. No build step required.

1. Open `index.html` in a browser
2. Or use a local server:
   ```bash
   npx serve .
   # or
   python -m http.server 8000
   ```

---

## How to Deploy

1. Push to a Git repository (GitHub, GitLab, Bitbucket)
2. Connect the repository to Vercel
3. Vercel auto-deploys on push
4. Custom domain: configure DNS to point to Vercel

---

## Portfolio Note

This project is a **concept design for portfolio purposes**. Meridian Smile Studio is a fictional practice. All business details, testimonials, and patient stories are invented. A "Concept design for portfolio purposes" label is displayed in the bottom-left corner of the site.
