## Starting the Simulation 

By default, this launch file starts ArduPilot SITL, Gazebo, and RViz with a single command.
```
ros2 launch ardupilot_gz_bringup iris_runway.launch.py
```
Start MAVProxy in another terminal:
```
mavproxy.py --console --map --aircraft test --master=:14550
```
```
param set DDS_ENABLE 1
```


#### Link
[Ardupilot-ros2-gazebo](https://ardupilot.org/dev/docs/ros2-gazebo.html)
[Ardupilot-ros2-sitl](https://ardupilot.org/dev/docs/ros2-sitl.html)
