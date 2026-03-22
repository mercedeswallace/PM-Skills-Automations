# SWOT Analysis Generator

**Skill ID:** `swot-analysis`
**Endpoint:** POST `/webhook/pm-strategy`

## Inputs
| Field | Required | Description |
|---|---|---|
| `company` | yes | Company or product name |
| `industry` | yes | What market you're in |
| `context` | yes | Current situation, recent events, strategic challenge |
| `question` | no | The specific question to answer. Default: "What should our strategic priorities be?" |

## Example Request
```json
{
  "skill": "swot-analysis",
  "inputs": {
    "company": "FlowState — AI-powered PM productivity tool",
    "industry": "B2B SaaS / Product Management tooling",
    "context": "We have 800 active users, strong NPS of 72, but struggling to convert free to paid. Main competitor just raised $20M. We have 18 months runway.",
    "question": "Should we focus on converting existing free users or acquiring new paid users directly?"
  }
}
```

## Output Sections
1. Strengths (internal positives)
2. Weaknesses (internal negatives)
3. Opportunities (external positives)
4. Threats (external negatives)
5. Cross-quadrant strategies (SO, WO, ST, WT)
6. Top 3 recommended actions with rationale
