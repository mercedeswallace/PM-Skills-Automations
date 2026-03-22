# Survey Question Generator

**Skill ID:** `survey-generator`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `objective` | yes | What you want to learn |
| `respondents` | yes | Who you're surveying |
| `questions` | yes | Key questions to answer |
| `channel` | no | Default: email |
| `max_length` | no | Default: 5 minutes |

## Example Request
```json
{
  "skill": "survey-generator",
  "inputs": {
    "objective": "Understand why trial users don't convert to paid — what's the real blocker",
    "respondents": "Users who completed a 14-day trial but did not convert",
    "questions": "What was the main reason you didn't upgrade? What would have made you convert? Did you find value? What did you use instead?",
    "channel": "Email (sent 3 days after trial ends)",
    "max_length": "3 minutes"
  }
}
```
