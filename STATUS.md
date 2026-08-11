# FORGE — STATUS (model visibility)
**Updated:** 2026-08-11

Canonical detail: **forge-os-core** `STATUS.md`. Session continuity: **handoff/** in this repo.

## Now
- PC: `~/the-forge` (+ snapshot `~/forge-os-locked-pc`)
- NPU: visible (`CPU`, `GPU.0`, `GPU.1`, `NPU`)
- Tests: **62 passed** simple fabric baseline
- Finding live: `id, organ, severity:str, title, detail` (`fabric.types.Finding`)
- Bridge: code present; GitHub `server.py` still risks `ForgeKernel()` missing secret — see `bridge-patch/BOOT_FIX.md`
- Base44: glass only — not the spine

## Handoff (use these)
| File | Purpose |
|------|--------|
| `handoff/STATE.md` | Living snapshot |
| `handoff/NEXT.md` | Ordered steps |
| `handoff/RESUME_PROMPT.md` | Paste into any new model chat |
| `bridge-patch/BOOT_FIX.md` | Bridge boot fix |
| `versions/MODELS_AND_VERSIONS.md` | Psychology wall |

## Do not
- Treat Base44 as the spine
- Restore hash-chained internal ledger without product decision
- Invent a second Finding type

## Baseline command
```bash
cd ~/the-forge && source .venv/bin/activate
export PYTHONPATH=$HOME/the-forge/forge
python -m pytest forge/fabric -q \
  --ignore=forge/fabric/test_ledger.py \
  --ignore=forge/fabric/test_kernel.py \
  --ignore=forge/fabric/test_judge.py \
  --ignore=forge/fabric/test_sandbox.py \
  --ignore=forge/fabric/test_sequence.py \
  --ignore=forge/fabric/test_overseer.py \
  --ignore=forge/fabric/test_conduit.py \
  --ignore=forge/fabric/test_bridge_accessors.py \
  --ignore=forge/fabric/bind/test_bind.py
```

Full lock: `munnchue-gif/forge-os-core` → STATUS.md + LOCKED.md.
