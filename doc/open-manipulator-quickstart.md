[Tutorial link](https://emanual.robotis.com/docs/en/platform/openmanipulator_x/quick_start_guide/)  
Note: *you should type each command-line in a new terminal*  

# 1. Before starting, be sure that :  
* The robot is connected to your computer by USB  
* Check that the robot is powered  

# 2. Launch Roscore
```
roscore
```

# 3. Set the USB Latency Timer Setting (only if it is the firs time running the project since you restarted your laptop)
```
source ~/catkin_ws/devel/setup.bash
rosrun open_manipulator_controller create_udev_rules
```

# 4. Launch controller
## Controller Open-manipulator with the keyboard or ROBOTIS' GUI
```
roslaunch open_manipulator_controller open_manipulator_controller.launch dynamixel_usb_port:=/dev/ttyUSB0
```
## With moveit enabled:
```
roslaunch open_manipulator_controllers joint_trajectory_controller.launch dynamixel_usb_port:=/dev/ttyUSB0 sim:=false
```

# 5. Other utilities
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

## Start RViz
```
roslaunch open_manipulator_description open_manipulator_rviz.launch use_gui:=true
```
## MoveIt links

* [Moveit install an setting up on ROS website](https://ros-planning.github.io/moveit_tutorials/doc/getting_started/getting_started.html)  
* [Moveit1 tutorial on ROS website](https://ros-planning.github.io/moveit_tutorials/doc/move_group_python_interface/move_group_python_interface_tutorial.html)  
* [Moveit1 python commander on ROS website](https://ros-planning.github.io/moveit_tutorials/doc/moveit_commander_scripting/moveit_commander_scripting_tutorial.html)  
## Start the moveit confeditor
```
roslaunch moveit_setup_assistant setup_assistant.launch
```

