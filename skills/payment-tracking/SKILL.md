---
schema: agentcompanies/v1
kind: skill
name: "Payment Tracking"
slug: payment-tracking
description: "Match incoming payments to invoices and update the books."
metadata:
  department: back-office
  autonomy: unattended
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Back Office  |  **Autonomy:** `unattended`  |  **Cadence:** daily
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Payment Tracking

## Job
Match incoming payments to invoices and update the books.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Watch bank feeds for new payments.
2. Match to open invoices; log partials and mismatches.
3. Update the receivables record.
4. Unmatched payments queue for human resolution.

## Outputs
| Artifact | Location |
|---|---|
| payment-tracking.md | `payment-tracking.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
