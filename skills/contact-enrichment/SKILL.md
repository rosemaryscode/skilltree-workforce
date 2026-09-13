---
schema: agentcompanies/v1
kind: skill
name: "Contact Enrichment"
slug: contact-enrichment
description: "Enrich new contacts with role, company size, tech stack, and social links."
metadata:
  department: sales
  autonomy: unattended
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Sales  |  **Autonomy:** `unattended`  |  **Cadence:** daily
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Contact Enrichment

## Job
Enrich new contacts with role, company size, tech stack, and social links.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Watch for new rows in your task result (`list-building.md`).
2. Enrich each contact from approved data providers.
3. Write results back to your task result (`contact-enrichment.md`).
4. Flag contacts that fail enrichment for manual review.

## Outputs
| Artifact | Location |
|---|---|
| contact-enrichment.md | `contact-enrichment.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
