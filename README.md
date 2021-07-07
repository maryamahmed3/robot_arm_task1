# robot_arm_task1


Installing the package _robot_arm
Add the “arduino_robot_arm” package to “src” folder
	$ cd ~/catkin_ws/src
	$ sudo apt install git
	$ git clone https://github.com/smart-methods/arduino_robot_arm 
- Install all the dependencies 
	$ cd ~/catkin_ws
	$ rosdep install --from-paths src --ignore-src -r -y
	$ sudo apt-get install ros-melodic-moveit
	$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
	$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
	$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
Compile the package
$ catkin_make
$ roslaunch robot_arm_pkg check_motors.launch
![8853CFB4-5C63-4F7B-B196-D76510AB718C](https://user-images.githubusercontent.com/86611989/124684732-76a8ac80-ded8-11eb-84c4-1afdf04d3b4f.png)
