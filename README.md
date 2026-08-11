# forge-copilot

Protocol, handoff, and visibility layer for multi-model work on The Forge.

This repo does **not** contain the living fabric code. That lives in `the-forge`.

## Purpose
- Give every model a hard, consistent entry point so they stop drifting and burning tokens.
- Force STATUS-first behavior.
- Enforce the AI NODE COMMIT LOG format.
- Hold clean handoff state so sessions can resume instead of restarting.

## How a model enters
1. Read `the-forge/START_HERE.md`
2. Read current STATUS
3. Absorb `protocol/PRE_PROMPT.md` + `protocol/MASTER_PROMPT.md`
4. Work only inside the AI NODE COMMIT LOG format
5. End with validation commands and an updated handoff if needed

## Key files
| Path | Role |
|------|------|
| protocol/PRE_PROMPT.md | Hard entry rules |
| protocol/MASTER_PROMPT.md | Architecture role + commit log format |
| handoff/ | STATE / NEXT / RESUME for session continuity |
| node-logs/ | Append-only record of substantive model work |
| bridge-patch/ | Historical notes (bridge boot is now fixed in the-forge) |

## Rule
If the protocol and the live code disagree, the live code in `the-forge` + the current STATUS win. Update the protocol to match reality; do not invent a parallel architecture.
