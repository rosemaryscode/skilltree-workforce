---
schema: agentcompanies/v1
kind: skill
name: "Agreement Drafting"
slug: agreement-drafting
description: "Draft quotes, order forms, and agreements from deal terms."
metadata:
  department: deals
  autonomy: ai-drafts
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Deals  |  **Autonomy:** `ai-drafts`  |  **Cadence:** weekly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Agreement Drafting

## Job
Draft quotes, order forms, and agreements from deal terms.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read the agreed terms from the deal record.
2. Draft the agreement from the company-brain skill templates and standard terms.
3. Flag any non-standard clause for human/legal review.
4. Human approves before sending to signature.

## Outputs
| Artifact | Location |
|---|---|
| agreement-drafting.md | `agreement-drafting.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
