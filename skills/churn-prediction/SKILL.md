---
schema: agentcompanies/v1
kind: skill
name: "Churn Prediction"
slug: churn-prediction
description: "Predict which accounts are likely to churn and why."
metadata:
  department: customer
  autonomy: ai-drafts
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Customer  |  **Autonomy:** `ai-drafts`  |  **Cadence:** weekly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Churn Prediction

## Job
Predict which accounts are likely to churn and why.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read health scores and recent events.
2. Apply the churn model/rubric; state the top reason per account.
3. Recommend a specific save play per at-risk account.
4. Human chooses which plays to run.

## Outputs
| Artifact | Location |
|---|---|
| churn-prediction.md | `churn-prediction.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
