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

### Instructions

Create a folder to use for the ROS catkin workspace:

	mkdir auxos_ws
	cd auxos_ws

Depending the target vehicle (simulation, Segway, Ranger EV, etc.) the workspace will be created with different rosinstall files.  The repositories needed by all systems can be installed using the command

	wstool init -j8 src https://raw.github.com/GAVLab/auxos-ros-pkg/master/rosinstall/complete.rosinstall

Build the workspace:

	cd auxos_ws
	catkin_make

## Operation

### Simulation


### Segway System


### 