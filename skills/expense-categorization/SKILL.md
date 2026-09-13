---
schema: agentcompanies/v1
kind: skill
name: "Expense Categorization"
slug: expense-categorization
description: "Categorize every expense transaction against the chart of accounts."
metadata:
  department: back-office
  autonomy: unattended
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Back Office  |  **Autonomy:** `unattended`  |  **Cadence:** daily
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Expense Categorization

## Job
Categorize every expense transaction against the chart of accounts.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Import new transactions from linked accounts.
2. Categorize per the chart of accounts; flag unknowns.
3. Write the ledger additions to your task result (`expense-categorization.md`).
4. Human spot-checks weekly; unknowns get resolved manually.

## Outputs
| Artifact | Location |
|---|---|
| expense-categorization.md | `expense-categorization.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
