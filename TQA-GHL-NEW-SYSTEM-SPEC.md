# TQA GHL System Spec — The Clean Machine
## For Agresh: Build This Exactly. No Improvising.
## April 2, 2026

---

## WHAT DJ SHOULD SEE WHEN HE OPENS GHL

1. **Dashboard:** Pipeline with real numbers — 6 Applied ($15K), 7 Attended ($7K), 53 No Shows ($1.4K in briefing potential)
2. **Contacts:** Everyone tagged, segmented, assigned. No mystery leads.
3. **Workflows:** Clean automation running — new leads get nurtured, briefing registrants get prepped, post-briefing gets followed up. All automatic.
4. **Calendar:** Two options — Career Briefing (April 11) and Strategy Call (for Jay). Nothing else.
5. **Social:** LinkedIn connected. Posts scheduling from GHL.

DJ should NOT see: 10 calendars, 11 draft workflows, unassigned contacts, $0 pipeline, or extromarketingagency in the from field.

---

## STEP 1: FIX THE FOUNDATION (Agresh — 15 min)

### Timezone
- **Current:** America/Detroit
- **Change to:** America/New_York (briefings are 11 AM EST)
- Location Settings → General → Timezone

### From Email
- **Current:** extromarketingagency@gmail.com
- **Change to:** achieversquantum@gmail.com (or thequantumachievers@gmail.com)
- Location Settings → Business Info → Email
- Also update the "From Name" to "DJ Naronikar" or "The Quantum Achievers"

### Website
- **Current:** blank
- **Change to:** https://dmanwadefreedom.github.io/tqa-jumpstart/

---

## STEP 2: SIMPLIFY CALENDARS (Agresh — 10 min)

### Keep:
- **TQA Strategy Call** (id: 7c8TNv6D52KfbWXwPybk) — Jay books these after briefings
- **DJ's Personal Calendar** (id: 4ST14Q1ZC2o2w52seU96) — DJ's availability

### Delete:
- Career Assessment and Exploration
- Career Planning and Goal Setting
- Career Discovery
- Interview Preparation and Practice
- Schedule an Appointment
- Dylan W's Personal Calendar
- Shreyas B's Personal Calendar
- Agresh K's Personal Calendar (optional — keep if Agresh needs it for admin)

---

## STEP 3: THE NEW PIPELINE (Agresh — 20 min)

### Rename "Webinar Funnel" → "Career Briefing Funnel"

### New Stages (in order):

| Stage | What it means | Value | Who owns |
|-------|--------------|-------|----------|
| New Lead | Just entered system (Meta ad, LinkedIn, organic) | $0 | Automation |
| Briefing Registered | Paid $27, registered for April 11 | $27 | Automation |
| Briefing Attended | Showed up on April 11 | $27 | Jay |
| Briefing No Show | Registered but didn't attend | $27 | Automation |
| Accelerator Applied | Applied for $997 program | $997 | Jay |
| Accelerator Enrolled | Paid $997 (or started payment plan) | $997 | DJ |
| CISO Track Applied | Applied for $4,999+ tier | $4,999 | DJ |
| CISO Track Enrolled | Paid $4,999+ | $4,999 | DJ |
| Not a Fit | Disqualified or not interested | $0 | Archive |

### Keep the "Students" pipeline as-is — it will be used once people actually enroll.
### Delete or archive the "Marketing Pipeline" — it's empty and redundant.

### Current Pipeline Status (already cleaned via API):
- 6 contacts in "Applied" ($2,500 each — Sprint offer)
- 7 contacts in "Webinar Attended" ($997 each)
- 53 contacts in "Webinar No Show" ($27 each)
- Remaining contacts in "New Lead"

---

## STEP 4: THE WORKFLOW MAP (Agresh — 2-3 hours)

### Delete or archive these draft workflows:
- "1. New Lead Nurture (Fast 5) - Claim Offer" — replace with our new sequence
- "2. Appointment Confirmation + Reminders" — replace
- "3. Appt No Show" — replace
- "4. New Sale - Send Review Request" — premature
- "5. Long-Term Nurture" — replace with our Phase 2 value emails
- "6. Stale Leads" — replace with our cleanup email
- "TQA – Assign Webinar Date" — replace
- "WF1 – Meta Lead Registration" — replace with new version
- "TQA-Post Call — Payment Follow Up" — replace
- "TQA-Temporary Reminder" — delete (unknown purpose)

### Update these published workflows:
- **"TQA – Webinar Confirmation & Reminders"** → Change March 19 → April 11. Update Zoom link. Update from "masterclass" to "Career Briefing."
- **"TQA-Post Webinar — Attendees"** → Add Accelerator link (dmanwadefreedom.github.io/tqa-jumpstart/accelerator.html). Add Stripe checkout link when DJ creates it.
- **"TQA-Post Webinar — No Show"** → Add next briefing invite. Remove guilt language.

### Build these NEW workflows (using the 18-email copy from TQA-FULL-EMAIL-SEQUENCE.md):

**Workflow A: April Reactivation (trigger: manual or tag tqa-april11-funnel)**
- Email 1A → applicants (tag: tqa-reactivate-applicant)
- Email 1B → attended (tag: tqa-reactivate-attended)
- Email 1C → hot no-shows (tag: tqa-reactivate-hot-noshow)
- Email 1D → warm/cold/old (tag: tqa-reactivate-warm OR tqa-reactivate-cleanup)
- Wait 3 days
- If opened → add tag: tqa-engaged-april
- If not opened → re-send with different subject line

**Workflow B: Value Sequence (trigger: tag tqa-engaged-april)**
- Email 2A: "The 3 certifications that actually matter"
- Wait 2 days
- Email 2B: "What a hiring CISO sees on your LinkedIn"
- Wait 2 days
- Email 3A: "April 11: Cybersecurity Career Briefing"
- Tag: tqa-briefing-invited

**Workflow C: Briefing Registration (trigger: form submission or tag tqa-briefing-registrant)**
- Immediately: Confirmation email + trust video link + Zoom link
- Immediately: Confirmation SMS
- Wait: based on registration date
- Day 1: Email 4B (3 mistakes email)
- Day 2: Email 4C (Rob G case study)
- Day 3: Email 4D (AI urgency)
- Morning of April 11: Email 4E (we're live) + SMS
- -1 hour: SMS reminder
- -5 min: SMS "starting now"

**Workflow D: Post-Briefing Attendees (trigger: tag tqa-briefing-attended)**
- Within 2 hours: Email 5A (thanks + Accelerator link) + SMS
- Day 1: Email 5B (one insight + Accelerator link)
- Day 3: Email 5C (enrollment closing for this cohort)
- Day 5: Email 5D (doors closed, waitlist)
- Also: trigger VAPI Priya call within 24 hours (if VAPI is wired)

**Workflow E: Post-Briefing No Show (trigger: tag tqa-briefing-noshow)**
- Same day: Email 5E (missed you, key takeaway, next briefing invite) + SMS
- Move to long-term nurture

**Workflow F: New Meta Lead (trigger: form submission from Meta ad)**
- Immediately: Welcome email + quiz link or briefing invite
- Tag: meta-lead-april
- Enter Workflow B (Value Sequence)

**Workflow G: Long-Term Nurture (trigger: didn't buy after briefing, or cold leads)**
- Weekly value email (cybersecurity news, career tips — use LinkedIn post content)
- Every 3-4 weeks: next briefing invite
- After 90 days with no engagement: tag tqa-inactive, stop emails

---

## STEP 5: FORMS UPDATE (Agresh — 15 min)

### Update "TQA – Webinar Registration":
- Change all March 19 references to April 11
- Change "masterclass" to "Career Briefing"
- Add phone + SMS consent field
- Redirect after submit: Stripe $27 payment link (DJ creates this)
- On submit: tag tqa-briefing-registrant, enter Workflow C

### Update "TQA-Strategy Application":
- Change CTA link to: dmanwadefreedom.github.io/tqa-jumpstart/accelerator.html
- On submit: tag tqa-accelerator-applied, move to "Accelerator Applied" pipeline stage
- Notify Jay + DJ

### Audit "Form 2":
- If unused → delete
- If it's the claim offer form → update or merge into Meta Lead form

---

## STEP 6: CONTACT ASSIGNMENT (ALREADY DONE VIA API)

| Segment | Assigned To | Pipeline Stage |
|---------|-------------|---------------|
| 6 Applicants | DJ (WhatsApp outreach) | Applied ($2,500) |
| 7 Attended | Jay (Strategy call) | Webinar Attended ($997) |
| 53 Hot No-Shows | Automation (email sequence) | No Show ($27) |
| 24 Old/Cleanup | Automation (cleanup email) | New Lead ($0) |
| 10 Other | Automation | New Lead ($0) |

---

## STEP 7: CONNECT SOCIAL ACCOUNTS (DJ — 5 min)

In GHL Settings → Social Planner:
1. Connect LinkedIn (DJ's personal profile)
2. Connect Facebook (CISO360 page)
3. Optional: Connect Twitter/X

Once connected, the 10 LinkedIn posts we wrote can be scheduled directly from GHL.

---

## STEP 8: STRIPE INTEGRATION (DJ — 10 min)

DJ creates these Stripe payment links:
1. **$27 Career Briefing** — one-time payment
2. **$997 Accelerator** — one-time payment
3. **$347 x 3** — Accelerator payment plan
4. **$2,500 Sprint** — one-time (for the 6 applicants)

Then paste the links into:
- Briefing registration form (redirect after submit)
- Accelerator offer page (application form redirect)
- Post-webinar emails (CTA buttons)
- WhatsApp messages (Sprint offer)

---

## WHAT THE SYSTEM LOOKS LIKE WHEN IT'S DONE

```
Meta Ad / LinkedIn / YouTube content
        |
        v
New lead enters GHL → tagged → enters Value Sequence
        |
        v
Engaged? → Briefing invite email
        |
        v
Registers ($27) → Confirmation + Trust Video + SMS
        |
        v
Pre-briefing nurture (4 emails + SMS reminders)
        |
        v
APRIL 11 BRIEFING (DJ teaches, Jay is in chat)
        |
    +---+---+
    |       |
Attended    No Show
    |          |
    v          v
Post-briefing   "Missed you" email
follow-up       + next briefing invite
(5 emails +
VAPI call +
Jay strategy calls)
    |
    v
Accelerator Applied → Jay qualifies → Enrolled ($997)
    |
    v
90-day program → success → testimonial
    |
    v
Optional: CISO Track upgrade ($4,999+)
```

**Every step is automated except:**
- DJ's WhatsApp messages to applicants (personal touch)
- DJ's briefing presentation (live, can't automate)
- Jay's strategy calls (human closes better than bots for $997+)

Everything else runs on GHL workflows. DJ opens his dashboard and sees leads moving through the pipeline. No manual email sending. No guessing who to follow up with. The system handles it.
