---
schema: agentcompanies/v1
kind: skill
name: "Sop Generation"
slug: sop-generation
description: "Turn a demonstrated process into a written SOP any agent or hire can follow."
metadata:
  department: operations
  autonomy: ai-drafts
  frequency: monthly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Operations  |  **Autonomy:** `ai-drafts`  |  **Cadence:** monthly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Sop Generation

## Job
Turn a demonstrated process into a written SOP any agent or hire can follow.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Record or interview the person doing the work.
2. Draft the SOP: trigger, steps, decision points, done-when.
3. Place it in the owning department folder; link from here.
4. Human confirms the SOP matches reality before it becomes canonical.

## Outputs
| Artifact | Location |
|---|---|
| sop-generation.md | `sop-generation.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
