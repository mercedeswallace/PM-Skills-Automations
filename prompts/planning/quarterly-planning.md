# Quarterly Planning Template

**Skill ID:** `quarterly-planning`
**Endpoint:** POST `/webhook/pm-planning`

## Inputs
| Field | Required | Description |
|---|---|---|
| `company` | yes | Company or team name |
| `quarter` | yes | e.g. "Q2 2026" |
| `annual_goals` | yes | Annual OKRs or goals this quarter serves |
| `resources` | yes | Team headcount and budget |
| `constraints` | yes | What limits what you can do |
| `opportunities` | yes | What you could pursue |

## Example Request
```json
{
  "skill": "quarterly-planning",
  "inputs": {
    "company": "FlowState — AI PM tools",
    "quarter": "Q2 2026",
    "annual_goals": "Reach $1M ARR, achieve 60% activation rate, NPS > 50",
    "resources": "6 engineers, 1 PM, 1 designer, $50K marketing budget",
    "constraints": "No new hires until Q3, legacy billing system needs refactor before new pricing",
    "opportunities": "Enterprise inbound picking up, partnership with PM community (5K members), AI features driving trial signups"
  }
}
```
