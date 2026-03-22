# BCG Matrix Analyzer

**Skill ID:** `bcg-matrix`
**Endpoint:** POST `/webhook/pm-strategy`

## Inputs
| Field | Required | Description |
|---|---|---|
| `products` | yes | Array of products with context (see example) |
| `context` | no | Market context, company stage, resource constraints |

## Example Request
```json
{
  "skill": "bcg-matrix",
  "inputs": {
    "products": [
      { "name": "Core Analytics", "revenue": "$4M ARR", "growth": "5% YoY", "market_share": "high — #2 in segment" },
      { "name": "Mobile App", "revenue": "$800K ARR", "growth": "120% YoY", "market_share": "low — new entrant" },
      { "name": "Legacy Reports", "revenue": "$1.2M ARR", "growth": "-10% YoY", "market_share": "medium — declining market" },
      { "name": "AI Insights Beta", "revenue": "$50K ARR", "growth": "200% YoY", "market_share": "very low — emerging market" }
    ],
    "context": "Series B company, limited engineering resources, planning annual resource allocation"
  }
}
```

## Output Sections
1. BCG placement per product (Star / Cash Cow / Question Mark / Dog) with reasoning
2. Strategic recommendation per product (invest / milk / divest / nurture)
3. Specific actions for each
4. Portfolio-level assessment and rebalancing recommendations
