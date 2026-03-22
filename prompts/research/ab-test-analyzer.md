# A/B Test Analyzer

**Skill ID:** `ab-test-analyzer`
**Endpoint:** POST `/webhook/pm-research`

## Inputs
| Field | Required | Description |
|---|---|---|
| `test_name` | yes | Name of the test |
| `hypothesis` | yes | What you expected to happen |
| `control` | yes | Control group results |
| `variant` | yes | Variant group results |
| `sample_size` | yes | Number of users per group |
| `duration` | yes | How long the test ran |
| `significance` | no | Default: 95% |
| `secondary_metrics` | no | Guardrail metrics results |

## Example Request
```json
{
  "skill": "ab-test-analyzer",
  "inputs": {
    "test_name": "Onboarding checklist vs product tour",
    "hypothesis": "Checklist will increase activation by 15% by giving users clear next steps",
    "control": "Product tour — 23% completed onboarding, 18% activated in 7 days",
    "variant": "Checklist — 31% completed onboarding, 24% activated in 7 days",
    "sample_size": "850 users per group",
    "duration": "21 days",
    "significance": "95%",
    "secondary_metrics": "Churn in 30 days: control 12%, variant 10%. Support tickets: control 45, variant 38"
  }
}
```
