# ROS Tutorials
This workspace contains two tutorial related packages: _math_operation_ and _turtlesim_draw_shapes_.

_math_operation_ package contains two basic C++ nodes, which perform custom message (named _mathop_) publishing/subscribing tasks in ROS. 

_turtlesim_draw_shapes_ package contains C++ nodes that generate geometry_msgs and pass them to _turtlesim_node_. Those _geometry_msgs_ contains velocity instructions for turtle to move in straight lines, circles, or squares.

## How to install
1. Download the code
2. Navigate to the workspace
```bash
cd math_ws
```
3. CMake
```bash
catkin_make
```
If this leads to an error as python3 is not default version, use
```bash
catkin_make -DPYTHON_EXECUTABLE=/usr/bin/python3
```
_If catkin_make throws the exception that it cannot find "math_operation/mathop.h", run the command twice more until it succeeds._

4. Enable env
```bash
./devel/setup.bash
```
## How to run
### math_operation
```bash
roscore
```
In a new session,
```bash
roslaunch math_operation math_operation.launch
```

### turtlesim_draw_shapes
```bash
roscore
```
In a new session,
```bash
roslaunch turtlesim_draw_shapes <straightline.launch/circle.launch/square.launch>
```

