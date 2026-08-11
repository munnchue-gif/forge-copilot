# Resume prompt — paste into any model

Continue **Forge OS** (`~/the-forge` on Pop!_OS). Path: **2026-08-08 decoupled** — no Base44 spine.

## Green
- NPU visible; OpenVINO 2026.3.0 pinned; baseline **62** simple tests
- Finding live: id, organ, severity:str, title, detail (`fabric.types`)
- Contract v0.1.0; bridge at `forge/bridge/server.py`

## Next
1. Read forge-os-core STATUS.md + LOCKED.md
2. Bridge missing-secret → `_boot()` via `boot_forge()` or real ForgeKernel signature
3. Unify old Finding callers to live fields
4. App remains glass; no endpoints outside contract

## Never
- Base44 as fabric authority
- Second Finding type
- Manifesto scripts replacing forge/fabric/

```bash
cd ~/the-forge && source .venv/bin/activate
export PYTHONPATH=$HOME/the-forge/forge
```
