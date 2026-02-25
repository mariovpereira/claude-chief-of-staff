# /investor-update — Monthly Investor Update

## Description
Draft a monthly investor update email. Pull from goals, completed tasks,
email activity, and current status to produce an honest, send-ready update
in Mario's voice. Never sends without explicit approval.

## Instructions

You are drafting Mario's monthly investor update. This is one of the most
important recurring communications for a pre-seed founder — it builds trust,
keeps investors engaged, and creates a record of progress. Follow these
steps in order.

### Step 0: Get Current Date

Get the current date to determine the reporting period. The update covers
the previous calendar month unless Mario specifies otherwise.

### Step 1: Review Goals Progress

Read `~/.claude/goals.yaml` and for each active goal:
- What was the status at the start of the month vs now?
- Which milestones were hit?
- Which goals stalled or regressed?
- Any goals added or removed during the month?

### Step 2: Review Completed Tasks

Read `~/.claude/my-tasks.yaml` and identify:
- Tasks completed during the reporting period
- Tasks that were due but not completed (be honest)
- Major deliverables or outputs produced
- Group completions into themes (product, fundraise, team, etc.)

### Step 3: Scan Investor Communications

Search email for interactions with investors during the month:
- New introductions or meetings
- Follow-ups sent or received
- Any commitments made (intros promised, materials sent, etc.)
- Pipeline movement (who advanced, who went cold)

Also check `~/.claude/contacts/investors/` for recent updates.

### Step 4: Check Financial Context

If `~/.claude/fundraising/overview.md` exists, pull:
- Current cash position
- Burn rate
- Runway remaining
- Any fundraising milestones (term sheets, commitments, closes)

If the file does not exist, skip this section and note that financial
data was not available.

### Step 5: Draft the Update

Format the update as a send-ready email:

```
Subject: [Company Name] — [Month Year] Update

Hey everyone,

TL;DR
[Three sentences max. What happened, what matters, what's next.
This is the only part most investors will read — make it count.]

METRICS
[If applicable — only include if there are real numbers to share.
Table format preferred. Don't fabricate metrics.]

| Metric | Last Month | This Month | Delta |
|--------|-----------|------------|-------|
| [metric] | [value] | [value] | [+/-] |

HIGHLIGHTS
- [What went well — 2-4 bullets, specific and concrete]
- [Include wins, milestones, learnings that matter]

CHALLENGES
- [What's hard right now — 1-3 bullets, honest]
- [Investors respect founders who name their problems]

ASKS
- [Specific, actionable asks — intros, advice, resources]
- [Make it easy for investors to help. "Know anyone at X?" > "Help with BD"]

RUNWAY
- Cash on hand: $[amount]
- Monthly burn: $[amount]
- Runway: [X] months
- [Any fundraising status if relevant]

Thanks for being on this journey with us.

Mario
```

### Step 6: Review and Refine

Before presenting:
- Check that the tone is direct and honest — not corporate polish
- Verify the TL;DR captures the actual essence of the month
- Make sure challenges section is genuinely honest, not performative
- Confirm asks are specific enough that someone could act on them today
- Ensure no confidential information is included that shouldn't go to all investors

### Step 7: Present for Approval

Present the draft and explicitly state:

"Here's the draft investor update. I will NOT send this until you
approve it. Review and let me know what to change."

### Guidelines

- Mario's voice: direct, honest, founder energy. Not corporate, not polished, not performative.
- The TL;DR is the most important part. Most investors skim. Make those three sentences count.
- Challenges section is mandatory. An update with no challenges reads as either delusional or dishonest.
- Asks must be specific. "Intro to [specific person] at [specific company] for [specific reason]" beats "help with partnerships."
- If there are no real metrics yet, skip the metrics table. Don't invent vanity metrics.
- Runway section: be conservative. Round down on cash, round up on burn.
- Never fabricate progress. If it was a slow month, say so. Consistency and honesty build more trust than manufactured momentum.
- This email goes to people who wrote checks. Respect their investment with candor.
- Always wait for explicit approval before sending. No exceptions.
