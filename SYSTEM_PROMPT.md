# System Visibility Prompt (paste to any model)

**First read:** `munnchue-gif/forge-os-core` → `STATUS.md` (and this repo’s `STATUS.md` mirror).

## Access
Private: `forge-os-core`, `forge-arena`, `sovereign-forge-v4`, `forge-copilot`.  
Public fabric code: `munnchue-gif/the-forge`.  
PC canonical tree: `~/the-forge` (snapshot: `~/forge-os-locked-pc`).

## Hardware
MSI Arrow Lake + RTX 5080 + NPU. OpenVINO devices: CPU, GPU.0, GPU.1, NPU.  
NPU lock: OpenVINO 2026.3.0 + libze1 1.17.44 held.

## Philosophy (do not reopen lightly)
- Capsules = laborers (hire → work → flatten); identity in Wrap
- Overseer split: Watcher observe-only / Commander act-only via Gate
- One door: Gate (nonce per mint). Hash/sign at Gate + external adapters/sockets only
- Internal ledger = simple log (not hash-chained unless product demands)
- Base44 = optional glass, not the spine

## Finding (live)
`fabric.types.Finding(id, organ, severity: str, title, detail, ...)`  
Do not use old `section_id` / `kind` / int severity without mapping.

## Baseline green bar
62 pytest tests under `forge/fabric` with design-suite files ignored (see STATUS.md).

## When working
1. Read STATUS.md  
2. Prefer `~/the-forge` over Drive / ALLFORGE copies  
3. After code changes: re-run baseline; update STATUS date and counts  
4. Do not mix Base44 entities into fabric spine
