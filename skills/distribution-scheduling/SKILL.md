---
schema: agentcompanies/v1
kind: skill
name: "Distribution Scheduling"
slug: distribution-scheduling
description: "Distribution Scheduling (Marketing) - job contract, stub; complete before running."
metadata:
  department: marketing
  autonomy: unattended
  frequency: TODO
  status: stub
  source: ai-workforce
---

> **Department:** Marketing  |  **Autonomy:** `unattended`  |  **Cadence:** TODO
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Distribution Scheduling

## Job
TODO - define this job in one or two sentences. (Scaffold placeholder: named during Step 1
of the method, not yet encoded. Fill in Job, Inputs, Process, Outputs, then upgrade to a
full contract before running it.)

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |

## Process
1. TODO
2. TODO
3. TODO

## Outputs
| Artifact | Location |
|---|---|
| Distribution Scheduling result | your task result (`distribution-scheduling.md`) |

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
