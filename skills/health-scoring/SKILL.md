---
schema: agentcompanies/v1
kind: skill
name: "Health Scoring"
slug: health-scoring
description: "Score each account's health from usage, support, and payment signals."
metadata:
  department: customer
  autonomy: unattended
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Customer  |  **Autonomy:** `unattended`  |  **Cadence:** weekly
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Health Scoring

## Job
Score each account's health from usage, support, and payment signals.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Pull usage, ticket, and payment data per account.
2. Compute the health score per the agreed rubric.
3. Flag drops and rising-risk accounts.
4. Digest goes to the human owner; nothing auto-emails customers.

## Outputs
| Artifact | Location |
|---|---|
| health-scoring.md | `health-scoring.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
