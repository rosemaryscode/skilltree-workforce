---
schema: agentcompanies/v1
kind: skill
name: "Database Mining"
slug: database-mining
description: "Mine owned and third-party databases for accounts matching the ICP."
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

# Database Mining

## Job
Mine owned and third-party databases for accounts matching the ICP.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read your task result (`icp-definition.md`) criteria.
2. Query approved data sources (CRM, LinkedIn exports, data vendors).
3. Dedupe against existing CRM records.
4. Save matched accounts to your task result (`database-mining.md`).

## Outputs
| Artifact | Location |
|---|---|
| database-mining.md | `database-mining.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
