# Competitive Landscape Mapper

**Skill ID:** `competitive-landscape`
**Endpoint:** POST `/webhook/pm-strategy`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Your product and its core value |
| `target_customer` | yes | Who you serve |
| `competitors` | yes | List of competitors to analyze |
| `dimensions` | no | Axes for positioning map. Default: price vs value, features vs ease of use |
| `market` | no | Market context |

## Example Request
```json
{
  "skill": "competitive-landscape",
  "inputs": {
    "product": "FlowState — AI writing tool that helps PMs write specs, roadmaps, and updates 3x faster",
    "target_customer": "Senior PMs and Directors of Product at B2B SaaS companies",
    "competitors": "Notion AI, ChatGPT/Claude direct, Atlassian Intelligence, Coda AI, Saga",
    "dimensions": "AI quality vs PM-specificity, price vs depth of PM workflows",
    "market": "AI productivity tools for knowledge workers, specifically product management"
  }
}
```

## Output Sections
1. Competitor profiles table (what they do, who they target, positioning, strengths, weaknesses)
2. Text-based positioning matrix
3. White space opportunities
4. Top 3 strategic recommendations
