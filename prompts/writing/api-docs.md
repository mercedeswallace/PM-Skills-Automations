# API Documentation Writer

**Skill ID:** `api-docs`
**Endpoint:** POST `/webhook/pm-writing`

## Inputs
| Field | Required | Description |
|---|---|---|
| `api_name` | yes | Name of the API |
| `purpose` | yes | What the API does |
| `auth` | yes | Authentication method |
| `endpoints` | yes | List of endpoints to document |
| `base_url` | yes | Base URL |
| `audience` | no | Default: external developers |

## Example Request
```json
{
  "skill": "api-docs",
  "inputs": {
    "api_name": "FlowState API v1",
    "purpose": "Programmatic access to documents, roadmaps, and AI generation features",
    "auth": "Bearer token — API key passed in Authorization header",
    "endpoints": "GET /documents (list), POST /documents (create), GET /documents/:id, PUT /documents/:id, DELETE /documents/:id, POST /documents/:id/generate (trigger AI generation)",
    "base_url": "https://api.flowstatepm.com/v1",
    "audience": "External developers and enterprise customers building integrations"
  }
}
```
