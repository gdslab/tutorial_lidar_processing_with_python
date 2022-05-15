## Installing Conda/Anaconda and configuring Virtual Environments (50 min)

We will install the latest version of Anaconda here.


### Download Anaconda

Click [here](https://www.anaconda.com/products/individual) to download installation files for your operating system. If you have already installed anaconda or miniconda on your system, then you can skip this part.

### Open [Command line interface](https://docs.anaconda.com/anaconda/user-guide/getting-started/#open-anaconda-prompt)

Windows: You will need to run **Anaconda Prompt(Anaconda 3)** from the start menu.

OSX or Linux: You will need to open a terminal.

### Configuring conda environment

You will first need to check what virtual environments are already available on your system.
When you run the below command in the terminal, make it sure you have * symbol right next to the base environment. 

```bash
$ conda info --envs
```

You need to create a new virtual environment for this tutorial using the below command. We will use Python=3.6 version in this tutorial. 

```bash
$ conda create --name lidar python=3.8
```

After you create the new virtual environment, we need to activate the new environment using the below command. 

For Windows

```bash
$ conda activate lidar
```

For OSX and Linux

```bash
$ source ~/.bashrc
$ conda activate lidar
```

You need to check if the new environment is activated correctly using the below command. You should see * symbol right next to the lidar environment. 

```bash
$ conda info --envs
```

Once the new environment is activated, you need to install below packages in the new environment that are required for this tutorial.

```bash
$ conda install jupyter
$ conda install numpy matplotlib
$ conda install ipython
$ conda install gdal
$ conda install progressbar2
$ conda install -c conda-forge laspy
$ conda install -c conda-forge lastools
$ conda install pip
```

NOTE: The above commands will install laspy 2.0 version, and we will have to install additional packages to enable laz support. 

```bash
$ pip install lazrs
```

If the above command does not work, then you can do below as an alternative.

```bash
$ pip install laszip
```

For DTM generation, you will need to install *naturalneighbor* module as well.

```bash
$ pip install naturalneighbor
```

After installing the above packages, you need to confirm the installation by running the below commands.

```bash
$ conda activate lidar
$ ipython
```

```python
>>> import numpy
>>> import matplotlib
>>> import laspy
>>> from osgeo import gdal
```

You will also need to check jupyter notebook installation by running the below command.

```bash
$ jupyter notebook
```

## Installing Google Chrome on Windows Server 2019.

Open PowerShell and paste below command.

```
$Path = $env:TEMP; $Installer = “chrome_installer.exe”; Invoke-WebRequest “http://dl.google.com/chrome/chrome_installer.exe" -OutFile $Path\$Installer; Start-Process -FilePath $Path\$Installer -Args “/silent /install” -Verb RunAs -Wait; Remove-Item $Path\$Installer
```
