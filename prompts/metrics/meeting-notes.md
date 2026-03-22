# Meeting Notes Processor

**Skill ID:** `meeting-notes`
**Endpoint:** POST `/webhook/pm-metrics`

## Inputs
| Field | Required | Description |
|---|---|---|
| `meeting_type` | yes | e.g. Sprint planning, Executive review, Customer call |
| `attendees` | yes | Who was there |
| `notes` | yes | Raw notes — paste as-is |
| `date` | no | Default: today |

## Example Request
```json
{
  "skill": "meeting-notes",
  "inputs": {
    "meeting_type": "Q2 planning kickoff",
    "attendees": "Mercedes (PM), Ryan (CTO), Sarah (Design), Tom (Engineering Lead)",
    "notes": "Discussed Q2 priorities - everyone agrees revenue is #1. Ryan wants to focus on enterprise features. Mercedes pushed back saying churn is a bigger problem than new logos. Tom said the infra needs work before we can scale. Sarah showed mockups for onboarding v2 - everyone loved it. Decided to do onboarding first then enterprise. Ryan will talk to the 3 at-risk enterprise accounts this week. Mercedes to send revised Q2 plan by Friday. Need to decide on hiring - EM role still open. Tom thinks we need a data engineer more than EM right now.",
    "date": "2026-03-22"
  }
}
```
