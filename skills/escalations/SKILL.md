---
schema: agentcompanies/v1
kind: skill
name: "Escalations"
slug: escalations
description: "Own the escalation path when a customer issue outgrows normal support."
metadata:
  department: customer
  autonomy: human-led
  frequency: ad-hoc
  status: scaffolded
  source: ai-workforce
---

> **Department:** Customer  |  **Autonomy:** `human-led`  |  **Cadence:** ad-hoc
> **Oversight:** A human performs or signs off on this job. This file is their runbook. Require board/approval gate; do not run unattended.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Escalations

## Job
Own the escalation path when a customer issue outgrows normal support.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Declaring escalation is a human call using the triage flags.
2. Assemble the timeline, impact, and stakeholders doc.
3. Coordinate the response; keep the customer informed per cadence.
4. Post-mortem feeds back into operations/sop-generation.

## Outputs
| Artifact | Location |
|---|---|
| escalations.md | `escalations.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human performs this job; this file is the runbook they follow.
