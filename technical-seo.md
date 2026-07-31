# Meridian Smile Studio — Technical SEO Checklist

## Pre-Launch Technical SEO

### Crawlability

- [x] `robots.txt` exists and allows crawling of all public pages
- [x] `sitemap.xml` exists, is valid XML, and includes all public URLs
- [x] Sitemap is submitted in Google Search Console
- [x] No `noindex` tags on public pages (except 404.html)
- [x] No orphan pages (every page linked from at least one other page)
- [x] Clean URL structure (no query parameters, no session IDs)

### Indexability

- [x] Each page has a unique, descriptive `<title>` tag (50–60 characters)
- [x] Each page has a unique meta description (150–160 characters)
- [x] One `<h1>` per page, includes primary keyword
- [x] Heading hierarchy is logical (H1 → H2 → H3, no skipping levels)
- [x] Canonical tags on all pages pointing to self
- [x] No duplicate content between pages

### Mobile

- [x] Responsive design works at 360px, 390px, 430px, 768px, 1024px, 1440px
- [x] No horizontal scroll at any viewport
- [x] Touch targets minimum 44x44px
- [x] Viewport meta tag present: `<meta name="viewport" content="width=device-width, initial-scale=1">`
- [x] No Flash, no Java applets
- [x] Font sizes readable without zooming (minimum 16px body)

### Performance

- [x] First Contentful Paint (FCP) < 1.8s
- [x] Largest Contentful Paint (LCP) < 2.5s
- [x] Cumulative Layout Shift (CLS) < 0.1
- [x] Total Blocking Time (TBT) < 200ms
- [x] Lighthouse Performance score > 90
- [x] Images optimized (WebP where possible, lazy loading for below-fold)
- [x] Fonts loaded with `font-display: swap`
- [x] CSS inlined (no render-blocking external stylesheet)
- [x] JavaScript deferred/async
- [x] No console errors

### Security

- [x] HTTPS enforced (Vercel default)
- [x] No mixed content (all resources loaded over HTTPS)
- [x] Security headers configured (see vercel.json):
  - `X-Content-Type-Options: nosniff`
  - `X-Frame-Options: DENY`
  - `X-XSS-Protection: 1; mode=block`
  - `Referrer-Policy: strict-origin-when-cross-origin`
  - `Permissions-Policy: camera=(), microphone=(), geolocation=()`

### Structured Data

- [x] Dentist schema on homepage
- [x] Schema validates via Google Rich Results Test
- [x] No schema errors in Google Search Console

### Internal Linking

- [x] Homepage links to all key sections (services, about, gallery, process, contact)
- [x] Blog links back to homepage services
- [x] Navigation links to all pages
- [x] Footer links to all pages
- [x] No broken internal links

### Image Optimization

- [x] All images have descriptive `alt` text
- [x] Images use appropriate file formats (SVG for icons, WebP/AVIF for photos when available)
- [x] No images larger than 200KB (for current placeholder states)
- [x] Images sized appropriately for their display context

---

## Post-Launch Monitoring (Weekly)

| Check | Tool | Action if Failed |
|-------|------|-----------------|
| Crawl errors | Google Search Console | Fix 404s, redirect broken URLs |
| Index coverage | Google Search Console | Investigate excluded pages |
| Mobile usability | Google Search Console | Fix viewport/touch issues |
| Core Web Vitals | PageSpeed Insights | Optimize LCP/CLS/TBT |
| Security issues | Google Search Console | Address immediately |
| Broken links | Screaming Frog or manual | Fix or redirect |

---

## Post-Launch Monitoring (Monthly)

| Check | Tool | Action if Failed |
|-------|------|-----------------|
| Page speed | PageSpeed Insights | Optimize assets, caching |
| Schema validation | Google Rich Results Test | Fix markup errors |
| Sitemap status | Google Search Console | Resubmit if needed |
| Robots.txt | Manual review | Ensure no new blocks |
| HTTPS certificate | Browser check | Vercel auto-renews |
| Redirect chains | Screaming Frog | Flatten redirect paths |

---

## Vercel-Specific Configuration

### Headers (from vercel.json)

```json
{
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        { "key": "X-Content-Type-Options", "value": "nosniff" },
        { "key": "X-Frame-Options", "value": "DENY" },
        { "key": "X-XSS-Protection", "value": "1; mode=block" },
        { "key": "Referrer-Policy", "value": "strict-origin-when-cross-origin" },
        { "key": "Permissions-Policy", "value": "camera=(), microphone=(), geolocation=()" }
      ]
    }
  ]
}
```

### Cache Strategy

| Asset Type | Cache-Control |
|-----------|---------------|
| HTML pages | `public, max-age=0, must-revalidate` |
| Images/fonts | `public, max-age=31536000, immutable` |
| CSS/JS (if external) | `public, max-age=31536000, immutable` |

### Clean URLs

Vercel `cleanUrls: true` removes `.html` extensions:
- `/blog` serves `blog.html`
- `/404` serves `404.html`
- `/` serves `index.html`

---

## Technical Debt Log

| Issue | Severity | Status | Notes |
|-------|----------|--------|-------|
| Favicon is SVG placeholder | Low | Open | Replace with proper .ico + .png set |
| OG image is placeholder | Low | Open | Create 1200x630 branded image |
| Blog posts are single page | Medium | Open | Consider individual post pages for SEO |
| No RSS feed | Low | Open | Add if blog content scales |
