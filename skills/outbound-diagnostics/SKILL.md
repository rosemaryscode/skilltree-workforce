---
schema: agentcompanies/v1
kind: skill
name: "Outbound Diagnostics"
slug: outbound-diagnostics
description: "Outbound Diagnostics (Sales) - job contract, stub; complete before running."
metadata:
  department: sales
  autonomy: human-led
  frequency: TODO
  status: stub
  source: ai-workforce
---

> **Department:** Sales  |  **Autonomy:** `human-led`  |  **Cadence:** TODO
> **Oversight:** A human performs or signs off on this job. This file is their runbook. Require board/approval gate; do not run unattended.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Outbound Diagnostics

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
| Outbound Diagnostics result | your task result (`outbound-diagnostics.md`) |

## Human check
A human performs this job; this file is the runbook they follow.
