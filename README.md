# Panel Example Notebooks for New Users

Simple, opinionated example apps showing how to build interactive dashboards with [Panel](https://panel.holoviz.org/). Each notebook builds the same scatter plot explorer using a different viz library, so you can pick the one you already know.

See [panel#8223](https://github.com/holoviz/panel/issues/8223) for context.

## Notebooks

| Notebook | Viz Library | Interactive plots? |
|----------|------------|-------------------|
| [00_overview.ipynb](example_notebooks/00_overview.ipynb) | -- | Index and setup |
| [01_hvplot_scatter.ipynb](example_notebooks/01_hvplot_scatter.ipynb) | hvPlot | Yes |
| [02_matplotlib_scatter.ipynb](example_notebooks/02_matplotlib_scatter.ipynb) | Matplotlib | No (static images) |
| [03_bokeh_scatter.ipynb](example_notebooks/03_bokeh_scatter.ipynb) | Bokeh | Yes |

**Not sure where to start?** Open `01_hvplot_scatter.ipynb` -- least code, fully interactive.

## Setup

```bash
uv venv
source .venv/bin/activate
uv pip install -r requirements.txt
```

### Jupyter Kernel

Register a Jupyter kernel so notebooks use the venv's packages:

```bash
source .venv/bin/activate
python -m ipykernel install --user --name=panel-simple-docs-example
```

Then select the **panel-simple-docs-example** kernel when opening the notebooks in Jupyter.

## Usage

### In a notebook

Open any notebook in Jupyter and run all cells. The interactive explorer renders inline.

### As a standalone app

```bash
panel serve example_notebooks/01_hvplot_scatter.ipynb --dev --show
```

Replace `01_hvplot_scatter.ipynb` with whichever notebook you want to serve.
