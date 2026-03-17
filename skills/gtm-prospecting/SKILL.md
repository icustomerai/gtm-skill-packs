---
name: gtm-prospecting
description: >
  Build targeted prospect lists using ICP criteria and buying signal filters.
  Use when asked to find net-new accounts, build a target list, fill pipeline
  for a segment or campaign, or identify companies matching a given profile.
  Triggers: "build a prospect list," "find companies that match our ICP,"
  "who should we target in [vertical]," "I need to fill pipeline for Q[X]."
license: MIT
compatibility: Requires web search access for live signal sourcing.
metadata:
  author: iCustomer
  version: "1.0.0"
  website: https://icustomer.ai
---

> Prerequisite: `gtm-icp-definition` (ICP criteria) and `gtm-account-research` (research signals). If either is missing, prompt: *"Have you completed [skill]? It provides [what it produces] which this step needs."*
> Next: `gtm-qualification-scoring` — run full FIRE scoring on your prioritized prospect list.

# GTM Prospecting

Build a prospect list grounded in signals — not just firmographics. Every account
on the list needs at least one specific sourcing reason.

**Gate rule:** If candidate account discovery returns more than 10 accounts, complete
Step 3 (account prioritization) in full before proceeding to Step 4 (contact discovery).
Do not skip ahead to contacts on a broad, unranked list.

## Steps

1. **Clarify filters** — confirm: ICP segment, geography, size band, stack requirements,
   funding stage, volume needed. Ask if any are missing.
2. **Source by signal** — discover candidate accounts using:
   - LinkedIn (job postings, recent hires, content)
   - Crunchbase (funding, team size)
   - BuiltWith (tech stack)
   - Conference speaker/sponsor lists (intent)
   - Industry newsletters or analyst reports
3. **Prioritize accounts** — if discovery yields more than 10 accounts, apply FIRE
   scoring (Fit · Intent · Recency · Engagement, 1–10 each) to every candidate.
   Produce a ranked account table sorted by FIRE total descending. Select Top K
   accounts (default: 10, or the number specified by the user). Only carry Top K
   forward to contact discovery.
4. **Identify contacts** — for each Top K account only: Economic Buyer + Technical
   Champion. Name, title, LinkedIn, email if findable. Note any warm path
   (mutual connection, shared network).
5. **Output** — summary table first, then individual entries.

## FIRE Quick-Score (for list ranking)

Score each dimension 1–10:
- **F Fit**: Does the account match your ICP criteria?
- **I Intent**: Any active buying signals (job postings, RFP, content)?
- **R Recency**: How fresh is the signal? (≤30 days = 8–10, ≤90 days = 6–7)
- **E Engagement**: Any prior contact with your brand or network?

Total = (F + I + R + E) / 4 → 🔴 P1 ≥ 8.0 · 🟡 P2 ≥ 5.0 · ⚪ P3 < 5.0

## Output

Summary table:
```
| Rank | Company | Segment | FIRE | Key Signal | Primary Contact | Warm Path |
```

Per-account entry:
```
## [Company]
Website · Segment · Size · Stack signals
Signal: [Specific reason this company made the list — not generic]
Contact: [Name · Title · LinkedIn]
FIRE: F:[x] I:[x] R:[x] E:[x] → [x.x]/10
First Touch: [Channel + 1-sentence angle]
```

**Rule**: 10 well-sourced accounts beat 50 firmographic matches. Flag volume-padding.
