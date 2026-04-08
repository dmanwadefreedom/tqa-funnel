# Agresh — Setup Instructions (March 10, 2026)

## 1. RE-ENGAGEMENT PAGE WEBHOOK

Dylan built a re-engagement page for the 80 people who signed up but didn't attend. The form collects 3 questions + name + email. You need to create a webhook to receive this data.

**Steps:**
1. Go to GHL → Automation → Workflows → Create New Workflow
2. Add trigger: **Inbound Webhook**
3. Copy the webhook URL that GHL generates
4. Send the webhook URL to Dylan — he'll paste it into the re-engagement page code
5. Add these workflow steps after the trigger:
   - **Create/Update Contact** → map: first_name, last_name, email, source
   - **Add Tag** → `tqa-reengage`
   - **Add Tag** → `tqa-webinar-mar19`
   - **Add to workflow** → put them into the webinar reminder sequence
   - **Internal notification** → notify DJ that a re-engagement submission came in
6. **Publish the workflow**

The form sends this data:
```
{
  "first_name": "...",
  "last_name": "...",
  "email": "...",
  "source": "TQA Re-engagement Page",
  "reengage_q1_why_missed": "forgot | timing | uncertain | unsure",
  "reengage_q2_interest_level": "ready | exploring | later | moved_on",
  "reengage_q3_question_for_dj": "free text answer"
}
```

You can create custom fields for q1/q2/q3 if you want to store them on the contact record.

---

## 2. RE-ENGAGEMENT EMAIL SEQUENCE (3 emails for the 80 no-shows)

Once the 80 leads are imported into GHL (Shreyas needs to do the CSV upload), trigger this sequence. Create a new workflow with trigger: Tag Applied → `old-lead`

### Email 1 — Day 0 (immediately after import)
**Subject:** your cybersecurity seat is still open
**From:** DJ Naronikar <achieversquantum@gmail.com>

Body:
```
Hey {{contact.first_name}},

You signed up for the cybersecurity webinar a while back. Life happened — I get it.

I'm not writing to chase you. I just know the question doesn't go away: "Is a move into cybersecurity actually possible for me?"

I'm running another session on March 19 at 11 AM EST. Before I add you, I want to understand where you actually are right now.

3 quick questions. 2 minutes. No sales call waiting at the end.

→ [LINK TO RE-ENGAGEMENT PAGE]

— DJ
```

### Email 2 — Day 2
**Subject:** still thinking about the switch?
**From:** DJ Naronikar <achieversquantum@gmail.com>

Body:
```
{{contact.first_name}} —

One question: is cybersecurity still something you're thinking about?

If yes → I have a seat for you on March 19. Just need 2 minutes of your time first:
→ [LINK TO RE-ENGAGEMENT PAGE]

If no → no hard feelings. I'll stop reaching out.

— DJ
```

### Email 3 — Day 5
**Subject:** last call — march 19
**From:** DJ Naronikar <achieversquantum@gmail.com>

Body:
```
{{contact.first_name}},

This is my last email about this.

March 19, 11 AM EST — free live webinar. The exact path from IT to cybersecurity leadership. From someone who's been CISO at Deloitte, EY, and Shell.

If the timing is right: → [LINK TO RE-ENGAGEMENT PAGE]

If not, I respect that. You won't hear from me again on this.

— DJ Naronikar
28 years in cybersecurity. 400+ organisations. 4 continents.
```

---

## 3. SPLIT TEST LANDING PAGE

Dylan built a new version of the landing page (tqa-landing-v3.html) with:
- DJ's real event photos embedded (CIO Choice 2026, speaking, awards)
- Photo gallery section
- Trusted-by logo bar (Deloitte, ANZ)
- Same dark/gold luxury styling

**This was supposed to be added as a split test against the current thequantumachievers.com page. It hasn't been done yet.**

Options:
- A) Add as a new page in GHL funnels and split traffic 50/50
- B) Replace the current page entirely (if current conversion rate is unknown/low)
- C) Deploy to a subdomain or Netlify for A/B testing outside GHL

The HTML file is self-contained (all images are base64 embedded). It can be dropped into any hosting. Dylan will share the file.

---

## 4. THINGS THAT ARE STILL MISSING IN GHL

From the audit:

| Issue | Priority |
|-------|----------|
| `WF1 – Meta Lead Registration` is in DRAFT | HIGH — publish before ads launch |
| 8 template workflows from Dec 2025 still in project | LOW — delete them (they're junk) |
| No custom TQA funnel page in GHL | MEDIUM — using WordPress site directly |
| Location email is extromarketingagency@gmail.com | LOW — cosmetic |
| Post-webinar Zoom attendance automation | MEDIUM — Dylan is building this |

---

## 5. REMINDERS

- GHL timezone has been fixed to EST ✓
- The GHL form on thequantumachievers.com is working ✓
- Pre-webinar reminders (24hr, 1hr, 10min) are working ✓
- Scoring workflow is published and working ✓
- **Webinar is March 19 — 9 days away**
