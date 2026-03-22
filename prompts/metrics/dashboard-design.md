# Metrics Dashboard Designer

**Skill ID:** `dashboard-design`
**Endpoint:** POST `/webhook/pm-metrics`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name |
| `audience` | yes | Who will use this dashboard |
| `decisions` | yes | What decisions this should enable |
| `data_sources` | yes | Available data |
| `frequency` | no | Default: daily |
| `tool` | no | Metabase, Looker, Grafana, etc. |

## Example Request
```json
{
  "skill": "dashboard-design",
  "inputs": {
    "product": "FlowState",
    "audience": "Weekly product team review — PM, engineering lead, CEO",
    "decisions": "Is growth on track? Where are users dropping off? Which features drive retention? Should we change our onboarding?",
    "data_sources": "Mixpanel (user events), Stripe (revenue), Intercom (support volume), NPS tool",
    "frequency": "Weekly review, daily data refresh",
    "tool": "Metabase"
  }
}
```
