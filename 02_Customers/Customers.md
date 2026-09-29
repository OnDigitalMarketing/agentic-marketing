---
name: customer-evidence
description: The ideal customer profile, written from evidence rather than belief, plus the rules for reading customer data.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# Customers

The people you sell to, described from evidence. `00_customer_data` holds the raw material. This file is written from it. `01_acquisition` and `02_retention` carry the economics.

**Every claim below points at a file, with a sample size and a date.** A claim with no source is a hypothesis and gets labeled as one. This file loses to the data whenever they disagree.

## The arithmetic this folder owns

Everything in `02_Customers` hangs on one equation:

> **Customer Lifetime Value minus Customer Acquisition Cost = Post-Acquisition Value**

`02_retention` produces the first term. `01_acquisition` produces the second. This folder is where they meet, and the answer sets the ceiling that every campaign has to respect.

**State the ceiling explicitly here, because the campaign folders read it from this file.**

| Term | Current value | Source | Date | Confidence |
|---|---|---|---|---|
| Customer Lifetime Value (contribution profit, discounted) | [ ] | | | |
| Customer Acquisition Cost (blended) | [ ] | | | |
| Post-Acquisition Value | [ ] | | | |
| **Maximum acceptable acquisition cost** | **[ ]** | | | |

If Post-Acquisition Value is negative, stop. No campaign fixes it, and the constraint is product, pricing, or retention rather than marketing. Say that plainly rather than proposing a channel test.

If you do not have these numbers yet, write "unknown" rather than a guess, and say so every time a campaign asks for the ceiling. An unknown ceiling is a real finding. A fabricated one gets spent against.

## How work gets done here

1. Inventory the data first. Name each file, its date range, and its sample size. If you do not know what a file is, what one row represents, or what a column means, stop and ask.
2. Separate what customers did from what they said they would do. Behavior outranks stated intent.
3. Build the profile from repeated patterns, not from the most vivid single response.
4. Record what you do not know, and what evidence would close it.

## 1. The customer

Who they are, what they do all day, what they are responsible for. Write about observed behavior, not a demographic sketch.

*Source:* [file, n=, date]

### Qualification test

Three to five questions that separate a fit from a non-fit in a short conversation.

1.
2.
3.

## 2. What triggers them to act

The event that turns a background annoyance into a funded priority. This is usually the most valuable line in the file and the most commonly skipped.

*Source:* [file, n=, date]

## 3. What they do today instead

The current workaround, what it costs them, and why it persists.

## 4. The gap

The distance between who you reach today and who you want. In numbers if you have them.

## 5. Message architecture

| Segment | What they care about | The claim we make | Proof we have |
|---|---|---|---|
| | | | |

## 6. Where they actually are

Channels ranked by where this buyer already spends attention, not by which channel you enjoy.

| Rank | Channel | Why | Evidence |
|---|---|---|---|

## 7. Scale and kill rules

What result would make you spend more, and what result would make you stop.

## 8. Limits

What this file does not know. Be specific, because this section tells future readers how far to trust the rest.

## Guardrails

- Every number carries its unit, its denominator, and the file it came from. Every percentage carries its sample size.
- De-identified data stays de-identified. No verbatim responses, no row-level copies, no small-group breakdowns. Aggregates only.
- Licensed third-party research stays in `00_customer_data`. Do not redistribute it.
- Say plainly when a group is too small to support a claim.
