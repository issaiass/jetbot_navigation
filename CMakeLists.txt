cmake_minimum_required(VERSION 3.0.2)
project(jetbot_navigation)

find_package(catkin REQUIRED COMPONENTS
  amcl
  jetbot_viz
  map_server
  move_base
)

catkin_package()

roslaunch_add_file_check(launch)

include_directories(${catkin_INCLUDE_DIRS})

install(DIRECTORY launch maps param rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)