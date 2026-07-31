# Meridian Smile Studio — Meta Tags Reference

All meta tags for every page. Each entry includes the exact tag content, character count, and target keyword.

---

## index.html (Homepage)

### Title Tag
```
Meridian Smile Studio | Porcelain Veneers & Smile Design | San Francisco
```
**Characters:** 70 (within Google's display limit with truncation)
**Primary keyword:** "porcelain veneers san francisco"

### Meta Description
```
Porcelain veneers, Invisalign, and full smile design by Dr. Elena Cross in San Francisco's Financial District. Digital smile previews before treatment. By appointment.
```
**Characters:** 167 (within 150–160 target; slightly long but natural)

### Open Graph
```html
<meta property="og:title" content="Meridian Smile Studio | Porcelain Veneers & Smile Design">
<meta property="og:description" content="Porcelain veneers, Invisalign, and full smile design in San Francisco's Financial District. Digital previews before treatment begins.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://meridiansmilestudio.com/">
<meta property="og:image" content="https://meridiansmilestudio.com/og-image.jpg">
```

### Twitter Card
```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Meridian Smile Studio | Porcelain Veneers & Smile Design">
<meta name="twitter:description" content="Porcelain veneers, Invisalign, and full smile design in San Francisco's Financial District.">
```

### Canonical
```html
<link rel="canonical" href="https://meridiansmilestudio.com/">
```

---

## blog.html (Blog)

### Title Tag
```
Blog | Meridian Smile Studio | San Francisco Cosmetic Dentistry
```
**Characters:** 63

### Meta Description
```
Expert insights on porcelain veneers, Invisalign, smile makeovers, and cosmetic dentistry from Dr. Elena Cross in San Francisco.
```
**Characters:** 127

### Open Graph
```html
<meta property="og:title" content="Blog | Meridian Smile Studio">
<meta property="og:description" content="Expert insights on porcelain veneers, Invisalign, and cosmetic dentistry from Dr. Elena Cross.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://meridiansmilestudio.com/blog">
```

### Canonical
```html
<link rel="canonical" href="https://meridiansmilestudio.com/blog">
```

---

## 404.html

### Title Tag
```
Page Not Found | Meridian Smile Studio
```

### Meta Description
```
The page you're looking for doesn't exist. Return to Meridian Smile Studio homepage.
```

### Robots
```html
<meta name="robots" content="noindex">
```

---

## Blog Post: "How Digital Smile Design Changed Veneer Planning"

### Title Tag
```
Digital Smile Design: How We Plan Veneers Before Treatment | Meridian
```
**Characters:** 69

### Meta Description
```
Digital smile design lets you see your new veneers on screen before treatment begins. Dr. Elena Cross explains the process at Meridian Smile Studio.
```
**Characters:** 152

### Canonical
```html
<link rel="canonical" href="https://meridiansmilestudio.com/blog/digital-smile-design">
```

**Note:** Individual blog post URLs are not yet implemented as separate pages. When blog posts are expanded to individual pages, each will need its own meta tags following this pattern.

---

## Blog Post: "Invisalign at 40+"

### Title Tag
```
Invisalign at 40+: What Adults Need to Know | Meridian Smile Studio
```
**Characters:** 67

### Meta Description
```
Adult Invisalign is different from teenage treatment. Dr. Cross answers the most common questions from patients over 35.
```
**Characters:** 119

---

## Structured Data (Schema.org)

### Homepage — Dentist Schema
Already implemented in index.html. Key fields:

```json
{
  "@type": "Dentist",
  "name": "Meridian Smile Studio",
  "telephone": "+14155550142",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "88 Battery St, Suite 500",
    "addressLocality": "San Francisco",
    "addressRegion": "CA",
    "postalCode": "94111"
  },
  "founder": {
    "@type": "Person",
    "name": "Dr. Elena Cross",
    "hasCredential": [
      "Doctor of Dental Surgery — University of the Pacific",
      "Accredited Member — American Academy of Cosmetic Dentistry"
    ]
  }
}
```

### Blog — Article Schema (when individual posts are created)
```json
{
  "@type": "Article",
  "headline": "How Digital Smile Design Changed Veneer Planning",
  "author": {
    "@type": "Person",
    "name": "Dr. Elena Cross"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Meridian Smile Studio"
  },
  "datePublished": "2024-01-15",
  "dateModified": "2024-01-15"
}
```

---

## Implementation Notes

1. **Title tags** should be unique per page and under 60 characters where possible
2. **Meta descriptions** should be 150–160 characters, include the primary keyword, and end with a soft CTA
3. **Open Graph images** should be 1200x630px, branded with Meridian's visual identity
4. **Canonical URLs** must match the live URL exactly (no trailing slash inconsistency)
5. **Robots noindex** on 404.html and any utility pages
6. Update sitemap.xml whenever new pages are added
