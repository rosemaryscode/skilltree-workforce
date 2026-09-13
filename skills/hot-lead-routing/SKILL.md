---
schema: agentcompanies/v1
kind: skill
name: "Hot Lead Routing"
slug: hot-lead-routing
description: "Route qualified interest to the right human within minutes, with context attached."
metadata:
  department: deals
  autonomy: ai-drafts
  frequency: hourly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Deals  |  **Autonomy:** `ai-drafts`  |  **Cadence:** hourly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Hot Lead Routing

## Job
Route qualified interest to the right human within minutes, with context attached.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Take interested replies from your task result (`reply-classification.md`).
2. Score urgency; pick the right owner by segment and load.
3. Assemble a one-screen brief: who, what they said, suggested next step.
4. Notify the owner; log to your task result (`hot-lead-routing.md`).

## Outputs
| Artifact | Location |
|---|---|
| hot-lead-routing.md | `hot-lead-routing.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
