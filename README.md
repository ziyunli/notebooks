# Jupyter Notebook Collection

## Instructions

### Bootstrap

```sh
micromamba create -n fastai-gpu -c fastchan fastai==2.7.11 jupyterlab ipywidgets
```

### Pre-commit

Pre-commit hooks run all the auto-formatters (e.g. `black`), linters (e.g. `ruff`), and other quality
 checks to make sure the changeset is in good shape before a commit/push happens.

You can install the hooks with (runs for each commit):

```sh
pre-commit install
```

Or if you want them to run only for each push:

```sh
pre-commit install -t pre-push
```

Or if you want e.g. want to run all checks manually for all files:

```sh
pre-commit run --all-files
```

### Running Jupyter lab

```sh
micromamba activate fastai-gpu
jupyter-lab --ip 192.168.50.114 --port 8888
```

## Troubleshoting

### 1. Command not found: jupyter-lab

```
The virtual environment found in ~/Library/Caches/pypoetry/virtualenvs/notebooks-LKJk4kj6-py3.10 seems to be broken.
Recreating virtualenv notebooks-LKJk4kj6-py3.11 in ~/Library/Caches/pypoetry/virtualenvs/notebooks-LKJk4kj6-py3.11
Command not found: jupyter-lab
```

It seems like somehow it will use the previous generated venv, which is not compatible with the current python version.

Solution: delete the venv folder `~/Library/Caches/pypoetry/virtualenvs` and run `poetry install` again.
