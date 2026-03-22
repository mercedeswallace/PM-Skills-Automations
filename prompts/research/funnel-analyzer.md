# Funnel Analyzer

**Skill ID:** `funnel-analyzer`
**Endpoint:** POST `/webhook/pm-research`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product or flow being analyzed |
| `funnel` | yes | Steps and conversion rates |
| `segment` | no | User segment |
| `time_period` | no | Date range |
| `context` | no | Any known context |

## Example Request
```json
{
  "skill": "funnel-analyzer",
  "inputs": {
    "product": "FlowState signup to paid conversion funnel",
    "funnel": "1. Visit landing page: 10,000 users → 2. Start signup: 2,200 (22%) → 3. Complete signup: 1,800 (82%) → 4. Complete onboarding: 540 (30%) → 5. Create first doc: 380 (70%) → 6. Invite teammate: 95 (25%) → 7. Convert to paid: 57 (60%)",
    "segment": "All users, organic traffic",
    "time_period": "Q1 2026",
    "context": "Onboarding was redesigned in February — data includes both old and new flow"
  }
}
```
