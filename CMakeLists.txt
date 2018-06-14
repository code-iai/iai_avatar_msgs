cmake_minimum_required(VERSION 2.8.3)
project(iai_avatar_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

find_package(
	catkin REQUIRED COMPONENTS
	std_msgs
  geometry_msgs
	message_generation
)

## Generate messages in the 'msg' folder
add_message_files(
   FILES
)

## Generate services in the 'srv' folder
add_service_files(
   FILES
   MoveTo.srv
   PanTilt.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
   DEPENDENCIES
   std_msgs
   geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS
  message_runtime
  std_msgs
  geometry_msgs
)
