## Bootstrap

```sh
micromamba create -y -n pydata-book python=3.11
micromamba activate pydata-book

micromamba install -y pandas jupyter matplotlib lxml beautifulsoup4 html5lib openpyxl \
  requests sqlalchemy seaborn scipy statsmodels \
  patsy scikit-learn pyarrow pytables numba

micromamba env export -n pydata-book > pydata-book.yml
```

## Running

```sh
micromamba activate pydata-book
jupyter-lab --ip "your_ip" --port 8888
```
