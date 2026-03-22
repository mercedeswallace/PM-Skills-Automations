# Value Proposition Canvas

**Skill ID:** `value-prop`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name |
| `segment` | yes | Customer segment |
| `jobs` | yes | What customers are trying to do |
| `pains` | yes | What frustrates them |
| `gains` | yes | What they want to achieve |
| `features` | yes | Key product capabilities |

## Example Request
```json
{
  "skill": "value-prop",
  "inputs": {
    "product": "FlowState",
    "segment": "Senior PMs at Series B SaaS companies",
    "jobs": "Write clear specs engineers can build from, communicate roadmap to stakeholders, align team on priorities, stay on top of strategy",
    "pains": "Documentation takes forever and gets ignored anyway, stakeholders don't read what I write, context gets lost across tools",
    "gains": "Spend more time on strategy and less on docs, be seen as organized and strategic, ship faster with less miscommunication",
    "features": "AI doc generation, PM-specific templates, Notion/Jira integration, real-time collaboration"
  }
}
```
