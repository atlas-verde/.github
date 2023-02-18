# Ambiente Conda

Para el desarrollo del software, se configuró un ambiente [Conda](https://docs.conda.io/).

## Creación
```shell
# Creación de un ambiente Conda
conda update conda -y
conda create -y -n atlas-verde
conda activate atlas-verde
conda config --env --add channels conda-forge
conda config --env --set channel_priority strict
conda install -y mamba
mamba install -y r-base r-essentials r-vroom=1.5.7 r-ggthemes r-hrbrthemes r-plotly r-dt r-sf=1.0_6 r-leaflet r-shiny
```

## Borrado
```shell
# Borrado del ambiente Conda
conda deactivate
conda env remove --name atlas-verde
```
