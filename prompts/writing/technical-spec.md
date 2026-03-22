# Technical Spec Writer

**Skill ID:** `technical-spec`
**Endpoint:** POST `/webhook/pm-writing`

## Inputs
| Field | Required | Description |
|---|---|---|
| `feature` | yes | Feature or system name |
| `problem` | yes | Problem being solved |
| `solution` | yes | Proposed approach |
| `tech_stack` | no | Relevant tech |
| `constraints` | no | Technical or business constraints |
| `out_of_scope` | no | What's explicitly excluded |

## Example Request
```json
{
  "skill": "technical-spec",
  "inputs": {
    "feature": "Real-time collaborative editing — multiple users edit the same document simultaneously",
    "problem": "Users lose work when two people edit the same doc — last save wins, causing data loss and frustration",
    "solution": "Implement operational transformation (OT) or CRDT-based conflict resolution with presence indicators",
    "tech_stack": "React, Node.js, PostgreSQL, WebSockets via Socket.io",
    "constraints": "Must work offline and sync on reconnect, max 50ms latency target, no new infrastructure",
    "out_of_scope": "Version history UI, comment threading, mobile client"
  }
}
```
