---
schema: agentcompanies/v1
kind: skill
name: "Company Brain"
slug: company-brain
description: "The single company knowledge base every department reads first: offers, clients, brand voice, approved tools, and the definition of done."
metadata:
  role: shared-context
  source: ai-workforce
---

# Company Brain

Every agent reads this skill **before** running any job. It is the one node every
department starts from - the shared context that keeps 137 jobs consistent. Keep it
current: when offers, clients, voice, tools, or the quality bar change, edit them here
once and every agent inherits the change.

## Offers - what we sell

One home for product/pricing truth. Jobs point here; they never restate it.

## Primary offer
TODO - product, price, deliverable

## Secondary offers
TODO

## Disqualifiers (who we do NOT sell to)
TODO

---

## Clients - who we serve

One row per account that matters. Jobs link here instead of copying account facts.

| Account | Tier | Owner | Notes link |
|---|---|---|---|
| TODO | A | TODO | TODO |

---

## Voice - how we sound

## Sounds right
- TODO: paste example 1
- TODO: paste example 2

## Sounds wrong
- TODO: paste counter-example

## Rules
- TODO: 3-5 hard rules (person, tense, banned words, length)

---

## Tools - what agents may use

Anything not listed here is off-limits until a human adds it.

| Capability | Tool | Auth/where | Notes |
|---|---|---|---|
| CRM | TODO | TODO | TODO |
| Email/outbound | TODO | TODO | TODO |
| Data/enrichment | TODO | TODO | TODO |
| Scheduling | TODO | TODO | TODO |
| Payments/finance | TODO | TODO | TODO |
| Support desk | TODO | TODO | TODO |

---

## Definition of Done - the quality bar

An output ships only when:

1. Its job's audit list passes.
2. The job's Human check is satisfied for its autonomy grade.
3. It lives in the producing department's `your task workspace/` folder with frontmatter intact.
4. Anything the next department needs is linkable from this file's location.
