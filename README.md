# iCustomer GTM Skill Packs

> v1.0.0 · [icustomer.ai](https://icustomer.ai) · MIT License

A collection of 7 go-to-market skills for Claude Code and OpenClaw. Covers the full GTM loop — ICP definition through outbound execution — powered by the FIRE scoring framework.

---

## Install

### OpenClaw
```bash
openclaw skills add https://github.com/icustomer/gtm-skills
```

### Claude Code
Clone into your project root and Claude Code will automatically pick up `CLAUDE.md`:
```bash
git clone https://github.com/icustomer/gtm-skills .claude/skills/gtm
```
Or add to an existing project's `CLAUDE.md`:
```markdown
See skills in `.claude/skills/gtm/` for GTM workflows.
```

---

## Skills

| Skill | Trigger phrases |
|---|---|
| **gtm-icp-definition** | "help me define our ICP," "who are our best customers," "refine our ICP" |
| **gtm-account-research** | "research this account," "brief me on [company]," "prep for meeting with [company]" |
| **gtm-qualification-scoring** | "score this lead," "qualify this account," "rank my pipeline," "who do I call first" |
| **gtm-prospecting** | "build a prospect list," "find companies that match our ICP," "fill pipeline for Q[X]" |
| **gtm-meeting-prep** | "prep me for my call with X," "I have a meeting with [company] tomorrow" |
| **gtm-outbound-strategy** | "write a cold email," "build an outbound campaign," "draft a LinkedIn DM" |
| **gtm-inbound-strategy** | "design our inbound motion," "build a lead routing model," "our trial signups aren't activating" |

---

## Shared References

Skills load these on demand — you never reference them directly:

- **`shared/fire-framework.md`** — FIRE scoring rubric (Fit · Intent · Recency · Engagement), priority tier thresholds, and auto-escalation triggers
- **`shared/icp-segments.md`** — 5 ICP segments, negative ICP criteria, known clients list

---

## FIRE Framework

Every qualification and prospecting output is scored on:

| Dimension | What it measures | 8–10 signal |
|---|---|---|
| **F** Fit | ICP match: industry, size, stack, GTM model | Exact segment match, warehouse user, right buyer |
| **I** Intent | Active buying behavior | Job posting for CDP/data role, RFP in market |
| **R** Recency | Freshness of intent signals | Signal within 30 days |
| **E** Engagement | Prior contact with your brand | Demo request, event attendance, outreach reply |

**Tiers:** 🔴 P1 (8.0–10.0) · 🟡 P2 (5.0–7.9) · ⚪ P3 (1.0–4.9)

---

## Structure

```
├── CLAUDE.md                          # Auto-loaded by Claude Code
├── skills/
│   ├── gtm-account-research/SKILL.md
│   ├── gtm-icp-definition/SKILL.md
│   ├── gtm-inbound-strategy/SKILL.md
│   ├── gtm-meeting-prep/SKILL.md
│   ├── gtm-outbound-strategy/SKILL.md
│   ├── gtm-prospecting/SKILL.md
│   └── gtm-qualification-scoring/SKILL.md
└── shared/
    ├── fire-framework.md
    └── icp-segments.md
```

---

## License

MIT — see [LICENSE](LICENSE)
