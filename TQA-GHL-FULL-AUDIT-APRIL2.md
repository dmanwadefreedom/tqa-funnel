# TQA GHL Full Audit — April 2, 2026
## Location: cv0yehFtVK84960e2GsO
## Status: HALF-BUILT, COLD, NEEDS MAJOR CLEANUP

---

## CRITICAL ISSUES (fix these first)

### 1. TIMEZONE IS WRONG
- GHL is set to **America/Detroit**
- DJ is in **Australia**. Audience is **US-based (EST)**
- This CAUSED the March 19 webinar timezone errors
- **FIX:** Change to America/New_York (EST) since briefings are at 11 AM EST

### 2. FROM-EMAIL IS WRONG
- Emails are sent from **extromarketingagency@gmail.com**
- That is Agresh's agency email, not TQA
- Recipients see "extromarketingagency" — looks like spam
- **FIX:** Change to achieversquantum@gmail.com or a branded TQA email (thequantumachievers@gmail.com)

### 3. ALL 6 APPLICANTS ARE STUCK
- Sonny Pierre, Ejaz Khan, Muhammad Mazed, Rama Krishna, Shafiul Kh, Kenny Ganta
- All sitting in the SAME pipeline stage since March 16-23
- Status: "open." Value: $0. Nobody moved them. Nobody called them.
- **They have been waiting 2+ weeks for someone to follow up.**
- **FIX:** DJ WhatsApps them TODAY. Move them to "Applied" stage. Assign to DJ.

### 4. SYSTEM IS COLD — NOTHING SINCE MARCH 26
- Last email sent: March 26 (generic re-engagement blast to old leads)
- Zero replies from any contact
- Zero conversations since then
- The leads are going stale fast
- **FIX:** Fire the reactivation emails NOW

### 5. ALL 100 CONTACTS ARE UNASSIGNED
- Nobody owns these leads. Not DJ, not Agresh, not Jay.
- **FIX:** Assign applicants + attended to DJ. Assign hot no-shows to Agresh. Assign old leads to cleanup automation.

### 6. NO SOCIAL ACCOUNTS CONNECTED
- Cannot post to Facebook, Instagram, or LinkedIn from GHL
- All social posting is manual
- **FIX:** Connect DJ's social accounts (at minimum LinkedIn and Facebook)

---

## PIPELINE STATUS

| Pipeline | Opportunities | Value | Status |
|----------|--------------|-------|--------|
| Marketing | 0 | $0 | Empty — never used |
| Students | 0 | $0 | Empty — nobody has ever paid |
| Webinar Funnel | 100 | $0 | All "open," nobody moved through stages |

**The Webinar Funnel has stages for:** New Lead → Reminder → Attended → No Show → Applied → Paid 1:1 → Enrolled

**Reality:** 100 contacts are in the funnel. All are sitting in the same early stage. Zero have progressed to "Paid" or "Enrolled." The pipeline exists but nobody is managing it.

---

## WORKFLOW STATUS

### Running (6 published):
| Workflow | What it does | Problem |
|----------|-------------|---------|
| Application Processing | Processes new applications | Working but nobody has applied since March 19 |
| Old Lead Re-engagement | Sends re-engage emails | Sent March 26 blast — zero replies |
| Re-engagement Webhook | Handles re-engage form submissions | Working |
| Score Registration | Scores leads on signup (0-12 points) | Working — the lead scoring is solid |
| Webinar Confirmation & Reminders | Sends confirmation + reminders for webinar | Still configured for March 19 — NEEDS UPDATE to April 11 |
| Post Webinar Attendees | Follows up with people who attended | Running but has NO offer links, NO checkout URL |
| Post Webinar No Show | Follows up with no-shows | Running but has NO offer links |
| Temporary Reminder | Unknown purpose | Should audit and probably delete |

### Not Running (11 in draft):
| Workflow | What it should do | Why it matters |
|----------|------------------|---------------|
| New Lead Nurture (Fast 5) | Welcome sequence for new leads | CRITICAL — new leads get nothing right now |
| Appointment Confirmation | Confirm booked calls | Needed for strategy calls with Jay |
| Appt No Show | Follow up on missed calls | Needed |
| Long-Term Nurture | Ongoing email nurture | CRITICAL — leads that don't buy immediately need this |
| Stale Leads | Re-engage or clean old leads | Needed for list hygiene |
| Assign Webinar Date | Set webinar date on contact | Needs update for April 11 |
| Post Call Payment Follow Up | Follow up after strategy call | Needed once Jay starts taking calls |
| Meta Lead Registration | Handle new Meta ad leads | CRITICAL — if Shreyas launches ads, new leads get nothing |
| New Sale - Review Request | Ask for reviews after purchase | Premature — no sales yet |

**Bottom line:** The most critical workflows (New Lead Nurture, Meta Lead Registration, Long-Term Nurture) are all sitting in draft. New leads from ads would enter the system and get NOTHING.

---

## CONTACT DATA

### Volume
- **100 contacts pulled** (API pagination caps at 100, GHL says 197 total)
- **ALL created in March 2026** — DJ started from scratch with the March campaign
- **97 have phone numbers** — WhatsApp outreach viable for nearly everyone
- **98 have email**
- **0 on Do Not Disturb** — all contactable

### Sources
| Source | Count | % |
|--------|-------|---|
| Facebook (Meta ads) | 56 | 56% |
| Webinar Registration Form | 19 | 19% |
| Fluent Forms | 10 | 10% |
| Paid | 9 | 9% |
| TQA Re-engagement Page | 2 | 2% |
| Other | 4 | 4% |

### Segments (from our tagging)
| Segment | Count | Tag |
|---------|-------|-----|
| Hot no-shows | 54 | tqa-reactivate-hot-noshow |
| Old/cleanup leads | 24 | tqa-reactivate-cleanup |
| Warm no-shows | 7 | tqa-reactivate-warm |
| Applicants | 6 | tqa-reactivate-applicant |
| Attended | 6 | tqa-reactivate-attended |
| Untagged | 1 | — |
| Re-engage only | 2 | tqa-reengage |

### Tag Mess (duplicates to clean)
- "webinar attended" AND "webinar-attended" — same thing, different format
- "applied" AND "tqa-applied" — same thing
- "webinar no show" AND "webinar-no-show" — same thing
- **FIX:** Standardize on hyphenated format (webinar-attended, tqa-applied, webinar-no-show). Remove space-separated duplicates.

---

## CALENDARS (10 — needs to be 2)

| Calendar | Keep? |
|----------|-------|
| TQA Strategy Call | KEEP — for Jay's post-briefing calls |
| Career Assessment and Exploration | DELETE — merge into Strategy Call |
| Career Planning and Goal Setting | DELETE — merge into Strategy Call |
| Career Discovery | DELETE — merge into Strategy Call |
| Interview Preparation and Practice | DELETE — this is part of the Accelerator, not a standalone booking |
| DJ's Personal Calendar | KEEP — for DJ's availability |
| Agresh's Personal Calendar | Keep if needed for admin |
| Dylan's Personal Calendar | Remove — Dylan doesn't take TQA calls |
| Shreyas's Personal Calendar | Remove — Shreyas doesn't take TQA calls |
| Schedule an Appointment | DELETE — generic, unclear purpose |

**After cleanup: 2 calendars.** TQA Strategy Call (Jay books these) + DJ's Personal Calendar.

---

## FORMS (4)

| Form | Status | Action |
|------|--------|--------|
| TQA-Strategy Application | Active — this is the post-briefing application form | KEEP — update CTA link |
| TQA Webinar Registration | Active — still says March 19 | UPDATE to April 11 briefing |
| Marketing Form - Claim Offer | Active — for Meta ad leads | KEEP — verify it works |
| Form 2 | Unknown | AUDIT — probably delete |

---

## CUSTOM FIELDS (valuable — keep all)

Good data collection setup:
- Years of Experience, Industry, Current Job Title
- Driving interest in cybersecurity (free text — gold for personalization)
- Qualification Score (0-12 numerical)
- Years in IT (multiple choice)
- Investment readiness (multiple choice)
- Video application submitted (checkbox)
- Re-engage fields (why missed, interest level, question for DJ)

**This data is collected but nobody is USING it.** The qualification score exists but no workflow segments by it. The investment readiness field exists but nobody checks it before outreach.

---

## CONVERSATIONS

- 20 total conversations in GHL
- Last activity: March 26, 2026 (7 days ago)
- ALL are outbound emails from the re-engagement blast
- "A lot has changed in cybersecurity since we last connected..."
- **Zero replies. Zero engagement. Zero follow-up.**
- One test email from Dylan (March 26, DJ confirmed "Received")

---

## THE CLEANUP PLAN (for Agresh, ordered by priority)

### TODAY (15 minutes)
1. Fix timezone: America/Detroit → America/New_York
2. Fix from-email: extromarketingagency → achieversquantum@gmail.com
3. Assign 6 applicants to DJ in GHL
4. Move 6 applicants to "Applied" pipeline stage

### THIS WEEK (2-3 hours)
5. Update Webinar Registration form: March 19 → April 11
6. Update Webinar Confirmation workflow: March 19 → April 11, new Zoom link
7. Build the 18-email sequence (Phase 1-5) as new workflows — use our provided copy
8. Clean duplicate tags: remove space-separated versions, keep hyphenated
9. Delete 6 unnecessary calendars (keep Strategy Call + DJ Personal)
10. Delete or archive "Form 2" and "Temporary Reminder" workflow
11. Assign all contacts: hot no-shows → Agresh, old leads → automation

### BEFORE APRIL 11 (1-2 hours)
12. Publish "New Lead Nurture" workflow (critical for new ad leads)
13. Publish "Meta Lead Registration" workflow (critical before Shreyas launches ads)
14. Connect DJ's LinkedIn and Facebook to GHL social planner
15. Add $997 monetary value to Accelerator pipeline stage
16. Wire Stripe checkout links to the post-webinar workflows
17. Test the full flow: register → confirmation email → SMS → briefing → follow-up

---

## WHAT CAN DYLAN DO FROM HIS SIDE RIGHT NOW (via API)

1. **Assign contacts to DJ/Agresh** — API supports bulk contact updates
2. **Clean duplicate tags** — remove old tags, add standardized ones
3. **Move applicants in pipeline** — update opportunity stage
4. **Send the reactivation emails** — trigger via API (or just have Agresh press the button)

Want me to do #1-3 right now via API?
