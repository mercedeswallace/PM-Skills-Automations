# Feature Request Analyzer

**Skill ID:** `feature-requests`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product name |
| `requests` | yes | List of feature requests |
| `priorities` | yes | Current strategic priorities |
| `segments` | no | Customer segments making requests |

## Example Request
```json
{
  "skill": "feature-requests",
  "inputs": {
    "product": "FlowState",
    "requests": "1. Mobile app (requested by 34 users), 2. Dark mode (47 votes on feedback board), 3. Slack integration (8 enterprise requests), 4. Version history (12 requests, mostly power users), 5. Custom templates (22 requests), 6. Export to PDF (15 requests), 7. SSO/SAML (4 requests but all enterprise), 8. API access (6 developer requests), 9. Calendar view for roadmap (9 requests), 10. AI trained on our docs (3 enterprise requests)",
    "priorities": "Close enterprise deals, reduce churn among power users, grow to $1M ARR",
    "segments": "Enterprise (20%), power users (30%), casual users (50%)"
  }
}
```
