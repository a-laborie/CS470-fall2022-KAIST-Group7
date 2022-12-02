# Group10-CS470-fall2022
Github repo for Group 10 of KAIST CS470 course (introduction to AI) working on an application of the Open manipulator project sorting numbered objects into different boxes according to the number written on them.
 
 
 # Installation (Ubuntu 20.04 required, probably does not work with a virtual machine)
 
 ## ROS and open-manipulator packages
 Follow the steps detailed in [ROBOTIS' official tutorial]()
 Don't forget to [install Dynamixel](https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_wizard2/#software-installation) :) 
 
 ## Python packages
 ```
 pip install pyrealsense2
 pip install cv2
 pip install 
 pip install pillow
 pip install skimage
 ```
 
 # Quickstart

 
 ## Before starting, be sure that :  
* The robot is connected to your computer by USB    
* Check that the robot is powered    

open two terminals.  
# Launch Roscore
First terminal :  
```
roscore
```

# 3. Set the USB Latency Timer Setting (only if it is the firs time running the project since you restarted your laptop)
Second terminal:  
```
source ~/catkin_ws/devel/setup.bash
rosrun open_manipulator_controller create_udev_rules
```

# 4. Launch controller with moveit enabled
Second terminal:  
```
roslaunch open_manipulator_controllers joint_trajectory_controller.launch dynamixel_usb_port:=/dev/ttyUSB0 sim:=false
```
 
 For more info see [the quickstart guide](https://github.com/a-laborie/Group10-CS470-fall2022/blob/main/open-manipulator-quickstart.md)
