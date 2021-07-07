# robot_arm_task1

first i installed ROS melodic by these steps:

Setup your sources.list :

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

Set up your keys :

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

Installation:

sudo apt update

Desktop-Full Install: (Recommended) : ROS, rqt, rviz, robot-generic libraries, 2D/3D simulators and 2D/3D perception:

sudo apt install ros-melodic-desktop-full

Environment setup:

echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc

Dependencies for building packages:

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

Initialize rosdep:

sudo apt install python-rosdep

With the following, you can initialize rosdep.

sudo rosdep init
rosdep update


Installing the package _robot_arm

Add the “arduino_robot_arm” package to “src” folder

	$ cd ~/catkin_ws/src
	$ sudo apt install git
	$ git clone https://github.com/smart-methods/arduino_robot_arm 
- Install all the dependencies :
- 
	$ cd ~/catkin_ws
	
	$ rosdep install --from-paths src --ignore-src -r -y
	
	$ sudo apt-get install ros-melodic-moveit
	
	$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
	
	$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
	
	$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control


Compile the package:

$ catkin_make

$ roslaunch robot_arm_pkg check_motors.launch




![8853CFB4-5C63-4F7B-B196-D76510AB718C](https://user-images.githubusercontent.com/86611989/124684732-76a8ac80-ded8-11eb-84c4-1afdf04d3b4f.png)
