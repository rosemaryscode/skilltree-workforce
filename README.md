# SkillTree Workforce

An [Agent Company](https://agentcompanies.io) for [Paperclip](https://github.com/paperclipai/paperclip):
a full AI workforce of **7 departments and 137 jobs-to-be-done**, each job a runnable skill,
all reading from one shared **company brain**. Paperclip orchestrates it - org chart for
routing, scheduler for cadence, tasks for state.

## Org chart

CEO (`ceo`) -> seven department leads (hub-and-spoke). Every lead reads `company-brain` first.

| Department | Lead | Title | Jobs |
|---|---|---|---|
| Sales | `sales-lead` | VP of Sales | 22 |
| Deals | `deals-lead` | VP of Deals | 24 |
| Marketing | `marketing-lead` | VP of Marketing | 23 |
| Operations | `operations-lead` | Head of Operations | 19 |
| Intelligence | `intelligence-lead` | Head of Intelligence | 17 |
| Customer | `customer-lead` | Head of Customer | 14 |
| Back Office | `backoffice-lead` | Head of Back Office | 18 |
| **Total** | | | **137** |

## Autonomy grades

Every job carries an autonomy grade that maps to Paperclip oversight:

- `unattended` - runs on a schedule, spot-checked weekly
- `ai-drafts` - AI drafts, a human approves before downstream use
- `human-led` - a person performs or signs off; never unattended

## Getting started

```bash
paperclipai company import --from ./skilltree-workforce
```

After import: fill in the `company-brain` skill (offers, clients, voice, tools, definition
of done - the source ships with TODO placeholders), set a monthly budget, and review the
pre-wired heartbeats in `tasks/` (one scheduled task per unattended job). Ship one
department at a time.

---

Generated from the ai-workforce job map with the company-creator pattern from Paperclip.
Conforms to the [Agent Companies specification](https://agentcompanies.io/specification).
