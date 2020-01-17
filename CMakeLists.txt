cmake_minimum_required(VERSION 2.8.3)
project(iai_avatar_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

find_package(
	catkin REQUIRED COMPONENTS
	std_msgs
        geometry_msgs
	message_generation
        actionlib_msgs
        genmsg
)

## Generate messages in the 'msg' folder
add_message_files(
   FILES
)

## Generate actions in the 'action' folder
add_action_files(DIRECTORY action FILES QnA.action)

## Generate services in the 'srv' folder
add_service_files(
   FILES
   MoveTo.srv
   AvatarRotation.srv
   PositionDuration.srv
   PanTilt.srv
   NamedTargetInterpolation.srv
   Command.srv
   GeneralGrasp.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
   DEPENDENCIES
   actionlib_msgs
   std_msgs
   geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS
  message_runtime
  actionlib_msgs
  std_msgs
  geometry_msgs
)
