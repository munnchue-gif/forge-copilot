# FORGE COPILOT :: HANDOFF STATE

## 1. RECENT COMPLETED WORK
- Migrated `forge/fabric/judge.py` to live Finding shape via `make_finding`.
- Migrated `forge/fabric/bind/ollama_capsule.py` to live Finding shape.
- Migrated `forge/fabric/bind/openvino_seat.py` to live Finding shape.
- All three files construct Findings exclusively via `make_finding` from `fabric.types`.
- Zero remaining `section_id=` / `kind=` / bare `Finding(` / `fabric.overseer` / `.kind` / `.section_id` in the three files.

## 2. CURRENT ACTIVE BLOCK
- **Active Block:** `coder-context/blocks/2026-08-12-finding-unify/`
- **Objective:** Create correct Finding construction in live fabric modules (judge, ollama_capsule, openvino_seat, conduit).

## 3. IMMEDIATE NEXT STEP FOR NEW MODEL
- Generate / migrate `forge/fabric/conduit.py` only.
- Do NOT create a new `finding.py` (use existing `types.py`).
- Keep ledger.py and kernel.py untouched.

## 4. KNOWN TRAPS / WARNINGS
- Ignore anything inside `forge-spine` or `fabric-ui`.
- The `Gate` protocol must be wrapped around all privileged functions.
- `test_judge.py` is still legacy-shaped (reads `.kind`) — out of this block’s target list; refresh separately before claiming the judge suite green.
- Live severity is **str** (`info` / `warn` / `error` / `critical`). `make_finding` accepts int and maps it.

---

# HANDOFF — 2026-08-12-finding-unify

**Status:** Tasks 1–3 COMPLETE. Task #4 remaining.

- [x] Task 1 — forge/fabric/judge.py
- [x] Task 2 — forge/fabric/bind/ollama_capsule.py
- [x] Task 3 — forge/fabric/bind/openvino_seat.py
- [ ] Task 4 — forge/fabric/conduit.py   ← SOLE REMAINING TARGET

**Standard held:** all Findings via `make_finding` from `fabric.types`; live
fields only (id, organ, severity:str, title, detail); no `fabric.overseer`
imports; no `section_id=` / `kind=` / bare `Finding(...)`; no `.kind` /
`.section_id` reads. ledger.py and kernel.py untouched.

**Open follow-up (out of current block scope):** `test_judge.py` still uses the
dead Finding shape — refresh separately before claiming the judge suite green.

**Next command:** `BLOCK_OPEN coder-context/blocks/2026-08-12-finding-unify/` →
Task #4, conduit.py only.
