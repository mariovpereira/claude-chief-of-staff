# /weekly-review — Guided Weekly Reflection

## Description
Structured review of the past 7 days: what happened, what moved, what
stalled, and what it means. Combines calendar, tasks, goals, and
relationship data into an honest retrospective with clear focus for
the week ahead.

## Instructions

You are running Mario's weekly review. This is a deliberate pause to
assess the week honestly — not a status report, but a reflection that
drives better decisions next week. Follow these steps in order.

### Step 0: Get Current Date and Time Range

Get the current date. The review covers the past 7 days. Calculate the
exact date range (e.g., Monday Feb 17 through Sunday Feb 23).

### Step 1: Calendar Review — What Happened

Fetch calendar events for the past 7 days and analyze:
- Total number of meetings
- Total hours in meetings vs total available hours
- Meetings by category (investor, product, team, personal, other)
- Any cancelled or rescheduled meetings
- Meetings that ran without clear outcomes
- How much uninterrupted deep work time existed

### Step 2: Tasks — What Got Done vs What Was Planned

Read `~/.claude/my-tasks.yaml` and compare:
- Tasks completed this week (list them)
- Tasks that were due this week but not completed (list them)
- Tasks added this week (were they planned or reactive?)
- Completion rate: completed / (completed + overdue)
- Any tasks that were deferred or rescheduled

### Step 3: Goals — What Moved

Read `~/.claude/goals.yaml` and assess each active goal:
- Did it advance this week? How?
- Did it stall? Why?
- Is the current trajectory on track for the goal's timeline?
- Were any goals effectively abandoned without being closed?

### Step 4: Relationships — Who You Connected With

Scan contact files and calendar for relationship activity:
- Who did Mario meet with this week?
- Any new contacts or introductions?
- Key contacts who were NOT engaged this week but should have been
- Investor pipeline activity: any movement?
- Relationship investments that will pay off vs those that were reactive

### Step 5: Present the Structured Review

```
WEEKLY REVIEW — [Date Range]

WINS (What went right)
- [Specific accomplishments, breakthroughs, or progress]
- [Things that landed well, deals that advanced, problems solved]
- [Even small wins count — name them]

PROGRESS (Goal movement)
- [Goal 1]: [Status — advanced / stalled / regressed] — [specifics]
- [Goal 2]: [Status] — [specifics]
- [Goal 3]: [Status] — [specifics]

TASKS
- Completed: [X] of [Y] planned
- Overdue: [list if any]
- Added (reactive): [list if any]

RELATIONSHIPS (Who you connected with, who you didn't)
- Connected: [Key meetings and interactions]
- Missed: [Contacts who should have heard from you]
- Pipeline: [Investor or deal pipeline movement]

PATTERNS (What I notice about how time was spent)
- [Observations about meeting density, deep work availability]
- [Where time went vs where goals say it should go]
- [Reactive vs proactive ratio]
- [What kept coming up this week — recurring themes?]

GROWTH (What you learned this week)
- [Insights from meetings, reading, building, failing]
- [Anything that shifted your thinking]
- [Skills practiced or developed]

NEXT WEEK FOCUS (Top 3 priorities)
1. [Highest priority — specific and measurable]
2. [Second priority]
3. [Third priority]
```

### Step 6: Reflection Prompts

After the review, ask:

"Anything from this week you want to capture in book notes or
reference materials?"

Then ask:

"Any patterns or decision rules that emerged this week? If a
situation came up where you had to make a judgment call, we can
encode that as a rule in judgment.yaml so the system handles it
automatically next time."

### Step 7: Capture Outcomes

If Mario wants to capture notes:
- Book notes: Write to the appropriate location
- Judgment rules: Format as YAML and propose for `~/.claude/judgment.yaml`

If nothing to capture, that is fine. Not every week produces rules.

### Guidelines

- The review should take 5-10 minutes to read, not 30. Be concise.
- Wins section is mandatory even in a bad week. Name what went right, even if it is small.
- Patterns section is the highest-value part. Connect dots that Mario might not see in the daily grind.
- Be honest about stalled goals. Persistent stalling is a signal — either the goal is wrong or the approach is wrong.
- Next Week Focus should be three things, not ten. Fewer priorities means more gets done.
- For a pre-seed founder, the key tension is usually product vs fundraise vs operations. Name which got attention and which got starved.
- Completion rate is a useful signal but not a judgment. Some weeks are exploratory. That is fine if it was intentional.
- The judgment.yaml prompt is important. This is how the system gets smarter over time. But do not force it — if nothing emerged, say so.
- Growth section should be genuine, not performative. "Nothing notable this week" is a valid answer.
