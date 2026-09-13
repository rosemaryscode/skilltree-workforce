---
schema: agentcompanies/v1
kind: skill
name: "Cash Flow Forecasting"
slug: cash-flow-forecasting
description: "Maintain a rolling 13-week cash flow forecast."
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

# Cash Flow Forecasting

## Job
Maintain a rolling 13-week cash flow forecast.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read receivables, payables, payroll, and the expense ledger.
2. Update the rolling forecast with actuals and commitments.
3. Flag any week where cash dips below the floor.
4. Human reviews before any spending decision.

## Outputs
| Artifact | Location |
|---|---|
| cash-flow-forecasting.md | `cash-flow-forecasting.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
