---
schema: agentcompanies/v1
kind: skill
name: "Pricing Research"
slug: pricing-research
description: "Track competitor pricing and packaging changes."
metadata:
  department: intelligence
  autonomy: ai-drafts
  frequency: monthly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Intelligence  |  **Autonomy:** `ai-drafts`  |  **Cadence:** monthly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Pricing Research

## Job
Track competitor pricing and packaging changes.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Capture competitor pricing pages and changes over time.
2. Diff against last snapshot; note packaging shifts.
3. Summarize implications for our offers.
4. Human decides any pricing action; we never auto-change price.

## Outputs
| Artifact | Location |
|---|---|
| pricing-research.md | `pricing-research.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
