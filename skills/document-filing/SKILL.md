---
schema: agentcompanies/v1
kind: skill
name: "Document Filing"
slug: document-filing
description: "File signed agreements, receipts, and official docs in the right place."
metadata:
  department: back-office
  autonomy: unattended
  frequency: daily
  status: scaffolded
  source: ai-workforce
---

> **Department:** Back Office  |  **Autonomy:** `unattended`  |  **Cadence:** daily
> **Oversight:** Runs unattended on schedule. Spot-checked weekly. Safe to wire to a recurring task/heartbeat.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Document Filing

## Job
File signed agreements, receipts, and official docs in the right place.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Watch for new documents (signed agreements, receipts, tax notices).
2. Name and file per the convention; add frontmatter metadata.
3. Link the document from the relevant deal or vendor record.
4. Duplicates and unknowns go to a human queue.

## Outputs
| Artifact | Location |
|---|---|
| document-filing.md | `document-filing.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
Runs without a human gate. Spot-check weekly; alerts on failure go to operations/incident-response.
