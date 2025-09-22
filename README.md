# panel-simple-docs-example

Example of doing simple panel app for documentation purposes.

## Build Virtual Env with `uv`

```bash
uv venv
source .venv/bin/activate
uv pip install -r requirements.txt
```

## Build Jupyter Kernel

```bash
source .venv/bin/activate
uv run ipython kernel install --user --name=panel-simple-docs-example
```
