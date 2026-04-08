# TQA Web Presence Audit — April 6, 2026

## Sales Page Audit (tqa-funnel/index.html)
**Current URL:** dmanwadefreedom.github.io/tqa-funnel/
**Design Score:** 8/10 — clean, premium dark theme, good typography
**Conversion Score:** 4/10 — critical breaks below

> **NOTE:** This audit was run against the old tqa-jumpstart URL. It should be re-run against the current tqa-funnel site for updated findings.

### CRITICAL Issues

| # | Issue | Impact | Fix |
|---|-------|--------|-----|
| 1 | **CTAs link to `#checkout` — section doesn't exist** | 100% of clicks go nowhere. Zero conversions possible. | Add Stripe checkout embed or redirect to Stripe payment link |
| 2 | **Not on main domain** | Zero SEO juice. GitHub Pages subdomain has no authority. | Deploy to thequantumachievers.com/jumpstart or /start |
| 3 | **No upsell path** | No path from $97/mo Insider Brief to $4,997 Cybersecurity Accelerator. | Add "Accelerate Your Transition" upgrade section after checkout |
| 4 | **Contact email: achieversquantum@gmail.com** | Unprofessional. Kills trust. | Switch to dj@thequantumachievers.com or support@thequantumachievers.com |

### HIGH Priority Issues

| # | Issue | Fix |
|---|-------|-----|
| 5 | No schema markup (Course, EducationalOrganization) | Add JSON-LD (see schema-markup.html) |
| 6 | No favicon | Add TQA logo as favicon |
| 7 | No privacy policy / terms links in footer | Add links — required for Meta ads |
| 8 | Pricing should reflect current product ladder | Current ladder: $0 Quiz, $27 Career Briefing, $47 Career Scorecard, $97/mo Insider Brief, $4,997 Cybersecurity Accelerator. See TQA-SOURCE-OF-TRUTH.md |
| 9 | No video testimonials | Record 2-3 student video testimonials or use LinkedIn screenshot format |
| 10 | No aggregate numbers ("X students helped", "Y% got roles") | Add proof metrics — even "28 years mentoring" → "100+ career transitions guided" |

### MEDIUM Priority Issues

| # | Issue | Fix |
|---|-------|-----|
| 11 | Logo images use onerror text fallback | Verify all logo .webp files load from GitHub Pages |
| 12 | og:image points to WordPress upload URL | Host og:image in /assets/ or verify WP URL works |
| 13 | No Google Analytics / GA4 — only Meta Pixel | Add GA4 for organic traffic tracking |
| 14 | No exit-intent or email capture | Add email opt-in for "Free Cybersecurity Career Scorecard" |
| 15 | Footer has no social links | Add LinkedIn, YouTube if applicable |

### What's Working Well
- Premium dark design with gold accents — feels high-ticket
- Strong pain section (visa, ceiling, AI anxiety) — nails the avatar
- Value stack math ($893 → $97) — classic Hormozi
- DJ's credentials prominently displayed (Deloitte, EY, Shell, ISC2)
- Speaking photos and conference imagery build authority
- FAQ section addresses real objections
- Mobile-responsive CSS with good breakpoints
- Meta Pixel properly installed with InitiateCheckout event

---

## Domain Strategy

| Domain | Current State | Action |
|--------|--------------|--------|
| thequantumachievers.com | WordPress site. Webinar funnel. 2 pages in sitemap. No blog. | PRIMARY — all content here |
| thequantumadvantage.com | JS redirect → /lander (403). Dead. | 301 redirect → thequantumachievers.com |
| dmanwadefreedom.github.io/tqa-funnel/ | Best sales page. Wrong domain. | Move content to main WP domain |

### 301 Redirect Setup (thequantumadvantage.com)

**Option A: If domain uses Cloudflare:**
1. Add Page Rule: `thequantumadvantage.com/*` → 301 → `https://thequantumachievers.com/$1`
2. Add Page Rule: `www.thequantumadvantage.com/*` → 301 → `https://thequantumachievers.com/$1`

**Option B: If domain has hosting with .htaccess:**
```apache
RewriteEngine On
RewriteCond %{HTTP_HOST} ^(www\.)?thequantumadvantage\.com [NC]
RewriteRule ^(.*)$ https://thequantumachievers.com/$1 [R=301,L]
```

**Option C: If domain registrar supports forwarding:**
Set permanent (301) forward: thequantumadvantage.com → thequantumachievers.com

---

## WordPress Blog Setup

### Recommended Blog Categories
1. **Career Transition** — IT to cybersecurity paths, success stories
2. **Certifications** — Which certs, in what order, ROI analysis
3. **Industry Insights** — Market trends, salary data, hiring patterns
4. **Visa & Immigration** — H-1B specific cybersecurity guidance
5. **AI & Future of Work** — How AI impacts IT careers

### Blog Settings Needed
- Permalink structure: `/blog/%postname%/`
- Yoast SEO or RankMath plugin installed
- XML sitemap enabled and submitted to Google Search Console
- Blog page added to main navigation
- Author bio for DJ with headshot and credentials
- Related posts widget at bottom of each article

### 5 Cornerstone Articles (Ready to Publish)
See `/Documents/TQA/Client Files/blog-articles/` directory:
1. How to Switch from IT to Cybersecurity in 2026
2. Cybersecurity Salary Guide 2026
3. Best Cybersecurity Roles for H-1B Visa Holders
4. Which Cybersecurity Certifications to Get First
5. Is AI Replacing IT Jobs? What Smart Professionals Are Doing

Each article funnels → $47 Career Briefing CTA

---

## Systems Upgrade Recommendations

### Current Stack Assessment

| System | Status | Upgrade? |
|--------|--------|----------|
| WordPress (main site) | Running, basic | Add SEO plugin + blog |
| GitHub Pages (sales page) | Working but wrong domain | Migrate to WP or subdomain |
| GHL (cv0yehFtVK84960e2GsO) | Active, 197 contacts | Add blog subscriber workflow |
| Meta Pixel (1589502282075800) | Installed | Add GA4 alongside |
| Stripe | Payment links exist | Add checkout embed to sales page |
| VAPI (3 assistants) | Live | No change needed |

### Recommended Tech Upgrades
1. **Add GA4** — Track organic traffic from blog content
2. **Google Search Console** — Submit sitemap, monitor indexing
3. **RankMath/Yoast SEO** — WordPress SEO plugin for blog
4. **Stripe Checkout embed** — Fix the broken #checkout on sales page
5. **ConvertKit or GHL form** — Email capture for blog readers
6. **Calendly or GHL calendar** — Direct booking for $47 Career Briefing
