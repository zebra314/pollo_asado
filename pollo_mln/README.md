## Dependencies
```bash
    ros-$ROS_DISTRO-gmapping 
    ros-$ROS_DISTRO-map-server 
    ros-$ROS_DISTRO-navigation 
```

## Usage
- [localization.launch](./launch/localization.launch)
    - Spawn the robot in gazebo and localize it with amcl.
    ```bash
        roslaunch pollo_mln localization.launch
    ```

- [navigation.launch](./launch/navigation.launch)
    - Spawn the robot in gazebo and launch the navigation stack.
    ```bash
        roslaunch pollo_mln navigation.launch
    ```

- Clear costmaps
    ```bash
        rosservice call /move_base/clear_costmaps "{}"
    ```

## [Back](../README.md#usage)