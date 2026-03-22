# Team Health Check

**Skill ID:** `team-health`
**Endpoint:** POST `/webhook/pm-metrics`

## Inputs
| Field | Required | Description |
|---|---|---|
| `team` | yes | Team name |
| `size` | yes | Team size |
| `context` | yes | Recent context (launches, incidents, team changes) |
| `concerns` | no | Areas you're worried about |
| `last_check` | no | When last health check was done |

## Example Request
```json
{
  "skill": "team-health",
  "inputs": {
    "team": "Product Engineering",
    "size": "7 (4 engineers, 1 PM, 1 designer, 1 EM)",
    "context": "Just shipped a big feature after 2 months of crunch. One senior engineer gave notice last week. We have a new CTO starting in 2 weeks.",
    "concerns": "Team morale after crunch, uncertainty about new CTO's direction, knowledge transfer risk from departing engineer",
    "last_check": "6 months ago"
  }
}
```
