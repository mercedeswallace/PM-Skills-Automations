# Onboarding Flow Designer

**Skill ID:** `onboarding-flow`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name |
| `user` | yes | Target user persona |
| `aha_moment` | yes | First value moment — what makes them say "this is useful" |
| `current` | no | Current onboarding if any |
| `drop_offs` | no | Known drop-off points |
| `key_actions` | yes | Actions that predict long-term retention |

## Example Request
```json
{
  "skill": "onboarding-flow",
  "inputs": {
    "product": "FlowState",
    "user": "PM who just signed up, likely frustrated with how long writing docs takes",
    "aha_moment": "Seeing their first AI-generated PRD draft in under 2 minutes",
    "current": "Email verification → blank dashboard with 4 template options → no guidance after that",
    "drop_offs": "60% of users never create a second document. 40% don't complete their first doc.",
    "key_actions": "Create first doc, invite a teammate, connect Jira or Notion integration"
  }
}
```
