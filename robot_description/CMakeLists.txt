cmake_minimum_required(VERSION 3.8)
project(robot_description)

# Default to C++17 (standard in ROS2)
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
endif()

find_package(ament_cmake REQUIRED)

################################################
## Install resources (URDF, meshes, launch)  ##
################################################

install(
  DIRECTORY
    urdf
    meshes
    launch
  DESTINATION share/${PROJECT_NAME}
)

ament_package()