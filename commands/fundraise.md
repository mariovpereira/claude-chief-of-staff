# /fundraise — Fundraising Dashboard

## Description
Your fundraising command center. Scan investor contacts for stale relationships,
surface upcoming LP meetings, track term sheet status, review pipeline health,
and draft follow-up outreach. This is the command that earns its keep during
the roadshow.

## Arguments
- (no argument) — Full fundraising dashboard: pipeline, relationships, next actions
- `pipeline` — Pipeline summary only: stages, counts, coverage
- `outreach` — Draft follow-up messages for investors who need attention
- `stale` — Surface investor relationships that are cooling or overdue

## Instructions

You are running the fundraising dashboard for Mario. This command synthesizes
across investor contacts, calendar, email, and memory to give a complete
picture of the raise.

### Step 0: Load Context

**Memory recall:** Query Vestige (`recall`) for recent memories tagged
"fundraise", "investor", or "pipeline". Query Cortex (`get_context`) for
fundraising project context.

**Load files:**
- Read `~/.claude/fundraising/overview.md` for round details and committed capital
- Read `~/.claude/fundraising/pipeline.md` for pipeline stages
- Read `~/.claude/judgment.yaml` and apply any `escalation` rules related to investors

### Step 1: Pipeline Health Check

Scan all investor contact files in `~/.claude/contacts/investors/` and
`~/.claude/investors/`. For each investor:
- Current pipeline stage
- Last interaction date and channel
- Temperature (Hot/Warm/Cool/Cold)
- Open follow-ups or next steps
- Contact velocity: is this relationship accelerating, stable, or decelerating?

Compute pipeline summary:
- Total investors by stage
- Total dollar amounts discussed (if tracked)
- Pipeline coverage ratio (pipeline $ / target $) — aim for 3-5x
- Movement since last check (who advanced, who stalled, who went cold)

### Step 2: Relationship Velocity Scan

For each investor in active pipeline stages (First Meeting through Legal):
- Calculate days since last contact
- Compare to their typical response cadence
- Flag any relationship showing deceleration (responding slower, less engaged)
- Flag any relationship showing acceleration (responding faster, asking for more info)

Present velocity signals prominently — these are early indicators of
commitment or disengagement that matter more than absolute time gaps.

### Step 3: Calendar Scan

Check Google Calendar for:
- Upcoming investor meetings in the next 14 days
- Which of those have contact files with prep notes
- Any investor meetings in the last 7 days that may need follow-up
- Flag meetings with no follow-up sent within 24 hours

### Step 4: Email & Communication Scan

Check Gmail and Slack for:
- Unreplied investor messages (always Tier 1)
- Term sheet or investment-related keywords in recent messages
- Introductions made to new investors that need follow-up
- Any investor who sent a "pass" or "not right now" response

### Step 5: Present the Dashboard

```
FUNDRAISING DASHBOARD — [Date]

ROUND STATUS
Target: $[amount] | Committed: $[amount] | Pipeline: $[amount]
Coverage: [X]x target | Runway: [months] at current burn

PIPELINE ([total] investors)
  Committed:      [count] — $[amount]
  Term Sheet:     [count]
  Due Diligence:  [count]
  Follow-up:      [count] — [names]
  First Meeting:  [count] — [names]
  Outreach:       [count]
  Prospecting:    [count]

VELOCITY SIGNALS
  Accelerating: [names and what changed]
  Decelerating: [names and concern] — ACTION NEEDED
  Stale (no contact 7+ days in active stages): [names]

UPCOMING (next 14 days)
  [date] — [investor] — [meeting type] — [prep status]

NEEDS FOLLOW-UP
  [investor] — [last meeting date] — [what was discussed] — [suggested follow-up]

NEXT ACTIONS (prioritized)
1. [most urgent action]
2. [second action]
3. [third action]
```

### Step 6: Outreach Mode (if `outreach` argument)

For each investor needing follow-up or re-engagement:
1. Pull their contact file for context and communication style
2. Reference the last interaction and any open threads
3. Draft a personalized follow-up in Mario's voice
4. Include specific scheduling proposals (check calendar first)

**Never send without explicit approval.**

### Step 7: Persist to Memory

Use Vestige (`smart_ingest`) to store:
- Pipeline snapshot (for trend tracking over time)
- Velocity signals observed
- Any new information about investor sentiment

Tag with "fundraise" and today's date.

### Guidelines

- This is the most important command during an active raise. Treat it accordingly.
- Velocity matters more than absolute dates. An investor going from 24h responses to 4-day responses is a signal even if 4 days is "normal."
- Be direct about pipeline health. If coverage is thin, say so. If momentum is slowing, say so.
- Every investor in Follow-up or later stages should have a clear next step. If one doesn't, flag it.
- Term sheet activity is always the highest priority item in this dashboard.
- Don't draft outreach for investors who have passed unless Mario specifically asks.
- If the pipeline is healthy and momentum is good, say that too — founders need positive signals during a raise.
