# Forge OS — Living State (handoff)
**Updated:** 2026-08-11
**Canonical path:** 2026-08-08 decoupled (no Base44 spine)
**PC tree:** `~/the-forge` · snapshot `~/forge-os-locked-pc`

## Green
| Check | Result |
|-------|--------|
| NPU | OpenVINO sees CPU, GPU.0, GPU.1, **NPU** |
| OpenVINO pin | 2026.3.0 · libze1 1.17.44 **held** |
| Baseline tests | **62 passed** (simple fabric suite) |
| Finding | `fabric.types.Finding` — id, organ, severity:**str**, title, detail |
| Contract | v0.1.0 · App = glass only |
| Bridge code | `forge/bridge/server.py` on `the-forge` |

## Blockers
1. GitHub `server.py` still uses `ForgeKernel()` with no secret — verify PC uses `boot_forge()` or real signature.
2. Unify remaining `Finding(section_id=..., kind=..., severity=int)` → live shape.
3. Free port 8787 if bind fails.

## Hard rules
- No Base44 as spine
- Gate = one door; secrets env/client only
- No hash-chained internal ledger unless product decides
- Manifesto / OverSight / July Base44 = archive only

## Repo map
| Repo | Role |
|------|------|
| munnchue-gif/the-forge | Live fabric (public) |
| munnchue-gif/forge-os-core | Status + lock docs |
| munnchue-gif/forge-copilot | Any-model prompts + handoff |
| forge-arena / sovereign-forge-v4 | Post-build |
| git-concoctinating / the-forge-ui | Glass history — not spine |
