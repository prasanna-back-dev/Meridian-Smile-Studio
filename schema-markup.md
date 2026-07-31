# Meridian Smile Studio — Schema Markup Documentation

## Overview

Schema markup (structured data) helps Google understand the content of each page and can trigger rich results (knowledge panels, review stars, FAQs, breadcrumbs) in search results.

---

## Implemented Schema

### Dentist Schema (Homepage)

Already implemented in `index.html`:

```json
{
  "@context": "https://schema.org",
  "@type": "Dentist",
  "name": "Meridian Smile Studio",
  "description": "Cosmetic dental practice specializing in porcelain veneers, Invisalign, and full smile makeovers in San Francisco's Financial District.",
  "url": "https://meridiansmilestudio.com",
  "telephone": "+14155550142",
  "email": "hello@meridiansmilestudio.com",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "88 Battery St, Suite 500",
    "addressLocality": "San Francisco",
    "addressRegion": "CA",
    "postalCode": "94111",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 37.7937,
    "longitude": -122.3950
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
      "opens": "08:00",
      "closes": "18:00"
    }
  ],
  "priceRange": "$$$$",
  "areaServed": {
    "@type": "City",
    "name": "San Francisco"
  },
  "founder": {
    "@type": "Person",
    "name": "Dr. Elena Cross",
    "jobTitle": "DDS, Founder",
    "hasCredential": [
      "Doctor of Dental Surgery — University of the Pacific",
      "Accredited Member — American Academy of Cosmetic Dentistry"
    ]
  }
}
```

### Validation

Test the schema at:
- [Google Rich Results Test](https://search.google.com/test/rich-results)
- [Schema.org Validator](https://validator.schema.org/)

---

## Recommended Additional Schema

### FAQPage Schema (Add to index.html)

Add a `<script type="application/ld+json">` block for the FAQ section (if an FAQ section is added to the homepage):

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How much do porcelain veneers cost in San Francisco?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Porcelain veneers at Meridian Smile Studio start at $1,200 per tooth. We offer financing through CareCredit and Lending Club with 0% interest plans up to 24 months. A personalized quote is provided after your digital smile preview consultation."
      }
    },
    {
      "@type": "Question",
      "name": "How long does Invisalign take?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Most Invisalign cases at Meridian Smile Studio are completed in 6 to 14 months, depending on the complexity of alignment needed. Dr. Cross uses iTero scanning and ClinCheck software to map every stage before you begin."
      }
    },
    {
      "@type": "Question",
      "name": "What is digital smile design?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Digital smile design is a treatment planning process where your new smile is designed on screen using 3D software, then overlaid on your face so you can see the result before any treatment begins. At Meridian, we also create a trial smile you can wear for a week to test the look."
      }
    }
  ]
}
```

### BreadcrumbList Schema (Add to blog.html)

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://meridiansmilestudio.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Blog",
      "item": "https://meridiansmilestudio.com/blog"
    }
  ]
}
```

### Article Schema (For Individual Blog Posts)

When individual blog post pages are created:

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "How Digital Smile Design Changed Veneer Planning",
  "author": {
    "@type": "Person",
    "name": "Dr. Elena Cross",
    "url": "https://meridiansmilestudio.com/#about"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Meridian Smile Studio",
    "logo": {
      "@type": "ImageObject",
      "url": "https://meridiansmilestudio.com/logo.svg"
    }
  },
  "datePublished": "2024-01-15",
  "dateModified": "2024-01-15",
  "description": "Digital smile design lets you see your new veneers on screen before treatment begins.",
  "image": "https://meridiansmilestudio.com/og-image.jpg"
}
```

### LocalBusiness Schema (Alternative/Supplement)

If the Dentist schema doesn't trigger the desired rich results, add LocalBusiness as a supplement:

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Meridian Smile Studio",
  "image": "https://meridiansmilestudio.com/logo.svg",
  "telephone": "+14155550142",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "88 Battery St, Suite 500",
    "addressLocality": "San Francisco",
    "addressRegion": "CA",
    "postalCode": "94111"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.9",
    "reviewCount": "47"
  }
}
```

**Note:** Only add `aggregateRating` once real reviews exist. Fake ratings violate Google's guidelines.

---

## Schema Testing Checklist

Before deploying any schema changes:

- [ ] Validate at Google Rich Results Test
- [ ] Validate at Schema.org Validator
- [ ] Check for warnings (non-critical but should be addressed)
- [ ] Check for errors (must fix before deploying)
- [ ] Test in Google Search Console → Enhancements
- [ ] Monitor for new errors after deployment

---

## Rich Results Target

| Schema Type | Expected Rich Result | Page |
|-------------|---------------------|------|
| Dentist/LocalBusiness | Knowledge panel, map pack | Homepage |
| FAQPage | FAQ accordion in search results | Homepage (if FAQ added) |
| BreadcrumbList | Breadcrumb trail in results | Blog |
| Article | Article snippet with author | Blog posts |
| AggregateRating | Star rating in results | Homepage (after reviews) |

---

## Monitoring

After implementing schema:

1. **Week 1:** Check Google Search Console → Enhancements for errors
2. **Month 1:** Monitor if rich results appear in search
3. **Ongoing:** Check Search Console monthly for new schema errors

If rich results don't appear:
- Schema may be valid but Google chose not to display it (common for new sites)
- Ensure the page has sufficient content to support the schema type
- Build domain authority and content depth before expecting rich results
