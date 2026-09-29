# Agentic Marketing

A working marketing system built out of folders, markdown files, and a short set of rules about who may change what. Clone it, point it at your own venture, and run it with an AI agent.

## Why this shape

An AI agent needs five things before it produces anything worth keeping: an objective, context/data, tools, guardrails, and feedback. Most agent demos supply the objective inside a clever prompt and skip the other four, which is why the output looks impressive for about a minute and then turns out to be unusable.

A folder structure supplies four of the five, in a form you can read, correct, and hand to somebody else. `CLAUDE.md` at the root carries the guardrails. The numbered folders carry the context, separated by stage so the agent loads only what the question needs. Each folder's own markdown file carries the objective for that piece of work. The data folders carry the feedback, because that is where real evidence lands.

The part people underestimate is the fifth one. Your proprietary customer data and context are the only durable advantage here. Everyone has the same models these days.

## The rule that does the most work

Every file in this repository is either **source** or **derived**.

Source means original material that you or a data provider produced. A survey export. A call transcript. Last quarter's ad spend. Derived means something written from source material, usually by an agent. The ideal customer profile. The positioning document. The plan.

Derived files can be wrong, stale, or quietly circular, where an agent reads its own earlier conclusion and treats it as evidence. So derived never outranks source. When the markdown disagrees with the spreadsheet, the spreadsheet wins, and the agent says so before doing anything else.

That one rule prevents most of the ways these systems rot.

## The folders

```
00_CMO/                    the orchestrator. mission, rules, approval boundaries
01_Strategy/               positioning and the operating plan
02_Customers/              who you serve, and the economics of serving them
   01_acquisition/            how customers were won and what they cost
   02_retention/              whether they come back and what they are worth
03_Campaigns/
   00_Influencers/            creators, partners, earned distribution
   01_Paid_Media/
      00_Paid_Search/         buying demand that already exists
         00_Google_Ads   01_Microsoft_Ads   02_LLM_Ads
      01_Paid_Social/         creating demand that does not
         00_Instagram    01_TikTok          02_Facebook
         03_LinkedIn     04_YouTube         05_Reddit
   02_SEO/                    being found in conventional search
   03_GEO/                    being cited by AI assistants
   04_Owned_Media/            email, blog, podcast, community
04_Analytics/              site, revenue, campaigns, budget, forecast, cohorts
99_Outputs/                the only folder where new files are created
```

Numbers set the order at every level. When you ask for a full pass, the agent works through them in sequence, reading each folder's file as it arrives.

**One file per folder, named after the folder.** Open `03_LinkedIn/` and you find `LinkedIn.md`. Open `02_SEO/` and you find `SEO.md`. That file is pre-built and ready to use: it says how work gets done in that folder, and where a venture has to supply its own facts, it says so in brackets.

Folders ending in `_data` are the exception. They hold your source files and carry a `README.md` naming what belongs there. Twenty-three working files, thirty-one data READMEs, and no folder you open and wonder about.

SEO and GEO sit in separate folders because the work is genuinely different. Search returns a ranked list you can measure. An assistant returns a synthesized answer that changes between sessions, with no position to track and no console reporting your impressions. Same buyer, different problem.

## What actually goes in the data folders

This is the question everyone asks second, right after "where do I start." Every `_data` folder has its own README naming the exports that belong in it, the file naming convention, and the specific trap to watch for. Here is the whole map.

**Customers**

| Folder | Put files like these in it |
|---|---|
| `02_Customers/00_customer_data` | Voice of customer (VoC) call logs and transcripts, interview notes, post-purchase and post-course survey exports, Net Promoter Score results, win and loss notes from your customer relationship management (CRM) system, churn reasons, review text from G2 or the App Store, audience research |
| `01_acquisition/00_acquisition_data` | New customers with first-touch and last-touch source, spend by channel, lead-to-customer conversion rates, sales cycle length, first order value, your Customer Acquisition Cost working file |
| `02_retention/00_retention_data` | Repeat purchase history, cohort tables by acquisition month, churn and cancellation records including the free-text reason, renewal and downgrade events, your Customer Lifetime Value working file |

**Strategy and partners**

| Folder | Put files like these in it |
|---|---|
| `01_Strategy/00_market_data` | Competitor pricing pages and positioning copy you captured, analyst reports you are licensed to read, category sizing research, competitor job postings, earnings call notes |
| `00_Influencers/00_partner_data` | Partner and creator lists with audience overlap estimates, signed agreements, tracked link performance, referral traffic and discount code redemptions, rate cards |

**Paid media**

| Folder | Put files like these in it |
|---|---|
| `00_Google_Ads/00_Google_Ads_data` | Campaign, ad group, keyword, and ad exports, the search terms report, auction insights, impression share, negative keyword lists |
| `01_Microsoft_Ads/00_Microsoft_Ads_data` | The same exports from Bing, with search partner traffic segmented out and LinkedIn profile targeting breakdowns |
| `02_LLM_Ads/00_LLM_Ads_data` | Whatever the platform reports today, plus your own log of where placements appeared and what the surrounding answer said |
| `03_LinkedIn/00_LinkedIn_data` | Campaign Manager exports, and the demographic breakdown showing which seniorities were actually served |
| `01_TikTok/00_TikTok_data` | Ads Manager exports by creative, with hold rate and completion metrics, and creative launch and retirement dates |
| `00_Instagram`, `02_Facebook` | Meta Ads Manager exports with **placement split out**, since Meta blends the two by default |
| `04_YouTube`, `05_Reddit` | Google Ads video exports with placements; Reddit exports by subreddit, plus saved comment threads from your own ads |

**Search and AI visibility**

| Folder | Put files like these in it |
|---|---|
| `02_SEO/00_keyword_data` | Keyword exports with volume, difficulty, and intent from Semrush, Ahrefs, or Keyword Planner |
| `02_SEO/01_search_console_data` | Google Search Console query and page exports, coverage and indexing reports, Core Web Vitals |
| `02_SEO/02_competitor_data` | Competitor keyword and top-page exports, backlink profiles, share of voice trends |
| `02_SEO/03_technical_data` | Screaming Frog or Sitebulb crawls, PageSpeed results, redirect maps, schema validation |
| `03_GEO/00_citation_data` | Whether you were cited, per prompt per run, with the model, version, date, and full response saved |
| `03_GEO/01_prompt_test_data` | Your standing prompt set, the run schedule, and raw responses per model per date |
| `03_GEO/02_brand_mention_data` | Third-party mentions, Wikipedia and Wikidata entries, directory listings, podcast and article appearances |

**Owned media**

| Folder | Put files like these in it |
|---|---|
| `00_email_data` | Klaviyo, Mailchimp, or HubSpot exports with sends, opens, clicks, unsubscribes, list growth by source, flow performance |
| `01_blog_data` | Post-level sessions, time on page, scroll depth, conversions, publishing calendar, internal linking inventory |
| `02_podcast_data` | Downloads and listen-through by episode, platform breakdowns, guest list, show notes referral traffic |
| `03_community_data` | Membership growth, active members, posts per member, engagement by topic, repeating support questions |

**Analytics**

| Folder | Put files like these in it |
|---|---|
| `00_site_data` | Google Analytics 4, Microsoft Clarity, Plausible, or Adobe exports. Sessions by channel and landing page, funnel reports, site search queries |
| `01_revenue_data` | Shopify, Stripe, or enterprise resource planning (ERP) exports. Revenue by product and channel, refunds, discounts, contribution margin working files |
| `02_campaign_performance_data` | Cross-channel results in one file, the blended view no single platform will give you, plus the campaign calendar that explains most unexplained spikes |
| `03_budget_data` | Available capital by period, approved budgets by channel, spend to date and pacing, committed but unspent amounts, agency and tooling costs |
| `04_forecast_data` | Forecast spreadsheets with assumptions written inside them, base, upside and downside scenarios, prior forecasts kept next to actuals |
| `05_cohort_data` | Retention curves by acquisition month and channel, repeat purchase intervals, feature usage by cohort |

**Your data never leaves your machine.** Every `_data` folder is ignored by git and only its README is tracked. That is deliberate. Survey exports and licensed research do not belong in a public repository, and git history keeps them even after you delete the file.

## Your call as the operator

The folders exist so you have somewhere to put things. They are not a to-do list, and filling all of them is not the goal.

You decide which channels you actually run. Most ventures should run two or three well rather than nine badly, and the fastest way to waste a quarter is to open every folder because it is there. If you are not running paid search, `00_Paid_Search` stays empty, or you delete it. If your buyer is not on TikTok, that folder is noise in your repository and noise in your agent's context. Delete what you do not use. You can always add it back.

The same applies to depth. Some ventures need Instagram and Facebook reported separately because the two behave differently for them. Others should collapse both into one folder and move on. The structure should match how you actually make decisions, not how a marketing textbook organizes a chapter.

What the system will not do is choose for you. It can tell you what the evidence supports, what a channel would cost, and what would have to be true for it to work. Which bets you place, and which ones you stop, stays with you. That is the part of the job that does not delegate.

## Where the agent writes

Everything the agent produces lands in `99_Outputs`, named `YYYY-MM-DD_area_short-description.ext`.

That is a convention for tidiness rather than a technical limit. You are welcome to point it anywhere you like on your own machine, and for some workflows you should. The reason for one writable folder is that it keeps the repository clean and makes the whole system portable. You can hand this folder to a different assistant tomorrow, or open it in a different tool, and nothing breaks, because the outputs are separable from the thinking and both are plain text.

An agent with permission to write anywhere spreads files across your system, and you find them three weeks later with no idea which one is current.

## Start here

1. **Clone it and fill in the brackets.** Every working file is already written. The brackets mark the places only you can answer.
2. **Write `00_CMO/CMO.md` first.** It takes about an hour if you do it honestly. Every other folder reads it, so a vague one produces vague work everywhere downstream.
3. **Put one real dataset in.** Pick the least glamorous thing you have. Last quarter's ad performance, or twenty support tickets. A system with one real file beats a beautiful empty structure.
4. **Ask a question that spans folders.** Something like "given what is in `02_Customers`, which channel should get the next dollar, and what would make us stop?" Then read what comes back with the source and derived distinction in mind.

Write your own answer before you ask the agent. Then compare. The disagreements are the useful part, and the habit of committing first is what keeps you the editor rather than the audience.

## The arithmetic underneath

Two equations show up in nearly every folder, and any recommendation that cannot name its term in one of them is decoration.

**Sessions x Conversion Rate x Value = Revenue.** When revenue moves, say which of the three moved, because each one has a different fix.

**Customer Lifetime Value minus Customer Acquisition Cost = Post-Acquisition Value.** If a channel cannot clear that, better creative will not rescue it.

## What this is not

It will not invent evidence you do not have, and it should tell you when you are asking it to and challenge you directly. It does not publish, send, or spend, because those need a human who can be held responsible. It will not turn a vague objective into a strategy, and speeding up a system whose economics do not work just produces bad results faster.

## License

MIT. Use it, fork it, teach with it.

---

If you are deciding where to begin, the useful question is not which agent to use. It is which repeatable part of your marketing work would become dramatically more valuable if it could learn and act faster. Find that, put its data in the right folder, and start there.

Questions? Reach out at: [www.linkedin.com/in/jakecook](https://www.linkedin.com/in/jakecook)

Jake Cook  
Lecturer, Harvard Business School  
Cofounder, OnDigitalMarketing.com
