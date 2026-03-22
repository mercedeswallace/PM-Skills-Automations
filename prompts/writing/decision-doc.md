# Decision Document Creator

**Skill ID:** `decision-doc`
**Endpoint:** POST `/webhook/pm-writing`

## Inputs
| Field | Required | Description |
|---|---|---|
| `decision` | yes | The decision to be made |
| `context` | yes | Background and why this decision is needed now |
| `options` | yes | Options being considered |
| `constraints` | no | What limits the options |
| `stakeholders` | no | Who's involved |
| `deadline` | no | When the decision must be made |

## Example Request
```json
{
  "skill": "decision-doc",
  "inputs": {
    "decision": "Should we build our own AI model fine-tuning pipeline or use a third-party provider?",
    "context": "Customers are asking for personalized AI outputs trained on their team's writing style. We need to decide how to deliver this before Q3.",
    "options": "1. Build in-house fine-tuning pipeline on AWS, 2. Use OpenAI fine-tuning API, 3. Use Anthropic fine-tuning (when available), 4. Partner with a fine-tuning startup",
    "constraints": "2 ML engineers available, $80K annual budget for infrastructure, must be SOC2 compliant",
    "stakeholders": "CTO (approver), VP Engineering (contributor), Head of Product (driver), 3 enterprise customers (informed)",
    "deadline": "Decision needed by April 30 to hit Q3 launch"
  }
}
```
