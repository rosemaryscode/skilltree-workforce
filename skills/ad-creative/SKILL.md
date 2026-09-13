---
schema: agentcompanies/v1
kind: skill
name: "Ad Creative"
slug: ad-creative
description: "Draft ad copy and creative briefs for paid channels."
metadata:
  department: marketing
  autonomy: ai-drafts
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Marketing  |  **Autonomy:** `ai-drafts`  |  **Cadence:** weekly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Ad Creative

## Job
Draft ad copy and creative briefs for paid channels.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read approved hooks and campaign goal.
2. Write ad variants per platform spec (length, tone, CTA).
3. Attach creative direction notes for designers/AI image tools.
4. Human approves before anything goes live.

## Outputs
| Artifact | Location |
|---|---|
| ad-creative.md | `ad-creative.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
