# FORGE — STATUS (model visibility)
**Updated:** 2026-08-10

Canonical detail lives in **forge-os-core** `STATUS.md`. This copy is for co-pilot / any-model sessions.

## Now
- PC: `~/the-forge` (+ snapshot `~/forge-os-locked-pc`)
- NPU: visible (`CPU`, `GPU.0`, `GPU.1`, `NPU`)
- Bridge: `127.0.0.1:8787`
- Tests: **62 passed** simple fabric baseline
- Ledger: simple internal log; hash/sign at **Gate + external adapters only**
- Finding live shape: `id, organ, severity:str, title, detail` (`fabric.types.Finding`)

## Do not
- Treat Base44 as the spine
- Restore hash-chained internal ledger without an explicit product decision
- Invent a second Finding type — map old `section_id/kind/severity:int` → live fields

## Baseline command
```bash
cd ~/the-forge && source .venv/bin/activate
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

Full lock + next bricks: `munnchue-gif/forge-os-core` → `STATUS.md`.
