# lanelet2_standalone

## Overview
This is a standalone lanelet2 **python3** package for the [Lanelet2](https://github.com/fzi-forschungszentrum-informatik/Lanelet2) library, which **does not** require the ROS and catkin.

## Installation
pylanelet2 uses cmake and setuptools for building and is targeted towards Linux.

At least C++14 is required.

### Tested Configuration
* `Ubuntu 16.04 LTS`
* `python3.5`

### Dependencies
* `Boost` (from 1.58, for lanelet2_io)
* `eigen3`
* `pugixml` (for lanelet2_io)
* `boost-python/python3`
* `geographiclib` (for lanelet2_projection)

For Ubuntu:
```shell
sudo apt-get install libboost-dev libeigen3-dev libgeographic-dev libpugixml-dev libpython-dev libboost-python-dev
```

### Building
In the repo root folder,
```shell
sudo python3 setup.py install
```
or
```bash
/path/to/your/python3 setup.py install
```
