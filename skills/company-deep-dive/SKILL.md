---
schema: agentcompanies/v1
kind: skill
name: "Company Deep Dive"
slug: company-deep-dive
description: "Full research dossier on a target company before outreach or a meeting."
metadata:
  department: intelligence
  autonomy: ai-drafts
  frequency: ad-hoc
  status: scaffolded
  source: ai-workforce
---

> **Department:** Intelligence  |  **Autonomy:** `ai-drafts`  |  **Cadence:** ad-hoc
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Company Deep Dive

## Job
Full research dossier on a target company before outreach or a meeting.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read the account's basic enrichment from sales/contact-enrichment.
2. Research: business model, team, tech, news, funding, pains.
3. Structure per the dossier schema with sources.
4. Human reviews before it feeds any outreach.

## Outputs
| Artifact | Location |
|---|---|
| company-deep-dive.md | `company-deep-dive.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
