# Executive Update Generator

**Skill ID:** `exec-update`
**Endpoint:** POST `/webhook/pm-writing`

## Inputs
| Field | Required | Description |
|---|---|---|
| `topic` | yes | What this update is about |
| `audience` | no | Default: leadership team |
| `situation` | yes | Current state |
| `complication` | yes | What changed or is at risk |
| `data` | yes | Key supporting data points |
| `ask` | yes | What you need from them |

## Example Request
```json
{
  "skill": "exec-update",
  "inputs": {
    "topic": "Enterprise onboarding crisis — at risk of losing 2 accounts",
    "audience": "CEO and VP Customer Success",
    "situation": "Two enterprise accounts (combined $96K ARR) completed implementation 6 weeks ago and are in their 90-day review period",
    "complication": "Both accounts have low adoption — 23% and 31% seat utilization. Both CSMs flagged renewal risk. One account mentioned Notion as an alternative in last week's check-in.",
    "data": "Industry benchmark for healthy 90-day utilization is 60%+. Our average across all enterprise accounts is 58%. These two are outliers.",
    "ask": "Approve emergency onboarding rescue package: dedicated CSM for 30 days + free training sessions + 1-month extension on contract"
  }
}
```
