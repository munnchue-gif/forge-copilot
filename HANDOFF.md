# FORGE COPILOT :: HANDOFF STATE

## 1. RECENT COMPLETED WORK
- Creation Block `2026-08-12-finding-unify` CLOSED.
- Producers migrated: judge.py, ollama_capsule.py, openvino_seat.py, conduit.py all use `make_finding` + live fields.
- New Creation Block opened: `2026-08-12-consumer-cleanup`.

## 2. CURRENT ACTIVE BLOCK
- **Active Block:** `coder-context/blocks/2026-08-12-consumer-cleanup/`
- **Objective:** Migrate `forge/fabric/overseer.py` feed-log construction from dead fields (`section_id`, `kind`) to live Finding fields (`id`, `title`, `severity`, `detail`).

## 3. IMMEDIATE NEXT STEP FOR NEW MODEL
- Open only `coder-context/blocks/2026-08-12-consumer-cleanup/`.
- Target file: `forge/fabric/overseer.py`.
- Replace the getattr(`section_id` / `kind`) feed-log construction with live fields.
- Do not touch test files, producers, ledger, or kernel.

## 4. KNOWN TRAPS / WARNINGS
- Ignore anything inside `forge-spine` or `fabric-ui`.
- The `Gate` protocol must be wrapped around all privileged functions.
- `test_judge.py` and other design-suite tests are still legacy — out of this block’s scope.
- Live severity is **str** (`info` / `warn` / `error` / `critical`).
- Local PC branch is `master` (not `main`).

---

# HANDOFF — 2026-08-12-consumer-cleanup

**Status:** OPEN. Sole target is overseer.py feed-log.

- [ ] Task 1 — forge/fabric/overseer.py (feed-log + any other Finding field access)

**Standard held:** live fields only (`id`, `organ`, `severity`, `title`, `detail`); no `section_id` / `kind` reads on Findings.

**Next command:** `BLOCK_OPEN coder-context/blocks/2026-08-12-consumer-cleanup/`
