# Meridian Smile Studio — Google Analytics 4 Setup

## Prerequisites

- Google account with access to GA4
- Google Tag Manager account (optional but recommended)
- Vercel deployment live

---

## Step 1: Create GA4 Property

1. Go to [analytics.google.com](https://analytics.google.com)
2. Click **Admin** (gear icon) → **+ Create Property**
3. Property name: `Meridian Smile Studio`
4. Reporting time zone: `Pacific Time (US & Canada)`
5. Currency: `United States Dollar`
6. Click **Next**
7. Business size: `Small business`
8. Business objectives: `Generate leads` and `Drive online reservations`
9. Click **Create**

---

## Step 2: Set Up Data Stream

1. In GA4 Admin → **Data Streams** → **Add stream** → **Web**
2. Website URL: `meridiansmilestudio.com`
3. Stream name: `Meridian Website`
4. Enhanced measurement: **Enable** (scroll, outbound clicks, file downloads, page views)
5. Click **Create stream**
6. Copy the **Measurement ID** (format: `G-XXXXXXXXXX`)

---

## Step 3: Install GA4 on Website

### Option A: Direct Installation (Recommended for Static Site)

Add the following snippet to the `<head>` of `index.html` and `blog.html`:

```html
<!-- Google Analytics 4 -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

Replace `G-XXXXXXXXXX` with the actual Measurement ID.

### Option B: Google Tag Manager

1. Create a GTM container at [tagmanager.google.com](https://tagmanager.google.com)
2. Add GTM container snippet to all pages
3. Create a GA4 Configuration tag with the Measurement ID
4. Set trigger to **All Pages**
5. Publish the GTM container

---

## Step 4: Configure GA4 Settings

### Custom Dimensions

| Dimension Name | Parameter Name | Scope |
|---------------|---------------|-------|
| Service Interest | `service_interest` | Event |
| Consultation Type | `consultation_type` | Event |
| Blog Category | `blog_category` | Event |

### Custom Metrics

| Metric Name | Parameter Name | Scope |
|------------|---------------|-------|
| Quiz Completion | `quiz_completed` | Event |
| Time on Process Page | `process_time` | Event |

---

## Step 5: Set Up Conversions

See `conversion-tracking.md` for detailed conversion event setup.

### Key Conversion Events

| Event Name | Trigger | Value |
|-----------|---------|-------|
| `consultation_submit` | Form submission on contact section | — |
| `phone_call_click` | Click on phone number link | — |
| `email_click` | Click on email link | — |
| `quiz_complete` | Smile quiz completion | — |
| `blog_subscribe` | Newsletter subscription | — |

---

## Step 6: Build Reports

### Essential Reports (Pin to Dashboard)

1. **Overview Report** — Traffic, engagement, conversions summary
2. **Landing Pages** — Which pages drive consultations
3. **Traffic Acquisition** — Where patients come from (organic, direct, social)
4. **Event Count** — Which interactions happen most
5. **User Demographics** — Age, location, device

### Custom Exploration: Patient Journey

1. Go to **Explore** → **Free Form**
2. Dimensions: Landing page, Event name, Device category
3. Metrics: Sessions, Engagement rate, Conversions
4. Filter: Exclude internal traffic

---

## Step 7: Exclude Internal Traffic

1. GA4 Admin → **Data Streams** → Select stream → **Configure tag settings**
2. **Define internal traffic**
3. Rule name: "Office IP"
4. Traffic type: `Internal`
5. IP address equals: `[Office IP address]`
6. Save and apply

---

## Step 8: Link to Google Search Console

1. GA4 Admin → **Product Links** → **Search Console Links**
2. Click **Link**
3. Select the Search Console property
4. Select the GA4 web stream
5. Enable: **Enable Search Console reporting in GA4**

---

## Step 9: Link to Google Ads (If Running Ads)

1. GA4 Admin → **Product Links** → **Google Ads Links**
2. Click **Link**
3. Select the Google Ads account
4. Enable: **Enable personalized advertising**

---

## Reporting Schedule

| Report | Frequency | Owner |
|--------|-----------|-------|
| Traffic overview | Weekly | Marketing |
| Conversion report | Weekly | Marketing |
| Content performance | Monthly | Marketing |
| Acquisition channels | Monthly | Marketing |
| Full audit | Quarterly | Dr. Cross + Marketing |

---

## Privacy Compliance

- Add cookie consent banner if targeting EU visitors (not required for US-only)
- Anonymize IP addresses (GA4 does this by default)
- Data retention: 14 months (GA4 default)
- Do not collect personally identifiable information in GA4 events
