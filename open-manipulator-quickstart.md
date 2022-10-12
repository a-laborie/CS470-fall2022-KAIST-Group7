[Tutorial link](https://emanual.robotis.com/docs/en/platform/openmanipulator_x/quick_start_guide/)
*Note: you should type each command-line in a new terminal*
# Launch Roscore
```
roscore
```

# Set the USB Latency Timer Setting
```
rosrun open_manipulator_controller create_udev_rules
```
If it fails, do:
```
source ~/catkin_ws/devel/setup.bash
```
Launch controller (U2D2)
In the *same* terminal : 
```
roslaunch open_manipulator_controller open_manipulator_controller.launch
```
# Dynamixel (optionnal)
Start DinamixelWizard2.0 from the app lists.  
Scan till all of the robot parts are found. (may takes several times (: )
Beware of the USB ports.


# Check manipulator settings
```
rostopic pub /option std_msgs/String "print_open_manipulator_setting"
```
# Keyboard teleoperations (optionnal)
```
roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch

```

# GUI program (optionnal)
```
roslaunch open_manipulator_control_gui open_manipulator_control_gui.launch
```
Then, follow the [tutorial](https://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_operation/)
