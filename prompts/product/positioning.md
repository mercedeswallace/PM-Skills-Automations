# Positioning Statement Generator

**Skill ID:** `positioning`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name and what it does |
| `alternatives` | yes | What customers use today without you |
| `attributes` | yes | Unique capabilities competitors lack |
| `value` | yes | Benefit those attributes unlock |
| `target` | yes | Target customer |
| `market` | yes | Market category |

## Example Request
```json
{
  "skill": "positioning",
  "inputs": {
    "product": "FlowState — AI writing tool for product managers",
    "alternatives": "Blank docs in Notion/Confluence, generic ChatGPT prompts, spending 2+ hours writing PRDs manually",
    "attributes": "PM-specific templates and frameworks built-in, learns your product context, generates complete docs not just outlines",
    "value": "First draft of any PM document in 10 minutes instead of 2 hours",
    "target": "Senior PMs and Heads of Product at growth-stage SaaS companies",
    "market": "AI productivity tools for knowledge workers"
  }
}
```
