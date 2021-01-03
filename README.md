## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)

## General info
In this project, AMCL package is added into the robot project with predetermine the map with previously created gazebo world file.  Using the Robot Teleop package, operator can move the robot around and observing the convergency of the particle.

The name of this project is 'Where Am I".  This is the 4nd project for the Udacity Robotics Software Engineering program.  The purpose of this project is to familiarize with MCL algorithm by visualizing the particles while moving the robot.
	
## Technologies
Project is requires:
* Udacity Workspace or a Virtual Environment with image provided by Udacity
* Robot Operating System, “ROS"
* Gazebo
* RViz

The robot uses:
* A plugin for the camera sensor, libgazebo_ros_camera.so.
* A plugin for the Hokuyo lidar sensor, libgazebo_ros_laser.so.
* A plugin for the wheel joints actuator, libgazebo_ros_skid_steer_drive.so.
* ROS AMCL package (http://wiki.ros.org/amcl) 
* Robot Teleop Package (https://github.com/ros-teleop/teleop_twist_keyboard)

## Setup
To run this project, log into the the Udacity Workspace:

1. Open a console, download and build the project
```
$ cd <to the catkin workspace 'src' subfolder>
$ git clone https://github.com/peggycyggep/Project4
$ cd ..
$ catkin_make
```
2. In the same console or open another console, launch the robot
```
$ cd <to the catkin workspace>
$ source devel/setup
$ roslaunch my_robot world.launch
```
3. Open another console and launch the AMCL
```
$ cd <to the catkin workspace>
$ source devel/setup
$ roslaunch my_robot amcl.launch
```
4. Open another console and launch teleop
```
$ cd <to the catkin workspace>
$ source devel/setup.bash
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
