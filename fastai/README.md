# Jupyter Notebook Collection

## Instructions

### Bootstrap

```sh
micromamba create -n fastai -c fastchan fastai jupyterlab ipywidgets python=3.11
micromamba env export -n fastai > fastai.yml
```

### Running Jupyter lab

```sh
micromamba activate fastai
jupyter-lab --ip "your_ip" --port 8888
```
