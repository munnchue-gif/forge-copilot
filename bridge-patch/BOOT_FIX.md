# Bridge boot fix

GitHub `forge/bridge/server.py` still has:
```python
_kernel = ForgeKernel()  # fails: missing secret
```

Prefer:
```python
def _boot():
    global _kernel, _booted_at
    from fabric.kernel import boot_forge
    _kernel = boot_forge()
    _booted_at = time.time()
```

Or match `inspect.signature(ForgeKernel.__init__)`.
