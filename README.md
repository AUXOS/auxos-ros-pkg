# AUXOS ROS Package

## Installation

### Dependencies

Needed ROS stacks:


* standard ROS stacks (roscpp, rospy, etc…)
* joystick_driver
* actionlib
*  

### Recommended Installation

Create a ROS workspace (or to add to a current workspace skip to the next step):

	mkdir auxos_ws
	cd auxos_ws
	rosws init . /opt/ros/fuerte/

Install the AUXOS repositories for the Segway system:

	rosws merge hhttps://raw.github.com/GAVLab/auxos-ros-pkg/master/rosinstall/segway.rosinstall
	rosws update
	source setup.bash

### Modifications for OS X

The standard joystick_drivers package does not function

### ROSINSTALL Files

A list of all available rosinstall files in the package are given below:

	
	
## Simulating the Segway RMP400

### Teleop Simulation

	roslaunch segwayrmp400_sim teleop.launch
	
### Path Following Simulation

	roslaunch segwayrmp400_sim test_path_following.launch
	
When the user interface window is displayed, click follow path and browse to "simple_path.txt" in segwayrmp400_sim/data.  