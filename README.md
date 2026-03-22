# PM Skills — N8N Automation Suite

41 product management skills, each callable as a webhook that returns Claude-generated output saved to Notion.

Built by [Mercedes](https://flowstatepm.substack.com) — Principal PM, Flow State PM.

## How it works

Send a POST request with a skill name and inputs → Claude generates expert output → saved to your Notion PM Skills database → response returns the Notion URL.

```bash
curl -X POST http://localhost:5678/webhook/pm-strategy \
  -H "Content-Type: application/json" \
  -d '{
    "skill": "swot-analysis",
    "inputs": {
      "company": "My SaaS product",
      "industry": "B2B productivity tools",
      "context": "Strong retention, struggling with acquisition",
      "question": "Where should we focus for the next 6 months?"
    }
  }'
```

Response:
```json
{
  "status": "done",
  "skill": "swot-analysis",
  "notion_url": "https://notion.so/...",
  "word_count": 734,
  "generated_at": "2026-03-22T14:00:00.000Z"
}
```

## Skills

| Category | Endpoint | Skills |
|---|---|---|
| **Strategy** | `/webhook/pm-strategy` | Roadmap Builder, Go-to-Market Strategy, BCG Matrix Analyzer, SWOT Analysis, Pricing Strategy, Market Sizing, Competitive Landscape |
| **Planning** | `/webhook/pm-planning` | Sprint Planning, Quarterly Planning, Sprint Retro, Feature Decomposition, Backlog Prioritizer |
| **Research & Analysis** | `/webhook/pm-research` | App Review Analyzer, Win/Loss Analyzer, A/B Test Analyzer, A/B Test Designer, Funnel Analyzer, Experiment Designer, Competitive Profile |
| **Writing & Comms** | `/webhook/pm-writing` | Board Deck Generator, Customer Announcement, Technical Spec, Decision Document, Executive Update, API Docs, Sales Enablement Kit |
| **Product & Customer** | `/webhook/pm-product` | Positioning Statement, Value Proposition Canvas, Build vs Buy, Feature Request Analyzer, Product Brief, Onboarding Flow, CS Playbook, Survey Generator |
| **Metrics** | `/webhook/pm-metrics` | North Star Finder, Metric Framework, Dashboard Designer, Team Health Check, Meeting Notes Processor |

See `prompts/` for full input schemas and example requests for every skill.

## Setup

### Prerequisites
- [N8N](https://n8n.io) self-hosted
- Anthropic API key
- Notion integration token

### 1. Create a Notion database
Create a database called **PM Skills Output** with a `Name` title field. Copy its ID from the URL.

### 2. Set up N8N credentials
- **Anthropic:** Add a Header Auth credential with header `x-api-key` and your Anthropic API key
- **Notion:** Add a Notion API credential with your integration token

### 3. Import a workflow
1. Open N8N → Workflows → Import from file
2. Import any file from `workflows/`
3. In each workflow, update:
   - `YOUR_ANTHROPIC_CREDENTIAL_ID` → your Anthropic credential
   - `YOUR_NOTION_CREDENTIAL_ID` → your Notion credential
   - `YOUR_NOTION_PM_SKILLS_DB_ID` → your Notion database ID
4. Publish the workflow (green dot top-right)

### 4. Test it
Use the example request from any `prompts/` file, swap `localhost:5678` with your N8N URL.
