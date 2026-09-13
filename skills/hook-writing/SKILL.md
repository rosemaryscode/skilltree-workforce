---
schema: agentcompanies/v1
kind: skill
name: "Hook Writing"
slug: hook-writing
description: "Generate and rank opening hooks for content across channels."
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

# Hook Writing

## Job
Generate and rank opening hooks for content across channels.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read the company-brain skillvoice.md and top-performing past hooks.
2. Generate 20+ hooks per topic; cut to the strongest 5.
3. Rank by pattern (contrarian, number, question, story).
4. Human picks; winners feed script and ad stages.

## Outputs
| Artifact | Location |
|---|---|
| hook-writing.md | `hook-writing.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
