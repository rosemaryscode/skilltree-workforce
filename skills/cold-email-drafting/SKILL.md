---
schema: agentcompanies/v1
kind: skill
name: "Cold Email Drafting"
slug: cold-email-drafting
description: "Draft cold email sequences per segment using approved voice and offers."
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

# Cold Email Drafting

## Job
Draft cold email sequences per segment using approved voice and offers.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read the company-brain skillvoice.md and the company-brain skilloffers.md.
2. Draft 3-5 step sequences per segment with one idea per step.
3. Include proof points and a single clear CTA per email.
4. Human edits/approves before sequence-writing schedules them.

## Outputs
| Artifact | Location |
|---|---|
| cold-email-drafting.md | `cold-email-drafting.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
