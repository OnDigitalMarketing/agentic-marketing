---
name: customer-retention
description: What happens after the first purchase. Repeat behavior, churn, and what a customer is actually worth.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# 02_retention

Read `../SKILL.md` first.

## What this folder is for

The other half of the economics. Whether customers come back, how long they stay, why they leave, and what that makes them worth.

## Data folder

`00_retention_data`. Repeat purchase history by customer, cohort tables by acquisition month, churn and cancellation reasons, subscription or renewal data, support contact history, and your Customer Lifetime Value working file.

## How work gets done

1. Build cohorts by acquisition month. A single overall retention rate hides the thing you need to see, which is whether recent cohorts behave better or worse than older ones.
2. Separate the customers who lapsed from the customers who actively cancelled. They have different causes and different fixes.
3. Read the cancellation reasons as text before you count them. The categories in the dropdown were written by someone guessing.
4. Compute Customer Lifetime Value as contribution profit over time, discounted. Cumulative revenue is not lifetime value, and treating it as such is the most common way a venture talks itself into unaffordable acquisition.
5. Hand the result to `../01_acquisition`, because that is the number that sets the acquisition ceiling.

## The arithmetic

Customer Lifetime Value minus Customer Acquisition Cost is Post-Acquisition Value. If that number is negative, no amount of campaign optimization fixes the business, and the constraint is product, pricing, or retention rather than marketing.

## Guardrails

- A cohort with three months of history cannot tell you about a two year lifetime. Say what the data covers.
- Survivor bias runs through every retention analysis. The customers still present are not representative of the customers you acquired.
- Do not quote lifetime value to two decimal places on a sample of forty.

## Definition of done

Cohort table, churn separated from lapse, lifetime value stated as contribution profit with its assumptions visible, and the resulting acquisition ceiling.
