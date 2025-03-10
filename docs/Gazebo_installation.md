## Gazebo Installation



Instal ignition Fortress (Gazebo fortress) from:

https://gazebosim.org/docs/fortress/install_ubuntu/


### Control the installation:

Start gazebo:
```
ign gazebo visualize_lidar.sdf
```

Check if the topics are being published:
```
ign topic -l
```

Install ros_ign_bridge package:
```
sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'
sudo apt install ros-humble-ign-bridge
```

![image](https://github.com/user-attachments/assets/655c5c97-6a3a-4741-9c96-a26ed4e4ab82)


Run ros_gz_bridge:
```
ros2 run ros_gz_bridge parameter_bridge /gui/camera/pose@geometry_msgs/msg/Pose[ignition.msgs.Pose

```
