[Tutorial link](https://emanual.robotis.com/docs/en/platform/openmanipulator_x/quick_start_guide/)  
Note: *you should type each command-line in a new terminal*  

# 1. Before starting, be sure that :  
* The robot is connected to your computer by USB  
* Check that the robot is powered  

# 2. Launch Roscore
```
roscore
```

# 3. Set the USB Latency Timer Setting (optionnal)
```
source ~/catkin_ws/devel/setup.bash
rosrun open_manipulator_controller create_udev_rules
```

# 4. Launch controller
```
# roslaunch open_manipulator_controller open_manipulator_controller.launch is not working
roslaunch open_manipulator_controller open_manipulator_controller.launch dynamixel_usb_port:=/dev/ttyUSB0
```
If it fails, restart the process from roscore part.  

# Other utilities
## Keyboard teleoperations 
```
roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch

```

## GUI program 
```
roslaunch open_manipulator_control_gui open_manipulator_control_gui.launch
```
The GUI program will start. First, click on *Timer Start*.
Then, follow the [tutorial](https://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_operation/)


## Start the camera (Intel realSense 2)
```
realsense-viewer
```

## Start RViz
```
roslaunch open_manipulator_description open_manipulator_rviz.launch use_gui:=true
```
## Launch MoveIt
```
roslaunch open_manipulator_controllers joint_trajectory_controller.launch sim:=false
```
[Moveit1 tutorial](https://ros-planning.github.io/moveit_tutorials/doc/move_group_python_interface/move_group_python_interface_tutorial.html)
[Moveit1 python commander](https://ros-planning.github.io/moveit_tutorials/doc/moveit_commander_scripting/moveit_commander_scripting_tutorial.html)
