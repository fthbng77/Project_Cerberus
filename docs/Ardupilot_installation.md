## Ardupilot Installation

Git configuration:
```
git config --global http.postBuffer 524288000
git config --global http.lowSpeedLimit 0
git config --global http.lowSpeedTime 999999
```

Clone ardupilot:
```
git clone --depth 1 https://github.com/ArduPilot/ardupilot.git
```

Install prerequisites:
```
cd ardupilot
Tools/environment_install/install-prereqs-ubuntu.sh -y
```


## Ardupilot Gazebo packages

Clone ardupilot_gz packace:
```
cd colcon_ws
vcs import --input https://raw.githubusercontent.com/ArduPilot/ardupilot_gz/main/ros2_gz.repos --recursive src
```

```
colcon build
```

If fails try:
```
sudo apt update
sudo apt install libunwind-dev
sudo apt install -y libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev
```
