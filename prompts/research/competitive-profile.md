# Competitive Profile Builder

**Skill ID:** `competitive-profile`
**Endpoint:** POST `/webhook/pm-research`

## Inputs
| Field | Required | Description |
|---|---|---|
| `competitor` | yes | Competitor to profile |
| `our_product` | yes | Your product |
| `industry` | yes | Market context |
| `focus_areas` | no | Areas to analyze |

## Example Request
```json
{
  "skill": "competitive-profile",
  "inputs": {
    "competitor": "Linear",
    "our_product": "FlowState — AI-powered PM tool for roadmaps, specs, and strategy docs",
    "industry": "B2B SaaS product management and engineering tooling",
    "focus_areas": "product philosophy, target customer, pricing, AI features, go-to-market"
  }
}
```
