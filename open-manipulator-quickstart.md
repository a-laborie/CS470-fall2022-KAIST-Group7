[Tutorial link](https://emanual.robotis.com/docs/en/platform/openmanipulator_x/quick_start_guide/)
*Note: you should type each command-line in a new terminal*
# Launch Roscore
```
roscore
```

# Set the USB Latency Timer Setting (optionnal)
```
rosrun open_manipulator_controller create_udev_rules
```

# Launch controller
```
roslaunch open_manipulator_controller open_manipulator_controller.launch
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
