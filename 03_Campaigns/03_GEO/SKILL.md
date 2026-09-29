---
name: geo
description: Generative engine optimization. Being cited when somebody asks an AI assistant instead of a search engine.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# 03_GEO

Read `../SKILL.md` first.

## What this folder is for

Showing up inside answers rather than inside a list of links. When a buyer asks an assistant to compare options in your category, this folder is about whether you are one of the options it names.

## Why this is separate from SEO

The surfaces overlap and the work does not. Search returns a ranked list you can measure; an assistant returns a synthesized answer that varies by session, model, and phrasing. There is no position to track, no volume figure to pull, and no console reporting your impressions. What you can measure is whether you were mentioned, what was said, and what got cited instead.

## Data folders

`00_citation_data`, `01_prompt_test_data`, `02_brand_mention_data`.

## How work gets done

1. Write the questions your buyer would actually ask an assistant. Ten to twenty, in their words, taken from `02_Customers` rather than invented.
2. Run them on a fixed schedule across the assistants your buyer uses. Log the prompt, the model and version, the date, and the full response every time.
3. Record three things per run: were you named, what was said about you, and which sources were cited instead.
4. Read the cited sources. Those are the pages the models trust in your category, and that list is the most actionable thing in this folder.
5. Recommend based on the gap between what you publish and what gets cited.

## What actually seems to move it

Being quotable and being corroborated. Clear claims, specific numbers, plain structure, and the same facts about you repeated consistently across places a model already trusts. Third-party mentions carry weight your own site cannot supply on its own.

## Guardrails

- **Results are not reproducible.** The same prompt returns different answers across sessions. One run proves nothing, so track the rate across repeated runs and say how many you did.
- Do not report a citation rate without the prompt set, the models, and the dates behind it.
- This is a young discipline with more confident advice than evidence. Label your recommendations as hypotheses and test them.
- Never manufacture third-party mentions.

## Definition of done

The prompt set, the models and dates tested, mention rate across runs, what was cited instead, and one hypothesis to test next.
