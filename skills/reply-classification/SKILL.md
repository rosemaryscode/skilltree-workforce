---
schema: agentcompanies/v1
kind: skill
name: "Reply Classification"
slug: reply-classification
description: "Classify every inbound reply as interested, not-now, referral, or unsubscribe."
metadata:
  department: deals
  autonomy: unattended
  frequency: hourly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Deals  |  **Autonomy:** `unattended`  |  **Cadence:** hourly
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Reply Classification

## Job
Classify every inbound reply as interested, not-now, referral, or unsubscribe.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Watch the shared inbox export for new replies.
2. Classify by intent using the company-brain skilloffers.md context.
3. Route: interested -> hot-lead-routing; not-now -> sales/follow-up-nurturing; unsubscribe -> suppress list.
4. Write the log to your task result (`reply-classification.md`).

## Outputs
| Artifact | Location |
|---|---|
| reply-classification.md | `reply-classification.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
