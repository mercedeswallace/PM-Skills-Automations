# Product Brief Writer

**Skill ID:** `product-brief`
**Endpoint:** POST `/webhook/pm-product`

## Inputs
| Field | Required | Description |
|---|---|---|
| `feature` | yes | Feature or initiative name |
| `problem` | yes | Problem being solved |
| `user` | yes | Target user |
| `solution` | yes | Proposed solution |
| `metrics` | yes | How you'll measure success |
| `constraints` | no | Scope limits |
| `stakeholders` | no | Who needs to approve |

## Example Request
```json
{
  "skill": "product-brief",
  "inputs": {
    "feature": "Team Workspaces — shared space for entire PM team with unified roadmap view",
    "problem": "PMs using FlowState individually can't see each other's work — no visibility into what the team is building, leading to duplicated effort and misaligned roadmaps",
    "user": "Head of Product managing a team of 3-8 PMs",
    "solution": "Shared workspace with team roadmap view, member management, and cross-PM document linking",
    "metrics": "Workspace creation rate, multi-seat expansion within 30 days, team NPS vs individual NPS",
    "constraints": "Must not break existing individual workflows, no new infra, ship in one sprint",
    "stakeholders": "CEO (approve), CTO (technical review), 3 design partners to validate with"
  }
}
```
