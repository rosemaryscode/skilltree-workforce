---
schema: agentcompanies/v1
kind: skill
name: "Faq Self Serve"
slug: faq-self-serve
description: "Keep the public FAQ/self-serve docs matching the questions actually asked."
metadata:
  department: customer
  autonomy: ai-drafts
  frequency: monthly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Customer  |  **Autonomy:** `ai-drafts`  |  **Cadence:** monthly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Faq Self Serve

## Job
Keep the public FAQ/self-serve docs matching the questions actually asked.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Cluster real tickets by theme from customer/ticket-triage.
2. Draft or update FAQ entries for the top themes.
3. Human approves anything public.

## Outputs
| Artifact | Location |
|---|---|
| faq-self-serve.md | `faq-self-serve.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
