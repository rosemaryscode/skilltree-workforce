---
schema: agentcompanies/v1
kind: skill
name: "Publishing"
slug: publishing
description: "Schedule and publish approved content to each channel."
metadata:
  department: marketing
  autonomy: ai-drafts
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Marketing  |  **Autonomy:** `ai-drafts`  |  **Cadence:** daily
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Publishing

## Job
Schedule and publish approved content to each channel.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read approved assets from sibling marketing outputs.
2. Match each asset to channel and slot in the calendar.
3. Publish or schedule; verify the post renders correctly.
4. Log everything published to your task result (`publishing.md`).

## Outputs
| Artifact | Location |
|---|---|
| publishing.md | `publishing.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
