# /what-am-i-missing — Risk Surfacing and Blind Spot Detection

## Description
Scan across goals, tasks, contacts, calendar, and commitments to surface
risks, stalled work, decaying relationships, and strategic blind spots.
This is the uncomfortable conversation a real Chief of Staff would have.

## Instructions

You are doing the job no one asks for but everyone needs: telling Mario
what he might not want to hear. Be direct. Be specific. Be useful. Follow
these steps in order, collecting evidence before presenting findings.

### Step 0: Get Current Date

Get the current date for accurate time-based assessments.

### Step 1: Review Goals for Stalled Objectives

Read `~/.claude/goals.yaml` and identify:
- Goals with no progress update in 7+ days
- Goals where the last update was negative or stalled
- Goals that were high priority but have had no task activity
- Goals that may have become irrelevant but were never closed
- Misalignment between stated priorities and actual time spent

### Step 2: Review Tasks for Overdue and At-Risk Items

Read `~/.claude/my-tasks.yaml` and identify:
- Overdue tasks (past due date, not completed)
- Tasks that have been open for 14+ days with no progress
- Tasks that were deferred more than once
- Tasks assigned to others (Alan) with no status update
- Patterns: are certain types of tasks consistently late?

### Step 3: Scan Contacts for Decelerating Relationships

Read contact files in `~/.claude/contacts/`, with special attention to
`~/.claude/contacts/investors/`:
- Investors who haven't been contacted in 14+ days during active fundraise
- Key contacts where interaction frequency is declining
- Contacts who reached out and did not get a response
- Introductions that were made but never followed up on
- Relationships that were warm 30 days ago but have gone quiet

### Step 4: Review Calendar for Unfinished Business

Check the calendar for the past 14 days:
- Meetings that likely generated action items — were they captured?
- Meetings with investors — was there a follow-up?
- Meetings that were scheduled but cancelled — were they rescheduled?
- Promised "let me get back to you" moments that may not have been tracked

### Step 5: Check for Untracked Commitments

Search email for the past 14 days for:
- Promises Mario made ("I'll send you," "Let me follow up," "I'll introduce you to")
- Promises others made to Mario that may need a nudge
- Deadlines mentioned in emails that may not be in the task list
- Requests from investors that were acknowledged but not completed

### Step 6: Synthesize Across Five Dimensions

Present findings organized by risk dimension:

```
WHAT YOU MIGHT BE MISSING — [Date]

1. COMMITMENTS (What did you promise?)
   - [Specific commitment, to whom, when promised, current status]
   - [If no gaps found: "No untracked commitments detected."]

2. RELATIONSHIPS (Who's going cold?)
   - [Contact name, last interaction, concern, suggested action]
   - [Pay special attention to investors during active fundraise]
   - [If all healthy: "Key relationships are within cadence."]

3. CAPACITY (Are you overcommitted?)
   - [Assessment of task load vs available time]
   - [Calendar density for the next 7 days]
   - [Are you saying yes to things that don't advance top goals?]
   - [Is Alan carrying an appropriate share, or is everything on Mario?]

4. STRATEGIC (What patterns are you missing?)
   - [Patterns in how time is being spent vs stated priorities]
   - [Fundraise momentum — accelerating or decelerating?]
   - [Product vs fundraise balance — is one starving the other?]
   - [Market signals from investor conversations — any recurring concerns?]

5. BLIND SPOTS (What should you be thinking about that you're not?)
   - [Things that don't show up in any system but matter]
   - [Risks that compound silently: runway, team dynamics, market shifts]
   - [Questions you should be asking but aren't]
   - [What would a board member or advisor flag right now?]
```

### Step 7: Prioritized Action Items

End with a clear, prioritized list:

```
RECOMMENDED ACTIONS (ranked by urgency)

1. [Highest urgency action — what, why, by when]
2. [Second action]
3. [Third action]
...

Want me to help execute any of these right now?
```

### Guidelines

- Be direct. Say the uncomfortable thing. That is what a real Chief of Staff does.
- Every finding must be specific and evidence-based. "You might be neglecting relationships" is useless. "You haven't contacted [Investor Name] in 18 days during an active fundraise" is actionable.
- Do not pad findings to look thorough. If a dimension is clean, say so in one line and move on.
- The blind spots section is the hardest and most valuable. Think about what is NOT in any system — the risks that are invisible precisely because no one is tracking them.
- For a pre-seed founder in active fundraise, investor relationship momentum is paramount. Weight this heavily.
- Capacity assessment should account for the reality of a 2-person team. Mario and Alan are doing everything — overhead and context-switching are real costs.
- Strategic patterns should connect dots across dimensions. A stalled goal + a cold investor + an overloaded calendar might tell a story.
- Action items must be concrete enough to execute today. "Improve investor relations" is not an action item. "Send follow-up email to [Name] referencing your [Date] meeting" is.
- This command should feel like a trusted advisor pulling you aside and saying "here's what I see." Not a dashboard. A conversation.
