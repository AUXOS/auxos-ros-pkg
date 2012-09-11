# AUXOS ROS Package

## Installation

Create a ROS workspace:

	mkdir auxos_ws
	cd auxos_ws
	rosws init . /opt/ros/fuerte/

Install the AUXOS repositories for the Segway system:

	rosws merge hhttps://raw.github.com/GAVLab/auxos-ros-pkg/master/rosinstall/segway.rosinstall
	rosws update