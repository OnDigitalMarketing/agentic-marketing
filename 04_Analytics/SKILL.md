---
name: analytics
description: How performance gets measured, reported, and turned into a decision.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# 04_Analytics

## What this folder is for

The measurement layer. What happened, how confident we are, and what it means for the next decision.

## What goes in the data folder

Site analytics exports, revenue and order data, funnel and conversion reports, product or platform usage, cohort and retention pulls. Keep the date range in every filename.

## Before you start

Read the campaign or plan whose results you are reading. A number with no hypothesis behind it cannot be interpreted, only described.

## How work gets done

1. Restate the hypothesis and the success signal that were set before the work ran.
2. Pull the numbers. Report unit, denominator, sample size, date range, and source file for each.
3. Compare to the success signal and the kill rule.
4. Say what changed, and separately, say what you think caused it and how confident you are.
5. Recommend: scale, modify, or kill.
6. Name what should be written back into `01_Strategy` or `02_Customers`, and ask before writing it.

## The arithmetic

Revenue is Sessions x Conversion Rate x Value. When revenue moves, say which of the three moved, because the three have different fixes.

## Guardrails

- Correlation is not causation, and a platform's own conversion count is not an audit.
- Do not manufacture precision. Two significant figures on a sample of thirty is false confidence.
- If the sample is too small to support a claim, say so plainly and stop there.
- Report the result that contradicts the plan as loudly as the one that supports it.

## Definition of done

Hypothesis, result with sources and sample sizes, confidence stated honestly, and a scale, modify, or kill recommendation.
