---
schema: agentcompanies/v1
kind: skill
name: "Icp Definition"
slug: icp-definition
description: "Define and maintain the Ideal Customer Profile: firmographics, pains, buying triggers, and disqualifiers."
metadata:
  department: sales
  autonomy: human-led
  frequency: monthly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Sales  |  **Autonomy:** `human-led`  |  **Cadence:** monthly
> **Oversight:** A human performs or signs off on this job. This file is their runbook. Require board/approval gate; do not run unattended.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Icp Definition

## Job
Define and maintain the Ideal Customer Profile: firmographics, pains, buying triggers, and disqualifiers.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Pull closed-won, lost, and churned account data from your task result (`list-building`).
2. Cluster accounts by firmographics, pain, and deal size.
3. Draft ICP criteria and explicit disqualifiers.
4. Human approves; link the result from the company-brain skilloffers.md.

## Outputs
| Artifact | Location |
|---|---|
| icp-definition.md | `icp-definition.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human performs this job; this file is the runbook they follow.
