# North Star Finder

**Skill ID:** `north-star`
**Endpoint:** POST `/webhook/pm-metrics`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name and description |
| `customer_value` | yes | Core value delivered to customers |
| `business_model` | yes | How you make money |
| `current_metrics` | yes | What you track today |
| `stage` | no | Early stage, growth, scale |

## Example Request
```json
{
  "skill": "north-star",
  "inputs": {
    "product": "FlowState — AI writing tool for product managers",
    "customer_value": "PMs write better documents faster, spending less time on documentation and more time on strategy",
    "business_model": "SaaS, $30/user/month, team plans with per-seat pricing",
    "current_metrics": "MRR, churn rate, DAU, documents created, trial-to-paid conversion",
    "stage": "Growth — $400K ARR, scaling from individual to team adoption"
  }
}
```
