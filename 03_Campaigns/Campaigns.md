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

## The arithmetic

Two equations govern every campaign in every folder below this one. They answer different questions and you need both, because each one is misleading on its own.

> **Sessions x Conversion Rate x Value = Revenue**  *(is the campaign any good?)*
>
> **Customer Lifetime Value minus Customer Acquisition Cost = Post-Acquisition Value**  *(can we afford to keep doing it?)*

### Who owns which term

This is the part that makes the two equations work together. No single folder holds all the numbers.

| Term | Owned by | Where the number comes from |
|---|---|---|
| Sessions | **This folder** | Platform reporting and `04_Analytics/00_site_data` |
| Cost per session | **This folder** | Spend divided by sessions delivered |
| Conversion Rate | `04_Analytics` | `00_site_data` and `02_campaign_performance_data` |
| Value per conversion | `04_Analytics` and `02_Customers` | `01_revenue_data`, then lifetime value from `02_retention` |
| Acquisition ceiling | `02_Customers` | `Customers.md`, from lifetime value minus required margin |

A campaign buys sessions. It does not buy conversion rate, and it does not buy value. Those are earned by the offer, the page, and the product, and they are measured somewhere else. **Naming where each number will come from before you launch is the whole discipline here**, because after the fact everyone argues about attribution instead of about the business.

### Before you spend

**1. Name the term you are moving.** Sessions, conversion rate, or value. A campaign that lifts sessions while conversion rate falls has moved nothing, and it will still look busy in the report.

**2. Write down what you expect for all three,** not just the one you are moving. This is the forecast you will be judged against:

```
expected sessions  x  expected conversion rate  x  expected value  =  expected revenue
```

If you cannot estimate conversion rate and value, pull them from `04_Analytics` and `02_Customers` rather than inventing them. If they do not exist yet, say unknown and treat the campaign as a measurement exercise.

**3. Check the ceiling.** Read the maximum acceptable acquisition cost from `02_Customers/Customers.md`:

```
projected cost per acquisition  =  planned spend / (expected sessions x expected conversion rate)
```

Above the ceiling, the campaign is upside down before it launches. Three honest responses, in order of preference: change the campaign so it can clear the ceiling; say the ceiling is wrong and go fix that number in `02_Customers` with evidence; or run it as a bounded learning spend with the violation stated out loud and the loss you accept written down.

What you do not do is launch unchecked, find the gap in the retrospective, and relabel it a learning.

### After it runs, decompose

Compare actual against expected for each term separately. A single blended cost per acquisition hides which part broke, and the three failures have different owners and different fixes.

| What happened | What it means | Who fixes it |
|---|---|---|
| Sessions missed | Targeting, creative, or budget delivery | This folder |
| Sessions landed, conversion rate missed | The page or the offer did not match what the ad promised | `04_Analytics`, then the offer |
| Sessions and rate landed, value missed | You bought the wrong customer | `02_Customers` |
| All three landed, acquisition cost still too high | The channel cannot clear the ceiling at this volume | Strategy, not optimization |

### Why cost per acquisition alone will mislead you

It is one number standing in for three, so it hides the trade you actually made. A campaign can hit an acceptable cost per acquisition while acquiring customers who never return, which shows up two quarters later as falling lifetime value rather than as a campaign failure. Another can miss its cost per acquisition badly while proving a conversion rate that makes a whole channel viable.

Report cost per acquisition. Report the three terms underneath it too, or you have described the result without explaining it.

## Guardrails

- Never invent proof, testimonials, urgency, scarcity, or results.
- Publishing, sending, and spending all require approval. Permission to draft is not permission to launch.
- A campaign with no kill rule does not launch.
- Weak signal in volume is still weak signal.

## Definition of done

The seven items above, filled in, with a date, plus a named owner for the next action.
