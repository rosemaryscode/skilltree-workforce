---
schema: agentcompanies/v1
kind: skill
name: "Account Monitoring"
slug: account-monitoring
description: "Watch named accounts for trigger events: hiring, funding, leadership, product."
metadata:
  department: intelligence
  autonomy: unattended
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Intelligence  |  **Autonomy:** `unattended`  |  **Cadence:** daily
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Account Monitoring

## Job
Watch named accounts for trigger events: hiring, funding, leadership, product.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Maintain the watch list from active pipeline.
2. Poll approved sources daily; dedupe against known events.
3. Score triggers; push hot ones to deals/hot-lead-routing.
4. Keep the daily digest short and linkable.

## Outputs
| Artifact | Location |
|---|---|
| account-monitoring.md | `account-monitoring.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
