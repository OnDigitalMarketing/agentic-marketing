# analytics_data

**Source. Read only. Never committed.**

This folder is ignored by git. Put real exports here on your own machine.

## What goes here

| Example file | Where it comes from |
|---|---|
| Site analytics: sessions, users, channel, landing page | Google Analytics 4, Plausible, Fathom, Adobe |
| Advertising performance by campaign and creative | Google Ads, Meta Ads Manager, LinkedIn Campaign Manager, TikTok |
| Email performance: sends, opens, clicks, unsubscribes | Klaviyo, Mailchimp, ConvertKit, HubSpot |
| Revenue and order exports | Shopify, Stripe, your billing system |
| Funnel and conversion reports | Your analytics tool, or a query against your warehouse |
| Cohort and retention pulls | Amplitude, Mixpanel, a SQL export |
| Customer acquisition cost and lifetime value working files | Your own model, usually a spreadsheet |

## Naming

`YYYY-MM-DD_platform_report_date-range.ext`

`2026-09-28_ga4_channel-sessions_2026-07-01_to_2026-09-28.csv`
`2026-09-28_google-ads_campaign-performance_last-90d.csv`

The date range matters more than people expect. Two exports with the same name and different windows is the most common way a marketing analysis goes quietly wrong.

## Before anyone analyzes this

Know what a "session" means in your tool, what the attribution window is, and whether the conversion count is platform-reported or verified against your own revenue data. Those three choices can move a number by a factor of two.
