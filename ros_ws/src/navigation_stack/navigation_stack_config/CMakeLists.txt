cmake_minimum_required(VERSION 2.8.3)
project(navigation_stack_config)

## Compile as C++11, supported in ROS Kinetic and newer
set (CMAKE_CXX_STANDARD 11)


## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  drive_msgs
  roscpp
  rospy
  std_msgs
  vesc_msgs
  nav_msgs
  vesc_sim
)


###################################
## catkin specific configuration ##
###################################

## Declare things to be passed to dependent projects
catkin_package(
  CATKIN_DEPENDS drive_msgs roscpp rospy std_msgs vesc_msgs nav_msgs
)

## Errors and Warnings
set ( CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Wchar-subscripts -Wchkp -Wdouble-promotion -Wformat -Wnonnull -Wmain -Wswitch-bool -Winvalid-memory-model -Wunknown-pragmas -Warray-bounds -Wfloat-equal -Wlogical-op -Wpacked ")
# -Wpedantic cant be used because of ROS
