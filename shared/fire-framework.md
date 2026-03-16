# FIRE Scoring Reference
> iCustomer · v1.0.0

## Formula
FIRE Total = (F + I + R + E) / 4  [max 10.0]

## Dimension Signals

**F — Fit** (ICP match: industry, size, stack, GTM model)
- 8–10: Exact segment match, right size, warehouse user, correct buyer present
- 5–7: Partial match, 1–2 ICP criteria missing
- 1–4: Wrong industry, size, or no data infrastructure

**I — Intent** (active buying behavior)
- 8–10: Active job posting for CDP/data role, RFP in market, or vendor comparison
- 5–7: Conference attendance, published data strategy content, recent tech investment
- 1–4: No visible intent signals

**R — Recency** (freshness of intent signals)
- 8–10: Signal within 30 days
- 6–7: Signal 31–90 days ago
- 4–5: Signal 91–180 days ago
- 1–3: Older than 180 days or unknown

**E — Engagement** (prior contact with your brand or ecosystem)
- 8–10: Direct engagement (demo request, event attendance, reply to outreach)
- 6–7: Indirect (newsletter subscriber, mutual connection, AIC/GTM Partners network)
- 4–5: Warm ecosystem (LinkedIn follower, 2nd-degree connection)
- 1–3: Cold — no prior contact

## Priority Tiers
| FIRE Total | Tier | Action |
|---|---|---|
| 8.0–10.0 | 🔴 P1 | Personalized outreach this week |
| 5.0–7.9 | 🟡 P2 | Sequence within 30 days |
| 1.0–4.9 | ⚪ P3 | Nurture only |

## Auto-Escalate to P1 (regardless of score) ⚡
- Migrating off Segment, mParticle, Lytics, or Tealium
- Job posting: "composable CDP," "CDP replacement," or "data activation platform"
- Post-Series B with active paid media but no CDP
- Publicly described CDPs as "too expensive" or "too complex"
- Announced Retail Media Network in last 90 days
- Major Snowflake/BigQuery/Databricks expansion or certification

## Grounding Rules
- Every score needs traceable evidence — never assign a score without a reason
- Mark unverifiable signals as `[Unverified]`
- Score conservatively when evidence is thin
