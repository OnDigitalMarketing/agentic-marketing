# 00_site_data

**Source. Read only. Never committed.**

Git ignores every folder ending in `_data`. Only this README is tracked, so real files stay on your machine.

This folder owns the middle term of the revenue equation. Campaigns buy sessions. What those sessions do next is measured here, and `03_Campaigns/Campaigns.md` reads the conversion rate from this folder rather than inventing one.

## What goes here

**Behavioral analytics, which tell you what happened**

- Google Analytics 4, Plausible, Fathom, or Adobe exports
- Sessions and users by channel, source, medium, and landing page
- Funnel reports and conversion paths
- Landing page conversion rate, which is the number campaigns depend on
- Site search queries, which are free voice of customer data

**Experience analytics, which tell you why it happened**

- Microsoft Clarity exports: session recordings, heatmaps, rage clicks, dead clicks, excessive scrolling, and quick backs
- Hotjar, FullStory, or similar recordings and heatmaps
- Scroll depth and click maps by page
- Form abandonment, including which field people quit on
- Page speed and Core Web Vitals

## Naming

`YYYY-MM-DD_source_short-description.ext`

`2026-09-28_ga4_landing-page-conversion_2026-07-01_to_2026-09-28.csv`
`2026-09-28_clarity_rage-clicks_pricing-page.csv`

## Why both kinds matter

Analytics tells you the checkout page converts at two percent. It cannot tell you that a third of visitors rage click a disabled button before leaving. The first number sets the term in the equation. The second tells you what to fix, and it is usually cheaper to fix a broken page than to buy more traffic into it.

When a campaign misses its conversion rate, this folder is where you find out whether the problem was the traffic or the page.

## Before anyone analyzes this

Know what a session means in your tool and what the attribution window is set to. Those two settings can move a channel's apparent contribution by a factor of two.

Session recordings can capture personal information typed into forms. Confirm masking is on before exporting anything, and never move recording data into another folder.
