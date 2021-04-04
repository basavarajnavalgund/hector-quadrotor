# hector-quadrotor

It works with both ROS kinetic as well as ROS melodic


## Installing Hector Quadrotor
-----------------------------------------------------
Insted of installing package(hector_quadrotor), please install from source:
 
```
mkdir ~/catkin_ws

cd ~/catkin_ws

wstool init src https://raw.github.com/tu-darmstadt-ros-pkg/hector_quadrotor/kinetic-devel/tutorials.rosinstall

```



Install some required packages.

Note: If you are using ROS kinetic, please replace melodic with kinetic in below commands

```
sudo apt-get install ros-melodic-geographic-info

sudo apt-get install ros-melodic-ros-control

sudo apt-get install ros-melodic-gazebo-ros-control

sudo apt-get install ros-melodic-joy

sudo apt-get install ros-melodic-teleop-twist-keyboard


```
	

Compile and source the workspace:


```
catkin_make

source devel/setup.bash

```



To run **Gazebo and rviz**


	roslaunch hector_quadrotor_demo outdoor_flight_gazebo.launch




To **enable motors**


	rosservice call /enable_motors "enable: true"



To use keyboard teleop **teleop_twist_keyboard node**


	rosrun teleop_twist_keyboard teleop_twist_keyboard.py


