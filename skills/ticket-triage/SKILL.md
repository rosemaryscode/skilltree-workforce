---
schema: agentcompanies/v1
kind: skill
name: "Ticket Triage"
slug: ticket-triage
description: "Classify and route every inbound support ticket."
metadata:
  department: customer
  autonomy: unattended
  frequency: hourly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Customer  |  **Autonomy:** `unattended`  |  **Cadence:** hourly
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Ticket Triage

## Job
Classify and route every inbound support ticket.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Watch the support inbox/queue.
2. Classify: bug, question, billing, feature request.
3. Route with priority and suggested macro answer attached.
4. Log to your task result (`ticket-triage.md`); escalate per ../escalations.md rules.

## Outputs
| Artifact | Location |
|---|---|
| ticket-triage.md | `ticket-triage.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
