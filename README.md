# VPDC_Notebooks

## Repo for testing various cloud services and notebook workflows.


### Workflow:
Background and Goal: Share LDSim data from a Jupyter notebook. The data is hosted on a cloud server and accessed remotely. 
This repo relies on Google Cloud as our cloud server. 

To get started, click below to launch a binder, executable environment in your browser to immediately begin to explore the LDSim data: 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/alisterfx/VPDC_Notebooks/HEAD)
.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/alisterfx/VPDC_Notebooks/HEAD
## For users who would like to open this Jupyter notebook locally, follow the below steps for setting up the Jupyter environment. 

### Quick setup
  - Download and install Anaconda, an open-source Python distribution platform. The platform comes with all of the geoprocessing packages (such as GDAL) needed and makes it _very_ easy to create and work with Jupyter notebooks: <https://www.anaconda.com/products/distribution>
- Once Anaconda is successfully installed on your machine open Terminal and start a new Jupyter Notebook:  
`Jupyter notebook`
  - Convert LDSim shapefile data to FlatGeobuf using GDAL installed in the Anaconda packages above: <https://gdal.org/drivers/vector/flatgeobuf.html>
 
  ```ogr2ogr -~_srs "EPSG:4326" -f FlatGeobuf Documents/Yuba_gpu_prj.fgb Documents/Yuba_gpu.fgb```
- Create a Google Cloud account: <https://console.cloud.google.com/storage/browser/way-find.com/> and a data bucket to host VPDC data for testing
  -- Data bucket: <https://storage.googleapis.com/way-find.com/vpdc>
- Make the bucket publicly accessible:
  -- <https://cloud.google.com/storage/docs/access-control/making-data-public#console_1>
- Install Google Cloud CLI into WSL Linux instance: <https://cloud.google.com/sdk/docs/downloads-interactive#linux-mac> in order to copy files easily from CLI to google cloud
`gcloud storage cp or_hu4_prj.geojson gs://way-find.com/vpdc`
- Create the Jupyter Notebook
  - Import needed geoprocessing packages: geopandas, fiona and rasterio and play away

### Resources
  - Get started with Jupyter Notebook: <https://www.dataquest.io/blog/jupyter-notebook-tutorial/>
