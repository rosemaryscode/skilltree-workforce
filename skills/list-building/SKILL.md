---
schema: agentcompanies/v1
kind: skill
name: "List Building"
slug: list-building
description: "Turn mined accounts into a clean, scored prospect list for the week."
metadata:
  department: sales
  autonomy: ai-drafts
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Sales  |  **Autonomy:** `ai-drafts`  |  **Cadence:** weekly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# List Building

## Job
Turn mined accounts into a clean, scored prospect list for the week.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Take your task result (`database-mining.md`) as input.
2. Score fit against ICP; flag hot accounts.
3. Assign owners and tiers; export to CRM-ready format.
4. Human approves the list before it enters sequencing.

## Outputs
| Artifact | Location |
|---|---|
| list-building.md | `list-building.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
