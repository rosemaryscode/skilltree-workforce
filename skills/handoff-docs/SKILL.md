---
schema: agentcompanies/v1
kind: skill
name: "Handoff Docs"
slug: handoff-docs
description: "Write the doc that lets a new person (or agent) take over a responsibility."
metadata:
  department: operations
  autonomy: ai-drafts
  frequency: ad-hoc
  status: scaffolded
  source: ai-workforce
---

> **Department:** Operations  |  **Autonomy:** `ai-drafts`  |  **Cadence:** ad-hoc
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Handoff Docs

## Job
Write the doc that lets a new person (or agent) take over a responsibility.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Enumerate what the role owns, where state lives, and the recurring jobs.
2. Draft the handoff doc with links to every live file.
3. Walk test: a cold reader must be able to act on it.
4. Both parties sign off.

## Outputs
| Artifact | Location |
|---|---|
| handoff-docs.md | `handoff-docs.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
