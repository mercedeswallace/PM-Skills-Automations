# Feature Decomposition Tool

**Skill ID:** `feature-decomposition`
**Endpoint:** POST `/webhook/pm-planning`

## Inputs
| Field | Required | Description |
|---|---|---|
| `feature` | yes | Feature name and description |
| `user_story` | yes | As a [user], I want [goal] so that [benefit] |
| `tech_stack` | no | Relevant tech constraints |
| `team_size` | no | Who's working on it |
| `deadline` | no | Hard deadline if any |

## Example Request
```json
{
  "skill": "feature-decomposition",
  "inputs": {
    "feature": "In-app notifications system — users get notified when teammates comment on their specs",
    "user_story": "As a PM, I want to see notifications when someone comments on my work so I don't miss feedback",
    "tech_stack": "React frontend, Node.js backend, PostgreSQL, no real-time infra yet",
    "team_size": "2 engineers, 1 week each available",
    "deadline": "Must ship before April 15 for customer demo"
  }
}
```
