# App Review Analyzer

**Skill ID:** `app-review-analyzer`
**Endpoint:** POST `/webhook/pm-research`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | App/product name |
| `reviews` | yes | Paste raw reviews (copy from App Store, G2, etc.) |
| `rating_filter` | no | e.g. "1-3 stars only". Default: all |
| `time_period` | no | Date range of reviews |

## Example Request
```json
{
  "skill": "app-review-analyzer",
  "inputs": {
    "product": "FlowState PM Tool",
    "reviews": "★★★★★ Love the AI features, saves me hours per week. ★★☆☆☆ Keeps logging me out, super annoying. ★★★☆☆ Good concept but mobile is unusable. ★★★★☆ Best roadmap tool I've used. ★☆☆☆☆ Lost all my data after update. ★★★★★ The Notion integration is perfect. ★★☆☆☆ No dark mode in 2026?",
    "rating_filter": "all",
    "time_period": "Last 90 days"
  }
}
```
