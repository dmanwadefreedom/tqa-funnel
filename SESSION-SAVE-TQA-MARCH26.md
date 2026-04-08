# SESSION SAVE — TQA Funnel Audit + Launch Build
## March 26, 2026 | Score: 7/10
## Resume: Read THIS file first, then act on "STILL OPEN" section

---

## WHAT WAS BUILT THIS SESSION

### Funnel Architecture (Hormozi + Brunson audited)
- Grand Slam Offer audit: original Jumpstart scored 4/10, redesigned to target 8/10
- Dual funnel: Raj (IT pro, $47-$4,999) + Ravi (Security Manager, $10K CISO) — separate avatars, separate campaigns
- Self-funding model: $7 + $47 covers ad spend, $97/mo covers ops, everything above is profit
- Rebranded: "AI-Proof Career Plan" ($47) and "90-Day AI-Proof Career Accelerator" ($97/mo)

### Pages LIVE (GitHub Pages — dmanwadefreedom/tqa-jumpstart)
| Page | URL |
|------|-----|
| Launch Plan (share with DJ) | https://dmanwadefreedom.github.io/tqa-jumpstart/launch-plan.html |
| Free Quiz | https://dmanwadefreedom.github.io/tqa-jumpstart/quiz.html |
| $97/mo Accelerator Page | https://dmanwadefreedom.github.io/tqa-jumpstart/accelerator.html |
| Original Jumpstart | https://dmanwadefreedom.github.io/tqa-jumpstart/ |

### Stripe Products LIVE (DJ's account — sk_live_51MhRteDAq9P...)
| Product | Price | Checkout Link |
|---------|-------|--------------|
| AI-Proof Career Plan | $47 one-time | https://buy.stripe.com/4gM00j3hM7pV22U84s48008 |
| 90-Day AI-Proof Career Accelerator | $97/mo | https://buy.stripe.com/8x25kD5pU39FgXOdoM48009 |
| TQA Live Webinar Access | $7 one-time | https://buy.stripe.com/28EcN5dWq7pVePGacA4800a |
| Full Program PIF (existing) | $4,997 | https://buy.stripe.com/eVqdR96tYaC7fTKdoM48006 |
| Full Program Plan (existing) | $1,997/mo | https://buy.stripe.com/cNi3cv5pUeSn9vmckI48007 |

### Emails SENT (194 total via GHL API)
- 24 attended → "See where you actually stand" → quiz link
- 126 no-show → "2 minutes. Find out if cybersecurity is right for you." → quiz + replay
- 46 old leads → "How ready are you?" → quiz link
- 2 failed (Hilda Biat — invalid email)
- All emails link to FREE quiz. $47 upsell happens on quiz results page.

### Real Data Pulled (ALL from live APIs, not estimates)
- Meta ad spend: AUD $1,853.80 (USD $1,204.97) across 4 campaigns
- Best CPL: $4.11 USD (CBO Landing + Form Both)
- GHL: 197 contacts, 24 attended, 126 no-show, 12 applied, 0 paid, 0 enrolled
- Fathom: 3 TQA calls parsed (March 13, 17, 24) + March 24 full transcript saved
- WhatsApp: Stripe key found, all Drive links found, team messages parsed

### Files Created
| File | What |
|------|------|
| TQA-OFFER-AUDIT-GRAND-SLAM.md | Full Hormozi audit, scoring, fixes |
| TQA-PNL-CAMPAIGN-PLAN.md | P&L, 2-tier ad campaign, 90-day projections |
| TQA-JUMPSTART-LAUNCH-PACKAGE.md | 7 emails, form specs, delivery plan |
| TQA-97-DELIVERABLE-PLAN.md | Week-by-week 90-day program design |
| tqa-jumpstart-funnel-visual.html | Shareable visual (9 sections, all real data) |
| tqa-accelerator-offer.html | $97/mo product page (15 sections) |
| tqa-career-quiz.html | Free quiz with scoring + $47 upsell |
| sample-career-scorecard.html | Sample PDF output for "Vikram Sharma" |
| scorecard-claude-prompt.md | Claude API prompt template for generating plans |
| fathom-dj-call-march24.md | Full transcript extract + case studies + action items |

### Key Decisions
- DJ coined "Jumpstart" on March 24 call — evolved to "AI-Proof" this session
- DJ wants 5 pre-recorded videos ($499 tier) — his idea, his pricing
- DJ confirmed WhatsApp > Telegram for Indian audience
- DJ wants private WhatsApp group (DJ + Dylan + Akshaya only)
- Next webinar: Saturday April 11, 11 AM EST, $7 entry
- Ads launch: Sunday April 6 (5 days before webinar)
- DJ's daily rate: $2,000-$3,000/day — the $97/mo is genuinely underpriced
- CISO $10K funnel is separate avatar, separate campaign (Phase 2)

### DJ's Case Studies (from calls, use in all content)
1. Business Email Compromise — $300K wire transfer stopped
2. Qatar Central Bank — DJ wrote AI/data/cloud security policies, now law across all Qatar banks
3. Retail chain financial fraud prevention
4. 50-page disaster recovery plan (India company, US client)
5. CERT India ex-leader + CISO friends as guest speakers ($10K/hr forensics experts)

---

## STILL OPEN (next session priorities)

### BLOCKER: DJ's Courseware
- 120-130 pages, weeks 3-10 content (GRC, risk management, network security, case studies, threat modeling)
- NOT on Dylan's machine. Lives in DJ's Google Drive only.
- Drive folder: https://drive.google.com/drive/folders/1Y6DzytoOGP83OBGY7tAUcva8tSCK1u3-
- DJ shared a webinar recording folder to dylan@thedylanewing.com today — check if courseware is in there
- Dylan asked Shreyas in WhatsApp for the file too
- NEED: DJ to email the Word doc to dylan@thedylanewing.com
- This unlocks: AI assistant, $97/mo interactive curriculum, weekly task engine

### GHL Webhook
- Quiz captures leads in browser JavaScript only — data is LOST on page close
- Need: GHL form webhook receiving quiz submissions
- Or: redirect quiz form submission to GHL form endpoint
- Build time: 2 hours

### Post-Purchase Automation
- Someone pays $47 → redirect to Accelerator page (done) → but no email sequence after
- Need: GHL workflow triggered by Stripe webhook (tag: ai-proof-plan-purchased)
- Sequence: welcome email → intake form → deliver plan → Day 3 Accelerator upsell → Day 7 follow-up
- Build time: 3 hours (need Agresh for GHL workflow OR build via API)

### April 11 Webinar
- Date set: Saturday April 11, 11 AM EST
- $7 Stripe link exists
- NEED: landing page for webinar registration (ads point here)
- NEED: GHL workflow for $7 webinar registrants (confirmation, reminders, day-of)
- Ads launch April 6 (5 days before)
- Build time: 1 day

### thequantumachievers.com
- Still says "Reserve my Spot" for March 19 webinar
- Not blocking current funnel (emails/ads point to GitHub Pages quiz, not the website)
- Agresh or Shreyas needs to update — or we bypass entirely and use GitHub Pages for everything
- Need GoDaddy access to set up quiz.thequantumachievers.com subdomain

### CISO $10K Funnel (Phase 2)
- Visual exists in launch plan, no pages or campaigns built
- Need: separate landing page (application-only)
- Need: LinkedIn campaign via 15element (DJ's credentials)
- Need: LinkedIn profile scraping for Meta custom audience seed
- Target: after Funnel 1 ($47/$97) proves conversion

### LinkedIn / 15element
- Dylan has account: https://prospecting.15element.ai/ (dman_101@yahoo.com)
- Can't access from terminal (needs browser login)
- Need: DJ's LinkedIn credentials to set up outreach
- Target: "Information Security Manager" / "Cyber Security Manager" / "IT Security Manager"

### Manus / Meta Ads
- Meta acquired Manus AI — integrated into Ads Manager
- Shreyas needs to activate it on the TQA ad account (act_1126902421887543)
- Dylan meeting Shreyas 2x this week to train him on Manus
- Not something I can do — requires Meta Ads Manager browser access

---

## WHAT NOT TO TOUCH
- Do NOT re-send emails to the 194 contacts (already sent)
- Do NOT modify Stripe products (already live and named correctly)
- Do NOT touch OpenClaw, PM2, or JARVIS server.js (different session scope)
- Do NOT push to the tqa-jumpstart GitHub repo without checking what's deployed

## RESUME PROMPT
```
Read ~/Documents/TQA/Client Files/SESSION-SAVE-TQA-MARCH26.md first.

SCOPE: CLIENT: TQA — funnel build + $97/mo product

Status: 7/10. Emails sent (194). Quiz live. Stripe live. Missing: DJ courseware, GHL webhook, post-purchase automation, April 11 webinar page.

If Dylan has DJ's courseware: ingest it, build the AI assistant, wire the $97/mo interactive curriculum.
If not: build GHL webhook for quiz, build April 11 webinar landing page, wire post-purchase email sequence.

DO NOT touch: server.js, PM2, OpenClaw, Freedom Code, other client systems.
```
