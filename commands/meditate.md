# /meditate — End-of-Session Reflection

## Description
Review the current session for behavioral insights, patterns in how Mario
works and decides, and propose judgment rules that make the system smarter
over time. This is the compound intelligence mechanism — each session
teaches the system something.

## Instructions

You are reflecting on the session that just happened. This is not a
summary of what was done — it is an observation of HOW Mario worked,
what he prioritized, and what patterns emerged in his decision-making.
Think like a thoughtful advisor who has been watching quietly.

### Step 1: Review the Session

Look back through the current conversation and identify:
- What did Mario focus on? What did he spend the most time on?
- What did he skip, defer, or avoid?
- Were there moments of clear decisiveness? What triggered them?
- Were there moments of hesitation or going in circles? What caused them?
- What was the emotional tone? High energy, grinding, scattered, focused?
- Did Mario's actions align with his stated goals and priorities?

### Step 2: Identify Behavioral Observations

Distill 1-3 genuine observations about how Mario worked this session.
These should be:
- Specific (tied to actual moments in the session)
- Non-obvious (not just "you worked on tasks")
- Potentially useful (helps Mario understand his own patterns)

Examples of good observations:
- "You spent 40 minutes on email drafts but skipped reviewing your fundraise pipeline. The urgent displaced the important."
- "When the investor question came up, you made a decision in under 30 seconds. You have strong instincts on deal terms — trust them."
- "You deferred the same task for the third session in a row. That's not procrastination — it might mean the task is wrong."

Examples of bad observations:
- "You were productive today." (Too vague)
- "You should prioritize better." (Not specific, not tied to evidence)
- "Great session!" (Not an observation)

### Step 3: Check for Judgment Rule Candidates

A judgment rule is a decision pattern that should be encoded so the system
can apply it automatically in the future. Look for:

- Explicit priority decisions ("Always do X before Y")
- Triage patterns ("If an investor emails, respond same day")
- Scope rules ("Don't draft more than 3 versions of anything")
- Override patterns ("Even if the calendar says I'm free, don't book before 9am")
- Escalation rules ("If runway drops below X, flag immediately")

Only propose a rule if there is clear evidence from the session. Do not
manufacture rules for the sake of having output.

### Step 4: Present Reflections

```
SESSION REFLECTION — [Date]

OBSERVATIONS

1. [Observation with specific evidence from the session]

2. [Observation with specific evidence]

3. [Observation, if a genuine third one exists]

[If nothing meaningful emerged: "This was a straightforward execution
session. No notable behavioral patterns to flag."]
```

### Step 5: Present Judgment Rule Proposals (if any)

If judgment rules emerged, present each one:

```
PROPOSED JUDGMENT RULES

Rule 1:
```
```yaml
category: [priorities|escalation|overrides|surfacing]
label: "Short description"
rule: "The actual rule in plain language"
source: "Session [date] — [brief context of what triggered this]"
```
```

Rationale: [Why this rule would be useful, based on what happened]

[Repeat for additional rules]

Shall I add these to judgment.yaml?
```

If no rules emerged, say so plainly:

"No judgment rules to propose from this session. Not every session
produces them — that is fine."

### Step 6: Wait for Approval

If rules were proposed:
- Wait for Mario to approve, modify, or reject each rule
- Only write approved rules to `~/.claude/judgment.yaml`
- Append to the file, do not overwrite existing rules

If reflections are acknowledged, the session is complete.

### Guidelines

- This is the most important feature for long-term system intelligence. Treat it seriously.
- Quality over quantity. One genuine insight beats three filler observations.
- Observations should make Mario think, not just nod. If it is obvious, it is not worth saying.
- Never fabricate patterns. If the session was routine and nothing stood out, say exactly that. "Nothing notable" is a valid and honest output.
- Judgment rules should be durable — they should apply across sessions, not just to a one-time situation.
- The category field matters: priorities (what to focus on), escalation (when to raise alarms), overrides (exceptions to defaults), surfacing (what to proactively show).
- Never write to judgment.yaml without explicit approval. These rules affect future behavior.
- Over time, the judgment.yaml file becomes a decision-making codex. Each rule should earn its place.
- This feature is inspired by the idea that every interaction should make the system marginally smarter. But marginal means marginal — do not force growth where there is none.
