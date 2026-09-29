---
name: campaigns
description: How a campaign gets proposed, bounded, run, and killed. Applies to every channel sub-folder.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# 03_Campaigns

## What this folder is for

Everything that puts a message in front of a customer. Each channel has its own sub-folder and its own skill file. This file sets the rules they all share.

## Before you start

Read `01_Strategy/Strategy.md` and `02_Customers/Customers.md`. A campaign that does not trace back to the positioning and the customer file is a guess with a budget attached.

## The shared contract

Every campaign, in any channel, is written down before it runs:

1. **Hypothesis.** If we show [message] to [customer] on [channel], then [behavior] will change, because [reason].
2. **Customer.** Which segment from `02_Customers/Customers.md`, and how we know they are reachable here.
3. **Offer.** What the person gets and what they give up to get it.
4. **Investment.** Cash, founder hours, and team hours. All three.
5. **Success signal.** The specific number that would make this worth continuing.
6. **Kill rule.** The result that stops it. Written before launch, not after.
7. **Time to signal.** When we expect to know anything.

## The arithmetic, checked before you spend

Two equations govern every campaign in every folder below this one. Run both before committing money, not after the results come in.

> **Sessions x Conversion Rate x Value = Revenue**
>
> **Customer Lifetime Value minus Customer Acquisition Cost = Post-Acquisition Value**

**1. Name your term.** A campaign moves sessions, conversion rate, or value. Say which one before you start. A campaign that lifts sessions while conversion rate falls has done nothing, and it will still look busy in the report.

**2. Check the ceiling before you spend.** Read the maximum acceptable acquisition cost from `02_Customers/Customers.md`. Then compute what this campaign would have to deliver:

```
projected cost per acquisition  =  planned spend / expected conversions
```

If that number is above the ceiling, the campaign is upside down before it launches. Three honest responses, in order of preference:

- Change the campaign so it can clear the ceiling.
- Say the ceiling is wrong and go fix the number in `02_Customers` with evidence.
- Run it anyway as a bounded learning spend, with the violation stated out loud and the amount you are willing to lose written down.

What you do not do is launch without checking, discover the gap in the retrospective, and call it a learning.

**3. If the ceiling is unknown, say so.** A campaign built on an unknown ceiling is a bet, not a plan. That may be the right call early on. It is only the wrong call when nobody said it out loud.

## Guardrails

- Never invent proof, testimonials, urgency, scarcity, or results.
- Publishing, sending, and spending all require approval. Permission to draft is not permission to launch.
- A campaign with no kill rule does not launch.
- Weak signal in volume is still weak signal.

## Definition of done

The seven items above, filled in, with a date, plus a named owner for the next action.
