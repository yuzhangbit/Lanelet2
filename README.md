# lanelet2_standalone

## Overview
This is a standalone lanelet2 **python3** package for the [Lanelet2](https://github.com/fzi-forschungszentrum-informatik/Lanelet2) library, which **does not** require the ROS and catkin.

## Installation
pylanelet2 uses cmake and setuptools for building and packaging and is targeted towards Linux.

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
sudo apt-get install -y cmake libboost-all-dev libeigen3-dev libgeographic-dev libpugixml-dev libpython-dev libboost-python-dev libpython3-all-dev python3-pip python3-setuptools
```

### Installing
In the repo root folder,
```shell
sudo python3 setup.py install
```
or
```bash
/path/to/your/python3 setup.py install
```

### Usage
**Note:   
Importing submodules from the raw `liblanelet2_core_pyapi.so` library like below is not supported.**
```python
from lanelet2.liblanelet2_core_pyapi import AttributeMap # not supported!!!
```
you will get errors:
```
# not supported!!!
```

You can use
```python
from lanelet2 import core
# use core.AttributeMap
# or
from lanelet2.core import AttributeMap
```
instead.

* examples
```python
#!/usr/bin/env python
import lanelet2
from lanelet2 import core, io, projection, geometry
# or
from lanelet2.core import Lanelet, LineString3d, Point2d, Point3d, getId, LaneletMap, BoundingBox2d, BasicPoint2d
p = Point3d(getId(), 1, 100, 1000)
print(p)
assert p.x == 0
p.id = getId()
```
