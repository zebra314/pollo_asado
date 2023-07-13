## Setup
- 1.A Installation for local ROS environment :
```bash
    sudo apt-get install ros-$ROS_DISTRO-gmapping ros-$ROS_DISTRO-map-server ros-$ROS_DISTRO-navigation
```

- 1.B Installation for robostack conda environment : 
```bash
    mamba install -c robostack ros-$ROS_DISTRO-gmapping ros-$ROS_DISTRO-map-server 
    
    # robostack does not have ros-$ROS_DISTRO-navigation
    # use virtualbox or local env instead
```

## Usage
- 1. Build the map using gmapping :
```bash
    roslaunch asado_slam gmapping.launch
```

- 2. Save the map :
```bash
    rosrun map_server map_saver -f ~/map
```

- 3. Localize the robot using amcl :
```bash
    roslaunch asado_slam amcl.launch
```


## [Back](../README.md#setup-and-usage)