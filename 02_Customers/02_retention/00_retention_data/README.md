# 00_retention_data

**Source. Read only. Never committed.**

Git ignores every folder ending in `_data`. Only this README is tracked, so real files stay on your machine.

## What goes here

- Repeat purchase history by customer
- Cohort tables grouped by acquisition month
- Churn and cancellation records, including the free-text reason
- Subscription, renewal, and downgrade events
- Support contact history
- Your Customer Lifetime Value working file

## Naming

`YYYY-MM-DD_source_short-description.ext`

`2026-09-28_stripe_cohort-retention_2025-01_to_2026-09.csv`

## Before anyone analyzes this

Confirm whether a churn record means the customer cancelled or simply stopped. Lapse and cancellation have different causes and get counted together by default in most systems.
