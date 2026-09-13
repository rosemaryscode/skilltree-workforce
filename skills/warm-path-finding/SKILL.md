---
schema: agentcompanies/v1
kind: skill
name: "Warm Path Finding"
slug: warm-path-finding
description: "Find the warmest path into an account: shared connections, past overlaps, communities."
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

# Warm Path Finding

## Job
Find the warmest path into an account: shared connections, past overlaps, communities.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Map the target's people against our network and history.
2. Rank paths by warmth and plausibility.
3. Draft the intro ask, never the fake-familiar kind.
4. Human approves any message sent on their behalf.

## Outputs
| Artifact | Location |
|---|---|
| warm-path-finding.md | `warm-path-finding.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
