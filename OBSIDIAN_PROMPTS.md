# Forge Obsidian Prompt Pack
Copy any block into an Obsidian note or paste directly to a model.

---

## 1. Universal System Visibility (always start with this)
```
You are working on Forge OS / Sovereign Forge (2026-08-08 completed path).
Repos (private, munnchue-gif):
- forge-os-core
- forge-arena
- sovereign-forge-v4
- forge-copilot

NPU is FIXED (OpenVINO 2026.3.0 + libze1 held). Do not reinstall drivers or change OpenVINO version.
Stick to the decoupled masterwhitepage path. Do not mix Base44-coupled psychology.
Current goal: [state your goal here]
```

---

## 2. NPU / Hardware Status
```
Read forge-os-core/masterwhitepage_revised.md and npu-context.md.
Confirm NPU is visible with:
python3 -c "import openvino as ov; print(ov.Core().available_devices)"
If NPU is missing, follow the exact recovery steps in masterwhitepage_revised.md.
Do not change libze1 version or remove the hold.
```

---

## 3. Aider / Free Coder Resume
```
You are resuming work on the newest Forge path (sovereign-forge-v4 + forge-os-core).
NPU is already fixed. After any pip install that touches transformers/optimum, immediately run:
pip install "openvino==2026.3.0" --force-reinstall --no-deps
Continue from the last successful layer. Do not re-install drivers. Do not mix old Base44 code.
```

---

## 4. Overseer / Core Architecture
```
You are editing the Overseer (Watcher + Commander) and Fabric.
Read forge-os-core for the completed path.
Watcher only observes and produces Findings. Commander only acts through the FabricGate.
Never let the Watcher act or the Commander observe on its own.
Finding lives in fabric.types (decoupled).
```

---

## 5. UI / Web APP Wiring
```
You are connecting the real-time web APP to the Forge bridge.
Use the best pieces from forge-arena (Gallery, Critiques, Setup) and the SvelteKit cockpit ideas from sovereign-forge-v4.
Wire telemetry, capsule toggles, and NPU/GPU gauges to the live FastAPI / MessageBus endpoints.
Do not embed old Base44 entity models.
```

---

## 6. Arena Compilation Input (safe playground)
```
You are working only in the Arena input zone.
This is for collecting and scoring proposals about what to compile from the different versions.
Do not modify the core Forge or start the full system.
After scoring, list clear recommendations that can later be plugged into the Socket Bay.
```

---

## 7. Socket Bay / Agent Plug-in
```
You are preparing or reviewing a Socket Bay agent.
The agent must be a clean .py drop-in that registers via the MessageBus.
It must respect the hire → work → flatten capsule lifecycle.
It must never assume Base44 entities. Use only the decoupled types.
```

---

## 8. Security / Execution Register
```
You are touching the SecurityGuard or Execution Register.
It is a fixed-size array.array('Q') of 16384 slots. O(1) replay detection.
Never replace it with a deque or heap-allocated structure.
All reach-ins must go through the gate and be audited.
```

---

## 9. Co-Pilot / How-Do-I Agent
```
You are the lightweight co-pilot agent.
You only answer orientation and recovery questions.
You never run heavy models or change system packages.
Point the human to the correct repo and the exact recovery steps.
```

---

## 10. Full Status Check (one-shot)
```
Give me a clean status of:
1. NPU visibility
2. Which repo is the active target
3. Last known good layer
4. Any open risk of mixing old versions
Use only the 2026-08-08 completed path.
```
