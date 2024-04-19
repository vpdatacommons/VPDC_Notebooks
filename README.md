# VP Data Commons Jupyter Notebooks

A repository created by VP Data Commons to share the very best forestry data via Jupyter Notebooks.

## Getting started

The notebooks provided can be accessed directly through your web browser via cloud platforms like [Binder](https://jupyter.org/binder#:~:text=The%20Binder%20project%20offers%20an,and%20streamline%20sharing%20among%20teams.) or [Google Colaboratory](https://colab.research.google.com/#scrollTo=-Rh3-Vt9Nev9), as well as on your local machine. 

Note: because many notebooks contain complex spatial data, they require a dedicated GPU to run in a reasonable amount of time, so VP Data Commons recommends using cloud platforms that come with [CUDA](https://blogs.nvidia.com/blog/2012/09/10/what-is-cuda-2/) pre-installed.

## Open notebooks within this GitHub repo:

- LDSim 
  * [Explore LDSim GPU data via Jupyter notebook](notebooks/01_LDSim_Notebook.ipynb)
 
- Wildfire Ignition Probability
  * [Explore a subset of the Wildfire Ignition Probability data via Jupyter notebook](notebooks/02_WildfireIgnitionProbability_Notebook.ipynb)


## Running on a cloud platform

To run these notebooks on a cloud platform, click on your preferred platform badge in the table below (currently only Colab and Binder are offered):

| Notebook                                     | Colab                                                                                                                                                                                               | Binder                                                                                                                                                                                                   | Kaggle                                                                                                                                                                               | Studio Lab                                                                                                                                                                                                   |
|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Explore LDSim GPU data via Jupyter notebook   | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vpdatacommons/VPDC_Notebooks/blob/main/notebooks/01_LDSim_Notebook.ipynb)   | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/vpdatacommons/VPDC_Notebooks/39c9ffedd9e4e4d952571453cfac6be4ad0779c7?urlpath=lab%2Ftree%2Fnotebooks%2F01_LDSim_Notebook.ipynb) |   COMING SOON   | COMING SOON
| Explore Wildfire Ignition Probability data via Jupyter notebook                               | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vpdatacommons/VPDC_Notebooks/blob/main/notebooks/02_WildfireIgnitionProbability_Notebook.ipynb)              | [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/vpdatacommons/VPDC_Notebooks/HEAD?labpath=notebooks%2F02_WildfireIgnitionProbability_Notebook.ipynb) |  COMING SOON   | COMING SOON   



As mentioned before, many notebooks need ample GPUs and memory allocation to maximize performance and speed. Unfortunately, while Colab and Binder are fantastic community resources, they tend to be slower (Colab GPUs are often K80s, meaning limited memory - while Binder guarantees 1-2 GB of memory. This means that process speeds may be pretty slow, and the server may sometimes crash. Because of this, we recommend using [SageMaker Studio Lab](https://studiolab.sagemaker.aws/), [Kaggle](https://www.kaggle.com/docs/notebooks), or [Gradient](https://gradient.run/notebooks) since each of these platforms often provide more performant GPUs. Also, they are free!

> Note: some cloud platforms like Kaggle require you to restart the notebook after installing new packages.

## Running on your machine

#### Option 1: Manual environment setup 
To run the notebooks on your own machine, first clone the repository and navigate to it:

```bash
gh repo clone vpdatacommons/VPDC_Notebooks

cd notebooks
```

Next, run the following command to create a `conda` virtual environment that contains all the libraries needed to run the notebooks:

```bash
conda env create -f environment.yml
```

> Note: You'll need a GPU that supports NVIDIA's [CUDA Toolkit](https://developer.nvidia.com/cuda-toolkit) to build the environment. You'll need to verify that your OS supports it. 


```bash
conda env create -f environment-chapter7.yml
```

Once you've installed the dependencies, you can activate the `conda` environment and spin up the notebooks as follows:

```bash
conda activate book # TODO: Make sure that this is the right code
jupyter notebook
```

#### Option 2. Use the Anaconda ditribution platform
To run the notebooks on your own machine, first clone the repository and navigate to it:

```bash
gh repo clone vpdatacommons/VPDC_Notebooks

cd notebooks
```

Download and install Anaconda, an open-source Python distribution platform. The platform comes with all of the geoprocessing packages (such as GDAL) needed and makes it _very_ easy to create and work with Jupyter notebooks: <https://www.anaconda.com/products/distribution>
- Once Anaconda is successfully installed on your machine open Terminal and start a new Jupyter Notebook:  
```bash
Jupyter notebook
```
 Jupyter notebook will open automatically in your web browser in the main notebooks directory. Locate the Jupyter notebook that you'd like to explore and click to open it. 

## FAQ
_....COMING SOON_



## Related Resources

- [Get started with Jupyter Notebook](https://www.dataquest.io/blog/jupyter-notebook-tutorial)

- [Getting started with Anaconda](https://docs.anaconda.com/anaconda/user-guide/getting-started)
