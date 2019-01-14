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
sudo apt-get install libboost-dev libeigen3-dev libgeographic-dev libpugixml-dev libpython-dev libboost-python-dev libpython3-all-dev
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
```python
#!/usr/bin/env python
from lanelet2 import core, io, projection, geometry, traffic_rules
# or
from lanelet2.core import AttributeMap, TrafficLight, Lanelet, LineString3d, Point2d, Point3d, getId, LaneletMap, BoundingBox2d, BasicPoint2d
p = Point3d(getId(), 1, 100, 1000)
print(p)
assert p.x == 0
p.id = getId()
```
