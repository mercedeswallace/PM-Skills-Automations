# Sprint Planning Assistant

**Skill ID:** `sprint-planning`
**Endpoint:** POST `/webhook/pm-planning`

## Inputs
| Field | Required | Description |
|---|---|---|
| `sprint_goal` | yes | What this sprint is trying to achieve |
| `capacity` | yes | e.g. "4 engineers × 8 days = 32 eng-days" |
| `backlog` | yes | List of items to consider |
| `velocity` | no | Last 3 sprint velocity averages |
| `risks` | no | Known blockers or dependencies |

## Example Request
```json
{
  "skill": "sprint-planning",
  "inputs": {
    "sprint_goal": "Ship onboarding v2 — reduce time-to-value from 14 days to 3 days",
    "capacity": "4 engineers × 8 days = 32 eng-days, 1 designer × 5 days",
    "backlog": "Empty state redesign (5pts), Welcome email sequence (3pts), Product tour (8pts), Progress tracker (5pts), Onboarding analytics (3pts), Bug fixes from last sprint (2pts)",
    "velocity": "28, 31, 26 story points",
    "risks": "Designer out Thursday/Friday, API dependency on auth team"
  }
}
```
