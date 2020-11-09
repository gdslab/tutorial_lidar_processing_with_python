# Python LiDAR data processing tutorial

This tutorial uses Anaconda3 2020.07 version to navigate and process Indiana Statewide LiDAR data (2017-2019).
As a first part of the tutorial, we install Anaconda (Python and R) on our local machines for ease of programming.

## Session 1: Install Python and useful packages (20 min-1 hr)

### Install [Anaconda3](https://docs.anaconda.com/anaconda/install/)

### Open a [command line interface](https://docs.anaconda.com/anaconda/user-guide/getting-started/#open-anaconda-prompt)

### Run below commands to create a new [virtual environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) and install packages

Check the current Python environment. You should see an asterisk symbol next to the **base** environment in the output.

```wef
$ conda info --envs
```

Create a new virtual environment named lidar with Python 3.6 and jupyter notebook. We are going to use this environment to process the statewide lidar data set.
```bash
$ conda create --name lidar python=3.6 jupyter
```

Activate the **lidar** virtual environment.
```bash
$ conda activate lidar
```

Check the current environment again. Now **lidar** environment should be activated.
```bash
$ conda info --envs
```

Install Python packages for GIS and LiDAR data operations.
```bash
$ conda install -c conda-forge gdal
$ conda install numpy matplotlib scikit-learn pandas
$ conda install -c conda-forge laspy pyflann progressbar 
$ conda install -c plotly plotly 
$ conda install scikit-image
```

Now all the installation is **tentatively** finished, and we can import above packages to our Python projects in the next step.

### Run Python to check above packages are installed
From the Anaconda Prompt (windows) or terminal (mac, linux), run below commands to run Python in an interactive session.
```bash
$ conda activate lidar
$ python
```
In the acteractive session, run below commands to load packages for GIS, LiDAR operations. For your information, gdal, ogr and laspy package is useful for processing raster, vector, and LiDAR data, respectively.

```python
>>> import numpy
>>> import matplotlib
>>> import sklearn
>>> import gdal
>>> import ogr
>>> import laspy
```

[Exit the interactive session](https://realpython.com/interacting-with-python/#exiting-the-interpreter).


### Install GDAL as command line tool

Check you can use GDAL is command line tool by typing
```bash
$ gdalinfo --version
```
In case you don't see GDAL version and release date, install GDAL depending on your OS: [Windows](https://sandbox.idre.ucla.edu/sandbox/tutorials/installing-gdal-for-windows), [Mac](https://sandbox.idre.ucla.edu/sandbox/tutorials/installing-gdal-for-windows) or [Linux](https://tilemill-project.github.io/tilemill/docs/guides/gdal/). Be sure to run **gdalinfo --version** to verify the GDAL installation.

### Run Jupyter notebook
Jupyter Notebook is a useful tool that allows you to develop your code efficiently. In the Anaconda Prompt(windows) or terminal(mac, linux), run
```bash
$ jupyter notebook
```
If you see a Jupyter Notebook page pops up in your web browser, it means you successfully installed Jupyter. We will process LiDAR data using Jupyter Notebook in the later sessions.
Click the **Quit button (not the X button)** in the upper right corner.

In the session 2, we are going to learn how to load a statewide LiDAR data set and convert file format for faster processing.
