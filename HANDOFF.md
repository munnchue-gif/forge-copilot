# FORGE COPILOT :: HANDOFF STATE

## 1. RECENT COMPLETED WORK
- finding-unify CLOSED (producers clean).
- overseer.py feed-log + sandbox.py is_clean fixed (production consumers clean).
- test_judge.py modernized.
- New block opened: `2026-08-12-test-finding-refresh`.

## 2. CURRENT ACTIVE BLOCK
- **Active Block:** `coder-context/blocks/2026-08-12-test-finding-refresh/`
- **Objective:** Modernize remaining Finding-related tests (test_sandbox, test_conduit, test_overseer, others still on dead shape).

## 3. IMMEDIATE NEXT STEP FOR NEW MODEL
- Open only that block.
- Refresh the three named test files first; only touch others if grep still shows dead Finding usage.
- Do not touch production modules.

## 4. KNOWN TRAPS / WARNINGS
- Local PC branch is `master`.
- Capability `.kind` and ledger `"kind"` keys are not Finding fields — leave them alone.
- Live severity is str.

---

**Next command:** `BLOCK_OPEN coder-context/blocks/2026-08-12-test-finding-refresh/`
