# Build vs. Buy Analyzer

**Skill ID:** `build-vs-buy`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `capability` | yes | Capability or system needed |
| `build_option` | yes | What building it would involve |
| `buy_options` | yes | Vendor options and their details |
| `context` | yes | Strategic context |
| `capacity` | no | Engineering bandwidth |
| `budget` | no | Available budget |
| `timeline` | no | When you need it |

## Example Request
```json
{
  "skill": "build-vs-buy",
  "inputs": {
    "capability": "In-app analytics and user behavior tracking",
    "build_option": "Custom event tracking with PostgreSQL, Metabase for dashboards — 3 engineer-months",
    "buy_options": "Mixpanel ($833/mo, full featured), Amplitude ($995/mo, enterprise grade), PostHog ($0-450/mo, open source, self-hostable)",
    "context": "We need this for product decisions and customer health scoring. Core competency is PM tooling, not analytics infrastructure.",
    "capacity": "1 senior engineer available, other 3 are on roadmap features",
    "budget": "$15K/year for tools",
    "timeline": "Need basic analytics in 6 weeks"
  }
}
```
