# Impromptu Call: Dylan + Agresh — March 9, 2026
**Duration:** 7 min | **Source:** Fathom

---

## Key Outcomes
- Agresh created GHL API key for Dylan's AI system (TQA subaccount): `pit-0943cadd-0c8f-4fec-9da7-b7c08562d304` (updated March 16 — previous keys expired)
- Pre-webinar automation is DONE (scoring, reminder emails, workflows)
- Post-webinar automation NOT done yet — Zoom attendance tracking is the blocker

## Zoom + GHL Integration Issue
- Agresh can't easily automate Zoom attendance tracking in GHL
- Options discussed:
  1. Manually pull attendance from Zoom, upload to GHL, manual tagging (Agresh's current plan)
  2. Connect Zoom + GHL via webhook/API (better but harder)
  3. Create GHL calendar + Zoom integration (partial solution)
- **Dylan said he'll build an AI to monitor and self-correct this** — told Agresh to give him a day

## What Agresh Built (already working)
- Pre-webinar email sequence with reminder timing (24hr, 1hr, 10min)
- "Add to Calendar" link using addevent.com → short link in emails
- Two GHL custom values: webinar_calendar_link + zoom_link (recurring meeting)
- For future webinars: only need to change the date in automation + create new addevent calendar event
- GHL form embedded on thequantumachievers.com
- Tested from 2 accounts — emails working fine

## Action Items
- Dylan: analyze GHL via API, update Agresh with any changes needed
- Dylan: build post-webinar attendance automation
- Agresh: document all automations/emails in one place
- For next webinar: only change date + addevent link (everything else reusable)
