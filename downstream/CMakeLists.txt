cmake_minimum_required(VERSION 3.5)
project(pkg_downstream)

find_package(catkin)
find_package(pkg_a)
find_package(pkg_b)

catkin_package(CATKIN_DEPENDS pkg_a pkg_b pkg_c
        LIBRARIES ${PROJECT_NAME})

add_library(${PROJECT_NAME} src/empty.cc)
add_dependencies(${PROJECT_NAME} ${catkin_EXPORTED_TARGETS})
