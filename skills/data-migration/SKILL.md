---
schema: agentcompanies/v1
kind: skill
name: "Data Migration"
slug: data-migration
description: "Move data between systems with a verified, reversible plan."
metadata:
  department: operations
  autonomy: ai-drafts
  frequency: ad-hoc
  status: scaffolded
  source: ai-workforce
---

> **Department:** Operations  |  **Autonomy:** `ai-drafts`  |  **Cadence:** ad-hoc
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Data Migration

## Job
Move data between systems with a verified, reversible plan.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Map source and destination schemas.
2. Dry-run the migration on a sample; diff results.
3. Execute with a rollback checkpoint.
4. Human verifies counts and spot-checks records.

## Outputs
| Artifact | Location |
|---|---|
| data-migration.md | `data-migration.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
