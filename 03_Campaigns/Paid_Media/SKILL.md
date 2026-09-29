---
name: paid-media
description: Paid search and paid social. Economically bounded tests with a kill rule, not always-on spend.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# 03_Campaigns/Paid_Media

## What this folder is for

Channels where money buys attention. Paid search sits in `Paid_Search`, paid social in `Paid_Social`.

## What goes in the data folder

Platform exports by campaign, ad set, and creative: spend, impressions, clicks, cost per click, conversions, cost per acquisition. Keep the date range in the filename.

## Before you start

Read `02_Customers/icp.md` for who we are targeting, and get the current Customer Lifetime Value figure. Without it you cannot say what a customer is worth, and every number below is decoration.

## How work gets done

1. State the acquisition cost ceiling first. It comes from Customer Lifetime Value and the margin we need, not from what the platform suggests.
2. Set the test budget. Small enough that losing it teaches us something cheaply.
3. Define one variable to test. Audience, creative, or offer. Not all three.
4. Write the kill rule as a number and a date.
5. Run it. Do not touch it mid-flight unless the kill rule fires.
6. Report cost per acquisition against the ceiling, and say whether the channel can clear it at larger volume.

## Guardrails

- Budget changes require approval. Every time. An expired authorization is not a current one.
- Platform-reported conversions are the platform grading its own homework. Say so when you report them.
- Do not scale a channel on a sample too small to support the claim. State the sample size.
- Attribution is an estimate. Never present it as fact.

## Definition of done

Spend, cost per acquisition, the ceiling it was measured against, the sample size, and a scale, modify, or kill decision.
