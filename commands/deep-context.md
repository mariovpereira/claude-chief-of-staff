# /deep-context — Deep Memory and Context Pull

## Description
Pull together everything known about a topic — person, project, deal, or
concept — from across all data sources. Not a data dump, but a synthesized
narrative that connects the dots and surfaces what matters.

## Arguments
- `<topic>` — A person's name, project name, deal name, or concept

## Instructions

You are doing a deep context pull on a topic for Mario. The goal is to
assemble scattered information into a coherent picture that helps Mario
think and act. Follow these steps in order.

### Step 0: Classify the Topic

Determine what kind of topic this is:
- **Person** — A contact, investor, advisor, partner, or collaborator
- **Project/Deal** — A product initiative, partnership, investment deal, or workstream
- **Concept** — An idea, strategy, technology, or theme

The classification determines which sources to prioritize and how to
structure the output.

### Step 1: Search Contact Files

Search `~/.claude/contacts/` and `~/.claude/contacts/investors/` for:
- Direct matches (the topic IS a contact)
- Mentions of the topic in other contact files (related people)
- Shared projects, introductions, or connections

### Step 2: Search Goals and Tasks

Search `~/.claude/goals.yaml` and `~/.claude/my-tasks.yaml` for:
- Goals related to the topic
- Tasks related to the topic (active, completed, or overdue)
- Timeline of activity — when did work on this start, peak, and slow?

### Step 3: Search Documents and Notes

Search `~/.claude/` and subdirectories for any files mentioning the topic:
- Fundraising documents
- Meeting notes
- Strategy docs
- Book notes or reference materials
- Judgment rules that reference the topic

### Step 4: Search Email and Calendar

If email MCP is connected:
- Search email for threads involving or mentioning the topic
- Pull the most recent and most significant threads
- Note the arc: how has the conversation evolved over time?

If calendar MCP is connected:
- Search for meetings related to the topic
- Past meetings: what happened and when
- Upcoming meetings: what is scheduled

### Step 5: Search Memory Systems

If Vestige or Cortex memory systems are available:
- Query for memories related to the topic
- Pull any stored decisions, patterns, or context
- Surface memories that might connect to the topic indirectly

If memory systems are not available, skip this step silently.

### Step 6: Synthesize and Present

The output format depends on the topic type.

**For a Person:**
```
DEEP CONTEXT: [Name]

PROFILE
- [Role, company, location]
- [How you know them, who connected you]
- [Tier and relationship status]

RELATIONSHIP TIMELINE
- [Chronological history of interactions, decisions, and milestones]
- [Not just dates — the arc of the relationship]

CONNECTED PEOPLE
- [Other contacts related to this person — shared meetings, introductions, mutual connections]

OPEN ITEMS
- [Anything unresolved: promised follow-ups, pending asks, unanswered questions]

RELEVANT CONTEXT
- [Goals, tasks, or projects that involve this person]
- [Recent email threads or calendar events]
- [Anything from memory systems]

RELATIONSHIP ASSESSMENT
- [Current temperature: warm, cooling, cold, new, deepening]
- [What is the trajectory? Where is this heading?]
- [What would strengthen this relationship right now?]
```

**For a Project/Deal:**
```
DEEP CONTEXT: [Project/Deal Name]

OVERVIEW
- [What this is, when it started, current status]
- [Key people involved]

TIMELINE
- [Chronological decisions, milestones, and events]
- [The story of how this evolved]

KEY DECISIONS MADE
- [Decisions that shaped the current state]
- [Rationale where known]

OPEN QUESTIONS
- [Unresolved issues, pending decisions, blockers]

RELATED CONTACTS
- [People connected to this project/deal]
- [Their roles and current engagement level]

CURRENT STATUS
- [Where things stand right now]
- [What the next milestone or decision point is]
```

**For a Concept:**
```
DEEP CONTEXT: [Concept]

REFERENCES
- [Every mention found across all sources]
- [Organized by recency and relevance]

RELATED DECISIONS
- [Decisions that were influenced by or relate to this concept]

PATTERNS
- [How this concept has evolved in Mario's thinking]
- [Connections to other concepts, goals, or strategies]

CONNECTED PEOPLE
- [Contacts associated with this concept]

OPEN THREADS
- [Active work or discussions related to this concept]
```

### Step 7: Offer to Go Deeper

End every deep context pull with:

"What angle do you want to go deeper on?"

This invites Mario to direct the next level of exploration rather than
ending the conversation.

### Guidelines

- Synthesis, not data dump. The value is in connecting dots, not listing everything found.
- Present information as a narrative where possible. "You first met [Name] in October when [Context]. Since then, the relationship has..." is better than a table of dates.
- If a source has no relevant information, skip it silently. Do not report "no results found in goals.yaml" — just move on.
- Surface surprising connections. The best deep context pulls reveal things Mario did not realize were related.
- Be honest about gaps. If context is thin, say so: "Limited information available — only 2 email threads and one contact file."
- For investors during active fundraise, always flag the fundraise-relevant angles: pipeline stage, last contact, next step, any concerns.
- The "open items" or "open questions" section is critical. Unresolved items are where value leaks.
- Recency matters. Weight recent information more heavily, but do not ignore older context that still shapes the situation.
- If Vestige/Cortex are not available, do not mention them. Just work with what is available.
- The final "go deeper" prompt is important. Deep context is often the start of a decision process, not the end.
