# Task Two Artificial intelligence
## Arduino_robot_arm
### step 1 
#### Make sure install Oracle VM VirtualBox ,Ubuntu and Ros
### step 2
#### install arduino_robot_arm package to "src" folder
#### 1- open terminal
#### 2- writing commands

***cd ~/catkin_ws/src*** 
***sudo apt install git***
***git clone https://github.com/smart-methods/arduino_robot_arm.git***

#### install all the dependencies

 ***cd ~/catkin_ws***

 ***rosdep install --from-paths src --ignore-src -r -y***

 ***sudo apt-get install ros-noetic-moveit***

 ***sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui***

***sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher***

***sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control***

***close terminal***
### step 3
## Configuring Arduino with ROS
***1-Install Arduino IDE in Ubuntu https://www.arduino.cc/en/software to install run***
***write in terminal***

***$ sudo ./install.sh after unzipping the folder***


***2-Launch the Arduino IDE***

***3-Install the arduino package and ros library http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup***

***4-Make sure to change the port permission before uploading the Arduino code $ sudo chmod 777 /dev/ttyUSB0***
### step 4
## You can install rosserial for Arduino by running:
***write in termina***

***sudo apt-get install ros-indigo-rosserial-arduino***

***sudo apt-get install ros-indigo-rosserial***

### step 5
## creates the ros_lib directory.

***cd<sketchbook>/libraries***
 
  ***rm -rf ros_lib***
  
  ***rosrun rosserial_arduino make_libraries.py .***
  
  ##Runing
  # 1- USAGE
run this code in arduino [arduino_code](https://github.com/smart-methods/arduino_robot_arm/blob/main/arduino_code/arduino_code.ino)
# Controlling the robot arm by joint_state_publisher in the terminal 


```
$ roslaunch robot_arm_pkg check_motors.launch
```
![ardunoarm](https://user-images.githubusercontent.com/79949101/181657623-d14b96fc-f7ad-47b1-bbb6-803667e4693e.jpg)


# 2- Controlling the robot arm by Moveit and kinematics

```
$ roslaunch moveit_pkg demo.launch
```
![ARDUNOARM 2jpg](https://user-images.githubusercontent.com/79949101/181657673-eed44a84-763f-4e4c-859a-3696d52541a0.jpg)

  ## References
[smart-methods-arduino_robot_arm](https://github.com/smart-methods/arduino_robot_arm)
