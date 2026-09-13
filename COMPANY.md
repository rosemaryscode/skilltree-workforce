---
schema: agentcompanies/v1
kind: company
name: "SkillTree Workforce"
slug: skilltree-workforce
description: "A complete AI workforce - 7 departments, 137 jobs-to-be-done, one shared company brain."
version: 0.1.0
license: MIT
authors:
  - name: Jacob Wilkinson
goals:
  - Run the operational work of a business as 137 discrete jobs across 7 departments, each a runnable skill
  - Keep every department reading from one shared company brain so 137 jobs stay consistent
  - Honor an explicit autonomy grade on every job - unattended, ai-drafts, or human-led - so nothing risky runs without the right oversight
  - Ship one department at a time, starting with the highest-ROI unattended jobs in the worst bottleneck
---

# SkillTree Workforce

A business is not roles - it is jobs to be done. This company is the whole map: **7
departments, 137 jobs, one skill per job**, every one reading from a shared
`company-brain`. Paperclip orchestrates it: the org chart routes work, the scheduler
drives cadence, and tasks capture state.

## Organization (hub-and-spoke)

A **CEO** owns goals, budgets, and approvals and delegates to seven department leads:

- **Sales Lead** (`sales-lead`) - Finding demand, building lists, and starting conversations.
- **Deals Lead** (`deals-lead`) - From first reply to signed agreement: everything a deal needs to move.
- **Marketing Lead** (`marketing-lead`) - Attention in: content, campaigns, and the brand surface.
- **Operations Lead** (`operations-lead`) - Making the machine run: SOPs, migrations, QA, and incidents.
- **Intelligence Lead** (`intelligence-lead`) - Research and monitoring: knowing the market, accounts, and people.
- **Customer Lead** (`customer-lead`) - Keeping customers alive, healthy, and heard.
- **Back Office Lead** (`backoffice-lead`) - Money, people, and paperwork: finance ops and hiring.

Each lead owns that department's jobs as skills. Work is triggered by the user or by a
scheduled task; the lead runs the job's contract and returns its output; a human
reviews per the job's autonomy grade before anything downstream consumes it.

## The one rule

No job with a human check skips it. No output moves downstream until the person
responsible has read the last output.

## Autonomy grades map to Paperclip oversight

| Autonomy grade | Meaning | In Paperclip |
|---|---|---|
| `unattended` | Runs automated, spot-checked weekly | Recurring task / heartbeat; normal trust |
| `ai-drafts` | AI drafts, human approves | Task approval gate before downstream use |
| `human-led` | A person performs / signs off | Board-approval / low-trust review; never unattended |

---

Generated from the ai-workforce job map with the company-creator pattern from [Paperclip](https://github.com/paperclipai/paperclip). Conforms to the [Agent Companies specification](https://agentcompanies.io/specification).
