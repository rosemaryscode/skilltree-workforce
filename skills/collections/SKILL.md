---
schema: agentcompanies/v1
kind: skill
name: "Collections"
slug: collections
description: "Chase overdue invoices with escalating, polite sequences."
metadata:
  department: back-office
  autonomy: ai-drafts
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Back Office  |  **Autonomy:** `ai-drafts`  |  **Cadence:** weekly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Collections

## Job
Chase overdue invoices with escalating, polite sequences.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. List invoices past due, grouped by days overdue.
2. Draft the reminder per escalation stage (day 7/14/30).
3. Hold anything with an open dispute for human review.
4. Human approves sends above the gentle stage.

## Outputs
| Artifact | Location |
|---|---|
| collections.md | `collections.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
