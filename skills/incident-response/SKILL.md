---
schema: agentcompanies/v1
kind: skill
name: "Incident Response"
slug: incident-response
description: "Contain, fix, and post-mortem anything broken in the business's systems."
metadata:
  department: operations
  autonomy: human-led
  frequency: ad-hoc
  status: scaffolded
  source: ai-workforce
---

> **Department:** Operations  |  **Autonomy:** `human-led`  |  **Cadence:** ad-hoc
> **Oversight:** A human performs or signs off on this job. This file is their runbook. Require board/approval gate; do not run unattended.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Incident Response

## Job
Contain, fix, and post-mortem anything broken in the business's systems.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Declare the incident; note blast radius.
2. Contain first, root-cause second; log every action with timestamps.
3. Draft the post-mortem: cause, fix, and the SOP change that prevents it.
4. Human owns decisions throughout.

## Outputs
| Artifact | Location |
|---|---|
| incident-response.md | `incident-response.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human performs this job; this file is the runbook they follow.
