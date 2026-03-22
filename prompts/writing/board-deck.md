# Board Deck Generator

**Skill ID:** `board-deck`
**Endpoint:** POST `/webhook/pm-writing`

## Inputs
| Field | Required | Description |
|---|---|---|
| `company` | yes | Company name |
| `quarter` | yes | Quarter being reported |
| `metrics` | yes | Key metrics this period |
| `highlights` | yes | What went well |
| `challenges` | yes | What didn't go well |
| `strategy` | no | Strategic updates |
| `asks` | no | What you need from the board |
| `outlook` | yes | Next period outlook |

## Example Request
```json
{
  "skill": "board-deck",
  "inputs": {
    "company": "FlowState",
    "quarter": "Q1 2026",
    "metrics": "ARR: $420K (+18% QoQ), Churn: 4.2% (down from 6.1%), NPS: 54, New logos: 12, Trial-to-paid: 8.3%",
    "highlights": "Closed largest deal ever ($48K ARR), launched AI features ahead of schedule, churn improved significantly",
    "challenges": "Enterprise sales cycle longer than expected (avg 67 days), onboarding completion still at 34%",
    "strategy": "Pivoting upmarket to mid-market, hiring VP Sales in Q2",
    "asks": "Approve $300K bridge for VP Sales hire and marketing investment",
    "outlook": "Q2 target $540K ARR, 3 enterprise deals in pipeline totaling $180K"
  }
}
```
