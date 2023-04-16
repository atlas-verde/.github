# Ambiente Conda

Para el desarrollo del software, se configuró un ambiente [Conda](https://docs.conda.io/).

## Creación
```shell
# Creación de ambiente Conda
conda update conda -y
conda create -y -n atlas-verde
conda activate atlas-verde
conda config --env --add channels conda-forge
conda config --env --set channel_priority strict
conda install -y mamba
mamba install -y r-base r-essentials \
                 r-vroom=1.5.7 \
                 r-dplyr \
                 r-dt \
                 r-ggplot2 r-ggthemes r-hrbrthemes r-plotly \
                 r-sf=1.0_6 r-terra r-raster r-rgdal \
                 r-leaflet r-leaflet.providers r-leaflet.extras r-leaflet.minicharts r-leafem \
                 r-shiny r-shinydashboard r-shinythemes r-shinycssloaders \
                 r-rsconnect
```

En la consola de R, debe instalarse el paquete `leaflet.opacity` (no está disponible en `conda-forge`):
```
install.packages(leaflet.opacity)
```


## Borrado
```shell
# Borrado de ambiente Conda
conda deactivate
conda env remove --name atlas-verde
```
