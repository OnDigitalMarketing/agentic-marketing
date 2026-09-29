---
name: customer-evidence
description: How customer data is read, what may be reported from it, and how the ideal customer profile gets written.
version: 1.0
scope: internal-only
owner: [Your name]
updated: [YYYY-MM-DD]
---

# 02_Customers

## What this folder is for

The people we sell to, described from evidence rather than belief. `customer_data` holds the raw material. `icp.md` is written from it.

## What lives here

| Path | Status |
|---|---|
| `customer_data/` | **Source. Read only.** Never edited, never committed. |
| `icp.md` | Derived. Written from the data above. |

See `customer_data/README.md` for what belongs in that folder.

## Before you start

Read `customer_data/README.md` and list what is actually in the folder. If you do not know what a file is, what one row represents, or what a column means, stop and ask.

## How work gets done

1. Inventory the data. Name each file, its date range, and its sample size.
2. Separate what customers did from what they said they would do. Behavior outranks stated intent.
3. Build the profile from repeated patterns, not from the most vivid single response.
4. Write the qualification test: what you could ask a stranger to find out in five minutes whether they fit.
5. Name the gap between who we reach today and who we want. That gap is usually the whole proposition.
6. Record what you do not know, and what evidence would close it.

## Output contract

- Every number carries its unit, its denominator, and the file it came from.
- Every percentage carries its sample size.
- Say plainly when a group is too small to support a claim.
- Label each conclusion as evidence, inference, or hypothesis.

## Guardrails

- De-identified data stays de-identified. No verbatim responses, no row-level copies, no small-group breakdowns in any derived file. Aggregates only.
- Licensed third-party research stays in this folder. Do not redistribute it, and do not commit it.
- If a markdown file disagrees with the data, the data wins, and you say so before doing anything else.

## Definition of done

An ideal customer profile where every claim points at a file, a sample size, and a date.
