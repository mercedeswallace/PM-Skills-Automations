# PM Skills — N8N Automation Suite

## Project Overview
A suite of N8N workflows that expose 41 PM skills as webhook-triggered Claude AI automations. Each skill takes structured JSON input, generates expert output, saves to Notion, and returns the result.

---

## Architecture

### Pattern (same across all 41 skills)
```
POST /webhook/{category}  { "skill": "skill-name", "inputs": { ... } }
  → Code node "Build Prompt"  (JS switch — routes to correct system + user prompt)
  → HTTP Request "Claude"     (claude-sonnet-4-6, 8192 max_tokens)
  → Code node "Parse Response"
  → Notion "Create PM Skills page"
  → Notion "Append content blocks"
  → Respond to Webhook        { status: "done", notion_url: "..." }
```

### Webhook Endpoints
| Workflow | Endpoint | Skills |
|---|---|---|
| Strategy | POST `/webhook/pm-strategy` | roadmap-builder, go-to-market, bcg-matrix, swot-analysis, pricing-strategy, market-sizing, competitive-landscape |
| Planning | POST `/webhook/pm-planning` | sprint-planning, quarterly-planning, sprint-retro, feature-decomposition, backlog-prioritizer |
| Research & Analysis | POST `/webhook/pm-research` | app-review-analyzer, win-loss-analyzer, ab-test-analyzer, ab-test-designer, funnel-analyzer, experiment-designer, competitive-profile |
| Writing & Comms | POST `/webhook/pm-writing` | board-deck, customer-announcement, technical-spec, decision-doc, exec-update, api-docs, sales-enablement |
| Product & Customer | POST `/webhook/pm-product` | positioning, value-prop, build-vs-buy, feature-requests, product-brief, onboarding-flow, cs-playbook, survey-generator |
| Metrics | POST `/webhook/pm-metrics` | north-star, metric-framework, dashboard-design, team-health, meeting-notes |

### Request Format
```json
{
  "skill": "skill-name",
  "inputs": {
    "field1": "value",
    "field2": "value"
  }
}
```

### Response Format
```json
{
  "status": "done",
  "skill": "skill-name",
  "notion_url": "https://notion.so/...",
  "word_count": 842
}
```

---

## Notion Setup

### PM Skills Database
Create a Notion database called **PM Skills Output** with these fields:
- `Name` (title) — auto-set to `{Skill} — {date}`
- `Skill` (select) — the skill name
- `Category` (select) — Strategy / Planning / Research / Writing / Product / Metrics
- `Generated At` (date)

Database ID goes in: `YOUR_NOTION_PM_SKILLS_DB_ID` in each workflow.

### Content Storage
Content is appended as blocks (3 × 2000 chars), same pattern as the newsletter workflow.

---

## Claude Node Setup
All workflows use the same Anthropic Header Auth credential.
- Credential name: `Header Auth account`
- Header: `x-api-key: YOUR_ANTHROPIC_API_KEY`
- Additional header: `anthropic-version: 2023-06-01`

---

## Files
```
workflows/
  strategy.json          — 7 skills
  planning.json          — 5 skills
  research-analysis.json — 7 skills
  writing-comms.json     — 7 skills
  product-customer.json  — 8 skills
  metrics.json           — 5 skills (+ meeting notes)

prompts/
  strategy/              — one .md per skill (source of truth for prompts)
  planning/
  research/
  writing/
  product/
  metrics/
```

---

## Critical Rules
- Always provide the **entire** workflow JSON when making updates — never partial snippets
- Placeholder values to replace on import:
  - `YOUR_ANTHROPIC_CREDENTIAL_ID` — N8N credential ID for Anthropic Header Auth
  - `YOUR_NOTION_CREDENTIAL_ID` — N8N credential ID for Notion
  - `YOUR_NOTION_PM_SKILLS_DB_ID` — Notion database ID for PM Skills Output
- Webhook path must be **unique** per workflow — do not reuse paths
- Workflow must be **Published** (green dot) for production webhook to work
- Body Content Type must be `Raw` + `application/json` on all Claude HTTP Request nodes
