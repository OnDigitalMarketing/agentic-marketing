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

| Folder | What it holds | Status |
|---|---|---|
| `00_CMO` | The orchestrator. Mission, operating rules, approval boundaries. Start here. | Derived |
| `01_Strategy` | Positioning and the current operating plan | Derived |
| `02_Customers` | Customer evidence, and the ideal customer profile written from it | Source and derived |
| `03_Campaigns` | Owned media, paid media, search, and partner programs | Source and derived |
| `04_Analytics` | Measurement plan and performance data | Source and derived |
| `99_Outputs` | The only folder where new files may be created | Working area |

Numbers set the order. When you ask for a full pass, the agent works through them in sequence, reading each folder's `SKILL.md` as it arrives.

## What actually goes in the data folders

This is the question everyone asks second, right after "where do I start."

| Folder | Put files like these in it |
|---|---|
| `02_Customers/customer_data` | Voice of customer (VoC) call logs and transcripts, customer interview notes, post-purchase and post-course survey exports, Net Promoter Score results, win and loss notes from your customer relationship management (CRM) system, churn reasons, review text from G2 or the App Store, audience research |
| `03_Campaigns/SEO_GEO/keyword_data` | Keyword exports with volume and intent from Semrush or Ahrefs, Google Search Console performance pulls, competitor page exports, logged generative engine citation checks |
| `04_Analytics/analytics_data` | Site analytics by channel and landing page from Google Analytics 4, advertising performance by campaign and creative from Google Ads or Meta or LinkedIn, email performance from Klaviyo or Mailchimp, revenue and order exports from Shopify or Stripe, cohort and retention pulls, your customer acquisition cost and lifetime value working file |

Each of those folders has its own README with naming conventions and the questions to answer before anyone analyzes the file.

**Your data never leaves your machine.** Every data folder is ignored by git, and only the READMEs are tracked. That is deliberate. Survey exports and licensed research do not belong in a public repository, and git history keeps them even after you delete the file.

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
