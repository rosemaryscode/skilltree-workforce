---
schema: agentcompanies/v1
kind: skill
name: "Clip Extraction"
slug: clip-extraction
description: "Find and cut the strongest short-form clips from long-form video."
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

# Clip Extraction

## Job
Find and cut the strongest short-form clips from long-form video.

## Inputs
| Source | File/Location | Scope |
|---|---|---|
| Factory config | the company-brain skill | offers, voice, tools as relevant |
| Run inputs | your task workspace/ and sibling job outputs named in Process | current-run artifacts |

## Process
1. Transcribe source video with word-level timestamps.
2. Score moments on hook strength; pick the top 2-5.
3. Cut clips, crop to vertical, add captions per the company-brain skill rules.
4. Human approves clips before publishing.

## Outputs
| Artifact | Location |
|---|---|
| clip-extraction.md | `clip-extraction.md` (your task result) |

## Audit
- [ ] Output matches the job summary above
- [ ] Nothing invented that the inputs do not support
- [ ] Human check satisfied per autonomy grade

## Human check
A human reviews and approves the output before anything downstream uses it.
