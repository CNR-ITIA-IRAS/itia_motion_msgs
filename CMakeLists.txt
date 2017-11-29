cmake_minimum_required(VERSION 2.8.3)
project(itia_motion_msgs)

find_package( 	catkin REQUIRED COMPONENTS
        control_msgs
				genmsg
				message_generation
				roscpp
				std_msgs
				trajectory_msgs
)

add_service_files(
  FILES
  InterpolatePnt.srv
  reloadReferences.srv
)

generate_messages(
  DEPENDENCIES
  control_msgs
  std_msgs
  trajectory_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES itia_motion_msgs
  CATKIN_DEPENDS control_msgs roscpp std_msgs trajectory_msgs genmsg
#  DEPENDS system_lib
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)


