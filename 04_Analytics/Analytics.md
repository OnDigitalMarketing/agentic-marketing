---
name: analytics
description: How performance gets measured, turned into a decision, and shown on a dashboard somebody will actually read.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# 04_Analytics

## What this folder is for

The measurement layer. What happened, how confident we are, what it costs, what we expect next, and what any of that means for the next decision.

## Data folders

| Folder | What it holds |
|---|---|
| `00_site_data` | Google Analytics 4, Microsoft Clarity, Plausible, Adobe |
| `01_revenue_data` | Shopify, Stripe, enterprise resource planning (ERP) exports, invoices |
| `02_campaign_performance_data` | Cross-channel results pulled together in one place |
| `03_budget_data` | Available capital, budgets, spend to date, pacing |
| `04_forecast_data` | Forecast spreadsheets and models, with their assumptions |
| `05_cohort_data` | Retention curves and cohort tables |

## Before you start

Read the campaign or plan whose results you are reading. A number with no hypothesis behind it can be described but not interpreted.

## How work gets done

1. Restate the hypothesis and the success signal that were set before the work ran.
2. Pull the numbers. Report unit, denominator, sample size, date range, and source file for each one.
3. Compare to the success signal and the kill rule.
4. Say what changed. Then separately, say what you think caused it and how confident you are.
5. Check it against budget. A result that worked and consumed the quarter's capital is a different recommendation from the same result at a tenth of the cost.
6. Recommend: scale, modify, or kill.
7. Name what should be written back into `01_Strategy` or `02_Customers`, and ask before writing it.

## The arithmetic

Revenue is Sessions x Conversion Rate x Value. When revenue moves, say which of the three moved, because each has a different fix.

Marketing spend is capital allocation. Read `03_budget_data` before recommending more of anything. Money already committed is not available, and a recommendation that ignores pacing is a wish.

## Building dashboards

A dashboard is a decision aid, not a data dump. Before building one, answer: who reads this, what decision do they make with it, and how often?

1. **One question per view.** If a chart does not help answer the question at the top of the page, it belongs somewhere else.
2. **Lead with the number that triggers action,** then the trend, then the breakdown. Most people read the top left and stop.
3. **Show the comparison, not just the value.** A figure with no target, prior period, or benchmark next to it cannot be judged.
4. **Put the source and the refresh date on the page.** A dashboard nobody trusts gets rebuilt in a spreadsheet within a month.
5. **Say what is estimated.** Attributed conversions and modeled figures get labeled on the dashboard itself, not in a footnote nobody opens.
6. Build it in `99_Outputs` first and let it earn a permanent home.

Keep the chart honest: axes starting at zero for bar charts, no dual axes implying a relationship that was never tested, and no pie chart with nine slices.

## Guardrails

- Correlation is not causation, and a platform's own conversion count is not an audit.
- Do not manufacture precision. Two decimal places on a sample of thirty is false confidence.
- If the sample is too small to support a claim, say so plainly and stop there.
- Report the result that contradicts the plan as loudly as the one that supports it.
- A forecast carries its assumptions with it, or it is a guess wearing a suit.

## Definition of done

Hypothesis, result with sources and sample sizes, spend against budget, confidence stated honestly, and a scale, modify, or kill recommendation.
