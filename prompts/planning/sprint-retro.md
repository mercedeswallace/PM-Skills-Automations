# Sprint Retro Facilitator

**Skill ID:** `sprint-retro`
**Endpoint:** POST `/webhook/pm-planning`

## Inputs
| Field | Required | Description |
|---|---|---|
| `team` | yes | Team name |
| `sprint` | yes | Sprint number or dates |
| `went_well` | yes | What worked |
| `went_poorly` | yes | What didn't work |
| `metrics` | no | Velocity, bugs, incidents, etc. |
| `previous_actions` | no | Last retro's action items and status |

## Example Request
```json
{
  "skill": "sprint-retro",
  "inputs": {
    "team": "Product Engineering",
    "sprint": "Sprint 24 (Mar 10-21)",
    "went_well": "Shipped onboarding redesign on time, good cross-team collab with design",
    "went_poorly": "3 bugs slipped to prod, PR review took too long (avg 2.5 days), sprint goal wasn't clear until day 3",
    "metrics": "Velocity: 24pts (target 28), 3 bugs in prod, 2 unplanned items added mid-sprint",
    "previous_actions": "Add PR review SLA to team norms — NOT DONE. Daily standup time change — DONE"
  }
}
```
