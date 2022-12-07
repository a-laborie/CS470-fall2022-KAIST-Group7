
Github repo for Group 7 of KAIST CS470 course (Introduction to AI) working on an application of the Open manipulator project sorting numbered objects into different boxes according to the number written on them.

You can have an idea of what was the aim of our project in [the project poster](https://github.com/a-laborie/Group10-CS470-fall2022/blob/main/doc/Team_7_poster_file.pdf).
 
 # Installation 
 **(Ubuntu 20.04 required, very liekly not to work with a virtual machine)**
 
 ## ROS and open-manipulator packages
 Follow the steps detailed in [ROBOTIS' official tutorial]()
 Don't forget to [install Dynamixel](https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_wizard2/#software-installation) :) 
 
 ## Python packages
 ```
 pip install cv2
 pip install pillow
 pip install skimage
 pip install torch
 ```
 ## Realsense camera
 * Follow [this tutorial](https://github.com/a-laborie/Group10-CS470-fall2022/blob/main/doc/realsense-notice.md)  
 
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

# 3. Set the USB Latency Timer Setting 
(only if it is the firs time running the project since you restarted your laptop)
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

For more ROS launch info see [this guide](https://github.com/a-laborie/Group10-CS470-fall2022/blob/main/src/open-manipulator-quickstart.md)

# Execute the main code

Open the file oma_main.ipynb (located in src) with your favorite Python Notebook editor (VS code, Jupyter..). Beware, ROS is not installed by default on Google Collab.
Then you can execute the cells step by step.
Enjoy :)


**If you face some issue during the process, do not hesitate to contact us at alexandre.laborie0@orange.fr**

