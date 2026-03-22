# Market Sizing Calculator

**Skill ID:** `market-sizing`
**Endpoint:** POST `/webhook/pm-strategy`

## Inputs
| Field | Required | Description |
|---|---|---|
| `market` | yes | What market you're sizing |
| `target_customer` | yes | Specific customer profile |
| `geography` | no | Default: Global |
| `approach` | no | top-down, bottom-up, or both. Default: both |
| `context` | no | Any additional context that helps with assumptions |

## Example Request
```json
{
  "skill": "market-sizing",
  "inputs": {
    "market": "AI-powered product management tools for software teams",
    "target_customer": "Product managers at B2B SaaS companies with 10-500 employees",
    "geography": "US + Canada + UK + Australia",
    "approach": "both",
    "context": "We charge $30/user/month. Average team size is 3 PMs. Focus is on Series A-C companies."
  }
}
```

## Output Sections
1. Top-down calculation (TAM → SAM → SOM with math)
2. Bottom-up calculation (TAM → SAM → SOM with math)
3. Explicit assumptions for each number
4. Confidence levels (high/medium/low)
5. Recommended number to use for planning
