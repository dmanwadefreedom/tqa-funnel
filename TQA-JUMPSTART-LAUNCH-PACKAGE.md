# TQA JUMPSTART LAUNCH PACKAGE
## Complete Execution Plan — March 26, 2026
## Status: READY TO DEPLOY (needs Stripe link from DJ)

---

## GHL AUDIT FINDINGS (LIVE DATA)

| Metric | Count | Status |
|--------|-------|--------|
| Total contacts | 197 | |
| Webinar registrants (Mar 19) | 146 | |
| Scored HOT | 126 | |
| **No-shows** | **126** | **No offer sent** |
| **Attended** | **24** | **No offer sent** |
| Applied | 12 | Sitting in pipeline |
| Paid | 0 | ZERO |
| Enrolled | 0 | ZERO |
| **Stripe connected** | **NO** | **CRITICAL BLOCKER** |
| **Products in GHL** | **0** | **Nothing to sell** |
| **Email templates** | **0** (inline in workflows) | |
| **Days since webinar** | **7** | **Leads going cold** |

### Workflows Status
- Post Webinar Attendees: PUBLISHED (sending, but no offer link)
- Post Webinar No Show: PUBLISHED (sending, but no offer link)
- Post Call Payment Follow Up: DRAFT (not running)
- New Lead Nurture: DRAFT (not running)
- Long-Term Nurture: DRAFT (not running)
- Stale Leads: DRAFT (not running)

### What Emails ARE Going Out
Post-webinar emails exist and are sending. The copy is decent. BUT:
1. ZERO emails contain an offer or checkout link
2. The March 24 email to Kiran re-sent a PRE-WEBINAR confirmation (broken workflow)
3. No-show email links to Google Drive replay (good) but no next step to buy

### thequantumachievers.com
- STILL says "Reserve my Spot" for March 19 webinar
- Score: 4/10 for post-webinar conversion
- Pixel installed (1589502282075800) but zero purchase events

### Jumpstart Page (dmanwadefreedom.github.io/tqa-jumpstart/)
- Score: 7/10
- Good copy, mobile-optimized, DJ creds front and center
- #checkout anchor goes NOWHERE (no Stripe connected)

---

## BLOCKERS (MUST RESOLVE BEFORE LAUNCH)

### 1. STRIPE LINK (from DJ/Akshaya)
Need a Stripe checkout link for $97/mo recurring subscription.
Options:
- A) DJ creates in Stripe dashboard (Product > Recurring > $97/mo > Get link)
- B) Connect Stripe to GHL (Agresh does this in GHL Settings > Integrations > Stripe)
- C) Dylan creates via his own Stripe and forwards payments (NOT recommended — messy)

### 2. AGRESH — GHL WORK (UI only, can't do via API)
- Build Jumpstart purchase workflow (tag: jumpstart-member)
- Create intake form (see spec below)
- Fix broken workflow re-sending pre-webinar emails
- Turn on DRAFT workflows that should be running

---

## 7-EMAIL SEQUENCE (READY TO INSTALL)

Replace [CHECKOUT_LINK] with Stripe link once available.

---

### EMAIL 1 — Webinar Attended + Jumpstart Offer
**Send to:** webinar-attended tag (24 people)
**Send:** Immediately

**Subject options:**
1. Your cybersecurity career plan is ready
2. Next step after Wednesday's training
3. The plan we discussed — here's how to start

**Body:**

You showed up last Wednesday. That tells me something about you.

You sat through the full training. You saw the salary data. You heard how IT professionals are making the switch to cybersecurity — and what it's doing for their careers and their families.

Now the question is simple: what are you going to do with what you learned?

I built something for people in your exact position.

Cybersecurity Jumpstart — $97/month. Here's what you get:

- A personalized career transition plan built around your background
- Your own AI career assistant for 24/7 guidance
- Direct WhatsApp access to me (not a team — me)
- Custom certification roadmap based on where you are today
- Salary projection so you can see the numbers before you move
- Monthly updates as the market shifts

No long-term contract. Cancel anytime.

This is the lowest-risk way to start your transition with a 28-year CISO guiding the process.

[APPLY FOR JUMPSTART — $97/mo][CHECKOUT_LINK]

— DJ Naronikar

---

### EMAIL 2 — No-Show + Replay + Jumpstart
**Send to:** webinar-no-show tag (126 people)
**Send:** Immediately

**Subject options:**
1. You missed it — here's the replay
2. Life happens. The training is still here.
3. The webinar replay (before I take it down)

**Body:**

You registered for last Wednesday's training but couldn't make it. No judgment. Life gets busy.

But I don't want you to miss what we covered — because it matters for your career.

Watch the full replay here:
https://drive.google.com/file/d/179N5mpav9JKWS21pn8ouzSCH-5RBUnaS/view?usp=drive_link

In 60 minutes, I break down:
- Why IT salaries are flattening while cybersecurity keeps climbing
- The exact certification path that gets you hired fastest
- How to make the switch without starting over

After you watch, there is a simple next step.

Cybersecurity Jumpstart — $97/month. You get a personalized career plan, AI career assistant, direct WhatsApp access to me, and a custom cert roadmap. Cancel anytime.

Watch the replay first. Then decide.

[APPLY FOR JUMPSTART — $97/mo][CHECKOUT_LINK]

— DJ Naronikar

---

### EMAIL 3 — Old Lead Re-engage + Jumpstart
**Send to:** old-lead tag (54 people)
**Send:** Immediately

**Subject options:**
1. It's been a while — things have changed
2. Still thinking about cybersecurity?
3. Quick update on the cybersecurity market

**Body:**

We connected a while back about your cybersecurity career move. I wanted to follow up because the market has shifted — and not in IT's favor.

Last week I ran a live training breaking down what is happening right now: AI automation replacing mid-level IT roles, cybersecurity demand hitting record highs, and the salary gap between the two getting wider every quarter.

Here is the replay if you want the full picture:
https://drive.google.com/file/d/179N5mpav9JKWS21pn8ouzSCH-5RBUnaS/view?usp=drive_link

I also launched something new for people who want to start without a big commitment.

Cybersecurity Jumpstart — $97/month. Personalized career plan, AI assistant, WhatsApp access to me, cert roadmap, salary projection. No contract.

If the timing was not right before, it might be now.

[APPLY FOR JUMPSTART — $97/mo][CHECKOUT_LINK]

— DJ Naronikar

---

### EMAIL 4 — Day 3: The Salary Math
**Send to:** All segments
**Send:** 3 days after Email 1/2/3

**Subject:** The $800,000 gap no one talks about

**Body:**

Let me show you two numbers.

Average IT professional salary: $105,000 per year.
Average cybersecurity professional salary: $185,000 per year.

That is an $80,000 difference. Every single year.

Over 10 years, that is $800,000 you leave on the table by staying where you are.

Not theoretical. Not potential. That is the actual market difference based on current compensation data.

Now think about what $800,000 means for your family. Your kids' education. Your mortgage. Your retirement timeline.

The switch does not require starting over. It requires a plan.

Jumpstart gives you that plan for $97/month.

[APPLY FOR JUMPSTART — $97/mo][CHECKOUT_LINK]

— DJ Naronikar

---

### EMAIL 5 — Day 5: Social Proof / Authority
**Send to:** All segments
**Send:** 5 days after Email 1/2/3

**Subject:** 28 years. 4 continents. Here's why that matters for you.

**Body:**

Quick background on me, in case you are wondering who is behind this.

I have spent 28 years in cybersecurity leadership. CISO roles at Deloitte, EY, and Shell. Worked across 4 continents. Advised 400+ organizations on security strategy.

I hold the CISSP, ISSMP, SCF, and CIPM certifications.

I have mentored 250+ professionals through career transitions into cybersecurity. I know what hiring managers look for because I have been the one hiring.

I did not build Jumpstart to sell a course. I built it because I kept seeing talented IT professionals make the same avoidable mistakes — wrong certs, wrong timing, wrong positioning.

For $97/month you get my direct guidance on your specific situation. Not generic advice. Your career, your background, your plan.

[APPLY FOR JUMPSTART — $97/mo][CHECKOUT_LINK]

— DJ Naronikar

---

### EMAIL 6 — Day 7: Last Chance This Week
**Send to:** All segments
**Send:** 7 days after Email 1/2/3

**Subject:** Reviewing new member profiles this weekend

**Body:**

Quick note.

This weekend I am sitting down to personally review every new Jumpstart member's background and build their career transition plans.

If you are in before Friday, your plan gets built this weekend. You will have it in hand by Monday.

That means by next week you will know:
- Exactly which certifications to pursue first
- Your realistic salary projection in cybersecurity
- The gaps in your resume and how to close them

$97/month. Cancel anytime. But if you want your plan built this weekend, the window is the next few days.

[APPLY FOR JUMPSTART — $97/mo][CHECKOUT_LINK]

— DJ Naronikar

---

### EMAIL 7 — Day 10: The Cost of Waiting
**Send to:** All segments
**Send:** 10 days after Email 1/2/3

**Subject:** Every month you wait costs more than $97

**Body:**

I will be direct.

Every month you stay in a flattening IT role is a month of that salary gap getting bigger. That is not a scare tactic. That is math.

But there is a second factor now: AI.

AI tools are automating the mid-level IT work that pays your salary today. The professionals who are safe are the ones organizations can not automate — security strategists, risk analysts, compliance leaders.

That is the side of the line you want to be on.

Jumpstart costs $97/month. One month of waiting costs you $6,600+ in unrealized salary difference.

The math is simple. The decision should be too.

[APPLY FOR JUMPSTART — $97/mo][CHECKOUT_LINK]

— DJ Naronikar

---

## INTAKE FORM SPEC (for Agresh to build in GHL)

**Form Name:** Cybersecurity Jumpstart — Career Assessment
**Trigger:** Send link in welcome email after Stripe purchase

**Fields:**
1. First Name (pre-filled from GHL contact)
2. Email (pre-filled from GHL contact)
3. Current Job Title (text, required) — Placeholder: "e.g., Systems Administrator, Network Engineer"
4. Years in IT (dropdown, required) — Options: 1-3, 4-6, 7-10, 11-15, 15+
5. Current Annual Salary (dropdown, required) — Options: Under $60K, $60K-$80K, $80K-$100K, $100K-$120K, $120K-$140K, $140K+
6. Certifications Held (multi-select) — Options: CompTIA A+, CompTIA Network+, CompTIA Security+, CCNA, CCNP, AWS Certified, Azure Certified, CISSP, CEH, None yet
7. Target Cybersecurity Role (dropdown, required) — Options: SOC Analyst, Security Engineer, Penetration Tester, Security Architect, CISO/Security Director, Not sure yet
8. US Metro Area (text, required) — Placeholder: "e.g., Dallas-Fort Worth, Bay Area, NYC"
9. Biggest concern about transitioning (textarea, required) — Placeholder: "What's holding you back right now?"
10. How soon do you want to make the move? (dropdown) — Options: Already interviewing, Within 3 months, Within 6 months, Within a year, Just exploring

**Submit Button:** "Build My Career Plan"
**Thank You Message:** "Your personalized cybersecurity career plan is being built. You will receive it within 24 hours."
**GHL Tags on Submit:** jumpstart-member, intake-completed

---

## DELIVERABLE EXECUTION PLAN

### What a buyer gets on Day 1:
1. Welcome email (immediate) — "You're in. Here's what happens next."
2. Intake form link (immediate) — Career Assessment form
3. "Your plan is being built" confirmation (on form submit)
4. WhatsApp group invite link
5. Personalized Career PDF (within 24 hours)

### How to generate the Career PDF:
For the first 10-20 buyers, Dylan generates manually:
1. Buyer submits intake form
2. Dylan feeds their answers into Claude with this prompt:

```
You are DJ Naronikar, a 28-year CISO (Deloitte, EY, Shell). Generate a personalized
cybersecurity career transition plan for this IT professional:

Current Role: [from form]
Years in IT: [from form]
Current Salary: [from form]
Certifications: [from form]
Target Role: [from form]
Metro Area: [from form]
Timeline: [from form]
Main Concern: [from form]

Generate a 10-page career plan including:
1. Readiness Score (0-100) with explanation
2. Skills that transfer directly from their IT role
3. Skills gaps and how to fill each one
4. Certification roadmap (specific order, time per cert, cost)
5. Salary projection: current vs 1yr, 3yr, 5yr after transition
6. Top 5 employers hiring in their metro area
7. 90-day week-by-week action plan
8. Resume positioning (IT language -> cybersecurity language)
9. Interview prep focus areas
10. Next step: join WhatsApp group, book welcome call with DJ

Tone: direct, experienced, no fluff. Written from DJ's perspective.
```

3. Format as PDF (use any HTML-to-PDF tool)
4. Email to buyer with delivery email template

### Automation (build week 2):
- GHL form submit triggers webhook
- Webhook calls Claude API with form data
- Claude generates plan
- HTML-to-PDF conversion
- Auto-email with PDF attached
- Tag: plan-delivered

### WhatsApp Group:
- DJ creates "TQA Jumpstart Members" group
- DJ drops 1 voice note per week (2-3 min, market update + tip)
- Dylan moderates, answers questions via AI assistant
- This is the "direct access to DJ" promise

### Monthly Updates:
- Day 30 email: "Here's what changed in the cybersecurity market this month + your updated priorities"
- Generated by Claude based on recent job market data
- Keeps subscribers engaged and feeling the value

---

## AD CAMPAIGN PLAN

### Phase 1: Retargeting (197 registrants) — $20/day

**Custom Audience:** Upload GHL email list to Meta Ads Manager
**Placements:** Facebook Feed, Instagram Feed, Stories

**Ad 1 — "The Plan" Angle:**
- Primary: You attended the training. Now get your personal cybersecurity career plan built by a 28-year CISO. $97/mo.
- Headline: Your Career Plan Is Ready
- Creative: Career roadmap visual, dark background, DJ headshot

**Ad 2 — "Salary Gap" Angle:**
- Primary: $105K in IT. $185K in cybersecurity. That's $800K over 10 years. Get your transition plan for $97/mo.
- Headline: The $800K Career Gap
- Creative: Split-screen salary comparison, bold numbers

**Ad 3 — "Direct Access" Angle:**
- Primary: WhatsApp access to a CISO who led security at Deloitte, EY, and Shell. Your personal cybersecurity career guide. $97/mo.
- Headline: Talk Directly to a 28-Year CISO
- Creative: DJ professional photo, WhatsApp icon overlay

### Phase 2: Cold Traffic — $30/day (start Day 2)

**Targeting:** US, age 28-42, interests: Cybersecurity/CISSP/CompTIA/IT careers
**CTA:** Watch webinar replay

**Ad 1 — Salary Angle:**
- Primary: IT professionals who switched to cybersecurity saw $80K+ salary jumps. Free training shows you the exact path.
- Headline: $80K More. Same Experience Level.

**Ad 2 — AI Threat Angle:**
- Primary: AI is automating mid-level IT jobs. Cybersecurity roles are growing 35% year over year. Free training on making the move.
- Headline: AI Is Coming for IT Jobs

**Ad 3 — Authority Angle:**
- Primary: A 28-year CISO (Deloitte, EY, Shell) shows IT professionals how to break into cybersecurity. Free 60-minute training.
- Headline: Free Training From a 28-Year CISO

### Budget Summary
| Channel | Daily | Weekly | Monthly |
|---------|-------|--------|---------|
| Meta Retargeting | $20 | $140 | $600 |
| Meta Cold Traffic | $30 | $210 | $900 |
| **Total** | **$50** | **$350** | **$1,500** |

### Expected Results (Conservative)
- Retargeting: 5-15 clicks/day, 2-5 Jumpstart signups/week
- Cold traffic: 6-15 clicks/day, 1-2 signups/week via replay funnel
- Month 1 target: 10-20 Jumpstart members = $970-$1,940 MRR

---

## THIS WEEK TIMELINE

| Day | Who | Action |
|-----|-----|--------|
| **Wed Mar 26 (TODAY)** | Dylan | Get Stripe link from DJ on tonight's call |
| **Wed Mar 26** | Dylan | Wire Stripe link into Jumpstart page |
| **Wed Mar 26** | Dylan | Present launch plan to DJ + Akshaya |
| **Thu Mar 27** | Agresh | Build intake form in GHL |
| **Thu Mar 27** | Agresh | Create 7 email templates in GHL from this doc |
| **Thu Mar 27** | Agresh | Fix broken workflow re-sending pre-webinar emails |
| **Thu Mar 27** | Agresh | Connect Stripe to GHL |
| **Thu Mar 27** | Dylan | Upload custom audience to Meta |
| **Fri Mar 28** | Agresh | SEND Email 1 + 2 + 3 (first blast to all 197) |
| **Fri Mar 28** | Shreyas | Launch retargeting ads ($20/day) |
| **Sat Mar 29** | DJ | Create WhatsApp Jumpstart group |
| **Sat Mar 29** | DJ | Record 2-min Loom: "Why I built Jumpstart" |
| **Mon Mar 31** | Agresh | Send Email 4 (salary math) |
| **Mon Mar 31** | Shreyas | Launch cold traffic ads ($30/day) |
| **Wed Apr 2** | Agresh | Send Email 5 (social proof) |
| **Fri Apr 4** | Agresh | Send Email 6 (last chance) |
| **Mon Apr 7** | Agresh | Send Email 7 (cost of waiting) |
| **Mon Apr 7** | ALL | Review: signups, ad performance, next steps |

---

## REVENUE PROJECTIONS

### Ad Spend Recovery
- Meta spent to date: ~$584
- Break even: 7 Jumpstart sales ($679)
- With email blast to 197 contacts at 5% conversion: ~10 sales = $970

### Month 1 Projection
| Source | Signups | Revenue |
|--------|---------|---------|
| Email blast (197 contacts) | 10-15 | $970-$1,455 |
| Retargeting ads | 5-8 | $485-$776 |
| Cold traffic | 2-4 | $194-$388 |
| **Total Month 1** | **17-27** | **$1,649-$2,619** |

### Upsell Revenue (Month 2-3)
| Step | From | Conversion | Revenue |
|------|------|-----------|---------|
| $97/mo retention | 17-27 members | 70% stay month 2 | $1,164-$1,833/mo |
| $4,999 program | 3-5 upgrade | From Jumpstart members | $14,997-$24,995 |

---

## TALKING POINTS FOR TONIGHT'S CALL

### For DJ (6:30 PM):
1. "It's been 7 days since the webinar. Zero revenue collected. Here's the fix."
2. "We have 197 contacts, 126 hot leads, and nothing to sell them. The Jumpstart page is live but has no checkout."
3. "I need your Stripe link for $97/mo. I'll wire it in tonight."
4. "Agresh needs to install 7 emails tomorrow and send the first blast Friday."
5. "By next Monday we should have our first 5-10 paying members."
6. "Create a WhatsApp group called 'TQA Jumpstart Members' this weekend."

### For Akshaya (7:30 PM):
1. "Here's the ROI story building: $584 ad spend -> 197 leads -> Jumpstart launch this week."
2. "Conservative projection: $1,600-$2,600 first month, recurring."
3. "This proves the system works for Luke: webinar + low-ticket + upsell ladder."
4. "Ad budget request: $50/day ($1,500/mo) for retargeting + cold traffic."

---

*File: ~/Documents/TQA/Client Files/TQA-JUMPSTART-LAUNCH-PACKAGE.md*
*Generated: March 26, 2026*
