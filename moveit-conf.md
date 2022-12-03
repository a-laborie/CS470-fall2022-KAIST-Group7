Follow these steps to generate the moveit configuration folder.

* Be sure to have downloaded the Open-manipulator URDF file stored in 
* [ROBOTIS Open-manipulator github repo](https://github.com/ROBOTIS-GIT/open_manipulator/tree/master/open_manipulator_description/urdf)
* Start the MoveIt Setup Assistant:
```
roslaunch moveit_setup_assistant setup_assistant.launch
```
There is no official guide for setting moveit for open-manipulator, so you could look at 
[this webpage](https://roomedia.tistory.com/entry/44%EC%9D%BC%EC%B0%A8-OpenManipulator-MoveIt-%ED%8C%A8%ED%82%A4%EC%A7%80-%EC%83%9D%EC%84%B1%ED%95%98%EA%B8%B0),
or get some inspiration from the
[official tutorial, which is for another robotic arm called panda](https://roomedia.tistory.com/entry/44%EC%9D%BC%EC%B0%A8-OpenManipulator-MoveIt-%ED%8C%A8%ED%82%A4%EC%A7%80-%EC%83%9D%EC%84%B1%ED%95%98%EA%B8%B0)
Be especially cautious with the way you define the Planning group:
![](plannin.jpg)
