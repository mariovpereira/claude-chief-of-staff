# /pitch-prep — Pre-Meeting Investor Briefing

## Description
Generate a one-page investor briefing before any pitch meeting. Pull together
investor background, thesis alignment, interaction history, anticipated
questions, and relationship context so Mario walks in fully prepared.

## Arguments
- `<investor-name>` — Name of the investor (matches contact file name)

## Instructions

You are preparing Mario for an investor meeting. Follow these steps in order,
collecting all intelligence before presenting the final briefing.

### Step 0: Identify the Investor

Search `~/.claude/contacts/investors/` for a contact file matching the
provided name. Also check `~/.claude/contacts/` in case the file is there
instead. If no file exists, say so and offer to create one — but continue
with whatever information is available.

### Step 1: Pull Interaction History

From the contact file, extract:
- All logged interactions (dates, channels, summaries)
- Open commitments or follow-ups (either direction)
- Any notes on communication style or preferences
- Relationship temperature — warm, cold, new, re-engaged

### Step 2: Check Calendar and Email

- Search the calendar for upcoming meetings with this investor (next 14 days)
- Note the meeting date, time, location, and any other attendees
- Search email for recent threads with this investor
- Surface any unanswered emails or pending items
- Check if any materials were promised or requested

### Step 3: Research the Investor and Firm

Using available tools, research:
- The investor's firm, fund size, and stated thesis
- Recent investments (last 6-12 months) — especially in AI, developer tools, or adjacent spaces
- Portfolio companies that overlap with or compete with FrontPulse
- The investor's personal focus areas or public statements
- Any mutual connections or warm introductions that were used

If web search is not available, note what should be researched manually
and proceed with what is known from contact files and prior interactions.

### Step 4: Assess Thesis Alignment

Based on the research, articulate:
- How FrontPulse fits (or does not fit) the investor's thesis
- Which aspects of FrontPulse would resonate most with this investor
- Any potential objections based on their investment pattern
- Comparable portfolio companies — are they complementary or conflicting?

### Step 5: Anticipate Questions

Based on FrontPulse's stage (pre-seed, 2-person team, active fundraise),
prepare for likely questions:
- Team: "Why are you and Alan the right team?"
- Market: "How big is this market really?"
- Traction: "What do your numbers look like?"
- Competition: "Who else is doing this?"
- Use of funds: "What will you do with the money?"
- Technical: "What's your technical differentiation?"

Tailor these to the specific investor's known interests and style.

### Step 6: Generate the Briefing

Present the briefing in this format:

```
INVESTOR BRIEFING: [Investor Name]
Firm: [Firm Name] | Meeting: [Date, Time, Location]
Prepared: [Today's date]

INVESTOR BACKGROUND
- [Role, firm, fund details]
- [Investment focus and thesis]
- [Recent notable investments]
- [Personal interests or angles]

THESIS ALIGNMENT
- [How FrontPulse maps to their thesis]
- [Strongest resonance points]
- [Potential friction or gaps]

RELATIONSHIP CONTEXT
- [How you connected, who introduced you]
- [Previous interactions and their tone]
- [Open items: things promised, follow-ups pending]

ANTICIPATED QUESTIONS
1. [Question] — Suggested framing: [response angle]
2. [Question] — Suggested framing: [response angle]
3. [Question] — Suggested framing: [response angle]

THE ASK
- [What Mario is asking for — check size, terms, intro, advice]
- [What to avoid asking for at this stage]

TALKING POINTS
- [Key narrative beats to hit]
- [Specific data points or milestones to mention]
- [Stories or examples that land well for this investor type]

WATCH FOR
- [Red flags or sensitivities to be aware of]
- [Topics to steer toward or away from]
```

### Step 7: Offer Technical Prep

End the briefing with:

"Want me to also prep Alan on the technical questions this investor
is likely to ask?"

### Guidelines

- The briefing should fit on one page when printed. Be concise, not exhaustive.
- Lead with the most decision-relevant information.
- If the investor file is thin, say so — better to know gaps than to guess.
- Never fabricate investor details. If information is not available, flag it as "needs manual research."
- Relationship context matters as much as firm thesis. How warm is the connection?
- Frame everything through the lens of FrontPulse's current stage: pre-seed, 2-person team, Miami AI Lab.
- If there are unresolved follow-ups or broken commitments, surface them prominently — walking into a meeting with an open loop is a risk.
