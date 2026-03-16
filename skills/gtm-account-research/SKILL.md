---
name: gtm-account-research
description: >
  Deep-dive a target company and produce a structured account intelligence brief
  covering tech stack, buying signals, key personas, and a recommended engagement
  angle. Use before outreach, a first call, a demo, or setting up an ABM campaign.
  Triggered by: "research this account," "brief me on [company]," "what do I know
  about [company]," or when preparing for a meeting with a named account.
license: MIT
compatibility: Requires web search access for live signal research.
metadata:
  author: iCustomer
  version: "1.0.0"
  website: https://icustomer.ai
---

# GTM Account Research

Produce an Account Intelligence Brief for a named company. Ground every signal
in a specific, traceable source.

**Load `shared/icp-segments.md`** to assign the account's ICP segment.

## Steps

1. **Snapshot** — company name, HQ, size, business model, recent news (last 90 days)
2. **Tech stack** — focus on: data warehouse (Snowflake/BQ/Databricks), CDP/identity,
   CRM, paid channels, marketing automation. Use BuiltWith, job postings, engineering blogs.
3. **Buying signals** — job postings, conference attendance, funding events, published
   content on data strategy. Date every signal.
4. **Displacement triggers** — check against the list in `shared/fire-framework.md`.
   If any trigger fires, flag ⚡ immediately.
5. **Personas** — identify Economic Buyer (CDO/CMO/CRO), Technical Champion
   (VP Data/Marketing Ops), and End User. Name + LinkedIn URL when findable.
6. **Engagement angle** — one specific recommendation: what pain, which product
   (Decision OS or Audience Loop), what channel, who reaches out first.

**Load `references/stack-signals.md`** if the user asks about a specific tool,
asks how to detect stack signals, or the company's stack is unclear.

## Output

```
# Account Brief: [Company] | [Date]

Snapshot: [3 sentences — what they do, size, recent context]
ICP Segment: [#]
Stack: [Warehouse · CDP · CRM · Paid · MA — tool or "Unknown"]
Signals: [Bulleted — signal + source + date]
Displacement: [⚡ Yes — detail / None detected]
Personas: [Name · Title · LinkedIn · Pain point — one row per person]
Gaps: [What's missing that would sharpen the approach]

Engagement Angle:
[Specific: pain → product → channel → who reaches out → opening hook]
```

Keep the brief scannable. Flag any detail as `[Unverified]` if not directly observed.
