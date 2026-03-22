# Sales Enablement Kit

**Skill ID:** `sales-enablement`
**Endpoint:** POST `/webhook/pm-writing`

## Inputs
| Field | Required | Description |
|---|---|---|
| `product` | yes | Product or feature |
| `buyer` | yes | Target buyer persona |
| `differentiators` | yes | Key differentiators |
| `competitors` | yes | Main competitors |
| `objections` | yes | Common sales objections |
| `icp` | yes | Ideal customer profile |

## Example Request
```json
{
  "skill": "sales-enablement",
  "inputs": {
    "product": "FlowState Enterprise — AI-powered PM platform for mid-market teams",
    "buyer": "VP Product or Director of PM at Series B-D SaaS companies, 50-500 employees",
    "differentiators": "PM-specific AI (not generic), integrates with existing stack (Jira/Linear/Notion), saves 5+ hours/week per PM, onboards in 1 day",
    "competitors": "Notion (too generic), Confluence (legacy, slow), Jira (engineer-first), ProductBoard (expensive, complex)",
    "objections": "We already use Notion, Too expensive, My team won't adopt another tool, We built something internal",
    "icp": "Teams with 3+ PMs, already using Jira or Linear, frustrated with documentation overhead, growth-stage with fast-moving roadmap"
  }
}
```
