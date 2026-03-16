---
name: gtm-qualification-scoring
description: >
  Score and prioritize leads, accounts, or pipeline using the FIRE framework
  (Fit, Intent, Recency, Engagement). Use when asked to qualify a prospect,
  score a lead, rank accounts, triage pipeline, or decide who to call first.
license: MIT
compatibility: No code execution required. Works in claude.ai, Claude Code, and API.
metadata:
  author: iCustomer
  version: "1.0.0"
  website: https://icustomer.ai
---

# GTM Qualification Scoring

Score each account across FIRE (Fit · Intent · Recency · Engagement), assign a
priority tier, and recommend a next action. Every score needs traceable evidence.

**Load `shared/fire-framework.md`** before scoring any account — it contains the
full scoring rubric, tier thresholds, and auto-escalation triggers.

**Load `shared/icp-segments.md`** if the user hasn't specified a segment or you
need to identify which segment an account belongs to.

## Steps

1. Identify the account(s) to score
2. Assign the ICP segment (→ `shared/icp-segments.md` if needed)
3. Score each FIRE dimension 1–10 with specific evidence
4. Check auto-escalation triggers (→ `shared/fire-framework.md`)
5. Calculate total: (F + I + R + E) / 4
6. Assign priority tier and write the recommended next action
7. Flag any open intelligence gaps that would change the score

## Output

For a single account:
```
## [Company Name]
Segment: [#] | FIRE: F:[x] I:[x] R:[x] E:[x] → [x.x]/10 | Priority: [🔴/🟡/⚪] [P1/P2/P3]
Auto-Escalate: [⚡ Yes — reason / No]

Evidence: [One sentence per dimension — source + date]
Summary: [Why this account is or isn't worth pursuing right now]
Next Action: [Specific: who, channel, angle, when]
Gaps: [What info would change the score]
```

For 3+ accounts, lead with a ranked summary table, then individual entries sorted by score.

**Load `references/batch-template.md`** if the user provides a list of 5+ accounts
or asks for a CSV-style output.
