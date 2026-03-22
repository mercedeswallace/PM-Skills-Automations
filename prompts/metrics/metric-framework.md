# Metric Framework Builder

**Skill ID:** `metric-framework`
**Endpoint:** POST `/webhook/pm-metrics`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name |
| `business_model` | yes | SaaS, marketplace, etc. |
| `stage` | yes | Company/product stage |
| `team_structure` | no | How teams are organized |
| `data_available` | no | What data you can measure today |
| `framework` | no | AARRR or input/output. Default: AARRR |

## Example Request
```json
{
  "skill": "metric-framework",
  "inputs": {
    "product": "FlowState",
    "business_model": "B2B SaaS, individual and team plans",
    "stage": "Series A equivalent — product-market fit found, scaling GTM",
    "team_structure": "Product, Engineering, Growth, Customer Success",
    "data_available": "Mixpanel events, Stripe revenue data, Intercom support tickets, NPS surveys",
    "framework": "AARRR"
  }
}
```
