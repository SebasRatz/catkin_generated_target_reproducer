cmake_minimum_required(VERSION 3.5)
project(pkg_a)

find_package(catkin)
find_package(base_msgs)

catkin_package(CATKIN_DEPENDS base_msgs
	LIBRARIES ${PROJECT_NAME})

add_library(${PROJECT_NAME} src/empty.cc)
add_dependencies(${PROJECT_NAME} ${catkin_EXPORTED_TARGETS})
