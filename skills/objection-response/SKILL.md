---
schema: agentcompanies/v1
kind: skill
name: "Objection Response"
slug: objection-response
description: "Draft responses to objections (price, timing, authority, trust) for rep approval."
metadata:
  department: deals
  autonomy: ai-drafts
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Deals  |  **Autonomy:** `ai-drafts`  |  **Cadence:** daily
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Objection Response

## Job
Draft responses to objections (price, timing, authority, trust) for rep approval.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read the objection from the thread.
2. Match it to approved battlecards and proof points.
3. Draft a short reply that concedes nothing false and offers proof.
4. Rep approves or edits before sending.

## Outputs
| Artifact | Location |
|---|---|
| objection-response.md | `objection-response.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
