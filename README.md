# Reachy MoveIt config
Integration of the Reachy robot in MoveIt2 for ROS 2

![Reachy in RViz ROS Noetic](https://raw.githubusercontent.com/aubrune/reachy_moveit_config/master/doc/img/moveit.png)

## Getting started
### Install
1. Install [ROS2 Foxy](https://docs.ros.org/en/foxy/Installation.html) on top of [Ubuntu 20.04](https://ubuntu.com/download/desktop)
2. Install [MoveIt2](http://moveit2_tutorials.picknik.ai/doc/getting_started/getting_started.html#)
3. Configure [your ROS2 environment](https://docs.ros.org/en/foxy/Tutorials/Configuring-ROS2-Environment.html) so that you can sucessfully compile your ROS workspace (e.g. `~/ros2_ws`) with `colcon build` command
4. `cd ~/ros2_ws/src && git clone https://github.com/pollen-robotics/reachy_moveit_config_ros2`
5. `cd ~/ros2_ws/src && git clone https://github.com/pollen-robotics/reachy_description_ros2`
6. `cd ~/ros2_ws && colcon build --symlink-install`
7. `source ~/ros2_ws/install/setup.bash`

### Use
Just launch the regular MoveIt2 demo launch file:
```
ros2 launch reachy_moveit_config_ros2 demo.launch.py
```

Then pickup a group in the **Query Planning Group** from the **Motion Planning** panel (right arm, left arm or head) and move the blue ball appearing at the tip of the end effector to some goal pose. Then click **Plan and Execute** to plan a trajectory with obstacle avoidance and run it with fake trajectory controllers.
