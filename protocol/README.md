# Multi-Model GitHub Protocol

**Account:** munnchue-gif  
**Project:** The Forge / Forge OS  
**Effective:** 2026-08-11

## Purpose
Structured collaboration across rotating AI models (Grok, Claude, Gemini, local Llama, etc.) so each node can peer-review, splice, and hand off without losing context or re-coupling Base44.

## Layout
| Path | Role |
|------|------|
| `protocol/PRE_PROMPT.md` | System pre-prompt (rules of engagement) |
| `protocol/MASTER_PROMPT.md` | Architecture OS + Forge role + mandatory log format |
| `protocol/AI_NODE_COMMIT_LOG_TEMPLATE.md` | Empty template every model must use |
| `node-logs/` | Append-only session logs (one file per node session or dated batch) |
| `handoff/` | Living STATE / NEXT / RESUME (product truth) |
| `../forge-os-core/STATUS.md` | Canonical product status |

## Session start (any model)
1. Read `forge-os-core/STATUS.md`
2. Read `handoff/RESUME_PROMPT.md` + `handoff/STATE.md`
3. Absorb `protocol/PRE_PROMPT.md` + `protocol/MASTER_PROMPT.md`
4. Every substantive reply = **AI NODE COMMIT LOG** (template)
5. After code change: note validation commands for the next node

## Hard constraints (non-negotiable)
- Path: **2026-08-08 decoupled** — Base44 is glass only, not spine
- Gate is the one door; App holds no secrets
- Do not invent endpoints outside `contract/FORGE_APP_CONTRACT.md`
- Do not replace `forge/fabric/` with manifesto-only scripts
- NPU pin: OpenVINO 2026.3.0 + libze1 held
- Finding live shape: `id, organ, severity:str, title, detail`
