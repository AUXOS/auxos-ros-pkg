# AUXOS ROS Package

## Installation

Create a ROS workspace:
	mkdir auxos_ws
	cd auxos_ws
	rosws init . /opt/ros/fuerte/

Install the AUXOS repositories:
	rosws merge https://raw.github.com/GAVLab/auxos-ros-pkg/master/simulation/simulation.rosinstall
	rosws update