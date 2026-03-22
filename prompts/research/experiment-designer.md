# Experiment Designer

**Skill ID:** `experiment-designer`
**Endpoint:** POST `/webhook/pm-research`

## Inputs
| Field | Required | Description |
|---|---|---|
| `problem` | yes | What problem you're trying to solve |
| `hypothesis` | yes | Your hypothesis |
| `metrics` | yes | Primary success metric |
| `type` | no | A/B, multivariate, holdout, etc. |
| `constraints` | no | Traffic, time, technical limits |
| `risk_tolerance` | no | low/medium/high |

## Example Request
```json
{
  "skill": "experiment-designer",
  "inputs": {
    "problem": "Trial users aren't inviting teammates — only 25% do, blocking team adoption and conversion",
    "hypothesis": "Showing social proof (how many teammates similar companies invite) during onboarding will increase team invites by 30%",
    "metrics": "% of trial users who invite at least 1 teammate within 7 days",
    "type": "A/B test",
    "constraints": "500 new trial users per week, need results in 4 weeks, can't change core onboarding flow",
    "risk_tolerance": "medium"
  }
}
```
