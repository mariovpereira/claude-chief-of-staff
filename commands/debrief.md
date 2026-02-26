# /debrief — Post-Meeting Debrief

## Description
Capture decisions, follow-ups, relationship notes, and commitments from a
meeting in one shot. Updates the relevant contact file, commitment tracker,
and task list. Run this immediately after any important meeting — especially
investor meetings.

## Arguments
- `<person-name>` — Debrief a meeting with a specific person
- (no argument) — Debrief the most recent calendar event that just ended

## Instructions

You are running a post-meeting debrief for Mario. The goal is to capture
everything important before context fades, and route it to the right files.

### Step 0: Identify the Meeting

If a person name is provided, look up their contact file and find the most
recent calendar event with them.

If no argument, check Google Calendar for the most recent event that ended
in the last 2 hours. If multiple candidates, ask Mario which one.

Confirm: "Debriefing your [time] meeting with [person/people]. Correct?"

### Step 1: Gather the Debrief

Ask Mario (or accept if he's already typing):

```
Quick debrief — answer what applies:

1. What was decided?
2. What did you commit to? (follow-ups, deliverables, intros)
3. What did they commit to?
4. Key takeaways or signals? (enthusiasm, concerns, surprises)
5. Anything to remember for next time? (personal notes, preferences)
```

If Mario gives a stream-of-consciousness answer, that's fine — extract
the structured information from it. Don't force a rigid format on input.

### Step 2: Route to Files

Based on the debrief, update the following files:

**Contact file** (`~/.claude/contacts/` or `~/.claude/contacts/investors/`):
- Add to Interaction History: date, type (meeting), summary
- Update Last Interaction fields
- Add any new personal notes or talking points
- Update relationship temperature or pipeline stage if investor

**Commitment tracker** (`~/.claude/accountability/commitments.md`):
- Add any commitments Mario made (with due dates if mentioned)
- Note any commitments the other party made (for follow-up tracking)

**Task list** (`~/.claude/my-tasks.yaml`):
- Create tasks for any follow-ups with due dates
- Align to goals where applicable (investor meetings align to "close-pre-seed")

**Investor pipeline** (if investor meeting, `~/.claude/fundraising/pipeline.md`):
- Update pipeline stage if it changed
- Update temperature based on signals
- Add notes on their concerns or enthusiasm

### Step 3: Draft Follow-Up (if applicable)

If a follow-up message is warranted (it usually is after investor meetings):
- Draft a thank-you / follow-up email in Mario's voice
- Reference specific discussion points to show attentiveness
- Include any promised deliverables or next steps
- Propose specific times for the next meeting if discussed (check calendar)

Present the draft. **Never send without explicit approval.**

### Step 4: Persist to Memory

Use Vestige (`smart_ingest`) to store:
- Meeting summary with key decisions and signals
- Any relationship shifts observed (warming, cooling, new concerns)
- Commitments made by both sides

Tag with "debrief", the person's name, and today's date.

### Step 5: Confirm and Close

Present a summary of everything captured:

```
DEBRIEF CAPTURED — [Person], [Date]

Updated files:
  - contacts/[person].md — added interaction, updated [fields]
  - accountability/commitments.md — [N] new commitments
  - my-tasks.yaml — [N] new tasks
  - fundraising/pipeline.md — [stage change or "no change"]

Follow-up draft: [ready / not needed]

Stored to memory: [summary of what was persisted]

Anything else from this meeting?
```

### Guidelines

- Speed matters. Run this within 30 minutes of the meeting ending while context is fresh.
- Don't over-formalize Mario's input. Accept casual notes and structure them.
- For investor meetings, always update the pipeline stage and temperature.
- Every commitment made should become a tracked item — this is how trust is built.
- If Mario mentions something the other person said about a third party, consider whether it warrants updating that third party's contact file too.
- The follow-up draft should go out within 24 hours of the meeting. If it's an investor meeting, same-day is better.
- If the meeting went poorly, capture that honestly. Accurate records are more valuable than optimistic ones.
