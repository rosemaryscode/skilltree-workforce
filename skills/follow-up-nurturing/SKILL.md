---
schema: agentcompanies/v1
kind: skill
name: "Follow Up Nurturing"
slug: follow-up-nurturing
description: "Follow Up Nurturing (Sales) - job contract, stub; complete before running."
metadata:
  department: sales
  autonomy: ai-drafts
  frequency: TODO
  status: stub
  source: ai-workforce
---

> **Department:** Sales  |  **Autonomy:** `ai-drafts`  |  **Cadence:** TODO
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Follow Up Nurturing

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
| Follow Up Nurturing result | your task result (`follow-up-nurturing.md`) |

## Human check
A human reviews and approves the output before anything downstream uses it.
