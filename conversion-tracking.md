# Meridian Smile Studio — Conversion Tracking

## Primary Conversion Goal

**Consultation booking** — Every tracking decision should ladder up to measuring and optimizing consultation requests.

---

## Conversion Events

### Tier 1: Primary Conversions (Direct Revenue Impact)

| Event Name | Trigger | Where to Track | Value |
|-----------|---------|---------------|-------|
| `consultation_submit` | Contact form submitted successfully | index.html #contact form | — |
| `phone_call_click` | User taps/clicks the phone number link | index.html tel: link | — |
| `email_click` | User clicks the email link | index.html mailto: link | — |

### Tier 2: Secondary Conversions (Leading Indicators)

| Event Name | Trigger | Where to Track | Value |
|-----------|---------|---------------|-------|
| `quiz_complete` | User completes the smile quiz | index.html quiz | — |
| `blog_subscribe` | User subscribes to newsletter | blog.html footer | — |
| `cta_click` | User clicks any "Book a Visit" or "Request Preview" CTA | All pages | — |
| `process_view` | User scrolls to process section | index.html #process | — |
| `gallery_view` | User views gallery section | index.html #gallery | — |

### Tier 3: Engagement Metrics (Not Conversions, but Informs Strategy)

| Event Name | Trigger | Value |
|-----------|---------|-------|
| `scroll_depth` | User scrolls to 25%, 50%, 75%, 100% | Percentage |
| `time_on_page` | Time spent on page | Seconds |
| `outbound_click` | User clicks external link | URL |

---

## Implementation: GA4 Events

### Add to index.html

Add the following before the closing `</body>` tag (or within the existing `<script>` block):

```javascript
// Consultation form submission
const contactForm = document.querySelector('form');
if (contactForm) {
  contactForm.addEventListener('submit', function(e) {
    // After successful validation
    if (valid) {
      gtag('event', 'consultation_submit', {
        service_interest: document.querySelector('#service').value || 'unspecified',
        page_location: window.location.href
      });
    }
  });
}

// Phone call click
document.querySelectorAll('a[href^="tel:"]').forEach(function(el) {
  el.addEventListener('click', function() {
    gtag('event', 'phone_call_click', {
      page_location: window.location.href
    });
  });
});

// Email click
document.querySelectorAll('a[href^="mailto:"]').forEach(function(el) {
  el.addEventListener('click', function() {
    gtag('event', 'email_click', {
      page_location: window.location.href
    });
  });
});

// Quiz completion
const quizResult = document.querySelector('.quiz__result');
if (quizResult) {
  // After quiz completes, fire event
  gtag('event', 'quiz_complete', {
    page_location: window.location.href
  });
}

// CTA clicks
document.querySelectorAll('.btn--dark, .btn--brass, .btn--outline').forEach(function(el) {
  el.addEventListener('click', function() {
    gtag('event', 'cta_click', {
      cta_text: el.textContent.trim(),
      page_location: window.location.href
    });
  });
});

// Newsletter subscription
const nlBtn = document.querySelector('.footer__newsletter-btn');
if (nlBtn) {
  nlBtn.addEventListener('click', function() {
    gtag('event', 'blog_subscribe', {
      page_location: window.location.href
    });
  });
}
```

---

## GA4 Conversion Setup

### Mark Events as Conversions

1. GA4 Admin → **Events** → Find `consultation_submit`
2. Toggle **Mark as conversion** → ON
3. Repeat for `phone_call_click` and `quiz_complete`

### Conversion Funnel (Expected)

```
Landing Page → Process Section → Quiz/Contact Section → Form Submit → Consultation Booked
     100%            45%                25%                8%              100% (of form submits)
```

---

## UTM Parameters (For Paid Campaigns)

### Social Media Campaigns

```
?utm_source=instagram&utm_medium=social&utm_campaign=veneers_promo
```

### Email Campaigns

```
?utm_source=email&utm_medium=newsletter&utm_campaign=monthly_update
```

### Google Ads

```
?utm_source=google&utm_medium=cpc&utm_campaign=cosmetic_dentist_sf
```

---

## Dashboard Metrics

### Weekly Report (Google Looker Studio or Manual)

| Metric | Source | Target |
|--------|--------|--------|
| Consultation form submits | GA4 Events | 5/week |
| Phone call clicks | GA4 Events | 10/week |
| Quiz completions | GA4 Events | 8/week |
| Blog subscribers | GA4 Events | 3/week |
| Total sessions | GA4 | 150/week |
| Conversion rate (form/sessions) | GA4 | 3%+ |

### Monthly Report

| Metric | Month 1 | Month 3 | Month 6 |
|--------|---------|---------|---------|
| Total conversions | 10 | 25 | 50 |
| Conversion rate | 2% | 3% | 4% |
| Cost per conversion (if ads) | — | — | < $50 |

---

## Attribution Model

GA4 uses **data-driven attribution** by default. For a small practice:

- **First click** matters most (how did they find us?)
- **Last click** matters for conversion (what made them book?)
- Focus on **channel grouping** (organic, direct, social, referral) over individual source

---

## Testing

### Pre-Launch Testing Checklist

- [ ] Submit test form → verify `consultation_submit` fires in GA4 DebugView
- [ ] Click phone number → verify `phone_call_click` fires
- [ ] Click email → verify `email_click` fires
- [ ] Complete quiz → verify `quiz_complete` fires
- [ ] Subscribe to newsletter → verify `blog_subscribe` fires
- [ ] Check GA4 Realtime report shows events
- [ ] Verify no duplicate events firing
- [ ] Verify conversion marks are set in GA4 Admin
