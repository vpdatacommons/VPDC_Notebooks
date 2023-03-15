# VPDC_Notebooks
## A repo for testing various cloud services and notebook workflows.

## There are two options for accessing the Jupyter notebook: 
### Option 1. Access the data immediately in your web browser:
Can't wait to dive right in to the data? Access the Jupyter notebook by clicking the blue badge below. This will open a new [Binder](https://jupyter.org/binder#:~:text=The%20Binder%20project%20offers%20an,and%20streamline%20sharing%20among%20teams.) in your browser enabling you to immediately review and explore LDSim data 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/alisterfx/VPDC_Notebooks/HEAD)



### Option 2. Open the Jupyter notebook locally by manually setting up the environmnet
For users who would like to open this Jupyter notebook locally, follow the below steps for setting up the Jupyter environment. 

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
