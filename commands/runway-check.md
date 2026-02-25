# /runway-check — Cash and Burn Tracking

## Description
Review current cash position, calculate burn rate and runway, break down
expenses by category, and flag financial risks. Conservative projections,
early warnings, no sugarcoating.

## Instructions

You are running a financial health check for Mario. At pre-seed stage with
a 2-person team, every dollar matters and runway clarity is non-negotiable.
Follow these steps in order.

### Step 0: Get Current Date

Get the current date for accurate runway calculations.

### Step 1: Read Financial Data

Read `~/.claude/fundraising/overview.md` for:
- Current cash on hand
- Total raised to date
- Source of funds (SAFE notes, grants, personal, etc.)
- Any expected incoming funds (committed but not yet received)

If the file does not exist, ask Mario to provide:
- Current bank balance
- Monthly approximate spend
- Any expected inflows

Proceed with whatever data is available.

### Step 2: Calculate Burn Rate

If burn tracking data exists (in `~/.claude/fundraising/` or similar):
- Calculate average monthly burn over the last 3 months
- Identify the trend: increasing, decreasing, or stable
- Note any one-time expenses that skew the average

If detailed tracking is not available, work with whatever Mario provides
or what is documented in the overview file.

### Step 3: Compute Runway

Calculate:
- **Gross runway:** Cash on hand / average monthly burn
- **Net runway (if applicable):** Factor in any committed incoming funds
- **Conservative runway:** Cash on hand / highest monthly burn from last 3 months

Flag immediately if any of these drop below 6 months.

### Step 4: Break Down Burn by Category

Categorize expenses where data is available:

| Category | Monthly Cost | % of Burn | Notes |
|----------|-------------|-----------|-------|
| Cloud / Infrastructure | | | AWS, GCP, Vercel, etc. |
| AI / API Costs | | | Anthropic, OpenAI, etc. |
| Tools / SaaS | | | Dev tools, productivity, analytics |
| Legal / Accounting | | | Incorporation, IP, compliance |
| Payroll / Contractors | | | If applicable |
| Office / Co-working | | | If applicable |
| Marketing / Events | | | If applicable |
| Miscellaneous | | | Everything else |

If detailed category data is not available, note what categories should
be tracked and offer to set up a tracking template.

### Step 5: Compare Actual vs Projected

If projections exist in the fundraising docs:
- Compare actual burn to projected burn
- Flag any categories significantly over projection
- Note categories that came in under budget
- Assess whether original assumptions still hold

If no projections exist, skip this step and recommend creating them.

### Step 6: Present the Financial Summary

```
RUNWAY CHECK — [Date]

CASH POSITION
- Cash on hand: $[amount]
- Total raised: $[amount]
- Committed (not received): $[amount or "None"]

BURN RATE
- Average monthly burn (3-month): $[amount]
- Trend: [Increasing / Decreasing / Stable]
- Highest recent month: $[amount] ([month])
- Lowest recent month: $[amount] ([month])

RUNWAY
- Current runway: [X] months (to [month/year])
- Conservative runway: [X] months (to [month/year])
- [FLAG if < 6 months: "WARNING: Runway below 6 months. Fundraise timeline is critical."]
- [FLAG if < 3 months: "CRITICAL: Less than 3 months runway. This requires immediate action."]

BURN BREAKDOWN
[Category table from Step 4]

ACTUAL VS PROJECTED
[Comparison from Step 5, or "No projections on file — recommend creating them"]

PATH TO NEXT RAISE
- Estimated fundraise start needed: [date, based on 6-month runway buffer]
- Key milestones to hit before raising: [from goals.yaml if applicable]
- Current fundraise status: [active/planned/not started]

KEY FINANCIAL DATES
- [Any upcoming payments, deadlines, or milestones]
- [SAFE conversion triggers if applicable]
- [Grant deadlines or reporting dates]
```

### Step 7: Surface Risks and Recommendations

After the summary, provide:
- Top 1-3 financial risks right now
- Specific cost-reduction opportunities if runway is tight
- Recommendations for burn optimization
- Whether the current burn rate supports reaching the next fundraise milestone

### Guidelines

- Be conservative on all projections. Round cash down, round burn up.
- Flag concerns early and directly. A chief of staff who sugarcoats runway numbers is worse than useless.
- If data is incomplete, say exactly what is missing and why it matters.
- Do not fabricate financial numbers. If data is not available, say so.
- Runway below 6 months is a yellow flag. Below 3 months is red. Say it plainly.
- At pre-seed with a 2-person team, every unnecessary expense is weeks of runway. Be ruthless about calling out waste.
- The "path to next raise" section is critical — fundraising takes longer than founders expect. Build in buffer.
- If tracking data does not exist yet, offer to create a simple monthly tracking template. Good financial hygiene starts now.
- This is for Mario's eyes only. Treat all financial data as highly confidential.
