# Customer Success Playbook

**Skill ID:** `cs-playbook`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name |
| `segment` | yes | Customer segment |
| `stages` | no | Lifecycle stages. Default: onboarding, adoption, renewal, expansion |
| `failure_points` | yes | Common failure modes |
| `team_size` | no | CS team capacity |
| `renewal_target` | no | Renewal rate goal |

## Example Request
```json
{
  "skill": "cs-playbook",
  "inputs": {
    "product": "FlowState Enterprise",
    "segment": "Mid-market companies, 20-100 seats, 3+ PMs",
    "stages": "onboarding (days 1-30), adoption (days 31-90), renewal (60 days before), expansion",
    "failure_points": "Low seat utilization in first 60 days, champion leaves company, team doesn't see value beyond one PM using it",
    "team_size": "2 CSMs covering 40 accounts",
    "renewal_target": "92% gross renewal rate"
  }
}
```
