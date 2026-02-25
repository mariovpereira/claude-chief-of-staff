# Decision Log — Miami AI Lab

Track architectural and business decisions with full context so future-you understands why.

## Template

| Field | Value |
|-------|-------|
| **Date** | YYYY-MM-DD |
| **Decision** | What was decided |
| **Context** | Why this decision was needed |
| **Options Considered** | What alternatives were evaluated |
| **Rationale** | Why this option was chosen |
| **Impact** | What this affects |
| **Revisit By** | When to reconsider (if applicable) |

---

## Decisions

### 2026-02-25: AI Chief of Staff Selection

| Field | Value |
|-------|-------|
| **Date** | 2026-02-25 |
| **Decision** | Fork mimurchison/claude-chief-of-staff under MiamiAILab org |
| **Context** | Needed an operational backbone for founder productivity — email triage, relationship CRM, goal tracking |
| **Options Considered** | 5 projects evaluated: tomochang/ai-chief-of-staff (MIT), kbanc85/claudia (PolyForm NC), tronmongoose/chiefofstaff (no license), davekilleen/Dex (MIT), vinaysrao1/gws-mcp (not a CoS) |
| **Rationale** | MIT license (zero legal ambiguity), built by a peer CEO (Mike Murchison, Ada), clean architecture, extensible. Claudia was more mature but PolyForm Noncommercial license disqualified it for startup use. |
| **Impact** | Foundation for all operational workflows — triage, contacts, goals, fundraising |
| **Revisit By** | 2026-06-01 — evaluate if the system compounds as expected |
