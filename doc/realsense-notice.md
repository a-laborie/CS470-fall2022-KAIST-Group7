Software installation for [Intel Realsense D435 camera](https://www.intelrealsense.com/depth-camera-d435i#D415_D435)  

```
sudo apt-key adv --keyserver keys.gnupg.net --recv-key C8B3A55A6F3EFCDE || sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-key C8B3A55A6F3EFCDE  
sudo add-apt-repository deb http://realsense-hw-public.s3.amazonaws.com/Debian/apt-repo focal main" -u  
sudo apt-get install librealsense2-dev librealsense2-utils ros-noetic-rgbd-launch  
```
When we tried it, the repositories was unsigned, so we had to by pass this warning, replacing the second command-line with the following:  

```
sudo add-apt-repository deb [trusted=yes] http://realsense-hw-public.s3.amazonaws.com/Debian/apt-repo focal main" -u  
```
Recompile your catkin environment:  
```
cd ~/catkin_ws/src
git clone https://github.com/intel-ros/realsense.git
cd ~/catkin_ws && catkin_make
```

Install python package:  
```
pip install pyrealsense2
```
You can try the camera with  
```
rqt_image_view
```
