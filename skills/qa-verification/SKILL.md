---
schema: agentcompanies/v1
kind: skill
name: "Qa Verification"
slug: qa-verification
description: "Verify that recent automated outputs meet their quality bars."
metadata:
  department: operations
  autonomy: ai-drafts
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Operations  |  **Autonomy:** `ai-drafts`  |  **Cadence:** weekly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Qa Verification

## Job
Verify that recent automated outputs meet their quality bars.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Sample recent outputs from each department's your task workspace/ folder.
2. Check against each stage's audit list and the company-brain skilldefinition-of-done.md.
3. Log failures with the exact artifact and contract that failed.
4. Human reviews the failure list; fixes get filed as jobs.

## Outputs
| Artifact | Location |
|---|---|
| qa-verification.md | `qa-verification.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
