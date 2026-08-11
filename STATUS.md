# FORGE — STATUS (model visibility)
**Updated:** 2026-08-11 (post-cleanup)

Canonical detail: **forge-os-core** `STATUS.md`.  
Entry for every session: **the-forge/START_HERE.md**

## Now
- PC: `~/the-forge`
- Source of truth: `munnchue-gif/the-forge`
- Bridge: **FIXED** — uses `boot_forge()`. `/health` must show `booted: true`
- Tests: **62 passed** simple fabric baseline
- Finding: live shape in `fabric/types.py` + `make_finding` helper
- Base44: glass only — not the spine
- Protocol: hardened anti-drift PRE_PROMPT + MASTER_PROMPT

## Handoff (use these)
| File | Purpose |
|------|--------|
| `handoff/STATE.md` | Living snapshot |
| `handoff/NEXT.md` | Ordered steps |
| `handoff/RESUME_PROMPT.md` | Paste into any new model chat |
| `protocol/` | Hard entry rules + commit log format |

## Do not
- Treat Base44 as the spine
- Call `ForgeKernel()` bare (use `boot_forge()`)
- Invent a second Finding type
- Start over when the architecture already exists

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
