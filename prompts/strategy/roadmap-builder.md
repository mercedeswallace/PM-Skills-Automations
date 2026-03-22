# Roadmap Builder

**Skill ID:** `roadmap-builder`
**Endpoint:** POST `/webhook/pm-strategy`

## Inputs
| Field | Required | Description |
|---|---|---|
| `goals` | yes | What the roadmap is trying to achieve |
| `constraints` | yes | Budget, team size, tech debt, deadlines |
| `priorities` | yes | What matters most right now |
| `timeframe` | no | Default: 12 months |
| `team_size` | no | Helps calibrate capacity |

## Example Request
```json
{
  "skill": "roadmap-builder",
  "inputs": {
    "goals": "Increase activation rate from 30% to 60%, reduce churn from 8% to 4%",
    "constraints": "Team of 6 engineers, no new hires until Q3, legacy auth system needs refactor",
    "priorities": "Activation first, then retention, growth is secondary",
    "timeframe": "12 months",
    "team_size": "6 engineers, 1 designer"
  }
}
```

## Output Sections
1. Executive Summary
2. Goals & Success Metrics
3. Roadmap by Quarter
4. Key Risks & Dependencies
5. Open Questions
