# Introduction

The [FAST_LIO](https://github.com/hku-mars/FAST_LIO?tab=readme-ov-file) reproduction via Unitree L1 RM Lidar

# Environment Prequest

## PCL Version >= 1.8

In my Ubuntu 20.04 machine, I  downloaded and  compiled the [PCL 1.14](<https://github.com/PointCloudLibrary/pcl/releases/tag/pcl-1.14.0>) source code, it works fine.
> **_NOTE:_** The verson meaning  1.8 request by FAST_LIO seems a little different with source code version 1.14

You can check the PCL version via command `ldconfig -p | grep pcl`

## Eigen Version>=3.3.4

 In my Ubuntu 20.04 machine, I use the Eigen 3.3.7-2 version, and it works.

You can check the Eigen version via command `dpkg -s libeigen3-dev | grep Version`

if you already satisfied the Eigen lib request, just ignore it . But if you haven't install Eigen lib on your manchine, check this :[Eigen 3.4](<https://gitlab.com/libeigen/eigen/-/releases/3.4.0>)

# Reproduction

After cloning the unitree-fast-lio repo, make the unitree lidar is already connected to your ubuntu machine.

run:

```bash
cd <path2unitree-fast-lio>
catkin_make
source ./devel/setup.bash
roslaunch fast_lio mapping_unilidar_l1.launch
```

# Acknowledge

Thanks for members of HKU-Mars open source this wonderful robotics perception project!

Thanks for Unitree official usage guidance !
