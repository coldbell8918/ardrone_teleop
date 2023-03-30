cmake_minimum_required(VERSION 2.8.3)
project(teleop_ardrone)

find_package(catkin REQUIRED COMPONENTS
	geometry_msgs
	sensor_msgs
	roscpp
	joy
	)
	
	
catkin_package(
	CATKIN_DEPENDS geometry_msgs sensor_msgs roscpp joy)


## Mark executable scripts (Python etc.) for installation
## in contrast to setup.py, you can choose the destination
catkin_install_python(PROGRAMS
   src/teleop_ardrone_keyboard.py
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)


