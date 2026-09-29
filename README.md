# Agentic Marketing

A working marketing system built out of folders, markdown files, and a short set of rules about who may change what. Clone it, point it at your own venture, and run it with an AI agent.

## Why this shape

An AI agent needs five things before it produces anything worth keeping: an objective, context/data, tools, guardrails, and feedback. Most agent demos supply the objective inside a clever prompt and skip the other four, which is why the output looks impressive for about a minute and then turns out to be unusable.

A folder structure supplies four of the five, in a form you can read, correct, and hand to somebody else. `CLAUDE.md` at the root carries the guardrails. The numbered folders carry the context, separated by stage so the agent loads only what the question needs. Each folder's `SKILL.md` carries the objective for that piece of work. The data folders carry the feedback, because that is where real evidence lands.

The part people underestimate is the fifth one. Your proprietary customer data and context are the only durable advantage here. Everyone has the same models these days.

## The rule that does the most work

Every file in this repository is either **source** or **derived**.

Source means original material that you or a data provider produced. A survey export. A call transcript. Last quarter's ad spend. Derived means something written from source material, usually by an agent. The ideal customer profile. The positioning document. The plan.

Derived files can be wrong, stale, or quietly circular, where an agent reads its own earlier conclusion and treats it as evidence. So derived never outranks source. When the markdown disagrees with the spreadsheet, the spreadsheet wins, and the agent says so before doing anything else.

That one rule prevents most of the ways these systems rot.

## The folders

```
00_CMO/                       the orchestrator. mission, rules, approval boundaries
01_Strategy/                  positioning and the operating plan
02_Customers/                 who you serve, and the economics of serving them
   01_acquisition/               how customers were won and what they cost
   02_retention/                 whether they come back and what they are worth
03_Campaigns/
   00_Influencers/               creators, partners, earned distribution
   01_Paid_Media/
      00_Paid_Search/            buying demand that already exists
      01_Paid_Social/            creating demand that does not
         00_Instagram  01_TikTok  02_Facebook
         03_LinkedIn   04_YouTube 05_Reddit
   02_SEO_GEO/                   search engines and AI assistants
   03_Owned_Media/               email, blog, podcast, community
04_Analytics/                 site, revenue, and cohort measurement
99_Outputs/                   the only folder where new files may be created
```

Numbers set the order at every level. When you ask for a full pass, the agent works through them in sequence, reading each folder's `SKILL.md` as it arrives.

**Every folder carries exactly one of two files, and its name tells you which.** A folder where work happens has a `SKILL.md` describing how that work is done. A folder ending in `_data` holds source files and has a `README.md` describing what belongs there. Nineteen skill files and twenty-three data READMEs, so there is never a folder you open and wonder about.

## What actually goes in the data folders

This is the question everyone asks second, right after "where do I start." Every `_data` folder has a README naming the exports that belong in it, with a naming convention and the trap to watch for. A sample:

| Folder | Put files like these in it |
|---|---|
| `02_Customers/00_customer_data` | Voice of customer (VoC) call logs and transcripts, interview notes, survey exports, Net Promoter Score results, win and loss notes, churn reasons, review text |
| `02_Customers/01_acquisition/00_acquisition_data` | New customers by source, spend by channel, lead-to-customer rates, sales cycle length, your Customer Acquisition Cost working file |
| `02_Customers/02_retention/00_retention_data` | Repeat purchase history, cohort tables by acquisition month, churn and cancellation records, your Customer Lifetime Value working file |
| `01_Paid_Media/.../03_LinkedIn/00_LinkedIn_data` | Campaign Manager exports, and the demographic breakdown showing which seniorities were actually served |
| `02_SEO_GEO/01_search_console_data` | Google Search Console query and page exports, coverage reports |
| `02_SEO_GEO/03_geo_citation_data` | Logged prompts run against AI assistants, with the model, date, and full response saved |
| `03_Owned_Media/00_email_data` | Klaviyo or Mailchimp exports, list growth by source, flow performance |
| `04_Analytics/01_revenue_data` | Shopify or Stripe transactions, revenue by product and channel, contribution margin working files |

**Your data never leaves your machine.** Every `_data` folder is ignored by git and only its README is tracked. That is deliberate. Survey exports and licensed research do not belong in a public repository, and git history keeps them even after you delete the file.

## Start here

1. **Clone it and delete my examples.** Rename the three `.template.md` files by dropping `.template`, then fill them in for your venture.
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

Jake Cook
Harvard Business School
