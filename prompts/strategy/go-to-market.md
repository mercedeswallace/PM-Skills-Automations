# Go-to-Market Strategy

**Skill ID:** `go-to-market`
**Endpoint:** POST `/webhook/pm-strategy`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | What you're launching and what it does |
| `target_market` | yes | Who you're selling to |
| `launch_date` | yes | When you need to be live |
| `budget` | no | Marketing/launch budget |
| `differentiators` | yes | What makes this different from alternatives |
| `stage` | no | pre-launch, beta, GA. Default: pre-launch |

## Example Request
```json
{
  "skill": "go-to-market",
  "inputs": {
    "product": "AI-powered sprint planning tool that auto-generates tickets from meeting notes",
    "target_market": "Engineering managers at Series A-C SaaS companies (50-500 employees)",
    "launch_date": "May 1 2026",
    "budget": "$15,000",
    "differentiators": "Saves 3 hours per sprint, integrates with existing Jira/Linear, no behavior change required",
    "stage": "pre-launch"
  }
}
```

## Output Sections
1. Positioning statement
2. Channel strategy with specific tactics
3. Messaging framework (headline, proof points, objection handling)
4. 90-day launch timeline
5. Success metrics
