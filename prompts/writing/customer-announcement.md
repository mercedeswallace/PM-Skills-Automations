# Customer Announcement Writer

**Skill ID:** `customer-announcement`
**Endpoint:** POST `/webhook/pm-writing`

## Inputs
| Field | Required | Description |
|---|---|---|
| `launch` | yes | What's launching |
| `benefit` | yes | Key customer benefit |
| `audience` | no | Who it's for |
| `launch_date` | yes | When |
| `tone` | no | Default: professional and warm |
| `channels` | no | Default: email, in-app, social |

## Example Request
```json
{
  "skill": "customer-announcement",
  "inputs": {
    "launch": "AI Document Assistant — generates first drafts of PRDs, roadmaps, and strategy docs from a bullet list",
    "benefit": "Cut document writing time from 2 hours to 15 minutes",
    "audience": "All paid users",
    "launch_date": "April 1, 2026",
    "tone": "excited but not hypey",
    "channels": "email, in-app banner, Twitter/X"
  }
}
```
