---
schema: agentcompanies/v1
kind: task
name: "Feedback Logging"
slug: feedback-logging
assignee: customer-lead
schedule:
  timezone: America/Chicago
  startsAt: 2026-09-13T09:00:00-05:00
  recurrence:
    frequency: daily
    interval: 1
    time: { hour: 9, minute: 0 }
---

# Feedback Logging (scheduled)

Unattended job on a **daily** cadence. Read the `company-brain` skill, run the
`feedback-logging` skill's contract, and return the result as this task's output.

This job is graded **unattended**: it runs automatically and is spot-checked weekly.
If anything is low-confidence, anomalous, or would spend money / contact a customer,
stop and flag it for review instead of proceeding.
