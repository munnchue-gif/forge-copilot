# Aider / Free Coder Recovery

1. cd ~/the-forge && source .venv/bin/activate
2. Confirm NPU: python3 -c "import openvino as ov; print(ov.Core().available_devices)"
3. Protect OpenVINO: after any pip, force-reinstall openvino==2026.3.0 --no-deps
4. Launch aider with --read of this RECOVERY.md and the core READMEs
5. Tell it: Continue from last successful layer. Do not touch libze1 or OpenVINO version.
