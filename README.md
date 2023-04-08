# Jupyter Notebook Collection

## Instructions


## Troubleshoting

### 1. Command not found: jupyter-lab

```
The virtual environment found in ~/Library/Caches/pypoetry/virtualenvs/notebooks-LKJk4kj6-py3.10 seems to be broken.
Recreating virtualenv notebooks-LKJk4kj6-py3.11 in ~/Library/Caches/pypoetry/virtualenvs/notebooks-LKJk4kj6-py3.11
Command not found: jupyter-lab
```

It seems like somehow it will use the previous generated venv, which is not compatible with the current python version.

Solution: delete the venv folder `~/Library/Caches/pypoetry/virtualenvs` and run `poetry install` again.
