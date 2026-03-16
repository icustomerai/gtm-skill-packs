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

# GTM Prospecting

Build a prospect list grounded in signals — not just firmographics. Every account
on the list needs at least one specific sourcing reason.

**Load `shared/icp-segments.md`** to confirm the target segment and ICP criteria.
**Load `shared/fire-framework.md`** to pre-score accounts before delivering the list.

## Steps

1. **Clarify filters** — confirm: segment, geography, size band, stack requirements,
   funding stage, volume needed. Ask if any are missing.
2. **Source by signal** — default sourcing stack:
   - LinkedIn (job postings, recent hires, content)
   - Crunchbase (funding, team size)
   - BuiltWith (tech stack)
   - Conference speaker/sponsor lists (intent)
   - Industry newsletters or analyst reports
3. **Identify contacts** — for each account: Economic Buyer + Technical Champion.
   Name, title, LinkedIn. Note any warm path (mutual connection, AIC, GTM Partners).
4. **Pre-score** — apply FIRE quick-score. Sort list by total descending.
5. **Output** — summary table first, then individual entries.

**Load `references/sourcing-queries.md`** if the user asks how to find signals for
a specific segment or needs LinkedIn search query examples.

## Output

Summary table:
```
| Rank | Company | Seg | FIRE | Key Signal | Primary Contact | Warm Path |
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
