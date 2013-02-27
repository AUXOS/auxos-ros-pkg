# AUXOS ROS Package

## Installation

### Prerequisites

The AUXOS ROS packages make use of the new Catkin build system and are designed for ROS Groovy.  ROS should be installed following the instructions at: http://www.ros.org/wiki/groovy/Installation/Ubuntu.  Additional information on Catkin can be found at: http://www.ros.org/wiki/catkin

The new wstool (http://www.ros.org/wiki/wstool) is also preferred to rosinstall and should be installed using:
	
	sudo apt-get install python-wstool

The simulation portions of the packages require the MORSE simulator and the IS4S addtions to the simulator.  These must be installed previously using:

	cd ~/devel
	git clone git@github.com:davidhodo/morse.git
	cd morse
	mkdir build
	cd build
	cmake -DBUILD_ROS_SUPPORT=ON ../
	make
	sudo make install

	cd ~/devel
	git clone https://github.com/davidhodo/is4s_morse_additions
	cd is4s_morse_additions
	mkdir build
	cd build
	cmake ../
	sudo make install

Needed ROS stacks:

* standard ROS stacks (roscpp, rospy, etc…)
* joystick_driver
* actionlib
*  

### Instructions

Create a folder to use for the ROS catkin workspace:

	mkdir auxos_ws
	cd auxos_ws

Depending on the target vehicle (simulation, Segway, Ranger EV, etc.) the workspace will be created with different rosinstall files.  The repositories needed by all systems can be installed using the command

	wstool init -j8 src https://raw.github.com/GAVLab/auxos-ros-pkg/master/rosinstall/complete.rosinstall

Build the workspace (from auxos_ws):

	catkin_make


## Simulating the Segway RMP400

### Teleop Simulation

	roslaunch segwayrmp400_sim teleop.launch
	
### Path Following Simulation

	roslaunch segwayrmp400_sim test_path_following.launch
	
When the user interface window is displayed, click follow path and browse to "simple_path.txt" in segwayrmp400_sim/data.  

### Modifications for OS X

The standard joystick_drivers package does not function

### ROSINSTALL Files

A list of all available rosinstall files in the package are given below:
	
	