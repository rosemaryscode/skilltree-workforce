---
schema: agentcompanies/v1
kind: skill
name: "Meeting Booking"
slug: meeting-booking
description: "Get a qualified prospect on the calendar with the right person, fast."
metadata:
  department: deals
  autonomy: ai-drafts
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Deals  |  **Autonomy:** `ai-drafts`  |  **Cadence:** daily
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Meeting Booking

## Job
Get a qualified prospect on the calendar with the right person, fast.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read routed leads and their briefs.
2. Offer 2-3 concrete times; handle reschedules.
3. Confirm with agenda and pre-call questions.
4. Log bookings to your task result (`meeting-booking.md`).

## Outputs
| Artifact | Location |
|---|---|
| meeting-booking.md | `meeting-booking.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
