---
schema: agentcompanies/v1
kind: skill
name: "Campaign Orchestration"
slug: campaign-orchestration
description: "Run active outbound campaigns: schedule sends, apply pauses, log outcomes."
metadata:
  department: sales
  autonomy: ai-drafts
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Sales  |  **Autonomy:** `ai-drafts`  |  **Cadence:** daily
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Campaign Orchestration

## Job
Run active outbound campaigns: schedule sends, apply pauses, log outcomes.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read approved sequences and the active list.
2. Schedule sends respecting caps, time zones, and deliverability rules.
3. Pause prospects who reply or book; hand off to deals/reply-classification.
4. Log campaign state to your task result (`campaign-orchestration.md`).

## Outputs
| Artifact | Location |
|---|---|
| campaign-orchestration.md | `campaign-orchestration.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
