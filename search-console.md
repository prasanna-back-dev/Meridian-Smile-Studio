# Meridian Smile Studio — Google Search Console Setup

## Step 1: Verify Property

1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Click **Add Property**
3. Choose **URL prefix** → Enter `https://meridiansmilestudio.com`
4. Verification method: **HTML tag**
5. Copy the verification meta tag
6. Add to `<head>` of `index.html`:
   ```html
   <meta name="google-site-verification" content="YOUR_VERIFICATION_CODE" />
   ```
7. Deploy to Vercel
8. Click **Verify** in Search Console

---

## Step 2: Submit Sitemap

1. Search Console → **Sitemaps**
2. Enter `sitemap.xml` in the "Add a new sitemap" field
3. Click **Submit**
4. Verify status shows "Success"

---

## Step 3: Set Up Essential Reports

### Pin These Reports to Dashboard

1. **Overview** — High-level performance summary
2. **Pages** — Which pages get impressions and clicks
3. **Queries** — What people search to find Meridian
4. **Core Web Vitals** — Page speed metrics
5. **Mobile Usability** — Mobile issues
6. **Manual Actions** — Penalties (should be empty)
7. **Security Issues** — Hacking/malware (should be empty)

---

## Step 4: Configure Settings

### Default Country

1. Settings → **International targeting**
2. Set United States as default country (if not already set)

### crawl Budget

For a small site (< 20 pages), crawl budget is not a concern. No action needed.

### URL Inspection

Use the **URL Inspection** tool to:
- Check if specific pages are indexed
- Request indexing for new/updated pages
- Debug indexing issues

---

## Step 5: Initial Indexing Check

After launch, check indexing status:

| Page | Expected Status | Action |
|------|----------------|--------|
| `/` (index.html) | Indexed | Verify in URL Inspection |
| `/blog` (blog.html) | Indexed | Request indexing if not |
| `/404.html` | Excluded (noindex) | Verify noindex is working |
| `/sitemap.xml` | Discovered via sitemap | Check in Sitemaps report |

---

## Step 6: Monitor Search Performance

### Key Metrics to Track

| Metric | What It Tells You | Target |
|--------|-------------------|--------|
| Total clicks | How many people visited from search | Growing month-over-month |
| Total impressions | How many times Meridian appeared in results | Growing month-over-month |
| Average CTR | Click-through rate from search results | > 3% for branded, > 1% for non-branded |
| Average position | Where Meridian ranks on average | Improving toward top 10 |
| Core Web Vitals | Page experience signals | All "Good" |

### Weekly Monitoring Tasks

1. Check **Performance** report for new queries
2. Check **Coverage** report for errors
3. Check **Core Web Vitals** for regressions
4. Check **Manual Actions** (should always be empty)
5. Check **Security Issues** (should always be empty)

---

## Step 7: Query Analysis

### Expected Queries (Month 1–3)

| Query Type | Examples | Expected Volume |
|-----------|----------|-----------------|
| Branded | "meridian smile studio", "meridian dental sf" | Low (building awareness) |
| Local | "cosmetic dentist financial district" | Medium |
| Service | "porcelain veneers san francisco" | Medium |
| Informational | "how much do veneers cost" | High |
| Competitor | "pacific dental studio reviews" | Low |

### Monthly Query Review

1. Export top 50 queries from Performance report
2. Identify queries with high impressions but low CTR (title/description optimization opportunity)
3. Identify queries where Meridian ranks 5–20 (quick wins with content improvement)
4. Identify new queries not in the keyword research (content opportunity)

---

## Step 8: Page Experience

### Core Web Vitals Target

| Metric | Good | Needs Improvement | Poor |
|--------|------|-------------------|------|
| LCP | < 2.5s | 2.5–4.0s | > 4.0s |
| FID | < 100ms | 100–300ms | > 300ms |
| CLS | < 0.1 | 0.1–0.25 | > 0.25 |

### Mobile Usability Issues to Monitor

- Text too small to read
- Clickable elements too close together
- Content wider than screen
- Viewport not set

---

## Step 9: Link Building Monitoring

### Internal Links Report

1. Search Console → **Links** → **Internal Links**
2. Ensure homepage links to all key pages
3. Check for orphan pages (pages with few/no internal links)

### External Links Report

1. Search Console → **Links** → **External Links**
2. Monitor which sites link to Meridian
3. Identify link building opportunities from sites that link to competitors

---

## Troubleshooting

| Issue | Likely Cause | Fix |
|-------|-------------|-----|
| Page not indexed | Noindex tag, robots.txt block, thin content | Check meta tags, content quality |
| Low impressions | Poor keyword targeting, low domain authority | Improve content, build links |
| High impressions, low CTR | Weak title/description | Optimize meta tags |
| Core Web Vitals failing | Slow loading, layout shift | Optimize images, fix layout |
| Manual action | Spammy links, thin content | Review and disavow/recreate |
