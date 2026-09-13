---
schema: agentcompanies/v1
kind: skill
name: "Thumbnail Design"
slug: thumbnail-design
description: "Produce thumbnails for videos and posts."
metadata:
  department: marketing
  autonomy: ai-drafts
  frequency: weekly
  status: scaffolded
  source: ai-workforce
---

> **Department:** Marketing  |  **Autonomy:** `ai-drafts`  |  **Cadence:** weekly
> **Oversight:** AI drafts; a human approves the output before anything downstream uses it. Gate behind task approval.
>
> Read the `company-brain` skill first. Run the contract below and return your
> result as the task output; a human reviews per the autonomy grade before anything
> downstream consumes it.

# Thumbnail Design

## Job
Produce thumbnails for videos and posts.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Read the clip/post content and title.
2. Generate 3 thumbnail concepts with clear focal subject and 3-word max text.
3. Export per platform size specs.
4. Human picks and may edit.

## Outputs
| Artifact | Location |
|---|---|
| thumbnail-design.md | `thumbnail-design.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
