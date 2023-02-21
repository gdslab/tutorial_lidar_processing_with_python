
## LiDAR file I/O using laspy (60 min)

This tutorial will cover LiDAR file Input and Output using laspy module.


### Tutorial data download

You will need to clone this tutorial github repository using the below command. If you don't have git installed on your machine, then you should be able to download a zip file as well. 

```bash
$ git clone https://github.com/gdslab/tutorial_lidar_processing_with_python.git
```

You can also download any LiDAR tiles from https://lidar.digitalforestry.org if you want.

### Activate the lidar virtual environment

Open a Anaconda Prompt and run the below command to activate the lidar virtual environment you created in the previous section.

For Windows

```bash
$ conda activate lidar
```

For OSX or Linux

Open a terminal window and run the below commands. 

```bash
$ source ~/.bashrc
$ conda activate lidar
```

### Converting .laz file (compressed format) into .las file (las version 1.3)

First check information of the LiDAR data using below command. 

```bash
$ lasinfo in2018_29651885_12.laz
```

Optionally, you can convert .laz file into .las file using below commands. The reason why you may want to convert .laz file into .las (1.3 version) is because the CloudCompare software can't visualize 1.4 version las file at this moment. 

```bash
$ las2las -i in2018_29651885_12.laz -o in2018_29651885_12.las
$ lascopy in2018_29651885_12.las in2018_29651885_12_las13.las 3 1.3
```

### Visualizing LiDAR file

Download [CloudCompare](https://www.danielgm.net/cc/) and install. Using this software, you should be able to visualize in2018_29651885_12_las13.las in 3D. 

```bash
$ snap install cloudcompare
```
