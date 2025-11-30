# Build steps

1. Install build tools:

```bash
pip install build twine
```

2. Build:

> [!NOTE]
> Make sure to update the version number in `pyproject.toml` before you build.

```bash
python -m build
```

3. Publish:

```bash
python -m twine upload dist/*
```
