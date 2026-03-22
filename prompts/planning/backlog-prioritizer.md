# Backlog Prioritizer

**Skill ID:** `backlog-prioritizer`
**Endpoint:** POST `/webhook/pm-planning`

## Inputs
| Field | Required | Description |
|---|---|---|
| `items` | yes | List of backlog items to prioritize |
| `context` | yes | Strategic context and current priorities |
| `framework` | no | RICE, ICE, or custom. Default: RICE |
| `capacity` | no | Available team capacity |
| `focus` | no | Current quarter focus area |

## Example Request
```json
{
  "skill": "backlog-prioritizer",
  "inputs": {
    "items": "1. CSV export (many enterprise requests), 2. Dark mode (high votes, low biz value), 3. Zapier integration (enables 3 customer expansions), 4. Performance improvements (complaints increasing), 5. API v2 (unlocks partnership), 6. Mobile app (1 big customer request), 7. SSO/SAML (blocker for 4 enterprise deals)",
    "context": "Q2 focus is revenue — close enterprise deals and reduce churn. We have $500K pipeline blocked on features.",
    "framework": "RICE",
    "capacity": "20 eng-days this quarter after bug fixes",
    "focus": "Enterprise readiness and churn reduction"
  }
}
```
