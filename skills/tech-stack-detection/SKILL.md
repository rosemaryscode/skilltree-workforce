---
schema: agentcompanies/v1
kind: skill
name: "Tech Stack Detection"
slug: tech-stack-detection
description: "Detect the technology a company runs to qualify fit and timing."
metadata:
  department: intelligence
  autonomy: unattended
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Intelligence  |  **Autonomy:** `unattended`  |  **Cadence:** weekly
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Tech Stack Detection

## Job
Detect the technology a company runs to qualify fit and timing.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Run stack detection on new accounts in the active list.
2. Flag matches and conflicts with our integrations.
3. Write results to the enrichment record.
4. Alert on high-signal installs only.

## Outputs
| Artifact | Location |
|---|---|
| tech-stack-detection.md | `tech-stack-detection.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
