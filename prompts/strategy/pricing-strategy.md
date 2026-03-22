# Pricing Strategy Analyzer

**Skill ID:** `pricing-strategy`
**Endpoint:** POST `/webhook/pm-strategy`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | What the product does and its core value |
| `current_pricing` | yes | Current price/model, or "not set" |
| `competitors` | yes | Competitors and their pricing |
| `target_segment` | yes | Who you're pricing for |
| `business_model` | no | SaaS, usage-based, marketplace, etc. Default: SaaS |
| `revenue_target` | no | Annual revenue goal |

## Example Request
```json
{
  "skill": "pricing-strategy",
  "inputs": {
    "product": "AI meeting notes tool that auto-generates action items, summaries, and Jira tickets from calls",
    "current_pricing": "$25/user/month flat, no tiers",
    "competitors": "Otter.ai ($16/user), Fireflies ($18/user), Notion AI (bundled), Gong ($100+/user enterprise)",
    "target_segment": "Mid-market engineering and product teams (20-200 users)",
    "business_model": "SaaS",
    "revenue_target": "$2M ARR by end of year"
  }
}
```

## Output Sections
1. Recommended pricing model with rationale
2. Packaging tiers (name, price, what's included, who it's for)
3. Competitive positioning
4. Simple revenue projection at each tier
5. Implementation risks and watch-outs
