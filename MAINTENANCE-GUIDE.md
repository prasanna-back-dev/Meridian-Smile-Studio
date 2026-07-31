# Meridian Smile Studio — Maintenance Guide

## Overview

This guide covers ongoing maintenance tasks to keep the website secure, fast, and effective. Most tasks require no technical expertise.

---

## Weekly Tasks (15 minutes)

### Content Updates

- [ ] Check for new patient reviews on Google
- [ ] Respond to any reviews (positive or negative) within 24 hours
- [ ] Publish 1 Google Business Profile post
- [ ] Check if any contact form submissions need follow-up

### Health Check

- [ ] Visit the website — does it load? Does it look correct?
- [ ] Test the contact form — does it submit?
- [ ] Check phone number click-to-call on mobile

---

## Monthly Tasks (1–2 hours)

### Content

- [ ] Write and publish 1 blog post (or have Dr. Cross write it)
- [ ] Update GBP with 3–4 new posts
- [ ] Add any new photos to GBP (office, team, results)
- [ ] Check if any content is outdated (dates, prices, services)

### Technical

- [ ] Check Google Search Console for crawl errors
- [ ] Check GA4 for traffic trends
- [ ] Test the site on mobile (iPhone + Android if possible)
- [ ] Check page speed at PageSpeed Insights
- [ ] Verify all links still work

### SEO

- [ ] Check keyword rankings (top 5 target keywords)
- [ ] Review which pages get the most traffic
- [ ] Identify any new content opportunities
- [ ] Check if competitors have made changes

---

## Quarterly Tasks (2–4 hours)

### Comprehensive Review

- [ ] Full site audit (all pages, all links, all forms)
- [ ] Update sitemap.xml if new pages were added
- [ ] Review and update meta tags if needed
- [ ] Check schema markup still validates
- [ ] Review Core Web Vitals trends
- [ ] Update competitor analysis
- [ ] Review content calendar for next quarter

### Security

- [ ] Check for any security alerts in Search Console
- [ ] Verify SSL certificate is valid
- [ ] Review any suspicious form submissions (spam)
- [ ] Update any third-party dependencies (if applicable)

### Performance

- [ ] Run full Lighthouse audit
- [ ] Compare performance metrics to baseline
- [ ] Identify and fix any performance regressions
- [ ] Optimize any slow-loading images

---

## Annual Tasks (Half day)

### Full Audit

- [ ] Complete site redesign assessment (is the design still current?)
- [ ] Update brand guidelines if needed
- [ ] Review and update all documentation
- [ ] Archive old blog posts that are no longer relevant
- [ ] Update the sitemap.xml with current dates
- [ ] Review hosting and domain renewal dates
- [ ] Plan major content updates for the year

### Business Review

- [ ] Review annual analytics (traffic, conversions, rankings)
- [ ] Compare to industry benchmarks
- [ ] Set goals for the coming year
- [ ] Budget for any needed design or development updates

---

## Content Update Procedures

### Adding a Blog Post

1. Write the post content (Word doc or Google Doc)
2. Include: title, excerpt, full body, category tag
3. Send to developer for formatting and upload
4. Developer adds to `blog.html`
5. Developer updates `sitemap.xml`
6. Share on GBP and social media

### Updating the Homepage

1. Identify what needs to change (text, image, pricing, etc.)
2. Send the exact change to the developer
3. Developer makes the edit
4. Verify the change on the live site
5. No sitemap update needed (same URL)

### Adding a New Page

1. Plan the page content and purpose
2. Get Dr. Cross's approval on content
3. Developer creates the new HTML file
4. Add to navigation (header + footer)
5. Add to `sitemap.xml`
6. Submit to Google Search Console for indexing
7. Link from relevant existing pages

---

## Emergency Procedures

### Site Down

1. Check Vercel status page: [vercel.com/status](https://vercel.com/status)
2. If Vercel is operational, check the deployment logs
3. If the issue is with the code, revert to the last working deployment
4. Contact developer if the issue persists

### Form Not Working

1. Test the form yourself
2. Check if JavaScript is disabled (form uses client-side validation)
3. Check browser console for errors
4. If the issue persists, contact developer

### Security Issue

1. Do not ignore any security alerts in Google Search Console
2. Take the site offline if there's evidence of a compromise
3. Contact developer immediately
4. Change any passwords that may have been exposed
5. Review server logs if available

### Slow Loading

1. Test at PageSpeed Insights
2. Check if images were recently updated (large file sizes?)
3. Check if any external scripts were added
4. Clear Vercel cache (automatic on next deploy)
5. If persistent, contact developer

---

## Contacts

| Role | Contact | When to Use |
|------|---------|-------------|
| Developer | [developer email] | Technical issues, code changes |
| Dr. Cross | [dr.cross email] | Content approval, business decisions |
| Hosting (Vercel) | [Vercel support] | Server/deployment issues |
| Domain registrar | [registrar contact] | DNS, domain renewal |
