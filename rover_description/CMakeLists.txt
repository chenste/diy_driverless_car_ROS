cmake_minimum_required(VERSION 2.8.3)
project(rover_description)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()
catkin_add_env_hooks(60.husky_custom_description
  SHELLS sh DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)

install(
  DIRECTORY meshes urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
