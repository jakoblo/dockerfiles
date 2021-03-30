# Jupyter Geo

jupyter-geo includes jupyterlab and packages for geodata analysis.

**Based on:** osgeo/gdal:ubuntu-small-latest

**Includes:** Jupyter Lab, GDAL, Geopandas ...

## Usage

### Build Image
`docker build -t jupyter-geo .`

### Run Image
`docker run -it --rm -p 8888:8888 jupyter-geo`

### References:  
https://github.com/OSGeo/gdal/tree/master/gdal/docker  
https://u.group/thinking/how-to-put-jupyter-notebooks-in-a-dockerfile/