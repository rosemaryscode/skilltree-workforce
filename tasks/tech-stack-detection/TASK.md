---
schema: agentcompanies/v1
kind: task
name: "Tech Stack Detection"
slug: tech-stack-detection
assignee: intelligence-lead
schedule:
  timezone: America/Chicago
  startsAt: 2026-09-14T09:00:00-05:00
  recurrence:
    frequency: weekly
    interval: 1
    weekdays: [monday]
    time: { hour: 9, minute: 0 }
---

# Tech Stack Detection (scheduled)

Unattended job on a **weekly** cadence. Read the `company-brain` skill, run the
`tech-stack-detection` skill's contract, and return the result as this task's output.

This job is graded **unattended**: it runs automatically and is spot-checked weekly.
If anything is low-confidence, anomalous, or would spend money / contact a customer,
stop and flag it for review instead of proceeding.
