# Win/Loss Analyzer

**Skill ID:** `win-loss-analyzer`
**Endpoint:** POST `/webhook/pm-research`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Your product |
| `wins` | yes | Won deal notes/patterns |
| `losses` | yes | Lost deal notes/patterns |
| `competitors` | no | Competitors involved |
| `segment` | no | Deal size or customer type |
| `time_period` | no | Date range |

## Example Request
```json
{
  "skill": "win-loss-analyzer",
  "inputs": {
    "product": "FlowState PM Tool",
    "wins": "Won Acme Corp (50 seats) — beat Notion on PM-specific features. Won TechCo (20 seats) — price was key. Won StartupX — founder loved the AI writing.",
    "losses": "Lost MegaCorp to Jira — needed enterprise SSO. Lost MidSize Inc to Confluence — already in Atlassian ecosystem. Lost Agency LLC — needed client portal we don't have.",
    "competitors": "Jira, Confluence, Notion, Linear",
    "segment": "Mid-market, 20-200 employees"
  }
}
```
